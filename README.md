# Linux Practice Project
___

## Introduction to Linux and Basic Commands
Linux is a family of open-source Unox operating systems based on the Linux Kernel. They include Ubuntu, Fedora, Debian, openSUSE and Red Hat. Using Linux to manage a Virtual Private Server (VPS) is common practice.

When operating Linux, you need to use a shell - a program that gives you access to the operating system's services. Most Linux distributions use a graphical user interface (GUI), making them beginner-friendly.

However, we recommend utilizing the command-line interface (CLI) because it's quicker and offers more control. Tasks that require multiple steps on the GUI can be done in a matter of seconds by entering commands into the CLI.

So if you want to use Linux, learning the common utilities or commands will go a long way.

## What Is a Linux Command?
A Linux command is a program or utility that runs on the CLI - a console that interacts with the system via texts and processes.

It's similar to the Command Prompt application in Windows.
Linux commands are executed on Terminal by pressing Enter at the end of the line. You can run commands to perform various tasks, from package installation to user management and file manipulation.

Here's what a Linux command's general syntax looks like:

```bash
CommandName [options(s)] [parameter(s)]
```

A command may contain an option or a parameter. In some cases, it can still run without them. These are the three most common parts of a command:

CommandName is the rule that you want to perform. Option or flag modifies a command's operation. To invoke it, use hyphens (-) or double hyphens (-).

Parameter or argument specifies any necessary information for the command.

## TAKE NOTE
1. All Linux commands are case-sensitive.

2. For persons who do not have access to a linux machine you can access a light weight linux machine here free of charges Reacted.

## File Manipulation
## 1. sudo command:
The sudo command stands for "super user do" and it lets you perform tasks that require adminstrative or root user permissions. When using the sudo command, the system will promt the user to auntheticate themselves with a password.

Then, the Linus system will launch a timestap as a tracker. By default, every user can run sudo commands for 15 minutes/session.

Here's the general syntax:

```bash
sudo (command e.g apt upgrade)
```

so it becomes:
```bash
sudo apt upgrade
```

![sudo_command](./images/1.%20sudo%20command.png)

## 2. pwd command
The pwd command stands for "print working directory" and it is used to find the path of the current working directory.

The pwd command uses the following syntax:

```bash
pwd [option]
```

It has two acceptable options (flags):
* -L or logical prints environment variable content, including symbolic links.
* -P or physical prints the actual pth of the current directory.

```bash
pwd
```

## 3. cd command:
The cd command is used to navigate through the Linux files and directories. Depending on your working directory, it requires either the full path or the directory name.

Running the command will take you to the home folder. Keep in mind that only users with sudo privileges can execute it.

Let's say you're in /home directory and want to go to a sub directory called ekeikenna. Enter the following command:

```bash
cd ekeikenna
```

If you want to switch to a completely new directory, for example: /home/ekeikenna/Learning_Linux, you have to enter the cd followed by the directory's absolute path:
 
 ```bash
cd /home/ekeikenna/Learning_Linux
 ```
To move to the prevous directory. You enter the following command:

```bash
cd ..
```

## 4. ls command:
The ls command is used to list files and directories running with a system. Running it without a flag will show the current working directory's content.

```bash
ls
```
To see other directory's content, type ls followed by the desired path. For example, to view files in the Learning_Linux folder, enter:

```bash
ls /home/ekeikenna/Learning_Linux
```

Here are some options you can use with the ls command:
* lists all the files in the subdirectories:

```bash
ls -R
```

* shows hidden files in additon to the visible ones:

```bash
ls -a
```

* shows the file sizes in easily readable formats, suhc as MB, GB and TB:

```bash
ls -lh
```

## 5. cat command:
The concatenate "cat" command is the most frequently used Linux command. It lists, combines and writes file content to the standard output. To run the cat command, type cat followed by the file name and its extension. For instance:

```bash
cat sim1.txt
```

Here are other ways to use the cat command, you can try this on your own:

* Merge sim1.txt and sim2.txt and store the output in sim4.txt.

```bash
cat sim1.txt sim2.txt > sim4.txt
```

* Displays content in reverse order.

```bash
tac sim4.txt
```

