
202401100946
Status: #idea
Tags: #mathematics #definitions

# Permutations and combinations

A **combination** is a selection of items in which the order does not matter.

A **permutation** is an arrangement of items where the order does matter.

## Mathematical Definitions

**Permutations**
The number of permutations of $n$ distinct objects taken $k$ at a time, noted $P(n,k)$ is the number of order arrangements of $k$ objects chosen from the $n$ objects available. It is calculated using the formula:

$P(n,k) = \frac{n!}{(n-k)!}$

**Combinations**
The number of combinations of $n$ objects taken $k$ at a time, noted $C(n,k)$ is the number of different groups or sets of $k$ objects chosen from the $n$ available, where the order of objects within each group does not matter. It is calculated with the formula:

$C(n,k) = \frac{n!}{k! \cdot (n-k)!}$

The number of combinations is inferior to the number of permutations as two permutations with the same items but a different orders represent a single combination of this set of items

## Example
Consider a set containing the letters A, B and C. There are six different permutations of 2 letters:
1. AB
2. BA
3. AC
4. CA
5. BC
6. CB
This intuition is validated by the formula for $P(n,k)$:
$P(3,2) = \frac{3!}{(3-2)!} = 6$

There are however only 3 combinations, as AB and BA are single combination. Same goes for 3-4 and 5-6.

This intuition is confirmed by the formula for $C(n,k)$:
$C(3,2) = \frac{3!}{2!(3-2)!} = 3$

### For all lengths of combinations and permutations

As a quick note, the total number combinations of all lengths is $2^n$.

In our examples, this is $2^3 = 8$. The combinations include: {}, {A}, {B}, {C}, {A,B}, {B,C}, {A,C}, {A,B,C}

To calculate all permutations, we need to compute the sum of all permutations at all lengths: $\frac{n!}{(n-1)!} + \frac{n!}{(n-2)!} + ... + \frac{n!}{(n-n)!}$

Which simplifies to: $n + n(n-1) + ... + n!$




___
# References

Good old GPT-4, 10/01/2024