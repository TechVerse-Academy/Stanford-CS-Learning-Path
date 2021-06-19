## Pipelines Input/Output Redirection

The capability of commands to read data from standard input and send to standard output is utilized by a shell feature called pipelines.  

**1. Print lines matching a pattern with grep**  

The *grep* command is a powerful program used to find text patterns within files.  It’s used like this as follows.
```
grep pattern file_name
```
When grep encounters a “pattern” in the file, it prints out the lines containing it. The patterns that grep can match can be very complex, but for now we will concentrate on simple text matches.  
[*We’ll cover the advanced patterns, called regular expressions*]()
**1. Piping lets you use the output of one command as the input of another**  
Using the pipe operator |, the standard output of one command can be piped into the standard input of another.
```

```

**2. Use “>” to output into a file**   

**3 ./conversation.py < name**    

**4. Use “tee” when you want to know what is being outputed to a file**  