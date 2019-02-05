#### Clone specific branch from github:
```
  git clone -b branch_name git@github.com:user/myproject.git
```

#### Deleting a remote branch:
```
  git push origin --delete <branch>  # Git version 1.7.0 or newer
  git push origin :<branch>          # Git versions older than 1.7.0
```

#### Deleting a local branch:
```
  git branch --delete <branch>
  git branch -d <branch> # Shorter version
  git branch -D <branch> # Force delete un-merged branches
```
