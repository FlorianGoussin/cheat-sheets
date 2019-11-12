# Git cheat sheet
Some useful git commands

## config

Set:
```git
git config --local user.email <email>
```

Get:
```git
git config --local user.email
```

## push

Delete remote branch:
`--no-verify` to prevent triggering any potential git hook
```git
git push --no-verify -d origin <branch>
```

## stash

Prevent stashing the staged files:
```git
git stash save --keep-index
```

## branch

Find branches the commit is on:
```git
git branch --contains <commit>
```

## merge

```git
git merge -X theirs <branch>
```

For specific files:
```git
git checkout --ours -- <paths>
git checkout --theirs -- <paths>
```

## remove

Stop tracking:
```git
git rm -r --cached <path>
```

