# OverTheWire
## Bandit Level 1 → Level 2

## Level Goal
The password for the next level is stored in a file called - located in the home directory
Commands you may need to solve this level
ls, cd, cat, file, du, find
Helpful Reading Material
    • Google Search for “dashed filename” 
    • Advanced Bash-scripting Guide - Chapter 3 - Special Characters 

----------------------------------------------------------------------------------------------------------------------------
## Walkthrough

1. Connect via ssh: 
	```
	ssh bandit1@bandit.labs.overthewire.org -p 2220
	```
	The password is: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

1. List the files in your home directory. (ls command)

	![list files in home dir](images/level1to2.listing.files.with.dashes.in.linux.bandit1.png)

	As you can see the file is named with a single dash. After reading the Helpful Reading Material I was able to read the file with this command. 

1. ` cat ./-`

	![read linux file with a dash that starts in the name](images/level1to2.reading.dashed.file.names.inlinux.bandit1.png)

1. Password: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
