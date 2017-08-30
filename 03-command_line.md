# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > Cheat sheet of commands
* show current working directory path - pwd
* creating a directory - mkdir
* deleting a directory - rmdir
* creating a file using `touch` command - touch new_file 
* deleting a file - rm
* renaming a file - mv
* listing hidden files - ls -ld .?*
* copying a file from one directory to another cp source destination
* changing permissions - chmod 777 filename
* checking scratch usage - free -g
---


### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  - list
`ls -a`  - list all
`ls -l`  - long list
`ls -lh`  - long list human readable
`ls -lah`  - long list all human readable
`ls -t`  - sort list my modification time
`ls -Glp`  - do not list group as part of long list and append indicator slash to directories

> > 

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ll -goh
ll -t
ll -u
ll -gon
ls -lah

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs takes a command as an argument and applies that command on data it takes in from standard input
The following command takes two arguments in from standard input separted by a space and takes them as arguments in the find command i.e. find all files ending in .csv or .txt.
xargs -n 1 find -name
"*.csv" "*.txt"


 

