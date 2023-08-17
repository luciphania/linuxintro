# Linux command assignment

## Create a user
Create a user named **"epiphania"** using the useradd command: sudo useradd epiphania
Set a password for the user **"epiphania"**
![create user](<create user-1.png>)


## Set an expiry date of 2 weeks for the user
To set an expiry date of 2weeks for the user we used the command *sudo usermod -e 2023-08-30 epiphania* to set the expiry date for two weeks.

![expiration date](<password change-1.png>)


## Prompt the user to change their password upon login
To prompt the user to change their password upon login we use the command *sudo passwd -e epiphania* and then we also used the command * sudo passwd -x 14 epiphania*.

![password change](<password expiration date-1.png>)

## Attach the user to a group called altschool
 To attach user to a group we first created the alschool group using the command *sudo groupadd altschool* then we added the user epiphania into the altschool group usng the command *sudo usermod -a -G altschool epiphania*.

 ![group addition](<group addition-1.png>)


## Allow altschool group to be able to run only cat command on /etc/
to do this, we used the command *sudo visudo* to enabe us edit the epiphania root visudo by adding the command line *%altschool ALL=(ALL) / bin/cat /etc/* so that the altschool group can only  run the *cat*command.

![cat command](<cat command-1.png>)


## Create another user. make sure that this user doesn't have a home directory.
To create another user that doesnt have a home directory we made use of the command *sudo useradd -M emoshioke* to create the user **emoshioke** without an home directory.

![create userwith no home directory](<create user without directory.png>)
