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
