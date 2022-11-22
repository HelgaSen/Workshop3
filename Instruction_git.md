# <img src=https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png width="30"> **Version control system GIT. How to use.** 

## What is <span style="color:#f14e32"> GIT</span>?

Git is free and open source software for distributed version control: tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.

**Git is a version control system that developers use all over the world.**

You can use GIT with VS Code or similar programm.

In order to check if you already have Git installed on your computer you can type the command 

    git version 
    
in the terminal.

---

## Repository initialization

To create an empty Git repository or reinitialize an existing one, use command:

    git init

Running git init in an existing repository is safe. It will not overwrite things that are already there. The primary reason for rerunning git init is to pick up newly added templates.

---

## Status checking 

Use the command below to see the working tree status:

    git status

Displays paths that have differences between the index file and the current HEAD commit, paths that have differences between the working tree and the index file, and paths in the working tree that are not tracked by Git. 

The first are what you would commit by running **<span style="color:#ffff00"> git</span> commit***; the second and third are what you could commit by running **<span style="color:#ffff00"> git</span> add*** before running git commit.

 <font size = 1> \* Read below for more details about this commands</font>

 ---

## Updating the index

To add file contents to the index, use command:

    git add <filename>

This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.

The "index" holds a snapshot of the content of the working tree, and it is this snapshot that is taken as the contents of the next commit.

This command can be performed multiple times before a commit.

---

## Recording changes

To save changes added to the index, use command:

    git commit

To make your actions clear for you and others, it is necessary to make log message describing the changes. Rigth syntax for this command is:
    
    git commit -m "commit massage"

That will be great if you'll make your commit message short, clear and simple.

---

## Git commit command options

In some cases - for making our work with git simpler and quicker - we can use special options of commit command. For example, "-a", "all":

    git commit -a

This command automatically stage **ALL** files that have been modified and deleted, **BUT** new files you have not told Git about are not affected. 

Another useful option for git commit command is:

    git commit -am

This syntax combines git add and git commit -m commands. 

**<span style="color:#CD5C5C"> Be careful</span>** - **ALL** files and changes will be commited.

---

## Changes list review

Git allows you to look through all saved changes and even shift betweem whem.

All changes you've made (commited) recorded in changes list called log.

To look through log, use command:

    git log

The output is given in reverse chronological order by default and contains info about commits that are reachable by following the parent links from the given commit.

Full log info shows you data about commits: hash number, author, date and message. 

---

## Git log command options

If it is no need to look through info about authors and dates git allows you to get a short log version which only contains short hashcode and commit message. To get it use command with special attribute:

    git log --oneline
    




