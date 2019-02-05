# Branches + Merging #
Branching is the way you can test things out. It's an isolated environment where you can edit and play with your code before merging back onto the master once it's stable.

### Creating a Branch
To create a branch you need to enter the commands
`$ git branch branchname`

To checkout of the master branch and into your branch you need to type

### Going into the Branch###

`$ git checkout branchname`
Now you'll have switched into your branch (instead of the master)

NOTE: Switching branches changes files in your working directory
It’s important to note that when you switch branches in Git, files in your working directory will change. If you switch to an older branch, your working directory will be reverted to look like it did the last time you committed on that branch. If Git cannot do it cleanly, it will not let you switch at all.

### You can now type to clear the text in your GitBash ###

`$ git clear`

### Seeing what you have and deleting branches ###

To see the branches you have you can type
`$ git branch -a`

To delete branches you'll have to switch back into the master
`$ git checkout master`

and type

`$ git branch -d branchname` - once it's been merged or
`$ git branch -D branchname`

### Merging a Branch to the master ###
You have to go back to the master branch.

`$ git merge branchname`



### Merge Conflicts ###
Happens when Git doesn't know which version we want. This happens when someone else has made an edit in the time you have edited your branch. Once you have resolved the conflict, you can simply type

`$ merge commit` These doesn't require a commit message.

To check the log you can types
`$ git log --oneline`
