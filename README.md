RHCSA (RED HAT SYSTEM ADMINITRATOR)
=======
***

[TOC]

Understand and Use Essenctial Tools
------





##### Essencials :
---
	>  #(std) satandar output
    2> #(stderr) standar error
	sort < list > sorted_list #combined input output
    ls  2> error 2>&1


###### Commands

Three types of comands:
	* Aliases
	* excecuted before anything else
	* internal Commands
	* Is part of the sheel itself, doe snot have to be loaded from te disk,
	* External Commands
	* is a command that existe on the disk as a separate file.


	type command can be used to know what type of command it is
    which coomand can be use to find out which command the sheel will be using

###### VIM

`vimtutor` is ca coomand which helps you lest vim
 Vim basic:

 |command | explanation |
 |------|--------|
 |esc |  enter command mode |
 |i | 'insert' behind the carrot|
 |a | 'append' after the carrot|
 |o | edit in new line below carrot|
 |O | edit in line above carrot |
 | :w | 'write' do disk|
 | q| 'quit'|
 |:w filename | 'write' document into filename|
 | dd | 'delete' line|
 | yy | 'yank' line |
 | v | enter 'visual' mode|
 | u | 'undo'|
 | Crtl-r | 'redo'|
 | gg| gos to first line in doc |
 | G | goes to last line in do |
 | /text | searches for text in doc|
 | ?text | searches for text backward in doc|
 | ^ | frist posicion in current line |
 | $ | last posicion in current line |
 | !ls | adds the outlut of ls, into the file|
 | :%s/old/new/g  | 'subtitudes' old with new in whole file'|


###### Enviroment




##### Grep and Regex
---
##### SSH (Secure Shell)
---

system width configs

	/etc/ssh/ssh_config

user file, overrides system configs

	~/.ssh/config
###### Keys
Generates a public and privates keys

	ssh-keygen

saves to

	~/.ssh/id_rsa
	~/.ssh/id_rsa.pub


Copies your public id over th te target

	ssh-copy-id


###### X11 Forwarding

I think it sends a single window trough the ssh connection

	ssh -X user@server



| Old | Replaced  by |
|-----|-----|
|Telnet | ssh |
|rcp (remote copy) | scp (secure copy)|
|ftp (file tranfer protocol) | sftp  ( secure file tranfer protocol)|


##### Logging in and Switchign users:
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

###### Login shell
Runs as part to the user loggin into the system as opposued to a non-login which can be automated process

`.bash_profile`


Commands run when log out
* .bash_logout

Command history
* .bash_history
* search hisory `crl-r`



#####Compression and Archives:
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

###### Compression - Gzip

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
`d` => directory



Operate Running System
-----

##### Managing the boot proccess
---

UEFI/BIOS -> GRUP2


Grub
>ls -> disks
>cat
>rd.break
>emergency
>rescue


##### Managing Individual Processes
- - -
top


ps
> acceps difrent rypes od opstions:
UNIX: which may be a be a groupd and must be preceded by a dash ( -aux )
GNU: which my be grouped and must not be used with a dash ( aux )
BSD: long options wch are receded by two dashes ( --group )
> a all process
> u display usr format
> x all Proceses

pgrep [options] pattern
> compbines the grep and ps to give relevant infomation
> -l process nams
> -u Limited the matches to user
> -v incerse result

Kill Signals
> kill  [options] pattern
> compbines the grep and ps to give relevant infomation
> -l list kill signals
> 15 SIGTERM Ask the process to end politely
> 9  SIGKILL Stops thhe process imidetly (leave file open...)
> 9  SIGHUP Stops tthe process in the shell eviroment, the binary must be have the configuration to be able to to interact with it
> 2  SIGINT ( crl-c )
> 19  SIGSTOP Tells a preocess to stop, similar to how the crtl-z
> 18  SIGCONT Tells a proccess to continue
> 20  SIGTSTP (Terminal Stop) relies on the binary on knowing how to process the signal

###### Niceness
The more priority a process has the less nice it is, and vv
>High priority, not nice [-20, 19] nice, low propieirty
>The lower the level the highest the priority, the less nice it is
renice
> 0 just share the CPU

###### Load Average
> Average of teads or processes waiting for a resorces over a period of time
> 1, 5, 15 minustes

load average over the last 1 minute: 1.05
load average over the last 5 minutes: 0.70
load average over the last 15 minutes: 5.09
>over the last 1 minute: The computer was overloaded by 5% on average. On average, .05 processes were waiting for the CPU. (1.05)
over the last 5 minutes: The CPU idled for 30% of the time. (0.70)
over the last 15 minutes: The computer was overloaded by 409% on average. On average, 4.09 processes were waiting for the CPU. (5.09)


	/dev/null produces no output.
	/dev/zero produces a continuous stream of NULL (zero value) bytes.
###### Logging

come back to it


###### VMs

come back to it

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
