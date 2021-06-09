RHCSA (RED HAT SYSTEM ADMINITRATOR)
=======

[TOC]

Understand and Use Essenctial Tools
------




##### Essencials :
---
	>  #(std) satandar output
    2> #(stderr) standar error
	sort < list > sorted_list #combined input output
    ls  2> error 2>&1

##### Grep and Regex
---
##### SSH (Secure Shell)
---

system width configs

	/etc/ssh/ssh_config

user file, overrides system configs

	~/.ssh/config
###### keys
Generates a public and privates keys

	ssh-keygen

saves to

	~/.ssh/id_rsa
	~/.ssh/id_rsa.pub


Copies your public id over th te target

	ssh-copy-id


###### X11 Forwarding

I think it sends a single window trough the ssh connection

	sssh -X user@server



| Old | Replaced  by |
|-----|-----|
|Telnet | ssh |
|rcp (remote copy) | scp (secure copy)|
|ftp (file tranfer protocol) | sftp  ( secure file tranfer protocol)|


##### logging in and switchign usrs:
---
suptitude user


`su`

Set up the enviroment when

`su - lucy`

Run a single command as an other user

`su -C "fdisk -l" `


###### Interactive shells
Means that the shell is run wit the interaction of the usr, suh as opening the terminal, as opposued to the non-interactive shell.

`.bashrc` runs when in interactive

###### login shell
Runs as part to the user loggin into the system as opposued to a non-login which can be automated process

`.bash_profile`


Commands run when log out
* .bash_logout

Command history
* .bash_history
* search hisory `crl-r`



##### Compression and Archives:
---
`tar cvf home.tar /home`
* create a tar archive
* verbose
* filename

`tar xvf home.tar /home`
* extracts a tar archive
* Verbose
* filename

`-z` or `-j` compresses behaivor

###### Compression
###### Gzip

`gzip bigfile.stuff`
`gzip -d bigfile.stuff.gz`

###### Bzip
`bzip2 bigfile.stuff`
`bzip2 -d bigfile.stuff.bz2`

###### Zip Files
`zip -r zippedFileName.zip /home`
`unzip zippedFileName.zp`

##### Creating and Manipulation Files:
---
A File:

>A Pointer to a 'inode' which live on the disk
>`ls -i file.stuff`

Commands:
* find
* locate
`locate https.config`
* cat
* less
* more
* head
* less
* sort
`-r` revese
* wc
`-l` line count
* diff
* patch


##### Using File Links:
---

###### Hard Links:yy
Point to the same inode to the disk

###### Hard Links:yy
is a pointer to the filenames of other files




##### File Permissions:
---
type of file:
`-` => regualr files
`-` => regualr files



Operate Running System
-----

Configure Local Storage
----

Create and Configure File systems
----

Deloy, Configure, and Maintain Systems
-----


Manage User and Groups
-----


Manage Security
-----

Exam Eviroment
----
