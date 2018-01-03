# ExplodingCan

An implementation of ExplodingCan's exploit extracted from FuzzBunch, the "Metasploit" of the NSA.

## Details

* **Vulnerability**: Microsoft IIS WebDav 'ScStoragePathFromUrl' Remote Buffer Overflow
* **CVE**: [CVE-2017-7269](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-7269)
* **Disclosure date**: March 31 2017
* **Affected product**: Microsoft Windows Server 2003 R2 SP2 x86


## Why?
Months ago I needed to study this exploit, and finally I implemented it in python.

## Links

* [Fuzzbunch framework](https://github.com/x0rz/EQGRP_Lost_in_Translation)
* [Metasploit module](https://www.rapid7.com/db/modules/exploit/windows/iis/iis_webdav_scstoragepathfromurl)
* [0patching the "Immortal" CVE-2017-7269](https://0patch.blogspot.com.es/2017/03/0patching-immortal-cve-2017-7269.html)
