I started by performing an Nmap scan to identify open ports and services on the target machine.
<img width="1276" height="811" alt="pickle" src="https://github.com/user-attachments/assets/16fa6515-4b87-48cc-80a4-c492a7544f73" />

From the scan results, I identified open ports and a web service running on the target.
I navigated to the target IP address in the browser.
<img width="1919" height="960" alt="pickle2" src="https://github.com/user-attachments/assets/53340b3f-9ca8-42ef-8ab1-5bfd104b513f" />

Then, I viewed the page source to look for any hidden information.
<img width="1264" height="658" alt="pickle3" src="https://github.com/user-attachments/assets/bdc11d91-bd6d-4536-b66d-3933b20ffb1c" />

Next, I checked the robots.txt file to discover hidden paths or useful information.This revealed a message that would later be useful.
<img width="1056" height="184" alt="pickle4" src="https://github.com/user-attachments/assets/366b770a-b74c-414b-89a9-e7b370a25a1a" />

I used Gobuster to enumerate hidden directories and files.
<img width="1829" height="517" alt="pickle5" src="https://github.com/user-attachments/assets/6a8b7dfb-c623-4e09-aa5b-96ad7f57f1eb" />

I discovered a login.php page and i navigated to the login page.
<img width="1919" height="961" alt="pickle6" src="https://github.com/user-attachments/assets/c0f65ed2-0dc8-4b6a-ab2a-1e2765936ee6" />

Using the username and the message found in robots.txt as credentials, i successfully logged in.
<img width="1919" height="962" alt="pickle7" src="https://github.com/user-attachments/assets/cbd0d017-e86c-45c8-a0cd-f94431830820" />

After logging in, i gained access to a command execution panel.
<img width="1919" height="961" alt="pickle8" src="https://github.com/user-attachments/assets/7a314c58-d3fb-4793-b33b-be28101c53f9" />

I started by listing files using 'ls' command:
<img width="1919" height="960" alt="pickle9" src="https://github.com/user-attachments/assets/9935423a-59c4-4805-896d-a1d6179e269a" />

I found a file named Sup3rS3cretPickl3Ingred.txt, Initially, I tried reading the file using 'cat' command. 
<img width="1919" height="956" alt="pickle10" src="https://github.com/user-attachments/assets/d1918c95-0773-471d-b77d-709ba4ad34f6" />

it didnt work so i tried 'less' command:
<img width="1919" height="964" alt="pickle11" src="https://github.com/user-attachments/assets/1e361294-d7c8-4fe0-8293-1ef4679a79ef" />

This revealed the first flag.I listed files again and found clue.txt.
<img width="1917" height="966" alt="pickle12" src="https://github.com/user-attachments/assets/e2fda4c8-d548-4f1a-a194-65f11fc9a222" />

Using the command panel, i established a reverse shell using PHP and Netcat.
<img width="1918" height="954" alt="pickle13" src="https://github.com/user-attachments/assets/34ec616b-15bc-46fe-87fc-db2749a0f462" />
<img width="989" height="396" alt="pickle14" src="https://github.com/user-attachments/assets/ebe9f27e-92ae-4472-9f48-e9aaa3785034" />

then ı connected and i explored the file system and navigated to the /home directory. Inside, i found a user named rick and used 'cat' command to read second\ ingredients
<img width="260" height="908" alt="pickle15" src="https://github.com/user-attachments/assets/042d4e1a-62f7-4fe8-94e2-60a8702746dc" />
<img width="647" height="323" alt="pickle16" src="https://github.com/user-attachments/assets/139a25e0-f6dc-4006-b4c8-f7a8e0d5e233" />

thats how ı retrieved the second flag.Attempting to access the root directory initially failed due to insufficient permissions.I then used 'sudo su' command.This granted root access, allowing me to retrieve the third flag.
<img width="444" height="297" alt="pickle17" src="https://github.com/user-attachments/assets/bfc6ce95-e525-49f8-b017-1bcde90cc757" />


