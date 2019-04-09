# OSD
Open Search &amp; Destroy

# Run :

## For Centos 7

`sudo yum install gcc`

`sudo yum install gcc-c++`

`sudo yum install python-devel`

`sudo pip install pycrypto`

## For other Linux

`sudo pip install pycrypto`

`wget -Nnv https://raw.githubusercontent.com/liberodark/OSD/master/osd.py && sudo python3 osd.py`

# Build :

Stadalone : `nuitka3 --standalone --recurse-on --python-version=3.7 osd.py`

Normal : `nuitka3 --recurse-on --python-version=3.7 osd.py`

# How to use :

`osd` : scan current directory

`osd /home` : scan a directory

`osd -r` : recursively scan the current directoy

`osd -i` : only show infected files

`osd --remove` : remove infected files

`osd --quarantine` : put infected files in quarantine

`osd --decrypt` : decrypt file from quarantine

`osd --send` : send file to virustotal

`osd --help` : show help

# Exemples : 

`osd -r -i --remove` (To recursively scan the current folder and only show infected files and remove them)

`osd -r -i --quarantine` (To recursively scan the current folder and only show infected files and put them in quarantine)

# Status of files :

File.pdf : OK ("OK", the file is on virustotal database but is not a virus)

Virus.exe : Infected ("Infected", the file is on virustotal database and is detected as a virus)

File1.txt : NC ("No Checked", the file is not on virustotal database)

# Summuary :

Files Scanned: 100 (Number of files scanned)

Files OK: 98 (Number of verified files)

Files NC: 1 (Number of files not checked)

Files Infected: 1 (Number of infected files)

Files Cleaned: 1 (Number of files deleted or moved in quarantine)

Time: 3min (Time of analysis)

# Quarantine :

Linux : `cd /opt/osd/quarantine/`

Windows : `cd c:\osd\quarantine\`
