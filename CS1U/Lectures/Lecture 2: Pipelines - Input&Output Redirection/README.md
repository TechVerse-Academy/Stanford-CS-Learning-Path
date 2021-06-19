## Pipelines Input/Output Redirection

The capability of commands to read data from standard input and send to standard output is utilized by a shell feature called pipelines. Using the pipe operator |, the standard output of one command can be piped into the standard input of another.

**1. Print lines matching a pattern with grep**  

The *grep* command is a powerful program used to find text patterns within files.  It’s used like this as follows.
```
grep pattern file_name
```
When grep encounters a “pattern” in the file, it prints out the lines containing it. The patterns that grep can match can be very complex, but for now we will concentrate on simple text matches.  
```
junryo@xyz ~%cat content.txt | grep Vietnam
Hello. I'm Trung Anh. I am from Vietnam.
```  
There are a couple of handy options for grep.

|#   	|option   	|description   	                                                                                 |
|---	|---	      |---	                                                                                             |
|1   	|-i       	|which causes grep to ignore case when performing the search (normally searches are case sensitive)|
|2   	|-v      	|which tells grep to print only those lines that do not match the pattern                        	|

[*We’ll cover the advanced patterns, called regular expressions*]()  
 
**2. Use “>” to output into a file**   
```
junryo@xyz ~%cat content.txt | grep Vietnam > content2.txt
junryo@xyz ~%cat content2.txt
Hello. I'm Trung Anh. I am from Vietnam.
```
**3 ./conversation.py < name**    

**4. Use “tee” when you want to know what is being outputed to a file**  