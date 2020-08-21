# OverTheWire
## Bandit Level 11 to Level 12

## Level Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions


## Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Helpful Reading Material

    Rot13 on Wikipedia
    
--------------------------------------------------------------------------------------------------------------------------------------------------------------



1. Connect via ssh:

    `ssh bandit10@bandit.labs.overthewire.org -p 2220`
    The password is: **IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR**

2. I know for this level I will need to rotate the letters 13 places. After looking at all my helpful commands for this level I think I will man page the tr command. 

3. After reading the man pages the **tr** command seems like it will do the job. From what I read it looks like I can have two sets to *translate* from and to. 

4. I piped the data.txt file into the **tr** command with the two sets to do the translations. 

   ![](images/level11to12.translate.rot13.file.jpg?raw=true)

5. The password for the next level is: **5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu**

