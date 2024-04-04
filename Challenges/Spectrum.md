## Tools 
- [PhotoRec](https://www.cgsecurity.org/wiki/PhotoRec)
- [fcrackzip](https://www.kali.org/tools/fcrackzip/)
- [stegseek](https://github.com/RickdeJager/stegseek)
- [CyberChef](https://cyberchef.org/)
## Hints
The file we will be looking at is a disk dump file with [*.dd* extension](https://filext.com/file-extension/DD). 
It took me some time to figure out how to open it on linux system and review it's contents.
Finally I decided to give PhotoRec a shot, since thats the program challenge creators insist on using.

PhotoRec is a companion program to TestDisk utility and both of them are great tools. I will definitely be using them in the future for different appliances.
I strongly recommend you to visit (https://www.cgsecurity.org/) and show creators some love by donating or spreading the knowledge of this programs.

After unpacking the contents of the *.dd* file we will see that one of them is zipped. 
We can use `fcrackzip` to crack the password.

One of the *.wav* files contains information on coordinates of the "deal". In order to retrieve it we need to analyze it's audio spectrum.

Last file containing the date of the meet-up is hidden in one of the *.wav* files using steganography. In order to find the file we need to brute-force
the password. For this purpose we can use the `stegseek` tool (big kudos to RickdeJager).

After retrieving the file we have to decode it's contents to obtain the readable time. For this purpose we can utilize the CyberChef tool.
Decoded date still need to be figured out; the following string should serve as an clue.

And that's it!
