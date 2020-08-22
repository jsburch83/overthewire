
Bandit Level 17 → Level 18
Level Goal

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19
Commands you may need to solve this level

cat, grep, ls, diff

------------------------------------------------------------------------------

1. While connected to level17 from the previous level continue working through the levels. 

2. Reading my man pages on the diff command first. I first try on side by side look of the two files and I spot the different lines. 

`diff -y passwords.old passwords.new`

![](images/level17_diff_side_by_side.jpg)

3. I want to get less on the screen so I run the command with no options. 

`diff passwords.old passwords.new`

![](bandit/images/level17-diff-standard-out.jpg)

4. So, the different line in the passwords.new file is:
**kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd**

5. We will use that as our password to level18. 

6. When connect to level18 it will connect then display "ByeBye !" and disconnect. This is all part of the level18. 




