# Git cheat sheet
Some useful git commands assuming you're already confortable with git.

## config

Set:
```git
git config --local user.email <email>
```

Get:
```git
git config --local user.email
```

Create “last” alias (see branch section):
```git
git config alias.last '!git reflog | grep -i "checkout: moving" -m 10'
```

## log

Show commits only on branch2:
```git
git cherry -v <branch1> <branch2>
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

Apply/pop at a specific index:
```git
git stash pop "stash@{1}"
```

## branch

Find branches the commit is on:
```git
git branch --contains <commit>
```

Recent branches:
```git
git for-each-ref --sort=-<committerdate> refs/heads/
```

Latest branches:
```git
git reflog | grep -i "checkout: moving” -m 10
```

## diff

Save diff to a file:
```git
git diff --color > foo.txt
```

## merge

Fix merging conflict choosing the source branch:
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

## clean

Remove untracked files:
```git
git clean -fd
```
