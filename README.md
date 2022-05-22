# Linux-cheat-sheet-for-AWS-Devops

> Please click :star:if you like the project. 

### Table of Contents

---

| No. | Topic                                                                   |
| --- | ----------------------------------------------------------------------- |
| 1   | [**What is Linux?**](#what-is-linux?)                                   |
| 2   | [**Basic Linux Commands**](#basic-linux-commands)                       |
| 3   | [**Managing Users and Groups**](#managing-users-and-groups)                               |
| 4   | [**File permissions**](#file-permissions)                               |
| 5   | [**Search Files**](#search-files)                                       |
| 6   | [**Vi Vim commands**](#vi-vim-commands)                                 |
| 7   | [**Linux for AWS DevOps**](#linux-for-aws-devops)                           |
| 8   | [**Linux getting help**](#linux-getting-help)


                           |

1. ### What is Linux?

1. **Linux:** Linux is a family of open-source Unix-like operating systems based on the Linux kernel. We use the term “Linux” to refer to the Linux kernel.  

2. **Kernel:** A kernel is the core component of an operating system. The kernel  facilitates interactions between hardware and software components.
   

3. **Shell:** The shell is the interface that allows the users to communicate with the kernel.

  
4. **Popular Linux Distributions:** A Linux distribution  is created from a Linux kernel. To install Linux, we need to choose a distribution. There are around 600 Linux distributions, with more than 500 in active development. 

Debian

Ubuntu

Mint

Maniaro

openSUSE

RedHat

Fedora


   **[⬆ Back to Top](#table-of-contents)**

2. ### Basic Linux Commands

1. **pwd:** The pwd(Present Working Directory)  command outputs the name of the current working directory. 

   ```bash
   $ pwd
   ```

2. **cd:** The `cd` command in linux known as change directory command. It is used to change current working directory. 

    ```bash
   $ cd [directory]
    ```

    To change directory to the root directory:

    ```bash
   $ cd /
    ```

   To move inside a directory from a directory:

    ```bash
   $ cd dir_1/dir_2/dir_3
    ```

    To change directory to the home directory:

    ```bash
   $ cd ~
    ```  
    
    To move to the parent directory of current directory:

    ```bash
   $ cd ..
    ```  

3. **ls:** The `ls` command lists files and directories within the file system, and shows detailed information about them.

    ```bash
     
     ls [flags] [directory]

     Example:
     $ ls
     
     //Listing files and directories with details
     $ ls -l
     
     //Home directory
     $ ls ~
     
    ```

    The list of possible options for `ls` command:

    ```cmd
    -a Show all (including hidden)
    -R Recursive list
    -r Reverse order
    -t Sort by last modified
    -S Sort by file size
    -l Long listing format
    -1 One file per line
    -m Comma-­sep­arated output
    -Q Quoted output
    ```

4. **mkdir:** With `mkdir`(make directory) command you can create directories or folders.

   ```bash
   $ mkdir newfolder

   $ ls
   newfolder
   ```

   To create two or more directories:

   ```bash
   $ mkdir folder1 folder2 folder3

   $ ls
   folder1 folder2 folder3
   ```

5. **rmdir:** The `rmdir`(remove directories) is used to remove (empty) directories. 

   Syntax

   ```bash
   $ rmdir [option] directory
   ```
   
   Remove empty directory:

   ```bash
   $ rmdir foldername
   ```

   Remove multiple directories:

   ```bash
   $ rmdir foldername1 foldername2 foldername3
   ```

6. **touch**: The `touch` command is used to create, change and modify timestamps of a file. 

   Create a new (empty) file:

    ```bash
    $ touch file_name
    ```
   Create multiple files:

    ```bash
    $ touch file1_name file2_name file3_name
    ```
   
7. **rm**: The `rm`(remove) command is used to remove objects such as files, directories, symbolic links etc from the file system.

   Remove file: 

   ```bash
   rm file_name
   ```
      

8. **cat**: The `cat` command is very frequently used in Linux. It reads data from the file and gives their content as output. It helps us to create, view, concatenate files. So let us see some frequently used cat commands. 
     
    ```bash
    $ cat [OPTION] [FILE]
    ```

   To view a file:
   
    ```bash
    cat filename
    ```

    To view multiple files:
   
    ```bash
    cat filename1 filename2 filename3
    ```

    Create a new file:
   
    ```bash
    cat> mynewfile
    ```
    
    Copy the contents of one file to another file: 

    ```bash
    cat [filename-whose-contents-is-to-be-copied] > [destination-filename]
    ```
    To append the contents of one file to the end of another file:

    ```bash
    cat file1 >> file2
    ```

    To display content in reverse order using tac command:

    ```bash
    tac filename
    ```

9. **cp**: The `cp` command is ued to copy a file to another location.

10. **mv**: The `mv` command is used to move a file another location

11. **echo**: The `echo` command prints message to screen

**[⬆ Back to Top](#table-of-contents)**


3. ### Managing Users and Groups

1. **sudo**: The `sudo` (superuser do) command gives some admin privileges to non-admin users 

List available commands:

    ```bash
    sudo -l
    ```

Run command as root:

    ```bash
    sudo command
    ```

Run command as root:

    ```bash
    sudo -u root command
    ```

Run command as user:

    ```bash
    sudo -u user command
    ```

Switch to the superuser account:

    ```bash
    sudo su
    ```





4. ### File permissions


**1.Ownership:**


**2.Permissions:**


**[⬆ Back to Top](#table-of-contents)**

5. ### Search Files

1. **Pattern search:**
The `grep` command is used to search patterns in files.

```cmd
grep pattern files
grep -i	Returns the results for case insensitive strings
grep -n	Returns the matching strings along with their line number
grep -v	Returns the result of lines not matching the search string
grep -c	Returns the number of lines in which the results matched the search string

```

2. **Find files and directories:**

The `find` command is used to find or search files and directories by file name, folder name, creation date, modification date, owner and permissions etc and perform subsequent operations on them.

Search file with name:

```cmd
find ./directory_name -name file_name

```

Search for empty files or directories:

```cmd
find ./directory_name -empty

```



3. **Whereis to locate binary or source files for a command:**

**[⬆ Back to Top](#table-of-contents)**

6. ### Vi Vim commands

Vi is a text editor originally created for the Unix operating system.
Vim (Vi IMproved) as its name suggests, is a clone of Vi and offers more
features than Vi.

The reasons why we should use Vi/Vim editor.
● Vim is available on most linux distro’s.
● Vim Uses Less Amount of System Resources.
● Vim Supports All Programming Languages and File Formats
● Vim is Very Popular in the Linux World

Start with Vi Editor

**Command Mode:** It allows the entry of commands to manipulate text.
**Insert mode:** It allows typed characters on the keyboard into the current file.

You can create a new file or open an existing file using `vi filename` command.

```cmd
 vi newfile (Create a new file and open)
 or 
 vi existingfile (Open an existing file)

 Example to use:
 vi my_file.txt (create a new file or open the existing file)
 Press `i` to enter the insert mode
 Enter the text in the file
 Press `ESC` to quit from insert mode
 Press `:wq` to quit from vi

```

Exiting

    These commands are used to exit from the file.
    ```cmd
    :w	    # Write (save) the file, but don't exit
    :wq	    # Write (save) and quit
    :wq!	# Force write (save) and quit
    :q	    # Quit, but it fails if anything has changed
    :q!	    # Quit and throw away for any changes
    ```

**[⬆ Back to Top](#table-of-contents)**

7. ### Linux for AWS DevOps

**1.Linux Environment Variables**

- Variables can be classified into two main categories, `environment variables`, and `shell variables`. 

- `Shell variables` are valid in the current shell instance.

- `Environment variables` are variables that are valid system-wide.

**Shell variables**

The name of a variable can contain only letters (a to z or A to Z), numbers ( 0 to 9) or the underscore character (_) and beginning with a letter or underscore character.

Create a shell variable:

```bash
    $ shellvar="shell variable"
```
To call a shell variable:

```bash
    $ echo $shellvar
```

To remove a shell variable:

```bash
    $ unset shellvar
```

**Environment Variables**

Environment variables allow you to customize how the system works and the behavior of the applications on the system.

Create an environment variable:

```bash
    $ export ENVVAR="environment variable"
```
To call a shell variable:

```bash
    $ echo $ENVVAR
```
or

```bash
    $ printenv ENVVAR
```

To remove an environment variable:

```bash
    $ unset ENVVAR
```

**Other Commands**

To get a list of all shell variables, environmental variables and shell functions:

```bash
    $ set
```

To see path:

```bash
    $ printenv PATH
```

To add a directory to path:

```bash
    $ export PATH=$PATH:/home/ec2-user/test
```


8. ### Linux getting help

    1. The man pages
    2. The info pages
    3. The whatis command
    4. The help option


**[⬆ Back to Top](#table-of-contents)**
