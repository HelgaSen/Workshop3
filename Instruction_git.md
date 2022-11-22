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

## Добавление изменений в индекс

Чтобы добавить изменение в индекс для следующего коммита, нужно ввести команду:

    git add <filename>
