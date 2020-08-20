# OverTheWire
## Bandit Level 9→ Level 10

## Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
## Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd


----------------------------------------------------------------------------------------------------------------------------


1. Connect via ssh: 

	`ssh bandit9@bandit.labs.overthewire.org -p 2220`
    The password is: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
2. I already know that the data file is going to be some type of binary or something other than text just by reading the level’s goal. Reading the file returns this:

    ![](images/level9to10.reading.data.not.human.png?raw=true)

3. I know the file looks binary so let’s just see what grep produces if we try to search it for a couple of the “=” characters.

    ![](images/level9to10.grep.results.png?raw=true)

4. Grep didn’t work, but confirmed we are working with a binary file.  The helpful commands I see that look interesting is xxd and base64. This doesn’t look like a base64 file so I’m not even going to look at the man page on that. The xxd man pages tell me that xxd is for making a hex dump of a file. So, I try that next.

    ![](images/level9to10.xxd.hex.dump.png?raw=true)

5. I see the hex dump has a human readable side. I scroll through the hex dump and I see the password. I wonder if I can extract it from that column. I try to grep the = sign and get this:

    ![](images/level9to10.grep.hex.column.first.try.png?raw=true)


6. You can see it says **th password is trKLdj**. We know there are some following lines because no password for these level has been that short. Back to the man pages where I find the **-A** option allowing me to print more lines after the last matching line.

    ![](images/level9to10.hex.human.password.png?raw=true)

The password for the next level is: **truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk**