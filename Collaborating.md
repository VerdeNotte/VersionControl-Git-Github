### Working on Github together

When working with other people's repositories, there are a few basic Git commands to remember

`$ git clone`
`$ git fetch`
`$ git merge`
`$ git pull`

These commands are very useful when working with a remote repository.

 `clone` and `fetch` download remote code from a repo's remote URL to your local computer

 `merge` is used to merge different people's work together with yours

 `pull` is a combination of `fetch` and `merge`

 # Clone

 To grab a complete copy of another user's repository, you need to use `git clone`

 `git clone https://github.com/USERNAME/REPOSITORY.git`
Clones a repository to your computer

While logged in to GitHub, these URLs are available below the repository details:

![Clone](https://github.com/VerdeNotte/VersionControl-Git-Github/blob/master/Clone.PNG "Clone URL")

When you run git clone, the following actions occur:

> -A new folder called repo is made
> -It is initialized as a Git repository
> -A remote named `origin` is created, pointing to the URL you cloned from
> -All of the repository's files and commits are downloaded there
> -The default branch (usually called master) is checked out
