# OverTheWire

## Bandit Level 3 to Level 4

## Level Goal

The password for the next level is stored in a hidden file in the inhere directory.

## Commands you may need to solve this level

ls, cd, cat, file, du, find

----------------------------------------------------------------------------------------------------------------------------

1. Connect via ssh: 
	`ssh bandit3@bandit.labs.overthewire.org -p 2220`

The password is: **UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK**

2. Change directories to the **inhere** folder located in your home directory.

![list files in home directory](images/level3to4.chage.dir.inhere.png?raw=true)

This should be basic linux commands to get this password as the file is just hidden. Doing a basic ls command will not show the file. You will need to do at least a ls -a to view the file in the directory. 

3. `ls -a`

![list files in home directory](images/level3to4.list.hidden.files.png?raw=true)

4. Read the .hidden file with the cat command.

![list files in home directory](images/level3to4.read.hidden.file.png?raw=true)

5. The password for the next level is: **pIwrPrtPN36QITSp3EQaw936yaFoFgAB**