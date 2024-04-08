## Tools 
- Wireshark
- [md5sum](https://en.wikipedia.org/wiki/Md5sum)
- [VirusTotal](https://www.virustotal.com/gui/home/upload)
- [TeslaDecrypt](https://github.com/Cisco-Talos/TeslaDecrypt/releases/tag/1.0)
## Hints
For the operating system details we can go to Statistics -> Capture File Properties.

In order to download malicious file for further analysis go to File -> Export Objects -> HTTP...

Domain name can be found by filtering the output by *dns* protocol.

Fortunately, the ransomware from this challenge has already been shut down and official decryptor is available on github ([TestlaCrypt](https://github.com/Cisco-Talos/TeslaDecrypt/releases/tag/1.0)).
