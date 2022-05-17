# Linux-cheat-sheet-for-AWS-Devops

> Please click :star:if you like the project. 

### Table of Contents

---

| No. | Topic                                                                   |
| --- | ----------------------------------------------------------------------- |
| 1   | [**What is Linux?**](#what-is-linux?)                                   |
| 2   | [**Basic Linux Commands**](#basic-linux-commands)                       |
| 3   | [**File permissions**](#file-permissions)                               |
| 4   | [**Search Files**](#search-files)                                       |
| 5   | [**Vi/Vim commands**](#vi/vim-commands)                                 |
| 5   | [**Linux getting help**](#linux-getting-help)


                           |

### What is Linux?

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

### Basic Linux Commands

1. **pwd:** The pwd(Present Working Directory)  command outputs the name of the current working directory. 

   ```bash
   $ pwd
   ```

2. **ls:**: The `ls` command lists files and directories within the file system, and shows detailed information about them.

    ```bash
     
     ls [flags] [directory]

     Example:
     $ ls
     
     //Listing files & directories with details
     $ ls -l
     
     //Home directory
     $ ls ~
     
    ```

    The list of possible options for `ls` command,

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

3. **mkdir:** With `mkdir`(make directory) command you can create directories or folders.

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

4. **rmdir:**: The `rmdir`(remove directories) is used to remove (empty) directories. 

   Syntax

   ```bash
   rmdir [option] directory
   ```
   
   Remove empty directory:

   ```bash
   rmdir FolderName
   ```

   Remove multiple directories:

   ```bash
   rmdir FolderName1 FolderName2 FolderName3
   ```

5. **touch**: The `touch` command is used to create, change and modify timestamps of a file. 

   Create a new (empty) file:

       ```bash
       touch file_name
       ```
   Create multiple files:

       ```bash
       touch file1_name file2_name file3_name
       ```
   
6. **rm**: The `rm`(remove) command is used to remove objects such as files, directories, symbolic links etc from the file system.

   Remove file: 

   ```bash
   rm file_name
   ```
   
   Remove directory: 

   ```bash
   rm -r myDir
   ```
   

7. **cat**: The `cat` command is very frequently used in Linux. It reads data from the file and gives their content as output. It helps us to create, view, concatenate files. So let us see some frequently used cat commands. 
     
     ```bash
     $ cat [OPTION] [FILE]...
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

8. **cp**: The `cp` command is ued to copy a file to another location.

9. **mv**: The `mv` command is used to move a file another location

10. **echo**: The `echo` command prints message to screen

**[⬆ Back to Top](#table-of-contents)**

### File permissions


1. **Ownership:**


2. **Permissions:**

**Change access:**

**[⬆ Back to Top](#table-of-contents)**


**[⬆ Back to Top](#table-of-contents)**

### Search Files

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

### Vi/Vim commands

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


### Linux getting help

1. The man pages
2. The info pages
3. The whatis command
4. The help option
