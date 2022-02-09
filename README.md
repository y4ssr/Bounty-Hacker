![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/Bounty.jpeg?raw=true )

# Enumeration:
*let's run an nmap scan*.

*Command: $ nmap -sC -sV (ip)*

*replace the ip by your room's machine's ip without the quotes*

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/nmap.png?raw=true )

*As shown in the nmap scan, three ports are open*
#### 21 ftp
#### 22 ssh
#### 80 web page

## FTP: 
*let's try to login as anonymous*

*run the command : $ ftp (ip)*

*then login as ;
Username : anonymous
just hit enter no password is required*

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/files.png?raw=true )

*as you see there is two files, locks.txt and task.txt
let's use the command $ get to send them to our local machine where we can read them*

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/ftp%20files.png?raw=true )

*the first file gives us a bunch of passwords and the task.txt has something written in it as a well as a username at the end:)*
 
## Webpage:

*when going to the webpage we see almost nothing othar than dialogues btween some collegues or friends maybe *
*in this task i have used gobuster to check for any interesting hidden pages like logins maybe or some credetianls*
*lets use this command ; 
$ gobuster dir -w (wordlist) -U http://(ip)*


![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/gobuster.png?raw=true )

## Brute-Force:
*the only last thing is ssh so next thing to do is use hydra to brute-force the ssh login using the password list we got earlier (locks.txt)*

*Command : $ hydra ssh://(ip) -L lin -P locks.txt*

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/hydra.png?raw=true )

*Booom we got the lohin credetianls now let's use them to get into the ssh server*

## SSH:
*now that we have the username and password let's login :*
*Command : $ ssh (ip)*


![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/ssh.png?raw=true )

*We're in!!!*

## User Flag:

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/user.png?raw=true )

we got the first flag here 🚩!

## Privilege escalation:
*we can't access the root flag as we are just the user ***
*Let's run a $ sudo -l command to see what we can run as root without being root if it does make any sense to you😂


![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/sudo-l.png?raw=true )

*as you see we can run tar as root
*go to [gtfobins](https://gtfobins.github.io/) and search for 'tar'

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/gtfobins.png?raw=true )

