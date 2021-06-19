### Some main commands
1. List directory with ls  
The ls command is probably the most used command, and for good reason. With it, we can see directory contents and determine a variety of important file and directory attributes.   
  * Get a list of files and subdirectories contained in the current working directory  
```
junryo@MacBook-Pro ~ %ls  

Applications				Movies
Calibre Library				Music
Creative Cloud Files			Pictures
Desktop					Postman
Documents				Public
Downloads				Private
Library					miniconda
```
  * Besides the current working directory, we can specify the directory to list
```
junryo@MacBook-Pro ~ %ls /miniconda

LICENSE.txt	condabin	include		python.app	ssl
bin		envs		lib		share
conda-meta	etc		pkgs		shell
```
   * We can even specify multiple directories  
In the following example, we list both the user’s home directory (symbolized by the ~ character) and the /usr directory.
```
junryo@MacBook-Pro ~ %ls ~ /usr


/usr:
X11		bin		libexec		sbin		standalone
X11R6		lib		local		share
```
   * We can also change the format of the output to reveal more detail.
```
junryo@MacBook-Pro ~ %ls -l

total 87384
drwxr-xr-x    4 junryo  staff       128 Apr 15 13:10 Applications
drwxr-xr-x    2 junryo  staff        64 Nov 26  2020 Calibre Library
drwx------@   4 junryo  staff       128 May 20 08:19 Creative Cloud Files
drwx------@   4 junryo  staff       128 Jun 18 15:47 Desktop
drwx------@  20 junryo  staff       640 Jun 16 18:30 Documents
drwx------@ 503 junryo  staff     16096 Jun 19 10:35 Downloads
drwx------@  71 junryo  staff      2272 Mar 17 17:13 Library
drwx------    4 junryo  staff       128 Nov 20  2020 Movies
drwx------+   5 junryo  staff       160 May  6 10:12 Music
drwx------+   4 junryo  staff       128 Nov 20  2020 Pictures
drwxr-xr-x    3 junryo  staff        96 Jun  1 14:18 Postman
drwxr-xr-x+   4 junryo  staff       128 Nov 20  2020 Public
drwxr-xr-x   15 junryo  staff       480 Jun 15 21:07 miniconda
```
By adding -l to the command, we changed the output to the long format.  
* cd - change directory (will only look in my current directory)
* cd ~ : takes you to home folder
* cd / : go to root directory
* cd .. : one directory up
* tab completion: pressing tab automatically completes the file name
* clear : erase all commands
* up arrow lets you access previous commands you’ve used
* ctrl-c interrupt command
* ctrl-d disconnect (used for programs like python
* ctrl-z takes out of current process, like minimizing