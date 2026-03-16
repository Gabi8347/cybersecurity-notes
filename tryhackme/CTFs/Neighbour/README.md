İn this CTF ı first ı started with a quick network scan using nmap to identify open ports. The command I used was:
<img width="1919" height="1037" alt="nei7" src="https://github.com/user-attachments/assets/6877a1eb-f102-4b86-b581-ce6d9a9b37c5" />

This revealed two open ports, one of which was port 80, the HTTP port. I then proceeded to access the website by pasting the IP address into my browser and ı saw a login page:
<img width="1919" height="960" alt="neighbour1" src="https://github.com/user-attachments/assets/cceab6aa-f77f-4b6c-bd13-0ba2eca65673" />

I decided to view the source code of the page to look for potential credentials or hints.
<img width="1918" height="965" alt="nei2" src="https://github.com/user-attachments/assets/eb3d189b-ebd9-4229-ba39-03d45e213631" />

From the source code, I discovered the default login credentials: guest:guest. then ı tried on the login page:
<img width="1919" height="960" alt="nei3" src="https://github.com/user-attachments/assets/8b1573c6-3979-46e2-965e-be07040d429c" />

and then ı saw this page:
<img width="1919" height="965" alt="nei4" src="https://github.com/user-attachments/assets/7675c695-eb87-4570-8d0a-b291bd243b95" />

then ı view source code of this page too:
<img width="1919" height="960" alt="nei5" src="https://github.com/user-attachments/assets/e1cfa75c-3ec9-416c-9a1b-052f2b8ee34f" />

then ı noticed the message "admin account could be vulnerable, need to update" , then I modified the URL to change the user=guest parameter to user=admin.
<img width="1917" height="960" alt="nei6" src="https://github.com/user-attachments/assets/b9e5565b-200e-4f2d-afe5-459cf7d2c6e5" />

so thats how ı get the flag.




