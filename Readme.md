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



# The git merge --strategy= 
The git merge --strategy= option allows the user to specify a particular merge strategy to be used when combining two or more branches. Git provides several built-in merge strategies, each suited for different scenarios and desired outcomes.

Here are some of the common merge strategies:
<ol>
    <li>ORT (Ostensibly Recursive Three-way):
    This is the default strategy for merging a single branch. It is a robust three-way merge algorithm designed to simplify the merge process, reduce conflicts, and improve performance.</li>
    <li>Recursive: This is a three-way merge strategy, historically the default before ORT. It climbs the ancestry of the two competing lines of development to find a common ancestor and then attempts to reconcile the changes. It is effective for merging two heads.</li>
    <li>Resolve: This strategy can only resolve two heads using a three-way merge algorithm. It focuses on carefully detecting and resolving criss-cross merge ambiguities. </li>
    <li>Ours:This strategy resolves any number of heads, but the resulting tree of the merge is always that of the current branch head, effectively ignoring all changes from all other branches. It is useful for superseding old development history of side branches. Note that this is different from the -Xours option used with the recursive strategy. </li> 
    <li>Subtree:This is a modified ORT strategy. It is used when one branch corresponds to a subtree of another, adjusting the tree structure of the subtree branch to match the main branch before merging.</li> <li>Octopus:This strategy is designed for bundling topic branch heads together and is the default when merging more than one branch.</li>
</lo>

## Exemple: "using OURS option to make the current Git branch a master branch"
| commnad | descriptions |
|---------|--------------|
|git checkout {better_branch} |This is the branch whose commits you want to keep|
|git merge --strategy=**ours** master| keep the content of this branch, but record a merge|
|git checkout master |You want to **lose** all changes on this branch|
|git merge {better_branch} |fast-forward master up to the merge|

## clone wiki repo

git clone <name.wiki.git>

# References
https://www-markdownguide-org.translate.goog/basic-syntax/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc

https://stackoverflow.com/questions/2763006/make-the-current-git-branch-a-master-branch