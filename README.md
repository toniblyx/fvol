# fvol

Fast volatility script (fvol) is a wrapper script that will run volatility plugins against a memory dump and will save the output to a specific folder for later analysis. The output files are generated as every plugin runs so the analyst does not have to wait for the script to fully execute to start analyzing the information. The script can also run the dumping plugins (such as procdump,malfind,moddump,dumpfiles,etc.) that will allow to analyze the retrieved files using various techniques (strings, antivirus scanning, YARA, reversing, etc.). Every command is stored on the audit.txt file including the total execution time and the execution time of each plugin, which will help the analyst decide which plugins to enable and which ones should be executed first. If you know the profile of the memory dump, you can provide it, if not the script will try to determine it based on imageinfo output.

The intention of this script is to reduce the time needed to run volatility commands and wait for them to complete, now if you receive a memory dump at the end of the day or before lunch you can leave it running and come back to analyze the output. You will always have the chance to run additional plugins not covered by the initial execution.


TODO:

Flagging abnormal behavior of well-known Windows processes, based on the SANS Poster known evil. 
Calculating hash values of the dumped files and submitting hashes to Virus Total automatically using an API key to find known evil. 
Scanning the memory dump using a collection of memory based YARA rules. 
Scanning the dumped files with a collection of YARA rules. 
Compare the output against a known-good memory dump baseline.
Add support for Mac OS and Linux memory dumps.

Check a video of how it works: https://youtu.be/ZDNqx_jXdlc
