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
   * By adding -l to the command, we changed the output to the long format.
```
junryo@MacBook-Pro ~ %ls -l

total 24
-rw-r--r--    1 junryo  staff  11799 Dec 10  2020 LICENSE.txt
drwxr-xr-x   71 junryo  staff   2272 Jun 15 21:07 bin
drwxr-xr-x   38 junryo  staff   1216 Jun 15 21:07 conda-meta
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 condabin
drwxr-xr-x    4 junryo  staff    128 Jun 15 21:11 envs
drwxr-xr-x    4 junryo  staff    128 Jun 15 21:07 etc
drwxr-xr-x  114 junryo  staff   3648 Jun 15 21:07 include
drwxr-xr-x   90 junryo  staff   2880 Jun 15 21:07 lib
drwxr-xr-x  223 junryo  staff   7136 Jun 15 21:11 pkgs
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 python.app
drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 share
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 shell
drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 ssl
```   
  * Sort the result by the file’s modification time.
```
junryo@MacBook-Pro ~ %ls -lt

total 24
drwxr-xr-x    4 junryo  staff    128 Jun 15 21:11 envs
drwxr-xr-x  223 junryo  staff   7136 Jun 15 21:11 pkgs
drwxr-xr-x   38 junryo  staff   1216 Jun 15 21:07 conda-meta
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 python.app
drwxr-xr-x   71 junryo  staff   2272 Jun 15 21:07 bin
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 condabin
drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 shell
drwxr-xr-x    4 junryo  staff    128 Jun 15 21:07 etc
drwxr-xr-x   90 junryo  staff   2880 Jun 15 21:07 lib
drwxr-xr-x  114 junryo  staff   3648 Jun 15 21:07 include
drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 share
drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 ssl
-rw-r--r--    1 junryo  staff  11799 Dec 10  2020 LICENSE.txt
```  
   * Add the long option --reverse to reverse the order of the sort.
```
junryo@MacBook-Pro ~ %ls -lt -reverse

total 24
24 -rw-r--r--    1 junryo  staff  11799 Dec 10  2020 LICENSE.txt
 0 drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 ssl
 0 drwxr-xr-x    9 junryo  staff    288 Jun 15 21:07 share
 0 drwxr-xr-x  114 junryo  staff   3648 Jun 15 21:07 include
 0 drwxr-xr-x   90 junryo  staff   2880 Jun 15 21:07 lib
 0 drwxr-xr-x    4 junryo  staff    128 Jun 15 21:07 etc
 0 drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 shell
 0 drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 condabin
 0 drwxr-xr-x   71 junryo  staff   2272 Jun 15 21:07 bin
 0 drwxr-xr-x    3 junryo  staff     96 Jun 15 21:07 python.app
 0 drwxr-xr-x   38 junryo  staff   1216 Jun 15 21:07 conda-meta
 0 drwxr-xr-x  223 junryo  staff   7136 Jun 15 21:11 pkgs
 0 drwxr-xr-x    4 junryo  staff    128 Jun 15 21:11 envs
```
  * The ls command has a large number of possible options, the most common of which are listed in the following table.  

|   	|option   	        |description   	|
|---	|---	            |---	        |
|1   	|-all   	        |List all files, even those with names that begin with a period, which are normally not listed (that is, hidden).|
|2   	|-all -almost   	|   	|
|3   	|   	|   	|
|4   	|   	|   	|
|5   	|   	|   	|
|6   	|   	|   	|
|7   	|   	|   	|
|8   	|   	|   	|
|9   	|   	|   	|

* Change directory (will only look in my current directory) with cd
* cd ~ : takes you to home folder
* cd / : go to root directory
* cd .. : one directory up
* tab completion: pressing tab automatically completes the file name
* clear : erase all commands
* up arrow lets you access previous commands you’ve used
* ctrl-c interrupt command
* ctrl-d disconnect (used for programs like python
* ctrl-z takes out of current process, like minimizing

