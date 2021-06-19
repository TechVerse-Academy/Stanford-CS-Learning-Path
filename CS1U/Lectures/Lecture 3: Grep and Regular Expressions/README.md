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

Let's take a look at what this output means. The important thing to remember is that when diff is describing these differences to you, it's doing so in a prescriptive context: it's telling you how to change the first file to make it match the second file.

|#   	|change   	|description   	                                                                                            |
|---	|---	    |---                                                                                                       	|
|1   	|r1ar2   	|Append the lines at the position r2 in the second file to the position r1 in the first file.               |
|2   	|r1cr2   	|Change (replace) the lines at position r1 with the lines at the position r2 in the second file.            |
|3   	|r1dr2   	|Delete the lines in the first file at position r1, which would have appeared at range r2 in the second file|
|4   	|r2,r4cr2,r4|r2 through r4 in the first file need to be changed to match r2 through r4 in the second file.              |

  * The first line of the diff output will contain line numbers corresponding to the first file, a letter (a for add, c for change, or d for delete), and line numbers corresponding to the second file.

In our output above, "2d1" means: "Lines 2 in the first file need to be deleted to match lines 1 in the second file."  
  
> The *diff* command is often used by software developers to examine changes between different versions of program source code and thus has the ability to recursively examine directories of source code, often referred to as source trees.