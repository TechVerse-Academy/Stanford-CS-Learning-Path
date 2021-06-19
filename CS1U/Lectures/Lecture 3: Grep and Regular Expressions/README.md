## Grep and Regular Expressions

**1. Most basic use of diff is to get the difference between two files**  

The diff program is a much more complex tool, supporting many output formats and the ability to process large collections of text files at once.  
```
junryo@xyz ~%diff content.txt content2.txt 
2c2
< I am a computer scientist.
\ No newline at end of file
---
> Hello. I'm Trung Anh. I am from Vietnam.
```
The *diff* command is often used by software developers to examine changes between different versions of program source code and thus has the ability to recursively examine directories of source code, often referred to as source trees.