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

## Create and modify files:

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


 3. To start a new repository, use `git init`, then a message will show if it's been set up successfully.
```bash
$ git init
Initialized empty Git repository in /Users/Spencer/Desktop/gitPractice/.git/
```
 4. Use `git config` to identify the user of this repository.
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

 5. Now, you can add files to your repository by using `git add`.
```bash
$ git add .
$ git add *.html  
```
**add .**: adding all the files in the folder to the repository.\
**add \*.html**: adding all the HTML files in the folder to the repository.


6. After you've added files to the repository, `git status` will show the status of all files that has been added.

```bash
$ git status

Changes to be committed:
// modified files have been added but not yet committed.

Changes not staged for commit:
// modified files have not been added nor committed.

Untracked files:
// a whole new file to the repository.
```
**There are 3 file stages in git: untracked, staged, committed.**\
  1) **Untracked files**- The file is totally new to the repository. It has not been added, neither being committed.\
  2) **Staged**- The file has been added to the repository.\
  3) **Committed**- The file has not only being added to the repository, also it has been committed to the repository.