## 6. cp command:
The command is used to copy the content of files or directories. Take a look at the following use cases:

* To copy a file from the current directory to another directory, enter cp followed by the file name and the destination directory. For example:

```bash
cp sim1.txt /home/ekeikenna/Learning_Linux/new_folder/
```

* To copy files to a directory, enter the file names followed by the destination directory. Follow the format below:

```bash
cp sim1.txt sim2.txt sim3.txt /home/ekeikenna/Documents
```

* To copy the content of a file to a new file in the same directory, enter cp followed by the source file and the destination file as show below:

```bash
cp sim1.txt sim4.txt
```

* To copy an entire directoy, pass the -R flag before typing the source directory, followed by the destination directory as shown below:

```bash
cp -R /home/ekeikenna/Documents /home/ekeikenna/Documents_backup
```

## 7. mv command:
The mv command is used to move and rename files and directories. Additionally, it doesn't produce an output upon execution. An example on how to use the mv command is shown below:

```bash
mv somefile /home/ekeikenna/Learning_Linux/new_folder
```

* You can also use the mv command to rename file:

```bash
mv somefile newfile
```

## 8. mkdir command:
The mkdir command is used to create one or multiple directories at once and set permissions for each them. The user executing this command must have the privilege to make a new folder in the parent directory, or they may recieve a permission denied error. 

Here's the basic synthax:

```bash
mkdir [option] directory_name
```

* For example, you want to create a directory called Music:

```bash
mkdir Music
```

* To make a new directory called Songs inside Music, use this command:

```bash
mkdir Music/Songs
```

* The mkdir command accepts many such as: 
-p or -parents create a directory between two existing folders. For example, mkdir -p Music/2020/Songs will make the new "2020" directory.

```bash
mkdir -p Music/2020/Songs
```

* To create a directory with full read, write and execute permissions for all users, enter the following command:

```bash
mkdir -m777 albums
```

To create a directory that prints a message for each created directory. Enter the following command:

```bash
mkdir -v artists
```

## 9. rmdir command:
To permanently delete an empty directory, use the rmdir command. Remember that the user should have sudo privileges in the parent directory.

* The command below shows how to remove an empty directory:

```bash
rmdir Music/2020
```

## 10. rm command:
The rm command is used to delete files within directory. Make sure the user performing the command has write permissions. Remember the directory's location as this will remove file(s) and you can't undo it.

* Here's the general synthax:
```bash
rm filename
```

* To remove multiple files, enter the following command:

```bash
rm ufc1.txt ufc2.txt ufc3.txt
```

* To remove a file giving a system confirmation prompt before deletion:

```bash
rm -i ufc.txt
```

* To delete files without system confirmation is shown below:

```bash
rm -f  yaml.txt
```

* To delete files and directories recursively:

```bash
rm -r Songs
```

## 11. touch command:
The touch command allows you to create an empty file and modify a timestamp in Linux command line.

* For example, enter the following command to create an empty file:

```bash
touch html.index
```

## 12. locate command:
The locate command can find a file in the database system. However, you have to update the database before you use the locate command to fetch a file. To udpate the database is show below:

`sudo updatedb`

* Moreover, adding -i argument will turn off case sensitivity so you can search for a file even if you don't remember the exact name. The asterisk (*) wildcard can be used in combination to look for content that contains two or more words as show below:

```bash
locate -i html*
```

## 13. find command:
The find command is used to search for files with a specific file directory  and perform susbsequent operations. Here's the general syntax:

```bash
find [path] [option] [expression]
```

* For example, to look for a file called html.index within the home directory and its subfolders is shown below:

```bash
find /home -name index.html
```

# 14. grep command:
The grep "global regular expression print" command lets you find a word by all through texts in a specific file. Once the grep command finds a match, it prints all lines that contain the specific pattern. This command helps filter through large log files.

* An example of how to use grep is shown below:

```bash
ls -l | grep snap
```

## 15. df command:
The df command is used to report the sysem's disk space, shwon in percentage and kilobyte (KB). Here's the general syntax:

```bash
df [options] [file]
```

* For example, enter the follwoing command if you want to see the current directory's system disk space usage in a human readable format:

```bash
df -h
```

