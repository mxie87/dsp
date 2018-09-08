# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden fills	
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

**ls**       List all files and directories in the working directory.  

**pwd**      show current working directory path, pwd stands for "print working directory". It outputs the name of the directory you are currently in, called the working directory. Use this often to check that you are in the right directory  

**cd**       cd stamds for "change directory". cd switches you into the directory you specify. The cd command takes a directory name as an argument, and switches into that directory.

**cd ..**    move up one directory (predecessor) i.e. ../../ would move up 2 levels,"cd ../../2014/dec"    

**mkdir**    creating a directory  make directory. The mkdir command creates a new directory inside the working directory. It takes in a filename as an argument, and then creates an empty dir in the current working directory.

**touch**    The touch command creates a new file inside the working directory. It takes in a filename as an argument, and then creates an empty file in the current working directory.  

**ls -a**    lists all contents, including hidden files and directories
**ls -l**    lists all contents of a directory in long format (can be in a table format)
**ls -t**    order files and directories by the time they were last modified.

**cp** 	     The cp command copies files or directories. i.e. cp frida.txt lincoln.txt - Here, we copy the contents of frida.txt into lincoln.txt.

**mv**	     move or rename file. move file command, works just like the cp command

**rm**	     deleting a file. The rm command deletes files and directories. Input multiple file names to delete multiple files. Can use * option to remove all files containing specified elements.

**rm -r**    deleting a directory. The -r is an option that modifies the behavior of the rm command. The -r stands for "recursive," and is used to delete a directory and all of its child directories.

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

> >

`ls`        list all files and directories in the working directory.
`ls -a`     lists all contents, including hidden files and directories
`ls -l`     lists all contents of a directory in long format (can be in a table format)
`ls -lh`    lists contents in long format with readable file size
`ls -lah`   combines -l -a -h options
`ls -t`     order files and directories by the time they were last modified
`ls -Glp`    

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 


`ls -c` 	Displays files by file timestamp.
`ls -d` 	Displays only directories.
`ls -p` 	Displays directories with /
`ls -q`		Displays all nonprinting characters as ?
`ls -r`		Displays files in reverse order.


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 
Xargs is a command that allows you to convert inputted data (stdin) into executable commands, often used for passing the inputted data into other commands to be called on. It is often use with find, grep and other commands.

For example:
xargs find -name “*.txt” 
In this case the find command along with its “-name” option is the argument that is passed to xargs, and then you pass the name of the file (*.txt) you want the find command to search as input.  

find -name “*.txt” | xargs grep “abc”
In this case the find command, which returns all files with .txt is passed as input to xargs. The grep “abc” is the command passed to xargs which will then use the former as input


 

