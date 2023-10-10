# Challenge Description
we need to Identify the number of open services and the Harry's nc port running behind the system ip <43.205.129.227>
# Approach
Read the reference provided for the challenge,learned about namp. used the command `nmap -sV 43.205.129.227` to determaine the open ports and service running behind that
ip address. found a ssh service at port 22, acmsoda service at port 6969 and also an unrecognised service. Got a verbose stating **"Harry's\x20Port\x20is\x20969\n"**. Hence
I found that harry's port was 969. submitted the flag as per the format
# Flag found
`p3nt35t{3_969}`
