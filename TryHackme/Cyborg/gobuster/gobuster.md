gobuster dir -u http://10.10.170.174/ -w /usr/share/dirb/wordlists/common.txt 
===============================================================
Gobuster v3.1.0
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.10.170.174/
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/dirb/wordlists/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.1.0
[+] Timeout:                 10s
===============================================================
2022/10/01 10:34:37 Starting gobuster in directory enumeration mode
===============================================================
/.hta                 (Status: 403) [Size: 278]
/.htaccess            (Status: 403) [Size: 278]
/.htpasswd            (Status: 403) [Size: 278]
/admin                (Status: 301) [Size: 314] [--> http://10.10.170.174/admin/]
/etc                  (Status: 301) [Size: 312] [--> http://10.10.170.174/etc/]  
/index.html           (Status: 200) [Size: 11321]                                
/server-status        (Status: 403) [Size: 278]                                  
                                                                                 
===============================================================
2022/10/01 10:35:59 Finished
===============================================================
