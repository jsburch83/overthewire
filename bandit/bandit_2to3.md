# OverTheWire

# Bandit Level 2 to Level 3

## Level Goal

The password for the next level is stored in a file called spaces in this filename located in the home directory.

## Commands you may need to solve this level

ls, cd, cat, file, du, find 

## Helpful Reading Material
 
 Google search for "spaces in filename"

 --------------------------------------------------------------------------------

 1. Connect via ssh:
        `ssh bandit2@bandit.labs.overthewire.org -p 2220`

The password is: **CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9**

 2. List the files in your home directory. (ls command)

    ![list files in home directory](images/level2to3.listing.spaces.file.name.linux.png?raw=true)

As you can see the file name contains spaces. You will need to put a backslash before every whitespace in the file name. You could just use the terminal’s auto complete feature by tabbing over and letting Linux auto populate the file name since it’s the only thing in the home directory. Type cat then press the tab key. 
 
 3. `cat spaces\ in\ this\ filename`

    ![list files in home directory](images/level2to3.reading.spaces.file.name.linux.png?raw=true)

 4. Password: **UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK**

