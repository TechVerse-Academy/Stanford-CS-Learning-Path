**1. Piping lets you use the output of one command as the input of another**  
  * grep cat txt1 | grep bird  
  * send the output of grep cat txt1 into the second call to grep  
**2. Use “>” to output into a file**   
   grep cat txt1 > temp  
   will put output of grep call into temp file  
  it doesn’t append, it overwrites  
  To append, “>>”
  * ./conversation.py < name  
  name becomes the standard input for the python script  
  * Use “tee” when you want to know what is being outputed to a file  