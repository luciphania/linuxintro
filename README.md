# Linux User Management assignment

## Create a user

1. Create a user named "epiphania" using the `useradd` command:
   sudo useradd epiphania
2. Set a password for the user "epiphania" using the `passwd` command
3.
![create user](<create user-1.png>)


## Set an expiry date of 2 weeks for the user

1. Set an expiry date of 2 weeks for the user "epiphania" using the `usermod` command:
   sudo usermod -e 2023-08-30 epiphaniachage
2. To check the password history and account aging information:
   chage -l epiphania

![expiration date](<password change-1.png>)


## Prompt User to Change Password on Login

1. Use the `passwd` command to prompt user to change passwd on login
   sudo passwd -x 14 epiphania
2. To check if the user "epiphania" is prompted to change their password on login:
   sudo passwd -S epiphania

![password change](<password expiration date-1.png>)

## Attach the user to a group called altschool

1. Create the group "altschool using the  `groupadd` command:sudo groupadd altschool
2.  Attach the user "epiphania" to the group called "altschool" using the `usermod` command:
   sudo usermod -a -G altschool epiphania
3. To verify the user's group membership:
   getent group | grep altschool

 ![group addition](<group addition-1.png>)


## Allow Group to Run 'cat' Command on /etc/

1. Edit the sudoers file to allow the "altschool" group to run the `cat` command on `/etc/`:
   sudo visudo
   Add the following line:
plaintext
   %altschool ALL=(ALL:ALL) /bin/cat /etc/*
2. To verify the changes in the sudoers file:
   cat /etc/group | grep altschool

![cat command](<cat command-1.png>)


## Create Another User without a Home Directory

1. Create a user named "emoshioke" without a home directory using the `useradd` command with the `-M` option:
   sudo useradd -M emoshioke
2. To check the contents of the "/home" directory (to verify no home directory for "emoshioke"):
   ls -al /home


![create userwith no home directory](<create user without directory.png>)
