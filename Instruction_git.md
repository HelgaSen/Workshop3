# <img src=https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png width="30"> **Version control system GIT. How to use.** 

## What is <span style="color:#f14e32"> GIT</span>?

Git is free and open source software for distributed version control: tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.

 **Git is a version control system that developers use all over the world.**

You can use GIT with VS Code or similar programm.

In order to check if you already have Git installed on your computer you can type the command 

    git version 
 
in the terminal.

---

## ![Icon](icon.png) Repository initialization

To create an empty Git repository or reinitialize an existing one, use command:

    git init

Running git init in an existing repository is safe. It will not overwrite things that are already there. The primary reason for rerunning git init is to pick up newly added templates.

---

## ![Icon](icon.png) Status checking 

Use the command below to see the working tree status:

    git status

Displays paths that have differences between the index file and the current HEAD commit, paths that have differences between the working tree and the index file, and paths in the working tree that are not tracked by Git. 

The first are what you would commit by running **<span style="color:#ffff00"> git</span> commit***; the second and third are what you could commit by running **<span style="color:#ffff00"> git</span> add*** before running git commit.

 <font size = 1> \* Read below for more details about this commands</font>

 ---

## ![Icon](icon.png) Updating the index

To add file contents to the index, use command:

    git add <filename>

This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.

The "index" holds a snapshot of the content of the working tree, and it is this snapshot that is taken as the contents of the next commit.

This command can be performed multiple times before a commit.

---

## ![Icon](icon.png) Recording changes

To save changes added to the index, use command:

    git commit

To make your actions clear for you and others, it is necessary to make log message describing the changes. Rigth syntax for this command is:
    
    git commit -m "commit massage"

That will be great if you'll make your commit message short, clear and simple.

---

## ![Icon](icon.png) Git commit command options

In some cases - for making our work with git simpler and quicker - we can use special options of commit command. For example, "-a", "all":

    git commit -a

This command automatically stage **ALL** files that have been modified and deleted, **BUT** new files you have not told Git about are not affected. 

Another useful option for git commit command is:

    git commit -am

This syntax combines git add and git commit -m commands. 

**<span style="color:#CD5C5C"> Be careful</span>** - **ALL** files and changes will be commited.

---

## ![Icon](icon.png)Changes list review

Git allows you to look through all saved changes and even switch betweem them.

All changes you've made (commited) recorded in changes list called log.

To look through log, use command:

    git log

The output is given in reverse chronological order by default and contains info about commits that are reachable by following the parent links from the given commit.

Full log info shows you data about commits: hash number, author, date and message. 

---

## ![Icon](icon.png) Git log command options

If it is no need to look through info about authors and dates git allows you to get a short log version which only contains short hashcode and commit message. To get it use command with special attribute:

    git log --oneline
    
## ![Icon](icon.png) "Versions jumping"

Git allows you to switch between different versions of the project file. All commits you've made connected in git. Working area in certain place of repository called working **tree**.

You can observ working tree through git log.

The latest actual version marked as <span style="color:#00FA9A"> <span style="color:#FFFF00"> (</span>master<span style="color:#FFFF00">)</span></span>

You can go to any commit you see in log. All you need is commit hashcode and another useful command:

    git checkout 

Put down commit hashcode (enough 4-6 symbols) after aforementioned command and you'll switch to specified commit. For example, 

    git checkout 3f4daa

Current version you're working with now is marked as <span style="color:#00BFFF"> <span style="color:#FFFF00"> (</span>HEAD<span style="color:#FFFF00">)</span></span>

To go back to the latest actual version and continue your work use: 

    git checkout master

## ![Icon](icon.png) Git log command options \#2

Now you now how to switch file versions. For example, you went to one of the earliest version. It could be useful to have an apportunity to see the future - see what you or your collegues had alredy done. But if you use git log command after switching to earlier version, you will see onle part of log - from the very begginig to version there you are now.

To see all changes despite your current "place" use:

    git log --all

This argument shows you all log, where you current version would be marked as  <span style="color:#00BFFF"> <span style="color:#FFFF00"> (</span>HEAD<span style="color:#FFFF00">)</span></span>   

You can also use both arguments:

    git log -- oneline -- all

As a result you will see an entire commits list in it's short version.

## ![Icon](icon.png) What is the difference?

Imagine you work hard all nigth long, you are almost finished, added your changes to index and decided to make a cup of coffee before the final shoot...
And after you came back, you found out that you didn't commit last changes!

Don't panic. Use:

    git diff

This command shows you the difference between last complieted commit and the index.

You can also use 

    git diff hash1 hash2 

to compare different commits.

Note, using __*hash1*__ **hash2** you see how the second commit differ from the first.

Using __*hash2*__ **hash1** you get how the first commit differ from the second. 


## ![Icon](icon.png) Git and images

If you have a beautiful picture on your computer and want to add it in your *.md file, you need to place it in git tracked repository (folder) and use structure below:

    ![Replacing_text](image_file_name)

*Replacing_text* - it is what you see if program can't reach image file path.

*image_file_name* - name of file, which was placed into tracked repository. Watch the register!

![GitFamilyLogos](image.png)

GIT was made for changes  tracking in text files. And that it is brilliant in. It isn't used to track image files. It takes loads of memory and mistakes are possible. So, to avoid valueless efforts it is better to use special file __gitignore__.

You can create it with help of VSCode explorer. It is important to put dot before typing "gitignore". 

Don't forget to commit gitignore creation. 

Go to gitignore and type in image file name. Save and commit it. Done - git won't track image file.

You can use gitignore not only for images, but what ever you want git to ignore.

## ![Icon](icon.png) Branching

Branches in Git are used for

Branches in Git are used for encapsulating changes. In Git, branches are a part of everyday development process.  When you want to add a new feature or fix a bug — no matter how big or how small — you spawn a new branch.

### ![Icon](icon2.png) New branch creating

To create a new branch use

    git brabch <branch_name>

Be careful choosing _branch_name_ it would be great if name of the branch tell your collegues what part of your job in there.

### ![Icon](icon2.png) Branches switching



### ![Icon](icon2.png) Branches merge

To push changes from one branch to another...

#### Merge conflicts

If the same string/text in different file versions typed different then you will face conflict when trying merging.
