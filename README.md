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


