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

The below command will put output of the *grep* call into the content2.txt file. It doesn’t append, it overwrites.
```
junryo@xyz ~%cat content.txt | grep Vietnam > content2.txt
junryo@xyz ~%cat content2.txt
Hello. I'm Trung Anh. I am from Vietnam.
```
To append, use ">>".
```
junryo@xyz ~%cat content.txt | grep Vietnam >> content2.txt
junryo@xyz ~%cat content2.txt
Hello. I'm Trung Anh. I am from Vietnam.
Hello. I'm Trung Anh. I am from Vietnam.
```
**3 ./conversation.py < name**    

Using the < redirection operator, we change the source of standard input from the keyboard to the file lazy_dog.txt. 
**4. Read from stdin and output to stdout and files with tee**  

The tee program reads standard input and copies it to both standard output (allowing the data to continue down the pipeline) and to one or more files.   
```
junryo@xyz ~% ls /usr/bin | tee ls.txt | grep zip
bunzip2
bzip2
bzip2recover
funzip
gunzip
gzip
unzip
unzipsfx
zip
zipcloak
zipdetails
zipdetails5.18
zipdetails5.28
zipdetails5.30
zipgrep
zipinfo
zipnote
zipsplit
```