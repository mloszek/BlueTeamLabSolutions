## Tools
- [Volatility](https://volatilityfoundation.org/)
## Hints
Before starting this challenge it is advisable to get familiar with some basic functionality of Volatility tool.
I had some notes from BTL1 examination preparation but I strongly encourage everybody to take a look and practise with Volatility.
I used Volatility 3 (in older version one would have to set the profile before you start working on the sample) from terminal and not GUI.

To check the image info of the memory dump file we will use `vol.py -f {file} {platform}.info`, where *file* is the name of our `.vmem` file and *platform* is the current os, for example `windows.info`.

To check all the processes from the dump file, including the hidden ones, we use the command `python3 .\vol.py -f '\path\to\infected.vmem' windows.psscan`.

In order to inspect which process is the parent process we need to track the PPID column or use `pstree` command (windows.pstree.PsTree) just like we used `psscan` before. 
It's worth mentioning that, at least for me, the output of `pstree` was totally unreadable in the PowerShell window, so I had to direct the output of the command into a text file to be able to read it.
`pstree` can also give us the localization of the executables which will be useful in one of the questions.

At this point we will learn, that the malicious process is actually Wannacry. The best one can do right now is to read the [analysis of this threat](https://www.secureworks.com/research/wcry-ransomware-analysis). It will make the rest of this challege quite easy.
In the documentation we will find the answer for the "public key" question as well.
