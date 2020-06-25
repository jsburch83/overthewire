# OverTheWire
## Bandit Level 0 → Level 1

## Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
Commands you may need to solve this level
ls, cd, cat, file, du, find
----------------------------------------------------------------------------------------------------------------------------
1. Connect via ssh: 
	```bash
 	ssh bandit0@bandit.labs.overthewire.org -p 2220
	```
1. The password is: `bandit0` 
1. List the files in your home directory.
 
    ![list files in home directory](images/level0to1.list.files.png?raw=true)

1. Read the readme file that contains the next level’s password. (cat command)

1. Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1
