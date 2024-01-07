
202401071617
Status: #idea
Tags: #data-engineering #data

# Three SQL join algorithms
In an AWS Auto1 workshop, I came across the three main database join algorithms. I found them interesting as they relate to algorithms and data structures which I have taught at XU Potsdam. I am including a quick summary below.

1. Nested Loop Join
	- Iterate over all rows of the largest table
	- For each row, filter the rows of the other table
	- Combine rows
	- Worst type of join, but doable when joining on index columns (see [[Database indices]])
2. Merge Join
	- Both tables need to be sorted or quick to sort
	- Similar idea to merge sort, iterate over both tables simultaneously
3. Hash Join
	- Build a hash table from the smaller table
	- Iterate over the rows of the larger table and query the hash table
	- Ideal when one of the tables is much smaller

## Some Python code


### Nested Join

```python
def nested_loop_join(df1, df2, key):
    joined_data = []
    for i, row1 in df1.iterrows():
        for j, row2 in df2.iterrows():
            if row1[key] == row2[key]:
                joined_data.append(row1.to_dict())
                joined_data[-1].update(row2.to_dict())
    return pd.DataFrame(joined_data)

# Perform Nested Loop Join
nested_loop_result = nested_loop_join(orders_df, customers_df, 'customer_id')
print(nested_loop_result)
```
### Sort Merge Join
```python
def sort_merge_join(df1, df2, key):
    df1_sorted = df1.sort_values(by=key).reset_index(drop=True)
    df2_sorted = df2.sort_values(by=key).reset_index(drop=True)
    i = j = 0
    joined_data = []
    while i < len(df1_sorted) and j < len(df2_sorted):
        if df1_sorted.loc[i, key] == df2_sorted.loc[j, key]:
            joined_row = {**df1_sorted.loc[i].to_dict(), **df2_sorted.loc[j].to_dict()}
            joined_data.append(joined_row)
            i += 1
            j += 1
        elif df1_sorted.loc[i, key] < df2_sorted.loc[j, key]:
            i += 1
        else:
            j += 1
    return pd.DataFrame(joined_data)
```
### Hash Join

```python
def hash_join(df1, df2, key):
    hash_table = {}
    for i, row in df2.iterrows():
        hash_key = row[key]
        if hash_key not in hash_table:
            hash_table[hash_key] = []
        hash_table[hash_key].append(row.to_dict())
    
    joined_data = []
    for i, row in df1.iterrows():
        hash_key = row[key]
        if hash_key in hash_table:
            for row2 in hash_table[hash_key]:
                joined_row = {**row.to_dict(), **row2}
                joined_data.append(joined_row)
    return pd.DataFrame(joined_data)

# Perform Hash Join
hash_join_result = hash_join(orders_df, customers_df, 'customer_id')
print(hash_join_result)
```
___
# References
GPT 4 Turbo