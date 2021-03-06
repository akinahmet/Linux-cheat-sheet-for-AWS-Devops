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
| 7   | [**Linux Variables**](#linux-variables)                                 |
| 8   | [**Linux getting help**](#linux-getting-help)                           |
| 9   | [**Filters and Control Operators**](#filters-and-control-operators)     |
| 10   | [**Using Package Managers in Linux**](#using-package-managers-in-linux)|
| 11   | [**Shell scripting**](#shell-scripting) 




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


### Managing Users and Groups

1. **sudo**: The `sudo` (superuser do) command gives some admin privileges to non-admin users 

    List available commands:

    ```bash
    sudo -l
    ```

    Run command as root:

    ```bash
    sudo 
    ```

    Run command as root:

    ```bash
    sudo -u root 
    ```

    Run command as user:

    ```bash
    sudo -u user 
    ```

    Switch to the superuser account:

    ```bash
    sudo su
    ```
2. **Basic User Commands**: 

    Your username is indicated by the `whoami` command.
    ```bash
    whoami
    ```

    The `who` command will provide you with details about who is logged on the system.
    ```bash
    who
    ```

    Command `who am i` the who command will only show the line that points to your current session.
    ```bash
    who am i
    ```

    The `w` command will inform you who is logged on and what they are doing.
    ```bash
    w
    ```

    The `id` command will provide your user id, your primary group id, and a list of the groups you belong to.
    ```bash
    id
    ```

    The `su` command enables a shell to be run as another user.
    ```bash
    su
    ```

    The `su` command retains the same shell environment by default. To become another user and also get the environment of the target user, issue the `su -` command followed by the target username.

    If `su` or `su -` is not provided with a username, the command assumes that root is the target.

    The root user does not have a password set on some Linux systems like Ubuntu and Xubuntu. On these Linux systems, You can become root user via `sudo su` command.

3. **User Management**:

    On Linux, the local user database is `/etc/passwd`.
    ```bash
    /etc/passwd
    ```

    `root` user also called the superuser is capable of doing almost everything.
    ```bash
    root
    ```

    The `useradd` command is used for creating a new user. 
    ```bash
    useradd
    ```

    You can delete a user with `userdel` command. 
    ```bash
    userdel
    ```

    With the `usermod` command, you can modify a user's properties. 
    ```bash
    usermod
    ```

    User passwords can be set with the `passwd` command.
    ```bash
    passwd
    ```

3. **Group Management**:

    `groupadd` command is used to create a new group.
    ```bash
    groupadd
    ```

    You can change group membership with the `useradd` or `usermod` command.
    ```bash
    useradd
    ```
    or
    ```bash
    usermod
    ```

    `groups` command is used to display a list of groups to which the user belongs.
    ```bash
    groups
    ```

    `groupmod` command can be used to change the group name.
    ```bash
    groupmod
    ```

    `groupdel` command is used to delete a group.
    ```bash
    groupdel
    ```

    With the `gpasswd` command, we can add a user to a group and to remove a user from a group. In the example below:
    ```bash
    gpasswd -a
    ```
    ```bash
    gpasswd -d
    ```


**[⬆ Back to Top](#table-of-contents)**

### File permissions


**1.Ownership:**

`chown` – change ownership.

**2.Permissions:**

`chmod` – change permissions

The breakdown of permissions:

    u – user

    g – group

    o – other

The permissions you can give to a file or folder:

    r – read

    w - write

    x - execute

    4 if read permission is desired.
    
    2 if write permission is desired.
    
    1 if execute permission is desired.

    Thus 7 means read+write+execute, 6 means read+write, and 5 means read+execute.    

Using the -R switch is important. If you want the permissions to apply from the parent object to  child objects (the sub-folders and files), you must use the -R (recursive).


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

### Vi Vim commands

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

### Linux Variables

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


### Linux getting help

    1. The man pages
    2. The info pages
    3. The whatis command
    4. The help option


**[⬆ Back to Top](#table-of-contents)**

### Filters and Control Operators

**1.Using Filters:**

​`cat`

    - Concatenate files and print on the standard output​
    - Create a folder and name it examples.​

    ```bash
    cat example.txt
    ```

​`tee`

- Read from standard input and write to standard output and files​
- Write the content of the example.txt file in reverse order to another file named temp.txt and display the content of temp.txt in reverse order.

    ```bash
    tac example.txt | tee temp.txt | tac
    ```

- Check whether the temp.txt file created and display the content.​

    ```bash
    ls
    cat temp.txt
    ```

​`grep`

- Print lines that match patterns. The most common use of grep is to filter lines of text containing (or not containing) a certain string.
- Create a text file named tennis.txt.​

    ```bash
    cat > tennis.txt
​
    Amelie Mauresmo, Fra

    Justine Henin, BEL

    Serena Williams, USA

    Venus Williams, USA
    ```

`tr`

- The command 'tr' stands for 'translate’. It is used to translate, like from lowercase to uppercase and vice versa or new lines into spaces.
- Create a text file named example.txt.​

    ```bash
    cat << EOF > example.txt
    Example:This is an example.
    EOF
    ```

- In the content of example.txt, replace or translate aer letters with 'QAZ'.​

    ```bash
    cat example.txt | tr aer QAZ
    ```

- Write the content of example.txt on the same line.​

    ```bash
    cat example.txt | tr '\n' ' '
    ```

- Delete all the vowels in the content of example.txt.​

    ```bash
    cat example.txt | tr -d aeiou
    ```

- Write the whole content of example.txt in capital letters.​

    ```bash
    cat example.txt | tr [a-z] [A-Z]
    ```

​`wc`

- Print line, word, and characters for each file.


    ```bash
    wc example.txt
    ```

- Find how many users are there in the computer.

    ```bash
    wc -l /etc/passwd
    ```

`sort`

- The sort filter will default to an alphabetical sort. The sort filter will default to an alphabetical sort.

    ```bash
    sort example.txt
    ```

- Sort the content of example.txt in reverse order.​

    ```bash
    sort -r marks.txt
    ```

`uniq`

- Report or omit repeated lines. With the help of uniq command you can form a sorted list in which every word will occur only once.


- Display only the unique names in the content of example.txt.​before using uniq command, the file must be sorted

    ```bash
    sort example.txt | uniq
    ```

`comm`

- Compare two sorted files line by line. By default, comm will always display three columns. First column indicates non-matching items of first file, second column indicates non-matching items of second file, and third column indicates matching items of both the files.

- Both the files has to be in sorted order for 'comm' command to be executed.​

    ```bash
    comm file1.txt file2.txt
    ```

**[⬆ Back to Top](#table-of-contents)**

**2.Using Control Operators:**

`;`
​
- More than one command can be used in a single line with `;`.

- Write two seperate cat command on the same line using ;.
​
```bash
cat days.txt ; cat count.txt 
```
`&`

- When a line ends with an ampersand &, the shell will not wait for the command to finish. You will get your shell prompt back, and the command is executed in background. You will get a message when this command has finished executing in background.
​
- Run sleep 20 command and let this command work behind while you're running other commands.
​
```bash
sleep  20 &
ls -l
cat count.txt
cat days.txt
```

`$?`
​
- This control operator is used to check the status of last executed command. If status shows '0' then command was successfully executed and if shows '1' then command was a failure.

- Run ls command and show that it is executed successfully.
​
```bash
ls
echo $?
```

- Run lss command and show that it failed.
​
```bash
lss
echo $?
```

`&&`

- The command shell interprets the && as the logical AND. When using this command, the second command will be executed only when the first one has been successfully executed.
​

`||`

- The command shell interprets the (||) as the logical `OR`. This is opposite of logical `AND`. Means second command will execute only when first command will be a failure.
​

`&& and ||`

- We can use this logical AND and logical OR to write an if-then-else structure on the command line. This example uses echo to display whether the rm command was successful.
​

`#`

- Everything written after a pound sign (#) is ignored by the shell. This is useful to write a shell comment but has no influence on the command execution or shell expansion.​


`\`

- Lines ending in a backslash are continued on the next line. The shell does not interpret the newline character and will wait on shell expansion and execution of the command line until a newline without backslash is encountered.

- Escaping characters are used to enable the use of control characters in the shell expansion but without interpreting it by the shell.

**[⬆ Back to Top](#table-of-contents)**

### Using Package Managers in Linux

**1.Amazon Linux Instance:**

- Update Amazon Linux Instance.
​
```bash
sudo yum update
```

- Check if 'git' is installed on Amazon Linux instance.
​
```bash
git --version
```

- Install git on Amazon Linux instance.
​
```bash
sudo yum install git
```
- Uninstall git on Amazon Linux instance.
​
```bash
sudo yum remove git
```

- Install git on Amazon Linux instance without any interruption.
​
```bash
sudo yum install git -y
```

- Uninstall git with dependencies on Amazon Linux instance without any interruption.
​
```bash
sudo yum autoremove git -y
```

- List all available packages for Amazon Linux instance.
​
```bash
sudo yum list
```

- List all available git packages for Amazon Linux instance.
​
```bash
sudo yum list git
```

- List all installed packages on Amazon Linux instance.
​
```bash
sudo yum list installed
```
- Check the available version of git with info command.
​
```bash
sudo yum list git
```

**[⬆ Back to Top](#table-of-contents)**

**2.Ubuntu:**

Update Ubuntu instance

```bash
sudo apt update
```
- Upgrade the packages. This command installs the listed available packages.

```bash
sudo apt upgrade
```

- Check if 'git' is installed on Ubuntu instance.
​
```bash
git --version
```

- Check the info for the git package installed on Ubuntu instance.
​
```bash
sudo apt info git
```

- List all available packages for Ubuntu instance.
​
```bash
sudo apt list
```

- List all installed packages on Ubuntu instance.
​
```bash
sudo apt list --installed
```
​
**[⬆ Back to Top](#table-of-contents)**

### Shell scripting

**Shell scripting basics**

- Create a folder and name it shell-scripting.

```bash
mkdir shell-scripting && cd shell-scripting
```

- Create a `script` file named `basic.sh`. Note all the scripts would have the .sh extension.

```bash
#!/bin/bash
echo "Hello World"
```

- Before we add anything else to our script, we need to alert the system that a shell script is being started.
This is done specifying `#!/bin/bash` on the first line.

- After to save the above content, we need to make the script executable.

```bash
chmod +x basic.sh
```

- Then we can execute the `basic.sh`. To execute basic.sh, it is required to add `./` beginning of the `basic.sh`. `./` means we're calling something in the current working directory. We have to specify the path for executables if they're outside our $PATH variable.

```bash
./basic.sh
```

- We can add the other shell commands to our script.

```bash
#!/bin/bash
echo "hello"
date
pwd
ls
```

- And execute again.

```bash
./basic.sh
```
​
**[⬆ Back to Top](#table-of-contents)**

**If Statement**


```bash
#!/bin/bash
read -p "Input a number: " number

if [[ $number -gt 50 ]]
then
  echo "The number is big."
fi
```

- Relational Operators

| Operator | Description |
| -------- | ----------- |
| -eq   | equal                  |
| -ne   | not equal              |
| -gt   | greater than           |
| -lt   | less than              |
| -ge   | greater than or equal  |
| -le   | less than or equal     |

- String Operators

| Operator | Description |
| -------- | ----------- |
| =    | equal            |
| !=   | not equal        |
| -z   | Empty string     |
| -n   | Not empty string |

- File Test Operators


| Operator | Description |
| -------- | ----------- |
| -d file   | directory  |
| -e file   | exists     |
| -f file   | ordinary file     |
| -r file   | readable          |
| -s file   | size is > 0 bytes |
| -w file   | writable          |
| -x FILE   | executable        |

**If Else Statements**


```bash
#!/bin/bash
read -p "Input a number: " number

if [[ $number -ge 10 ]]
then
  echo "The number is bigger than or equal to 10."
else 
  echo "The number is smaller than 10"
fi
```

**If Elif Else Statements**


```bash
#!/bin/bash
read -p "Input a number: " number

if [[ $number -eq 10 ]]
then
  echo "The number is equal to 10."
elif [[ $number -gt 10 ]]
then
  echo "The number is bigger than 10"
else 
  echo "The number is smaller than 10"
fi
```

**Boolean Operations**

The Boolean operators below are supported by the Bourne Shell.

| Operator | Description |
| -------- | ----------- |
| !        | negation    |
| &&       | and         |
| ||       | or          |

**[⬆ Back to Top](#table-of-contents)**

**While loops**

```bash
#!/bin/bash

number=1

while [[ $number -le 10  ]]
do
  echo $number
  ((number++))
done
echo "Now, number is $number"
```

**Until loops**

- The until loop is identical to the while loop, except that it will execute the commands within it until the test becomes true.

```bash
#!/bin/bash

number=1

until [[ $number -ge 10  ]]
do
  echo $number
  ((number++))
done
echo "Now, number is $number"
```

**For loops**

```bash
#!/bin/bash

echo "Numbers:"

for number in 0 1 2 3 4 5 6 7 8 9
do
   echo $number
done

echo "Names:"

for name in Joe David Matt John Timothy
do
   echo $name
done

echo "Files in current folder:"

for file in `pwd`/*
do
   echo $file
done
```
**[⬆ Back to Top](#table-of-contents)**

**Using arrays with the for loop**

```bash
#!/bin/bash

devops_tools=("docker" "kubernetes" "ansible" "terraform" "jenkins")

for tool in ${devops_tools[@]}
do
   echo $tool
done
```

**Continue and Break Statements**

```bash
#!/bin/bash

number=1

until [[ $number -lt 1  ]]
do
  ((number++))
  
  tens=$(($number % 10))
  
  if [[ $tens -eq 0 ]]
  then
    continue
  fi

  echo $number
    
  if [[ $number -gt 100 ]]
  then
    break
  fi
done
```

**Select loops**

```bash
#!/bin/bash

read -p "Input first number: " first_number
read -p "Input second number: " second_number

PS3="Select the operation: "

select operation in addition subtraction multiplication division exit
do
  case $operation in
    addition) 
      echo "result= $(( $first_number + $second_number))"
    ;;
    subtraction)
       echo "result= $(( $first_number - $second_number))"
    ;;
    multiplication)
       echo "result= $(( $first_number * $second_number))" 
       ;;
    division)
       echo "result= $(( $first_number / $second_number))"
    ;;
    exit)
       break
    ;;   
    *)
       echo "Wrong choice..." 
    ;;
  esac
done
```

**[⬆ Back to Top](#table-of-contents)**

**Shell Scripting/Functions**

```bash
mkdir functions && cd functions
```

```bash
#!/bin/bash

Welcome () {
    echo "Welcome to Linux Lessons"
}

Welcome
```

**Passing Arguments to Functions**

```bash
#!/bin/bash

Welcome () {
    echo "Welcome to Linux Lessons $1 $2 $3"
}

Welcome Joe Matt Timothy
```

**Returning Values from Functions**


```bash
pwd
echo $?  #0
pwt  # It is wrong command
echo $?  #127
```

- When a bash function completes, its return value is the status of the last statement executed in the function. We can speciy return status by using the `return` keyword. We can think the `return` keyword as exit status of function. 

- Add `return 3` line to `Welcome function`.

```bash
#!/bin/bash

Welcome () {
    echo "Welcome to Linux Lessons $1 $2 $3"
    return 3
    }

Welcome Joe Matt Timothy
echo $?
```

**Nested Functions**

```bash
#!/bin/bash

function_one () {
   echo "This is from the first function"
   function_two
}

function_two () {
   echo "This is from the second function"
}

function_one
```
**Variables Scope**

```bash
#!/bin/bash

var1='global 1'
var2='global 2'

var_scope () {
  local var1='function 1'
  var2='function 2'
  echo -e "Inside function:\nvar1: $var1\nvar2: $var2"
}

echo -e "Before calling function:\nvar1: $var1\nvar2: $var2"

var_scope

echo -e "After calling function:\nvar1: $var1\nvar2: $var2"
```