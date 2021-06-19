<div align="center">
	<img width="300" height="350" src="../media/logo.png" alt="Linux"></img>
</div>

## Contents  

Practical Unix is a practical introduction to using the Unix set of operating systems with a focus on Linux command line skills.  
- [Introduction](../Lecture%201:%20Intro)
- [Pipelines-Input/Output Redirection](../Lecture%202:%20Pipelines%20-%20Input%26Output%20Redirection)
- [Grep and Regular Expressions](#grep-and-regular-expressions)
- [Scripting](../Lecture%204:%20Scripting)
- [Web](../Lecture%205:%20Web)
- [Advanced Web](../Lecture%206:%20Advanced%20Web)


## Grep and Regular Expressions

**1. Most basic use of diff is to get the difference between two files**  

> The *diff* command is often used by software developers to examine changes between different versions of program source code and thus has the ability to recursively examine directories of source code, often referred to as source trees.

The diff program is a much more complex tool, supporting many output formats and the ability to process large collections of text files at once.  
```
diff options File1 File2 
```
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
  * The first line of the diff output will contain line numbers corresponding to the first file, a letter (a for add, c for change, or d for delete), and line numbers corresponding to the second file.

|#   	|change   	|description   	                                                                                            |
|---	|---	    |---                                                                                                       	|
|1   	|r1ar2   	|Append the lines at the position r2 in the second file to the position r1 in the first file.               |
|2   	|r1cr2   	|Change (replace) the lines at position r1 with the lines at the position r2 in the second file.            |
|3   	|r1dr2   	|Delete the lines in the first file at position r1, which would have appeared at range r2 in the second file|
|4   	|r2,r4cr2,r4|r2 through r4 in the first file need to be changed to match r2 through r4 in the second file.              |

In our output above, "2d1" means: "Lines 2 in the first file need to be deleted to match lines 1 in the second file."  
  * The examples above show the default output of diff. It's intended to be read by a computer, not a human, so for human purposes, sometimes it helps to see the context of the changes. When viewed using the context format (the -c option), we will see this.  
```
junryo@xyz ~%diff -c content.txt content2.txt 
*** content.txt	Sat Jun 19 14:19:23 2021
--- content2.txt	Sat Jun 19 14:19:56 2021
***************
*** 1,2 ****
  Hello. I'm Trung Anh. I am from Vietnam.
- I am a computer scientist.
\ No newline at end of file
--- 1 ----
```

  * The output begins with the names of the two files and their timestamps. The first file is marked with asterisks, and the second file is marked with dashes.

```
*** content.txt	Sat Jun 19 14:19:23 2021
--- content2.txt	Sat Jun 19 14:19:56 2021
***************
```
  * Next, we see groups of changes, including the default number of surrounding context lines. In the first group, we see the below which indicates lines 1 through 2 in the first file. 

```
*** 1,2 ****
```

  * Later we see as follows which indicates lines 1 in the second file. 

```
--- 1 ----
```

**2. You can compare two directories as well**

  * B (*--ignore-blank-lines*) flag will ignore things like blank lines

  * b (*--ignore-space-change*) flag will ignore things like blank spaces
  * y (*--side-by-side*) flag compares lines side-by-side
  * Use --width=50 (or another option) flag if you have a smaller screen

**3. Find files the hard way**  

Find command searches directories for a file based on a pattern that you give it. We’re going to spend a lot of time with find because it has a lot of interesting features that we will see again and again when we start to cover programming concepts in later lectures.

  * In its simplest use, find is given one or more names of directories to search. For example, to produce a listing of our home directory, we can use this.

```
junryo@xyz ~ % find ~  
```

  * On most active user accounts, this will produce a large list. Because the list is sent to standard output, we can pipe the list into other programs. Let’s use wc to count the number of files.
```
junryo@xyz ~ % find ~  ! wc -l
499524
```
  * To list directories from our search.
```
junryo@xyz ~ % find ~  -type d | wc -l
74530
```
**4. Locate is faster than find because it uses databases**
> You might notice that, on some distributions, locate fails to work just after the system is installed, but if you try again the next day, it works fine. What gives? The locate database is created by another program named updatedb. Usually, it is run periodically as a cron job, that is, a task performed at regular intervals by the cron daemon. Most systems equipped with locate run updatedb once a day. Because the database is not updated continuously, you will notice that very recent files do not show up when using locate. To overcome this, it’s possible to run the updatedb program manually by becoming the superuser and running updatedb at the prompt.

The locate program performs a rapid database search of pathnames and then outputs every name that matches a given substring. 
  * The locate progaram will search its database of pathnames and output any that contain the string bin/zip.
```
junryo@xyz ~ % locate bin/zip 
```
  * If the search requirement is not so simple, we can combine locate with other tools such as grep to design more interesting searches.
```
junryo@xyz ~ % locate zip | grep bin
```

**5. Regular expressions**  
  

## References
  * https://www.gnu.org/software/diffutils/manual/html_node/diff-Options.html

