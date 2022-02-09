![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/Bounty.jpeg?raw=true )

# Enumeration
*let's run an nmap scan*.

*Command: $ nmap -sC -sV (ip)*

*replace the ip by your room's machine's ip without the quotes*

![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/nmap.png?raw=true )

*As shown in the nmap scan, three ports are open*
#### 21 ftp
#### 22 ssh
#### 80 web page

## FTP 
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
 
## Webpage

*when going to the webpage we see almost nothing othar than dialogues btween some collegues or friends maybe *
*in this task i have used gobuster to check for any interesting hidden pages like logins maybe or some credetianls*
*lets use this command ; 
$ gobuster dir -w (wordlist) -U http://(ip)*


![Example](https://github.com/y4ssr/Bounty-Hacker/blob/main/images/gobuster.png?raw=true )

