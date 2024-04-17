## Tools 
- [FTK Imager](https://www.exterro.com/digital-forensics-software/ftk-imager)
## Hints
Firstly we need to export the browser files to our host system from the AccessData *.ad1* file. We will use the FTK Imager for that.

To recognize the profile folders we need to know how Chrome creates profiles and how they are stored.

To find the name of the theme try to find "theme" string in the Chrome folder with explorer search bar and then examine it in FTK Imager or open it with notepad.

In order to answer all extension related questions we need to find the folder in which Chrome stores it's extensions. We need to inspect every `manifest` file we find.

After we found the extension folder in which the mining script's data is being stored we will open the *.js* file and answer the remaining questions about it's logic.
