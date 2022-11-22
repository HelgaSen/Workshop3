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

## Проверка состояния репозитория 

Чтобы проверить состояние репозитория нужно ввести команду:

    git status

## Добавление изменений в индекс

Чтобы добавить изменение в индекс для следующего коммита, нужно ввести команду:

    git add <filename>
