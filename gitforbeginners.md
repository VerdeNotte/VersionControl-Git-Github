# Gitbash for Beginners
### What do you need to do to learn how to use Git?

**1. Installing Git**
- Install Git - this comes with 3 things, your Git, Gitbash and Gitgui
- Sign up to a Github account
- Use the CommandLine or GitBash, you'll need to learn some easy Git commands or a GUI

Differences between CommandLine and a GUI.

| Topic        | GUI | CommandLine|
| ------------- |:-------------:| -----:|
|Full Name|	Graphic User Interface	|Full name for CLL
|Kind|Sourcecoude,Gitgui,GitHubdesktop| CommandLine, GitBash|
|Type|	It is the simplest form of communication which can be done between the user and computer.	|It is the traditional way of making computers perform the required task.|
|Function|	Makes use of devices such as mouse or keyboard to input instructions and for the computer to perform them.	|Instructions have to be entered manually in the command window in few lines and the device ends up acting according to them.|
|Benefits|	GUI offers maximum control too but the advanced operations cannot be performed through it.	|There is more control when it comes to using the CLI and file systems|


I've been playing around with Gitbash(I like the colours)and creating repositories and files within that. There are commands to learn but they are fairly simple. I'll attach a list of relevant commands and what they do.

Once you have downloaded Git and created your login for GitHub. You now can start playing around with your GitBash (or CommandLine). If you want to use a GUI, you'll still need your CommandLine to do the configuration.

**2. Configuring Git**

You need to configure your Git. This allows your Git to know who's making the changes (and this is how it tracks the versions). These are the configuration values for every repository you interact with on this machine.

You do this by

`$ git config --global user.name "Your Name"`
`$ git config --global user.email "Your email"`

You also need to reset the proxy server so your local Git will be able to talk to your Remote Git.

`$ git config --global http.proxy http://10.248.8.12:8080`

**3. Creating a new repository**

You need to create a repository (folder or repo) on your computer. If you right click on your newly created repository, you should see GitBash here. Click that and GitBash will open with your repository.

You need to initalize the folder

`$ git init`

You use two repositories in Git to collaborate with others: a local repo and a remote repo. Your local repo (on your computer and what we are creating here) is where you do all your work then you'll be able to `$ git push` it onto your remote repo and then `$ git pull` the remote repo back into your local repo.

**3.1 Creating files**
You can either create the files by

`$ touch index.html` (This creates an html file called index)
or simply right click in your repository

*You can see what your files/Git is doing by typing*

`$ git status` - this is a very important command that you'll often use to check what's happening with your repository and files.

**3.2 Adding files**
Once you have created your files, you need to add them to your repository(and the staging Area) otherwise they will be untracked and you won't be able to commit them.

You can do this by

`$ git add <filename>` or if you want to add them all you can type `$ git add .`

You can also add all types of a file for example.
`$ git add *.html` or `git add *.txt`

or you can add all by
`$ git add .`

But if you want to remove the file only from the Git repository and not remove it from the filesystem, use:

`git rm --cached file1.txt`
`git commit -m "remove file1.txt"`

If you want to delete files permanently you need to
Use git rm:

`git rm file1.txt`
`git commit -m "remove file1.txt"`

Once you have modified your file, you'll have to add it again to the Staging Area before you can commit.

**4. Committing your file**
To commit your files to your repository you can enter

`$ git commit` *This will take you to a VIM editor. If you type, nothing will happen as you need to type* `i` *for it to go into insert mode. Once there, you can add comments with the #. To exit the VIM editor, press* `ESC` *then type* `:q!` and `enter`

Alternatively you can use the command below to avoid the VIM editor.

`$ git commit -m "typeyourcommentshere"`

You can check your status by again typing

`$ git status`

or you can check the log history by typing

`$ git log `

To exit the log press
`q`
