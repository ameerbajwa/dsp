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

> > Commands on terminal | Description
    -------------------- | -----------
    pwd | shows current working directiory path
    mkdir | creates a new directory in the working directory
    rm -r | removes directories 
    touch | creates a file in the current directory
    rm | removes a file
    mv | can move or rename a file
    ls -a | lists all files, unhidden and hidden in that directory
    cp | copies a file form one directory to another
    ls | lists all files and directories in the working directory
    cd | switches you into the directory you specifiy

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > Commands | Description
    -------- | -----------
    ls | lists all files and directories in the working directory
    ls -a | lists all files, unhidden and hidden in that directory
    ls -l | lists all content in long format
    ls -lh | lists all human readable content in long format
    ls -lah | lists all unhidden and hidden human readable content in long format
    ls -t | orders all files and directories by the time they were last modified
    ls -Glp | lists all content in long format while displaying the directories with '/', inhibiting displays of group information

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > Commands | Description
    -------- | -----------
    ls -c | displays files by timestamp
    ls -d | displays only directories
    ls -r | displays files in reverse order
    ls -t | displays newest files first
    ls -u | displays files by the file access time

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > The xargs command (by default) expects the input from stdin, and executes /bin/echo command over the input. Thus, whatever you type after xargs on terminal, will be echoed back one you type CTRL + d. 

 

