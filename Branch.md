Branching is the way you can test things out. It's an isolated environment where you can edit and play with your code before merging back onto the master once it's stable.

#Creating a Branch#
`$ git branch branchname` Creates the branch
Once you've created the branch, to edit within the branch you'll have to type
`$ git checkout branchname`
or this command does both for you
`$ git branch -b branchname` Creates and checkouts the branch

To see the branches you have you can type
`git branch -a`

To delete branches you'll have to switch back into the master
`$ git checkout master`

and type

`$ git branch -d branchname` - once it's been merged or
`$ git branch -D branchname`

#Merging a Branch to the master#
You have to go back to the master branch.

`$ git merge branchname`

#Merge Conflicts#
Happens when Git doesn't know which version we want. This happens when someone else has made an edit in the time you have edited your branch. Once you have resolved the conflict, you can simply type

`$ merge commit` These doesn't require a commit message.
