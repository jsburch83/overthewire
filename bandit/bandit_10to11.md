# OverTheWire
## Level 10 to 11

## Level Goal

The password for the next level is stored in the file data.txt, which contains base64 encoded data
## Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
Helpful Reading Material

    Base64 on Wikipedia

--------------------------------------------------------------------------------------------------------------------------------------------------

1. Connect via ssh: 

	`ssh bandit10@bandit.labs.overthewire.org -p 2220`
    The password is: **truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk**

2. I listed everything in my home directory to find the data.txt file. 
The goal of this is to decode a base64 file that has the password for the next level. I used the man pages to find the **-d** opiton will be used to decode the file. 

3. `base64 data.txt -d data.txt`

    ![](images/level10to11.base64.decode.data.txt.jpg?raw=true)


