# My app git practice 2

this is my app practice2

## Description
The main idea of creating this repository is to practice git command, also README.md documentation.

## What I use for the practice:
Git v2.19.1 and macOS Sierra v10.12.6

*To check your git version, start your Terminal on mac, and use `git version`, then it'll show the current version of git you have in your mac.*
```bash
$ git version
git version 2.19.1
```

## Create files:

 1. Go to desktop, create and open new folder 'gitPractice'
```bash
$ cd desktop
$ mkdir gitPractice
$ cd gitPractice
```
*You can make sure your location by entering `pwd` command.(should be at gitPractice folder.)*
```bash
$ pwd
/Users/Spencer/desktop/gitPractice
```

 2. Create 2 new files, a html file and another javaScript file.
```bash
$ touch index.html
$ touch app.js
```

*Edit these 2 files in your text editor(atom, vs code, sublime...etc.).*


## Create repository:

 **3. To start a new repository, use `git init`, then a message will show if it's been set up successfully.**
```bash
$ git init
Initialized empty Git repository in /Users/Spencer/Desktop/gitPractice/.git/
```
**4. Use `git config` to identify the user of this repository.**
```bash
$ git config --global user.name "John Doe"
$ git config --global user.email "jd7539@example.com"
```
*You can check your config input with command `git config --list`*
```bash
$ git config --list
user.name=John Doe
user.email=johndoe@example.com
```

## Adding files to repository:

**5. Now, you can add files to your repository by using `git add`.**
```bash
$ git add .
$ git add *.html  
```
**add .**: adding all the files in the folder to the repository.\
**add \*.html**: adding all the HTML files in the folder to the repository.


**6. After you've added files to the repository, `git status` will show the status of all files that has been added.**

```bash
$ git status

Changes to be committed:
// modified files have been added but not yet committed.

Changes not staged for commit:
// modified files have not been added nor committed.

Untracked files:
// a whole new file to the repository.
```
**There are 3 file stages in git: `untracked`, `staged`, `committed`.**
  1) **Untracked files**- The file is totally new to the repository. It has not been added, neither being committed.
  2) **Staged**- The file has been added, but not committed to the repository.
  3) **Committed**- The file has not only being added, also it has been committed to the repository.

## Not staging all the files?
By including those files' name in 'gitignore' document, you can select files that you do not wish to stage to the repository.

 **1. Create 'gitignore' file by `touch` command.**
 ```bash
 $ touch .gitignore //no need extension for this document.
 ```

**2. Create a new file(or use existing file) for being included in 'gitignore'**
```bash
$ touch ignoreme.txt
```
**3. Open 'gitignore' document with text editor, write down the file name you would like git ignore staging.**\
In this case, I'm ignoring the text file 'ignoreme.txt', so I'll write down the file name in 'gitignore' document.
```bash
ignoreme.txt
```
**4. Save the document, and stage files to the repository with `git add .`, and check `git status` to see file status in the repository.**
```bash
$ git add .
$ git status
```

## Commit to the repository!

After files has been staged, they will need to be committed to the repository. \
There are 2 way of committing files to the repository,

  1)  `git commit -m '(message)'`\
  I use this command almost every time, since it's easier than the another way.
```bash
$ git commit -m 'add gitignore'
```
  2) `git commit -a`\
  If you're committing by using this command, it will look like you've opened another window. It'll show you where you're at in the repository, also what are the modification included in this commitment.\
  *To finish and quit the commit command, press [esc] then type ':wq' [enter] to quit edit mode.*
```bash
$ git commit -a
```
```bash
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
# Your branch is up to date with 'origin/master'.
#
# Changes to be committed:
#       modified:   gitignore
:wq
```  

## Before going further...
Check `git status`, to see whether all files are committed to the branch, and ready to go on github.
```bash
$ git status
On branch master
nothing to commit, working tree clean
```

## Getting ready with github...

1. Go to github, log in and create a new repository.
2. Copy the https url. and back to local Terminal.
 *your url should look similar to: \
 https://github.com/(UserID)/(repository).git*

## Linking to github by remote branch:

1. Check remote branch with `remote`
```bash
$ git remote
origin
```
2. Connecting to your github repository by usign `git remote add origin (repository url)`
```bash
$ git remote add origin https://github.com/JessicaTHH/gitpractice.git
```
If there's a origin remote branch already, remove it and add again with the copied url from github.
```bash
$ git remote rm origin
$ git remote add origin https://github.com/JessicaTHH/gitpractice.git
```
3. Finally, push your local repository to your remote repository on github, using `git push -u origin master`
```bash
$ git push -u origin master
```
## A few more useful command that might need during the future.

`$ git push` *pushing local repository to github.*
`$ git pull` *to see changes if anyone has push their modified files onto the same repository.*
`$ git clone (repository url)` *clone the whole repository from github.*
`$ git checkout (branch)` *switching from current branch to the designated branch.*
`$ git merge (branch)` *merging the designated branch to the current branch.*
```bash
$ git checkout master // switching to master branch from the current branch.
$ git merge formerbranch //merging formerbranch with the current branch.
```
---

## README.md
*The first thing that shows when a viewer is visiting a repository, is READNE documentation.\
This is why README document should contain  basic info such as the summary of the repository, the guide lines of this repository or any other details that can assist viewers get to know the repository immediately.*

1. To **create a README document**, go to the location that you would want to put README document, then use command `touch`
```bash
$ touch README.md
```
2. **Open README.md in text editor**, and start editing the file.
This [helpful website](https://commonmark.org/help/) get me through formatting my README file. They also provide a [interactive tutorial](https://commonmark.org/help/tutorial/index.html), which is easy to learn and understand what is markdown text file format.

---
## Last but not least...

**always remember 3 steps to finish a project:**

1. `$ git add .` : adding all the completed files to the repository.
2. `$ git commit -m '(message)' ` : adding the message of final edit.
3. `$ git push .` : push all the commitment to the remote repository on github.
