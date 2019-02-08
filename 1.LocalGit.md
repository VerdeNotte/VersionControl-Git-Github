# Gitbash for Beginners
### What do you need to do to learn how to use Git?

**1. Installing Git**
- Install Git - this comes with 3 things, your Git, Gitbash and Gitgui
- Sign up to a Github account
- Use the CommandLine or GitBash, you'll need to learn some easy Git commands or a GUI
- Text editor: I've downloaded Atom - I'm assuming you might not need one but I've found it useful to type in for Markdown.  

Differences between CommandLine and a GUI.

| Topic        | GUI | CommandLine|
| ------------- |:-------------:| -----:|
|Full Name|	Graphic User Interface	|Full name for CLL
|Kind|Sourcecoude,Gitgui,GitHubdesktop| CommandLine, GitBash|
|Type|	It is the simplest form of communication which can be done between the user and computer.	|It is the traditional way of making computers perform the required task.|
|Function|	Makes use of devices such as mouse or keyboard to input instructions and for the computer to perform them.	|Instructions have to be entered manually in the command window in few lines and the device ends up acting according to them.|
|Benefits|	GUI offers maximum control too but the advanced operations cannot be performed through it.	|There is more control when it comes to using the CLI and file systems|


I've been playing around with Gitbash(I like the colours)and creating repositories and files within that. There are commands to learn but they are fairly simple.

Once you have downloaded Git and created your login for GitHub. You now can start playing around with your GitBash (or CommandLine). If you want to use a GUI, you'll still need your CommandLine to do the configuration.

**2. Configuring Git**

You need to configure your Git. This allows your Git to know who's making the changes (and this is how it tracks the versions). These are the configuration values for every repository you interact with on this machine.

You do this by

`$ git config --global user.name "Your Name"`
`$ git config --global user.email "Your email"`

You also need to reset the proxy server so your local Git will be able to talk to the remote Git.

`$ git config --global http.proxy http://10.248.8.12:8080`

**3. Creating a new repository**

You need to create a repository (folder or repo) on your computer. If you right click on your newly created repository, you should see GitBash here. Click that and GitBash will open with your repository.

You need to initialize the folder

`$ git init`

You use two repositories in Git to collaborate with others: a local repo and a remote repo. Your local repo (on your computer and what we are creating here) is where you do all your work then you'll be able to `$ git push` it onto your remote repo and then `$ git pull` the remote repo back into your local repo. (More on the pus/pull later)

To be able to see the git folder in your repository. You need to unhide the folder. You can do this by clicking on Control Panel, Folder Options, View and tick the 'Show hidden, files, folders and drive ' option. Don't worry about this git folder, it just lives in your repository.

**3.1 Creating files**
You can either create the files by

`$ touch index.txt` (This creates an txt file called index)
or simply right click in your repository

*You can see what your files/Git is doing by typing*

The main tool you use to determine which files are in which state is the `$ git status command`

If you run this command directly after a clone, you should see something like this:

```sh
$ git status
# On branch master
nothing to commit (working directory clean)
```

**3.2 Adding files**
Once you have created your files, you need to add them to your repository and the staging area otherwise they will be untracked and you won't be able to commit them.

You can do this by

`$ git add filename` or if you want to add them all you can type `$ git add .`

You can also add all types of a file for example.
`$ git add *.html` or `git add *.txt`

But if you want to remove the file only from the staging area and not from the repository, use:

`$ git rm --cached filename`

If you want to delete files permanently you need to
Use git rm but only once the files have been added (and committed)

`$ git rm filename`
`$ git commit -m "remove filename"`

Once you have modified your file, you'll have to add it again to the Staging Area before you can commit.

If you add a new file to your project, and the file didn't exist before, when you run a `$ git status` you should see your untracked file like this:

```sh
$ git status
# On branch master
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#   README
nothing added to commit but untracked files present (use "git add" to track)
```

**4. Committing your file**
To commit your files to your repository you can enter

`$ git commit` *This will take you to a VIM editor. If you type, nothing will happen as you need to type* `i` *for it to go into insert mode. Once there, you can add comments with the #. To exit the VIM editor, press* `ESC` *then type* `:q!` and `enter`

Alternatively you can use the command below to avoid the VIM editor.

`$ git commit -m "typeyourcommentshere"`

You can check your status by again typing

`$ git status`

or you can check the log history by typing

`$ git log --oneline` *A prettier version than the one below - you also don't have to exit this version*

`$ git log ` or
To exit the log press
`q`

**5. Gitignore**

A gitignore file specifies intentionally untracked files that Git should ignore.

You need to create a gitignore file.

`$ touch .gitignore `

Open it up in your text editor and simply add the names of the files you want Git to ignore.

Now, if you use `$ git add .` You'll see all your files added except the ones you added into .gitignore.
