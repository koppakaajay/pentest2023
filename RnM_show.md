# Challenge Description
we are provided credentials of a user who doesnt have sudo prvileages, but we need to become the root

# flag 1
## Approach 
After I logged with the given credentials, I first used the command `ls` to list the things in the directory. And found a user.txt file I used `cat user.txt` to check the contents of the file.

There was a clue (wherever you go it always follows you), I assumed this was similar to **root persuit** challenge, so I tried to view to shadow file (I explained in root persuit why I looked into the shadow file) using the command `cat /etc/shadow`

I was able to read that file but I wasn't able to change contents of the file, then i noticed that the users **admin and Rick had same hashes** for the password. So I switched to user Rick by the command `su Rick` and the password is **admin**

But I was still in /home/admin directory so I used ` cd ~ ` command to get to the home directory of Rick, and after doing ls and cat user.txt I found the 1st flag.
## Flag found
p3nt35t{Th3_w1z4rd5_dung30n}

# flag 2
## Approach
Inside the previous file I found a clue for the next challenge that Rick stores the password in his mysql database.
So I acessed the mysql using the command `mysql -u Rick -p` and I entered the password as **admin** when prompted.

Then after some research I learned the mysql commands, then I used show `databses;` command to list the databases. The first databse was dbrick. I selected it using `use dbrick` command

Then I used `Show tables;` to list them. I found an table called Users. I then used `describe users;` command to list the entries in it. I found 2 sections first one being the username and the other one being the password

I then used the commands `select username from users;` and `select password from users;` and I got morty's password as **Tr4c3734**. Now I did `su Morty` and entered the password and i found the flag
## Flag found
p3nt35t{Y0u_g0t_th3_su_pr1v1l4g3_4cc3ss}

# flag3
## Approach
I understood that I got sudo privelage because of the above flag, so I tried `sudo su` and after the password **Tr4c3734** I got root acess. Now I just did `cat /root/root.txt` and I got the last flag
## Flag found
p3nt35t{y0u_tr4c3d_1t}