* The df command can be used in combination with flags such as -m (displays file system usage in MBs), -T (displays the file system type in a new column) and -k (displays file system usage in KBs) as shown below:

## 16. du command:
The du command can be used to used to check how much space a file or directory takes up. It can be used to identify which part of the system uses the storage excessively.

* Remember, you must specify the directory path when using the du command as shown below:

```bash
du /home/ekeikenna/Learning_Linux/new_folder/Music/Music
```

* Adding flags to the du command will modify the operation, such as: -s offers the total size of a specified folder, -m provides folder and file information in MBs, -k displays information in KBs and -h displays information in human readble form in GBs as shown below:

## 17. head command:
The head command allows you to view the first 10 lines of a text. Adding an option lets you change the number of lines shown. The head command is also used to output piped date to CLI.

Here's the general syntax:

```bash
head [option] [file]
```

* For instance, you want to view the first ten line of document_list, located in the current directory:

```bash
head document_list
```

* Flags like -n or -lines prints the first customized number of lines. For example, enter head -n 5 document_list to show the first five lines of documnet_list, -c or -bytes prints the first customized number of bytes of each file, -q or -quiet will not print headers specifying the file name.They are shown below:

## 18. tail command:
The tail command displays the last ten lines of a file. It allows users to check whether a file has a new data or read error messages. Here is the general format:

```bash
tail [option] [file]
```
* For example, you want to show the last ten lines of the document_list file:

```bash
tail -10 document_list
```

## 19. diff command:
Short for difference, the diff command compares two contents of a file line by line. After analyzing them, it will display the parts that do not match. Programmers often use the diff command to alter a program instead of rewriting the entire source code. Here's the general format:

```bash
diff [option] file1 file2
```

* For example, you want to compare two files - document_list and document_list2

```bash
diff document_list document_list2
```

* Flags such as -c displays the difference between two files in a context form and -u displays the output without redundant information. They are shown below:

## 20. tar command:
The tar command archives multiples files into a TAR file -a common Linux format similar to ZIP with optional compression. Here's the basic syntax:

```bash
tar [options] [archive_file] [file or directory to be archived]
```

* For instance, you want to create a new TAR archive named newarchive.tar in the current working directory:

```bash
tar -cvf newarchive.tar newfolder
```

* The tar command accepts many options such as -x extracts a file, -t lists the content of a file and -u archives and adds to an existing archive file. They are shown below:

# File Permissions and Ownership
## 21. chmod command:
The chmod command modifies a fiel or directory's read, write and execute permissions. In Linux, each file is associated with 3 user classes - owner, group member and others. Here's the basic syntax:

```bash
chmod [option] [permission] [file_name]
```

* For example, the owner is currently the only one with full permissions to change the files deploy1.yml and deploy2.yml. To allow group members and others read, write and execute the file, chnage it to the -rwxrwxrwx permission type, whose numeric value is 777:

```bash
chmod 777 deploy1.yml deploy2.yml
```

* This command suports many options including -c or -changes displays information when a change is made, -f or -silent suppresses the error messages and -v or -v verbose displays a diagnostic for each processed file as shown below:

## 22. chown command:
The chown command lets you change the ownership of a file, directory or symbolic link to a specified username. Here's the basic format:

```bash
chown [options] owner[:group] file(s)
```

* For exampe, you want to make fabian the owner of deploy1.yml:

```bash
sudo chown fabian deploy1.yml
```

## 23. jobs command:
A job is a process that the shell starts. The job commands will display all the running processes along with their statuses. Remember that this command is only available in csh, bash, tcsh and ksh shells. This is the basic syntax:

```bash
jobs [options] jobID
```

To check the status of jobs in the current shell, simply enter jobs to the CLI. Here are some options you can use -l list process IDs along with their information, -n lists jobs whose statuses have changed since the last notification and -p lists process IDs only.

## 24. kill command:
Use the kill command to terminate an unresponsive program manually. It will signal misbehaving applications and instruct them to kill their processes.
* To kill a program, you must know its process idenfication number (PID). If you don't know the PID, run the following command:

```bash
ps ux
```

* After knowing what signal to use adn the program's PID, enter the following syntax:

```bash
kill [signal_option] pid
```

