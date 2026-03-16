İn this CTF i firstly did nmap scan:
<img width="1279" height="863" alt="cor1" src="https://github.com/user-attachments/assets/dc26e3f5-5400-4a88-bbde-b5f0d0f9895d" />

After identifying the IP, I navigated to the URL in my browser. The page displayed 13 different rooms. By analyzing the URLs of these rooms, I noticed that the room IDs were embedded in the URL, and they seemed to follow a MD5 hash pattern.I hypothesized that the room IDs were numeric (probably starting from 0), so I first tried id=0 and then tried id=14.
<img width="1919" height="960" alt="cor2" src="https://github.com/user-attachments/assets/67086a18-eddc-4b2d-a94f-6f25ec2ddcfd" />

so thats how ı captured flag

