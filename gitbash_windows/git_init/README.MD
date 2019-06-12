# A .git directory has a structure similar to the following one:

## objects/ folder

```
In this directory the data of your Git objects is stored – all the contents of the files you have ever checked in, your commits, trees and tag objects.
objects/[0-9a-f][0-9a-f] folders
A newly created object is stored in its own file. The objects are placed over 256 subdirectories using the first two characters of the SHA1 object name to keep the number of directory entries in objects itself to a manageable number. Objects found here are often called unpacked or loose objects.

objects/pack folder
Files that store many object in compressed form, along with index files to allow them to be randomly accessed are found in this directory.

objects/info folder
Additional information about the object stored is placed in this directory.
```
## refs folder
```
References are stored in subdirectories of this directory. The git prune command knows to preserve objects reachable from refs found in this directory and its subdirectories.
refs/heads/ folder
Contains commit objects.

refs/tags/ folder
Contains any object name.

refs/remotes/ folder
Contains commit objects of branches copied from a remote repository.

packed-refs file
The file consists of packed heads and tags. It is useful for an efficient repository access.
```
## HEAD file
```
This file holds a reference to the branch you are currently on. This tells Git what to use as the parent of your next commit
```
##  config file

```
This is the main Git configuration file. It keeps specific Git options for your project, such as your remotes, push configurations, tracking branches and more. Your configuration will be loaded first from this file, then from a ~/.gitconfig file and then from an /etc/gitconfig file, if they exist.
```
##  branches

```
A deprecated way to store shorthands to be used to specify a URL to git fetch, git pull and git push. This mechanism is legacy and not likely to be found in modern repositories.
```
## hooks folder
```
This directory contains shell scripts that are invoked after the corresponding Git commands. For example, after you run a commit, Git will try to execute the post-commit script.
```
## index file

```
The GIT index is used as a staging area between your working directory and your repository. You can use the index to build up a set of changes that you want to commit together. When you create a commit, what is committed is what is currently in the index, not what is in your working directory. It is a binary file containing a sorted list of path names, each with permissions and the SHA-1 of a blob object.
```

## info folder
```
Additional information about the repository is recorded in this directory.
```

## remotes folder
```
This folder contains shorthands for URL and default refnames for use when interacting with remote repositories via git fetch, git pull and git push commands. This mechanism is legacy and not likely to be found in modern repositories.
```
## logs folder
```
Stores the changes made to refs in repository.
logs/refs/heads/ folder
Records all changes made to the different branch tips

logs/refs/tags/ folder
Records all changes made to the different tags
```
```
modules folder
Contains the git-repositories of the submodules.

worktrees folder
Contains administrative data for linked working trees. Each subdirectory contains the working tree-related part of a linked working tree.
```