There are 64 signals that you can use, but these two are among the most commonly used:

       image here. kill1

* SIGTERM request a program to stop running and gives it some time to save all its progress. The system will use this by default if you don't specify the signal when entering the kill command. SIGKILL forces program to stop and you will lose unsaved progress. For example, the program's POD is 63773 and you want to force it to stop:

```bash
kill SIGKILL 63773
```

## 25. ping command:
The ping command is one of the most used basic Linux commands for checking whether a network or a server is reachable. In addition, it is used to troubleshoot various connectivity issues. Here's the general format:

```bash
ping [option] [hostname_or_IP_address]
```

* For example, you want to know whether you can connect to Google and measure its response time:

```bash
ping google.com
```

## 26. wget command:
The Linux command line lets you download files from the internet using the wget command. It wokrs in the background without hindering other running processes.

The wget command retrives files using HTTP, HTTPs and FTP protocols. It can perform recursive download which transfer website parts by follwoing directory structures and link creating local versions of the web pages. To use it, enter the following command:

```bash
wget [option] [url]
```

* For example, enter the follwoing command to download the latest version of WordPress:

```bash
wget https://wordpress.org/latest.zip
```

## 27. uname command:
The uname or unix name command will print detailed information about your Linux system and hardware. This includes the machine name, operating system and kernel. To run this command, simply enter uname into your CLI. Here's the basic syntax:

```bash
uname [option]
```

* These are the acceptable options to use -a prints all the system information, -s prints the kernel name and -n prints the system's node hostname.

## 28. top command:
The top command in Linux Terminal will display all the running processes and dynamic real-time view of the current system. It sums up the resouce utilization from CPU to memory usage.

The top command can also help you identify and terminate a process that may use too many system resources. To run the command, simply enter top into the CLI.

```bash
top
```

## 29. history:
With history, the system will up to 500 previously executed commands, allowing you to reuse them without re-entering. Keep in mind that only users with sudo privileges can execute this command. How this utility runs also depends on Linux shell you use. To run it, enter the command below:

```bash
history [option]
```

* This command supports many options, such as -c clears the complete history list, -d offset deletes the history entry at the OFFSET position and -a appends histroy lines.

## 30. man command:
The man command provides a user manual of any commands or utilities you can run in Terminal including the name, description and options. It cosists of nine sections:

* Executable programs or shell commands system calls Library calls Games Special files File formats and conventions System administration commands Kernel routines Miscellaneous to display the complete manual, enter:

```bash
man [command_name]
```

* For example, you want to access the manual for the ls command:

```bash
man ls
```

* Enter this command if yyou want to specify the displayed section:

```bash
man [option] [section_number] [command_name]
```

* For instance, you want to see section 2 of the ls command manual:

```bash
man 2 ls
```

## 31. echo command:
The echo command is a built-in utility that displays a line of text or string using the standard output. Here's the basic syntax:

```bash
echo [option] [string]
```

This command supports many options, such as -n displays the output without the trailing newline, -e enables the interpretation of the following backlash escapes, \a plays sound alert, \b removes spaces in between a text, \c produces no further output and -E displays the default option and disables the interpretation of backlash escapes.

## 32. zip, unzip commands:
The zip command is used to compress your files into a ZIP file, a universal format commonly used on Linux. It can automatically choose the best compression ratio. The zip command is also useful for archiving files, directories and reducing disk usage. 

* To use it, enter the following syntax: 

```bash
zip [options] zipfile file1 file2
```

* For example, you have a file named new.txt that you want to compress into archive.zip in the current directory:

```bash
zip archive.zip new.txt
```

* On the other hand, unzip command extracts the zipped files from an archive. Here's the general format:

```bash
unzip [option] file_name.zip
```

* So to unzip a file called archive.zip in the current directory, enter:

```bash
unzip archive.zip
```

## 33. hostname command:
Run the hostname to know the system's hostname. You can execute it with or without an option. Here's the general syntax:

```bash
hostname [option]
```

* There are many optional flags to use including -a or -alias displays the hostname's alias, -A or -all-fqdns displays the machine's Fully Qualified Domain Name (FQDN), -i or -ip-address displays the machine's IP address. For example, enter the following command to kmow your computer's IP address:

