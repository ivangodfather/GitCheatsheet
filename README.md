# GitCheatsheet

## Undo

· Undo tracked files
git reset --hard HEAD

· Remove new files
git clean -df
git clean -i (Shows what will do)

· Reset a file
git restore file

· Unstage file to be commited
git restore --stages file

· Remove last commit
git reset --hard HEAD^
git reset --hard HEAD~2 (last two commits)

· Undo stash
git stash show -p stash@{0} | git apply -R

## Stash
git stash push -m "message" // git stash
git stash list
git stash show stash@{0}
git stash apply/pop stash@{0}
git stash drop stash{0}
git stash show -p stash@{0} > my_patch.patch

## Handy
· Show commits from current branch
git log master..develop

· Show commit
git show commit_hash

· Delete all branches except
git branch| grep -v master| grep -v develop| xargs git branch -D

· Show changes in a file
git diff file

## Bisect
Start
git bisect start
Bad
git bisect bad
Good
git bisect good [SHA]?
Finish
git bisect reset

## Tag
List tags
git tag

Tag a commit
git tag tag_name
Tag with message (annotated)
git tag -a tag_name (will ask for a message)
Push tag origin
git push origin tag_name
Fetch all tags
git fetch --all --tags
Checkout a tag & creating branch
git checkout tag_name -b branch_name
Push tag
git push origin tag_name
