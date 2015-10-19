<pre>
# update-synology-index
Synology synoindexd service only works with FTP, SMB, AFP
this program index all files that synoindexd left
you can select extensions, modified time, user and paths
for the searching and treatment

Usage: update-synoindex-music.sh  --> first for create config file
       change values of config/update-synoindex-music-conf.txt
       update-synoindex-music.sh

Example of config file:
for only mp3 in the last hour for the user transmission with log directory /volume1/music/ in the path /volume1/music/sounds recursive


#extensions
MP3
#Modified time --> none or "command find time" --> 24 hours example = "-mtime 0" ----> 1 hour = "-mmin -60"
-mmin -60
#user: none, root, transmission, ftp, etc.
transmission
#directory for log/filename --> none or path or path/filename
/volume1/music/
#directories to treat --> 0 recursive, 1 no recursive
0 /volume1/music/sounds
</pre>
