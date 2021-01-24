# GitCheatsheet

## Table of contents
* [Undo](#undo)
* [Stash](#stash)
* [Handy Commands](#handy-commands)
* [Tags](#tags)


## Undo
```sh
# Reset current work
$ git reset --hard HEAD

# Remove untracked files
$ git clean -df

# Reset a file
$ git restore file

# Unstage file
$ git restore -staged file

# Remove last commit
$ git reset --hard HEAD^
$ git reset --hard HEAD^2 (2 last commits)

# Undo stash
$ git stash show -p stash@{0} | git apply -R

```

## Stash
```sh
# Stash with message
$ git stash push -m "message"

# List
$ git stash list

# Show
$ git stash show stash@{0}

# Apply
$ git stash apply/pop stash@{0}

# Drop
$ git stash drop stash{0}

# Create path
$ git stash show -p stash@{0} > my_patch.patch
```

## Handy Commands
```sh
# Show commits from branch
$ git log master..develop

# Show commit changes
$ git show commit_hash

# Delete all branches except
$ git branch| grep -v master| grep -v develop| xargs git branch -D

# Show changes in a file
$ git diff file
```

## Bisect
```sh
# Start
$ git bisect start

# Bad
$ git bisect bad

# Good
$ git bisect good [SHA]?

# Finish
$ git bisect reset
```

## Tags
```sh
# List
$ git tag

# Tag a commit
$ git tag tag_name

# Tag with message (annotated)
$ git tag -a tag_name (will ask for a message)

# Push tag origin
$ git push origin tag_name


# Fetch all tags
$ git fetch --all --tags

# Checkout a tag & creating branch
$ git checkout tag_name -b branch_name
```
