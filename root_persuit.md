# Challenge Description
A hacker has gained root access to a company's vital systems using the basic credentials: username admin, password admin via SSH. Our objective is to unravel this breach.
# Approach 
I got connected to the machine with **default username and paswword as admin**.
After getting the hint i searched about shadow in linux, and I got to know that passwords of all users are stored in /etc/shadow in form of hashes and only root can view. But since I was able to view without being root this was a security vulnearability.

After a long research I found this website **`https://blog.geoda-security.com/2019/02/privilege-escalation-exploiting-write.html`** and I learnt about privelage escalation exploitation in that.

That website has a step-by-step instructions onh how to solve it. After going through it, I checked if I had write permission to that file and surprisingly I had it. Now the next biggest challenge was there was no text editor like nano, leaf or vim.

So I had to look through for it again, and then found we can edit using `cat >` command. Then i just did `cat /etc/shadow` then i copied the whole thing. pasted it in a text document in my system and replaced root's hash with admin's hash.
Then I copied it again and used the command `cat > /etc/shadow` and I pasted the whole thing and hit `ctrl+D` to write it.

Since now they both have the same hash the **password for root is also admin**. Now i logged into rootand got the flag from /root/root.txt
# Flag Found
`p3nt35t{y3s_th4t_1s_sh4d0w}`
