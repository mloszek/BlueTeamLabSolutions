## Tools
- [Ghidra](https://ghidra-sre.org/)
- any other reverse engineering tool
## Hints
After we open zip file of this challenge ew can find inside malicious *.exe* that we need to open using Ghidra or any other rev engineering tool.

When we inspect the code we can deduct, that the purpose of this file is to start a malicious process and obscure it inside the working memory.

The creation of the process happens when the `CreateProcessA()` API is being called.
In order to find the process creation flag that is being used we must study the official [MS documentation](https://learn.microsoft.com/en-us/windows/win32/procthread/process-creation-flags) of these flags.

In order to answer questions 3 and 4 we must notice, that some of the parameters of the PowerShell script that is being called are encoded in Base64.

Ntdll function starts with the 'nt' prefix.

For question 6: the behaviour of the functions is in their name, so look for the functions that writes and resumes.

To find the MITRE ID we must again acknowledge what does the script actually do: it creates the process and inject it in the memory.
