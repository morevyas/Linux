# Bash Script

Bash scripting is about writing scripts (programs) for the Unix/Linux shell to automate tasks. It’s widely used for **system admin, DevOps, and everyday command-line workflows**.

 -   Bash stands for **Bourne Again Shell**
    
 -   It is a **command-line interpreter**
    
 -   Default shell in most Linux systems
    
 -   Used to interact with the OS
 -   Writing a sequence of commands in a file
    
 -   File usually has **`.sh`** extension
    
 -   Automates repetitive tasks
    
 -   Executes commands line by line
 
 
### Bash
 - A **shell** is a program that lets you interact with the operating system
 
 - Bash is powerful because it combines **command execution +
   programming + automation** in one place.
   
 -   A **scripting language** you can write logic (loops, conditions, variables)


### features of bash ###

 - Command execution
 - Scripting capability
 - Pipes and redirection

### Bash Script
A **bash script** is a text file that contains a series of commands written for the **Bash shell** (a command-line interpreter commonly used on Linux and macOS). Instead of typing commands one by one into the terminal, you can put them into a script and run them all at once.

**A file end with `.sh`**

## Key Components of Bash Scripts

The **key components of a Bash script** are the basic building blocks that make the script work.


### 1) Shebang (Interpreter line)
The **shebang** (also called the _interpreter directive_) is the very first line in a script that tells the operating system **which interpreter should execute the file**.

	#!/bin/bash

### 2) Comments
Comments are used to explain your code, they are ignore by the shell during execution.

**Single line comments**
	
	#explain a code

**Multiline comment**

end with same first and last name same

	<< comment
	explain code
	comment

### 3) Variables
Variables in shell scripting(bash) are used to store data that you can reuse throught your script.
**They are simply but very powerful**

Variables are **Mutable** (their values can be changed).

 - Variables are case sensitive
 - Avoid using special character or reserved words
 - There are no data types, all variables in Bash are strings
 - use lowercase for variables & upper case for constant
 - They valid only in a shell
 

**Declaring variable**

	name=More

**Reading variable value**

	echo "name = $name"
			or
	echo $name

**i) Environment Variables** :-

Environment variables are a core concept in Bash and Unix-like systems. They are **named values stored in the shell that affect how processes behave** and can be shared with child processes.

ex:

	echo $HOME

output:

	/home/user

**ii) Reading Variable**
It is taking input from the user and storing it in a variable. This is done using the `read` command.
ex :

	read variable_name


Options

	

 - -p : prompt a message
 - -d : set delimiter
 - -s : hide the input values



**iii) Deleting Variables**
Deleting variables in Bash is straightforward

	unset
	
**basic deletion**

	unset variable_name

**Environment variables**

	export NAME="More"
	unset NAME


### A Simple addition program

	# Shebang line
	#!/bin/bash  
	x=10
	y=20
	result="$x + $y"
	add_result=$(( x + y ))
	echo "addition = $add_result"


## Arrays

**Arrays is a store a multiple values in a single variables.**
Array is a collection of similar or dissimilar types, and it is very useful when **working with lists** of items like files, names, or numbers.

**Declare an array**

	arr=(apple mango guava)

**Accessing an elements**

 Read the **first value**


	echo ${arr[0]}  # 0 is a index number

Read the **last element**	

	echo ${arr[2]}  #(2) you known a index value
	echo ${arr[-1]}
 Read the **all element**

	echo ${arr[0]}

Find the **length of array**

	echo ${#arr[@]}

**Add** a new element

	arr=$( "${fruits[@]}" "pineapple")
	echo ${arr[@]}

**Remove** a element

	unset arr[2]
	echo ${arr[@]}


	 
	

 

	
