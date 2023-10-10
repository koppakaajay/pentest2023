# Challenge Description
We need to find a way to connect an ssh server
# Approach
Found two of the most important clues for this challenge that the username was **john** and since the challenge name was hydra and as the '**rock you**' word was in bold, I
so I thought to bruteforce it with hydra using rockyou.txt file as a wordlist. found the password as "**eminem**"
logged into the ssh server with username as john and password as eminem, found the password in the **user.txt** file by simple ls and cat commands
# Flag found
  `p3nt35t{tr4c3_m4k3_1t_m0r3_t0ugh3r}`
