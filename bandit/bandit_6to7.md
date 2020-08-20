# OverTheWire
## Bandit Level 6 → Level 7


## Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:
    • owned by user bandit7 
    • owned by group bandit6 
    • 33 bytes in size 

## Commands you may need to solve this level
ls, cd, cat, file, du, find, grep

----------------------------------------------------------------------------------------------------------------------------

1. Connect via ssh: 

	`ssh bandit6@bandit.labs.overthewire.org -p 2220`
    The password is: **DXjZPULLxYr17uwoI01bNLQbtFemEgo7**

2. I will start by checking the man pages for **find** to see if there is any type of user/group owner attribute.

    ![](images/level6to7.find.attribute.manpages.group.png?raw=true)

    ![](images/level6to7.find.attribute.manpages.userowner.png?raw=true)


    I now have to attributes to feed the find command to satisfy our goal level requirments. The file has to be own by the user bandit7 and owned by the group bandit6. I also know that the file needs to be 33 bytes in size so that helps narrow down the password file as well. 


3. The command I will use is: `find -size 33c -group bandit6` 

    ![](images/level6to7.longlist.png?raw=true)

    I actually see the file I need to solve this level, but for better clarity let’s try to clean things up a bit. I need to pipe the results to grep and then make it exclude any files with denied on the line. So, I head over the man pages for grep and find there is an invert command that will allow me to pick non matching lines.
    The command I went with was:

    `cd /`
    `find -size 33c -group bandit6  2>&1 | grep -v "Permission denied" | grep -v`
    `"No such file or directory"`

    ![](images/level6to7.2files.to.list.png?raw=true)

    Looks like the file I want is the **var/lib/dpkg/info/bandit7.password**

    ![](images/level6to7.pass.png?raw=true)

    The password for the next level is: **HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs**