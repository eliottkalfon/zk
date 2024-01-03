
202401031918
Status: #ideas
Tags: #git

# Syncing zettelkasten with git

```bash
sync-zk() {
  # Navigate to the folder
  cd ~/Documents/zk || return

  # Check if the directory is a git repository
  if [ ! -d .git ]; then
    echo "Not a Git repository. Exiting."
    return 1
  fi

  # Check if there are any changes to be staged
  if git diff --quiet; then
    echo "No changes to be staged. Exiting without committing."
    return 1
  fi

  # Stage all changes
  git add .

  # Commit changes with a message following the pattern "YYYYMMDDHHmm"
  commit_message=$(date +'%Y%m%d%H%M')
  git commit -m "$commit_message"

  # Push changes to main
  git push origin main
}

# Usage: Execute the custom command
alias sync-zk="sync-zk"
```


___
# References

Merci GPT