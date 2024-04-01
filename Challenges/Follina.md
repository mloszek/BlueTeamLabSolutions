# Follina
## Tools 
- [VirusTotal](https://www.virustotal.com/gui/home/upload)
- [sha1sum](https://www.howtoforge.com/linux-sha1sum-command/)
## Hints
Calculating SHA1 checksum of the unpacked file from lab is pretty straightforward. We can use the `sha1sum` program if on Linux machine or PowerShell command `Get-FileHash {file} -Algorithm SHA1` if on Windows.

We then upload the *sample.doc* file into the VirusTotal and see the results. Questions 2, 8 and 9 can be answered using the knowledge from these analysis results.

It's worth mentioning that the file downloaded may actually affect your system, so in order to avoid any issues with it, it is highly advisable to work in sandbox environment. I used instance of Parrot OS in VMBox virtual machine. 
If we want to inspect the contents of the malicious file we need to change its type from *.doc* to *.zip* and extract it somewhere safe. Then we can freely examine the xml's that hides inside.

All remaining questions can be answered based on the knowledge from this great [Hack The Box article](https://www.hackthebox.com/blog/cve-2022-30190-follina-explained#mcetoc_1hbq9i5711a) by Kyser Clark.

In this challenge knowledge and understanding on how this vulnerability works is much more valuable than just answering the questions.
