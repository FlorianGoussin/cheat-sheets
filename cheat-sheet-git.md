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

For a specific file in all branches:
```git
git log --all -- path
```

Log changes not yet merged in the parent branch (don't forget the `..` at the end):
```git
git log --no-merges <branch>..
```

Or:
```git
git cherry -v <branch>
```

Cool log options:
```git
git log --graph --oneline --author=<authorName> --max-count=<count>
```

## show

Show Files from a commit:
```git
git diff-tree --no-commit-id --name-only -r <commit>
```

Show the recent files that have been changed:
```
git log --name-status -10 path/to/dir
```

Show the files of a serie of commits from start date to end date:
```git
git whatchanged --since '03/16/2020' --until '03/27/2020' --oneline --name-only --pretty=format: | sort | uniq >> changedlist.txt
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

Show diff between two commits:
```git
git diff <commit1> <commit2> <path>
```

You can use [`--name-only`](https://git-scm.com/docs/git-diff#Documentation/git-diff.txt---name-only) to show only names of changed files.

## merge

Fix merging conflict choosing the source branch:
```git
git merge -X theirs <branch>
```

For specific files:
```git
git checkout --ours -- <path>
git checkout --theirs -- <path>
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
