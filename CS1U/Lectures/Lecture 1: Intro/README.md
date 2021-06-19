### Some main commands
1. List directory with ls  

The ls command is probably the most used command, and for good reason. With it, we can see directory contents and determine a variety of important file and directory attributes.   
  * Get a list of files and subdirectories contained in the current working directory  
```
junryo@xyz ~ %ls  

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
junryo@xyz ~ %ls miniconda

LICENSE.txt	condabin	include		python.app	ssl
bin		envs		lib		share
conda-meta	etc		pkgs		shell
```
   * We can even specify multiple directories  

In the following example, we list both the user’s home directory (symbolized by the ~ character) and the /usr directory.
```
junryo@xyz ~ %ls ~ /usr


/usr:
X11		bin		libexec		sbin		standalone
X11R6		lib		local		share
```
   * By adding -l to the command, we changed the output to the long format.
```
junryo@xyz ~ %ls -l miniconda

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
junryo@xyz ~ %ls -lt miniconda

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
junryo@xyz ~ %ls -lt --reverse miniconda

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

|#   	|option |long option   	|description                                                                                             |
|---	|---	|---	        |---                                                                                                     |
|1   	|-a  	|--all          |List all files, even those with names that begin with a period, which are normally not listed.          |
|2   	|-A   	|--all-almost   |Like the -a option except it does not list . (current directory) and .. (parent directory).             |
|3   	|-d   	|--directory   	|Ordinarily, if a directory is specified, ls will list the contents of the directory, not the directory itself. Use this option in conjunction with the -l option to see details about the directory rather than its contents.                   |
|4   	|-F   	|--classify   	|This option will append an indicator character to the end of each listed name. For example, it will append a forward slash (/) if the name is a directory.                                                                                          |
|5   	|-h   	|   	        |In long format listings, display file sizes in human-readable format rather than in bytes.              |
|6   	|-l   	|   	        |Display results in long format.                                                                         |
|7   	|-r   	|--reverse   	|Display the results in reverse order. Normally, ls displays its results in ascending alphabetical order.|
|8   	|-S   	|   	        |Sort results by file size.                                                                              |
|9   	|-t   	|   	        |Sort by modification time.                                                                              |

2. Print name of current working directory with pwd  

To display the current working directory, we use the pwd (print working directory) command.
```
junryo@xyz ~ %pwd  

/Users/junryo
```
3. Change directory (will only look in my current directory) with cd  

To change our working directory (where we are standing in the tree-shaped maze), we use the cd command.  
  * Absolute pathnames
```
junryo@xyz ~ %cd /usr/bin 
junryo@xyz bin %pwd  
/usr/bin
```
  * Relative pathnames  

The . notation refers to the working directory, and the .. notation refers to the working directory’s parent directory. Here is how it works. Let’s change the working directory to /usr/bin again.
```
junryo@xyz ~ %cd /usr/bin 
```
We wanted to change the working directory to the parent of /usr/bin, which is /usr. 
```
junryo@xyz bin %cd ..
```
We can change the working directory from /usr to /usr/bin using an relative pathname.
```
junryo@xyz %cd ./bin
junryo@xyz bin %pwd

usr/bin
```
* cd ~ : takes you to home folder
```
junryo@xyz bin %cd ~
junryo@xyz ~ %pwd
/Users/junryo
```
* cd / : go to root directory
```
junryo@xyz ~ %cd /
/
```
* tab completion: pressing tab automatically completes the file name  

Tab completion is an extremely helpful feature in nearly any command-line environment, whether you’re using the Bash shell on Linux, Command Prompt or PowerShell on Windows, or a terminal window on Mac OS X. This feature can dramatically help you speed up typing commands. Just hit Tab while typing a command, option, or file name and the shell environment will automatically complete what you’re typing or suggest options to you. 
```
junryo@xyz ~% pip
pip     pip3    pip3.8  pip3.9
```
3. Erase all commands with clear  

Clear is a computer operating system command which is used to bring the command line on top of the computer terminal.
```
junryo@xyz ~ %clear
```
* up arrow lets you access previous commands you’ve used
* ctrl-c interrupt command
* ctrl-d disconnect (used for programs like python
* ctrl-z takes out of current process, like minimizing

