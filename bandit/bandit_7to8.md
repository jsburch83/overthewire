# OverTheWire
## Bandit Level 7 to Level 8


## Level Goal
The password for the next level is stored in the file data.txt next to the word millionth
## Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

----------------------------------------------------------------------------------------------------------------------------


1. Connect via ssh: 

	`ssh bandit7@bandit.labs.overthewire.org -p 2220`
    The password is: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

2. I read in the data.txt file in my home directly and notice the terminal scrolling with lines of data.

    ![](images/level6to7.longlist.png?raw=true)


3. I need to find the word **millionth** and get the password from that line. I already know the first thing I’m going to try is the grep command. 

    ![](images/level7to8_grep_password_in_data_file.png?raw=true)
    
The password for the next level is: cvX2JJa4CFALtqS87jk27qwqGhBM9plV