<h1>>Local Area Network Denial Attack</h1>

<h2>Description</h2>
During my time in the Georgia Tech Cyber & Network Security Bootcamp, I was tasked with coming up with my own project. When it comes to the field of cyber security, I am more so interested in the attacks and penetration testing side of things. For this reason I decided to look up some form of an attack that I would be able to launch on my own. I ended up deciding to do LAND attack. A LAND attack is conducted by the attacker sending spoofed TCP SYN packets where the source and destination IP and ports are the same. The target machine then continiously tries to reply to itself, resulting in all of its' resources being used and it freezing up or crashing.

<br />


<h2>Technology & Tools</h2>

- <b>Windows XP</b></br>
- <b>Kali Linux</b></br>
- <b>Nmap</b></br>
- <b>Hping3</b></br>
- <b>Ping</b></br>


<h2>Steps to Conduct the Attack</h2>

- <b>1. Next I needed to make sure that I knew the IP addresses to my Windows XP machine and the Kali Linux machine, so I used the ifconfig / ipconfig command to do so.</b></br>
- <b>2. The two machines needed to be able to talk to one another, so next I pinged the Windows XP machine from the Kali Linux machine and vice versa.</b></br>
- <b>3. Since I'm simulating an attack, I have to conduct reconnaissance, so I ran an Nmap scan on the IP address for the Windows XP machine (192.168.56.101) I found that port 135 was open.</b></br>
- <b>4. Since I'm simulating an attack, I have to conduct reconnaissance, so I ran an Nmap scan on the IP address for the Windows XP machine (192.168.56.101) to see what ports (135, 139, 445) are open.</b></br>
- <b>5. Next, I used Hping3 and ran the following command: "hping3 -S 192.168.56.101 -a 192.168.56.101 -k -s 135 -p 135 --flood"</b></br>

- <b><a href="https://docs.google.com/presentation/d/16_dxqSPwF-r8-rtiIK-lcZNwy8_tziCDOjyGTKN1a9Q/edit?usp=sharing">Splunk Log Analysis</a></b>

<p align="center">
