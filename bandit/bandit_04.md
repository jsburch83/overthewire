# OverTheWire
## Bandit Level 4 → Level 5


## Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
## Commands you may need to solve this level

ls, cd, cat, file, du, find

----------------------------------------------------------------------------------------------------------------------------

1. Connect via ssh: 

	`ssh bandit4@bandit.labs.overthewire.org -p 2220`
    The password is: **pIwrPrtPN36QITSp3EQaw936yaFoFgAB**

2. Change directories to the “inhere” folder located in your home directory.

    ![list files in home directory](images/level4to5.change.to.inhere.directory.png?raw=true)


3. Next, I will list the contents of the directory.  

    ![list files in home directory](images/level4to5.list.inhere.png?raw=true)

As you can see we have a bunch of files, but we need to know which one is human readable. So, I will go with the file command. I don’t want to call each file individual so, I will call all the files with an asterisk.   

4. `file ./*`

    ![list files in home directory](images/level4to5.list.dash.human.readable.file.png?raw=true)
    

As you can see from the screenshot that the only human readable file is **-file07**


5. Now lets read that file. 

    ![list files in home directory](images/level4to5.read.human.readable.file.png?raw=true)


6. The password for the next level is: **koReBOKuIDDepwhWk7jZC0RTdopnAYKh**