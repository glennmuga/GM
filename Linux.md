
## Linux commands 

Linux commands are a type of Unix command or shell procedure. 

They are the basic tools used to interact with Linux on an individual level. 

Linux commands are used to perform a variety of tasks, including displaying information about files and directories.

Linux operating system is used on servers, desktops, and maybe even your smartphone. It has a lot of command line tools that can be used for virtually everything on the system.

Basic Linux Terminal Commands

Linux Commands

Functions

1. Is command in Linux
-- Displays information about files in the current directory.
2. pwd command in Linux
-- Displays the current working directory.
3. mkdir command in Linux
-- Creates a directory.
4. cd command in Linux
-- To navigate between different folders.
5. rmdir command in Linux
-- Removes empty directories from the directory lists.
6. cp command in Linux
-- Copy files from one directory to another.
7. mv command in Linux
-- Rename and Replace the files
8. rm command in Linux
-- Delete files
9. uname command in Linux
-- Command to get basic information about the OS
10. locate command in Linux
-- Find a file in the database.
11. touch command in Linux
-- Create empty files
12. ln command in Linux
-- Create shortcuts to other files
13. cat command in Linux
-- Display file contents on terminal
14. clear command in Linux
-- Clear terminal 
15. ps command in Linux
-- Display the processes in terminal
16. man command in Linux
-- Access manual for all Linux commands
17. grep command in Linux
-- Search for a specific string in an output
18. echo command in Linux
-- Print string or text to the terminal
19. wget command in Linux
-- download files from the internet.
20. whoami command in Linux
-- Displays the current users name
21. sort command in Linux
-- sort the file content
22. cal command in Linux
View Calendar in terminal
23. whereis command in Linux
View the exact location of any command typed after this command
24. df command in Linux
Check the details of the file system
25. wc command in Linux
Check the lines, word count, and characters in a file using different options

## Questions 
# 1. What is Linux?
Linus Torvalds developed Linux, a Unix-like, free, open-source, and kernel operating system. 

Mainly it is designed for systems, servers, embedded devices, mobile devices, and mainframes and is also supported on major computer platforms such as ARM, x86, and SPARC

# 2.What are the major differences between Linux and Windows?
The following table will help in understanding the differences between Linux and Windows:

## Comparison Factor

## Linux
It is a free and open-source OS.
Linux is highly secure.
As a path separator, it uses a forward slash.
Linux is more efficient than Windows.
It uses a monolithic kernel.
Linux file systems are case-sensitive.

## Windows
It is not open-source and is free to use.
Windows is less secure compared to Linux.
Windows uses a backward slash between the directories.
Windows is less efficient.
It uses a microkernel.
Its file system is case-insensitive.

## 3. what is hard link and soft link
Hard Link : In the Linux operating system, a hard link is equivalent to a file stored in the hard drive – and it actually references or points to a spot on a hard drive. A hard link is a mirror copy of the original file.
Soft Link : In Linux, a soft link, also known as a symbolic link, is a special sort of file that points at a different file. In Windows vocabulary, you could think of it like a shortcut.

## 4.How do you mount and unmount filesystems in Linux?
In this case, you can use the ‘mount’ and ‘umount’ commands.

For mounting:

First, identify the partition through the fdisk -l command. You can also use the lsblk command for it.
After identifying the partition, create the directory which will work as the mount point. For example, running the mkdir /mnt/mountpnt will create the mountpnt directory as the mount point.
Finally, you can run sudo mount <partition> <mount_point_directory> to complete the mounting.

For Unmounting:
Once you check if the specific filesystem is in use, you can run the `sudo umount <mount_point_directory>` for unmounting.

## 5.What is the chmod command in Linux, and how do you use it?
You can use the chmod command to change the file permissions of the directories. It offers a simple way to control the read and write permissions. For instance, if you want to change the permission of the ABC.sh script and give it the write and executable permission, you can run the below command:
chmod u+wx ABC.sh

## 6. df and df -h 
df Command:

The df or disk-free command shows the used and the available disk space. You can use the additional options to check disk space differently. For instance, you can use the df -h command to check the disk usage in the human-readable format.

## 7.What is the rsync command, and how do you use this command for synchronization?
The rsync command is used to synchronize and transfer the files in Linux. 
It synchronizes files between two local systems, directories, or a network. The basic rsync command contains the following:
rsync -av ~/Documents ~/Downloads

## 8.How do you format a disk in Linux?
The mkfs or make file system command helps format the disk in the Linux system. All you need to do is use the following method to format the disk:

First, run the lsblk command to list the available partitions and identify which disk you want to format.

## 9.What is the difference between /etc/passwd and /etc/shadow files?
The /etc/passwd file stores essential user information like usernames, user IDs, home directories, and default shells. Each line in the file represents a user account.

The /etc/shadow file contains encrypted passwords and other security-related information. It is only accessible by the root user or privileged processes

## 10. chown 
 the Linux operating system, file ownership is a crucial aspect of system security and user management. The `chown` command, short for “change owner,” is a powerful tool that allows users to change the owner of files and directories

 ## 11. ls commands 
 ls -a command will display all the files including hidden files

ls -f will display all the files, but without in a sorted orde

 ls -l. The -l option signifies the long list format. This shows a lot more information presented to the user than the standard command. You will see the file permissions, the number of links, owner name, owner group, file size, time of last modification, and the file or directory name

 
