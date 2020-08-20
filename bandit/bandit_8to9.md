# OverTheWire
## Bandit Level 8 to Level 9
## Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
## Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
## Helpful Reading Material
    • Piping and Redirection 

----------------------------------------------------------------------------------------------------------------------------

1. Connect via ssh: 
	
    `ssh bandit8@bandit.labs.overthewire.org -p 2220`
    The password is: **cvX2JJa4CFALtqS87jk27qwqGhBM9plV**

2.  I read in the **data.txt** file in my home directory and see that it’s random lines of data. I need to find the line that only occurs once.

    ![](images/level8to9.reading.random.data.png?raw=true)

3. I see that uniq is one of the hint commands. After reading the man pages I see it should be straight forward process with -u to only print the unique lines.

4. I tried `cat data.txt | uniq -u` and I tried `uniq -u data.txt` neither of these gave me the 1 line that was unique. I went back to the man pages and read the description a little closer. It’ says matching line from the input or standard input. Something is a foot here. I think I might need to sort the file first.

5. Running the **data.txt** file through **sort** put all the duplicates together in the list.

    ![](images/level8to9.sort.file.first.png?raw=true)

6. Now, I’m about to pipe that to the uniq command and see if I get the unique line. 

    ![](images/level8to9.uniq.password.png?raw=true)


    The password for the next level is: **UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR**