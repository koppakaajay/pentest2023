# challenge Description
This is a boot2root challenge where we have to try to exploit the vulnerabilities in the system so that we can get root privelages

# Flag 1
## Approach
Here I first ran nmap to look out for open ports with the command `nmap 15.207.72.201 -p- 1000` because the clue was jedi is always like the first 1000 portals, and I found a port (port no. 234) also with an unknown service. I used netcat to 
connect to it by the command `nc 15.207.72.201 234` and I got my first flag
## Flag found


# Flag 8
## Approach
After i found port 80 was open in itsystem I connected to it, to findout more about this challenge. But i couldn't find anything so I used the dirb command `dirb 15.207.72.201:80` to search for hidden links and texts. I then found the link robots.txt at http://15.207.72.201/robots.txt
In that I found the link to two pages one is f1ag.txt at http://15.207.72.201/f1ag.txt, where I found the flag. and there was other link to login.html at http://15.207.72.201/login.html
## Flag found
`p3nt35t{7HErEs_AlwAys_4_BI9ger_F1sh}`
