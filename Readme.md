# HELLO WORLD 

# GIT COMMANDS
## Add files and update repositories
git add reame
git commit -m "small changes"
git push                      ! to publish

git remote get-url origin     ! Verify URL of the repository

git tab
git checkout 0.1.1

## Update local version 

git pull => update the local version of a repository from a remote. 

git reset --hard origin/main => reset local branch to what's at remote.  For exemple to get back a removed file

## branch-related commands
|command | description|
|---|---|
git branch     | see available branches 
git branch -r  | see remote branches
git checkout <branch_name> | Switch to an existing branch 

## Creating new branch
| commnad | descriptions |
|---------|--------------|
| git checkout -b MyNewBranch | creating a new branch |
| git commit -m 'comments" |commit the breanch for upload |'
| git push --set-upstream origin MyNewBranch | upload MyNewBranch|

## clone wiki repo

git clone <name.wiki.git>
