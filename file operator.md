### File operators are used in conditional statements in shell scripting to perform operations on files and to make decisions based on the status of such files.
 Examples of file operators includes;

1) `-e`: Checks if a file exists, When a file is a directory but still exists, the existence check is true. if yes, the condition is met. [ -e $file ]

2) `-f`: Checks if a file exists and is a regular file, The condition is true if the file is an ordinary file as opposed to a directory or special file. [ -f $file ]

3) `-d`: Checks if a file exists and is a directory; if yes, the condition is met.	[ -d $file ]

4) `-r`: Checks if a file is readable, to see if the file can be read; if yes, the condition is met.	[ -r $file ]

5) `-w`: Checks if a file is writable,to see if the file can be written; if yes, the condition is met.	[ -w $file ]

6) `-x`: Checks if a file is executable, if yes, the condition is met.
[ -x $file ]

7) `-s`: Checks if a file is not empty, to see if the file is larger than zero; if yes, the condition is met.
[ -s $file ]

8) `-L`: Checks if a file is a symbolic link

9) `-nt`: Checks if a file is newer than another file

10) `-ot`: Checks if a file is older than another file

11) `-eq`: Checks if two files have the same device and inode numbers

12) `-ne`: Checks if two files have different device and inode numbers

13) `-gt`: Checks if one file is newer than another file

14) `-lt`: Checks if one file is older than another file

15) `-ge`: Checks if one file is newer than or the same as another file

16) `-le`: Checks if one file is older than or the same as another file

17) `-k`: Checks if a file has its sticky bit set, to see if the file's sticky bit is set; if it is, the condition is met.	[ -k $file ]


18) `-u`: Checks if a file has its setuid bit set, The condition is true if the file's Set User ID (SUID) bit is set.	[ -u $file ]

19) `-g`: Checks if a file has its setgid bit set, to see if the file's set group ID (SGID) bit is set; if yes, the condition is met.	[ -g $file ]

20) `-O`: Checks if a file is owned by the current user
