## Grep and Regular Expressions

**1. Most basic use of diff is to get the difference between two files**  

The diff program is a much more complex tool, supporting many output formats and the ability to process large collections of text files at once.  
For example, consider two files, content.txt, and context2.txt in the [previous lecture](../Lecture%202:%20Pipelines%20-%20Input%26Output%20Redirection).  
  * If context.txt contains the following two lines of text:
```
Hello. I'm Trung Anh. I am from Vietnam.
I am a computer scientist.
```
* and content2.txt contains these two lines:
```
Hello. I'm Trung Anh. I am from Vietnam.

```

then we can use diff to automatically display for us which lines differ between the two files with this command as follows.
```
junryo@xyz ~%diff content.txt content2.txt 
```
  * and the output will be
```
2d1
< I am a computer scientist.
\ No newline at end of file
```


The *diff* command is often used by software developers to examine changes between different versions of program source code and thus has the ability to recursively examine directories of source code, often referred to as source trees.