```bash
hostname -i
```

## 34. adduser, deluser commands:
Linux is a multi-user system meaning more than one person can use it simultaneously, adduser is used to create a new account while the passwd command allows you add/modify a password to a user. Only those with root privileges or sudo can run the adduser command.

When you use the adduser command, it performs some major changes. Edits the /etc/passwd, /etc/shadow, /etc/group and /etc/gshadow files for the newly created accounts. Creates and populates a home directory for the user. Sets file permissions and ownerships to the home directory. Here's the basic syntax:

```bash
adduser [option] username
```

* To set password:

```bash 
passwd the_password_combination
```

* For example, to add a new person named frank and modify the password, enter the following command simultaneously:

```bash
adduser frank
```

```bash
passwd frank
```

* To delete a user account, use the deluser commmand:

```bash
deluser frank
```

## 35. apt-get command:
apt-get is a command line for handling Advanced Package Tool (APT) libraries in Linux. It lets you retrieve information and bundles from auntheticated sources to mange, update, remove and install software and its dependencies. Runnig the apt-get command requires you to use sudo or root privileges.

* Here's the main syntax:

```bash
apt-get [options] (command)
```

* These are the most common you can add to apt-get: updae synchronizes the package files from their sources, upgrade installs the lastes version of all installed packages, check updates the package cache and checks broken dependencies.

```bash
apt-get update
```

## 36. nano, vi, jed commands:
Linux allows users to edit and manage files via text editor, such as nano, vi or jed. nano and vi come wiht the operating system, while jed has to be installed. 

* The nano command denotes keywords and can work with most languages. To use it, enter the followuing command:

```bash
nano filename
```

* vi uses the two operating modes to work - insert and command. insert is used to edit and create a text file. On the other hand, the command performs operations such as saving, opening, copying and pasting a file. To use vi on a file, enter:

```bash
vi filename
```

* jed has a drop-down menu interface that allows users to perform actions without entering keyboard combinations or commands. Like vi, it has modes to load modules or plugins to write specific texts. To open the program, simply enter jed to then command line.

## 37. alias, unalias commands:
alias allows you to create a shortcut with the same functionality as a command, file name or text. When executed, it instructs the shell to replace one string with another. To use the alias command, enter this syntax:

```bash
alias Name=String
```

* For example, you want to make k the alias for the kill command:

```bash
alias l='ls -ltr'
```

* On the other hand, the unalias commadn deletes an existing alias. Here's what the general syntax looks like:

```bash
unalias [alias_name]
```

## 38. su commad:
The switch user or su command allows you to run a program as a different user. It changes the adminstrative account in the current log-in session. This command is especially beneficial for accessing the system through SSH or using GUI display manager when the root user is unavailable. Here's the geberal syntax of the command:

```bash
su [options] [username [argument]]
```

When executed without any option or argument, the su command runs through root privileges. It will prompt you to aunthenticate and ise the privileges temporarily.

* Here are some acceptable options to use -p or -preserve environment keeps the same shell environment, consisting HOME, SHELL, USER and LOGNAME; -s or -shell lets you specify a different shell environment to run; -l or -login runs a login script to switch to a different username. Executing it requires you to enter the user's password.

## 39. htop command:
The htop command is an interactive program that monitors system resources and server processes in real time. It is available on most Linux distributions and you can install it usimng the default package manager.

Compared to the top command, htop has improvements and additonal features such as mouse operation and visual indicators. To use it, run the following command:

```bash
htop [options]
```

* You can also add options such as -d or -delay shows the delay between updates in tenths of seconfs, -C or -no-color enables the monochrome mode, -h or -help displays the help message and exit.

```bash
htop  -d 10
```

```bash
htop -C
```

```bash
htop -h
```

## 40. ps command:
The process status or ps command produces a snapshot of all running processes in your system.The static results are taken from the virtual files in the /proc file system.

Executing the ps command without an option or argument will list the running processes in the shell along with the unique process ID (PID), the type of the terminal (TTY), the running time (TIME) the command that launces the process (CMD)

* Here are some acceptable options you can use: -T displays all processes associated witht he current shell session, -u username lists processes associated with a specific user, -A or -e shows all the running processes.