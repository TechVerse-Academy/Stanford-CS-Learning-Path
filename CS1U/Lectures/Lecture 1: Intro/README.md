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