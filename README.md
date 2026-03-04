# spotify-ads
Basically blocks all Spotify ads on desktop. Only tested on Windows — may not work on other operating systems.


## Installation 
Pretty simple — download the spotify-blocker.bat file, run it as administrator, wait for it to finish, fully close Spotify through Task Manager, and you’re good to go!


## Uninstall / Revert
It will tell you how to restore the backup if needed (or manually delete the lines starting with # === Spotify Ad Blocker from C:\Windows\System32\drivers\etc\hosts using Notepad as admin)


## Issues
It will work for most regular ads. Spotify rotates some CDN domains occasionally, so if an ad slips through after a few weeks, just run the script again (it adds the latest safe entries without duplicates).
