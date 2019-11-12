# Git cheat sheet
Some useful git commands

## Config

Set:
```git
git config --local user.email "email@domain.tld"
```

Get:
```git
git config --local user.email
```

## push

Delete remote branch:
`--no-verify` to prevent triggering any potential git hook
```git
git push --no-verify -d origin my-branch-to-delete
```

## stash

Prevent stashing the staged files:
```git
git stash save --keep-index
```

## merge

```git
git merge -X theirs branch-to-merge
```

For specific files:
```git
git checkout --ours -- <paths>
git checkout --theirs -- <paths>
```

