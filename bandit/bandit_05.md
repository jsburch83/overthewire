# OverTheWire
## Bandit Level 5 → Level 6

## Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
    • human-readable 
    • 1033 bytes in size 
    • not executable 
## Commands you may need to solve this level
ls, cd, cat, file, du, find


----------------------------------------------------------------------------------------------------------------------------


1. Connect via ssh: 

	`ssh bandit5@bandit.labs.overthewire.org -p 2220`

    The password is: **koReBOKuIDDepwhWk7jZC0RTdopnAYKh**

2. Change directories to the “inhere” folder located in your home directory and list its contents.

    ![](images/level5to6.list.inhere.contents.png?raw=true)

    That’s a lot of directories/files to look through. I need to automate the search to locate the password file or I will wasting time.  I know I need to use the **find** command so I fire up the man pages and see if there is an argument for files sizes. Sure enough there is a file size command. 
    
    ![file command](images/level5to6.find.command.by.size.of.file.png?raw=true)

3. I go with: `find -size 1033c` 

    ![](images/level5to6.find.passfile.png?raw=true)

4. So, the **.file2** is the only file that is that actual size. So, let’s read the file with the cat command and see if has the password. 

    ![](images/level5to6.read.passwordfile.png?raw=true)


5. The password for the next level is: **DXjZPULLxYr17uwoI01bNLQbtFemEgo7**