# Eric Bolander 
## Dr. Politz
## Lab 1 - CSE 15L
Today in lab we learned how to navigate different commands within the Ed Workspace. Given a directory through GitHub called lecture 1, we were first able to clone the directory into our workspace using git 
clone command. 
We then used cd, ls, and cat commands to navigate the directory and the files within:
1. ## Example using these commands with no arguments:
  ## ``` cd command  ``` from ``` /home  ``` and  ``` lecture 1 ```
   ![Image](cd1.png)
   * This command when used from outside of a directory produced no output, however when used from inside the directory took us back out of the directory.
   * Directory - lecture1
   * No errors
   * Additional insights: when used from deep within multiple directories, cd took us out of all directories
   * This was unexpected, I thought it would just take you one directory back
     ![Image](directory2.png)
 
   ## ``` ls command ```, ```/home ```, ```lecture 1 ```: 
   ![Image](ls1.png)
   * This command listed all the contents of the active directory
   * Directory- lecture1
   * No errors

   ## ``` cat command ```, ``` /home ```, ``` lecture 1 ```
   ![Image](cat1.png)
   * The cat command shows a files contents, so with no command it prompts an input
   * Repeated or reprinted any input given
   * Directory- lecture1
   * No errors
   * Used Ctrl D to stop.
     
3. ## Example using commands with directory argument
   ## ``` cd ```, ``` /home ``` ``` lecture 1 ```, ``` messages ```
    ![Image](cd2.png)
    * The cd command navigated to specified 'messages' directory and now allows us to access any files inside.
    * Directory- lecture1
    * No errors
    
   ## ``` ls ```, ``` /home ```, ``` lecture 1 ```,``` messages ``` 
    ![Image](ls2.png)
   * The ls command is a listing command and when used here with messages as an argument it listed all the files inside 'messages'
   * Directory-lecture1
   * no errors
     
   ## ``` cat ```, ``` /home ```, ``` lecture 1 ```, ``` messages ```
    ![Image](cat2.png)
   * The cat command is used for files, so when used with a directory as an argument the output was simply 'lecture1 is a directory'.
   * Directory- lecture1
     
5. ## Example using commands with file argument
   ## ``` cd ```, ``` lecture 1 ```, ``` /messages ```, ``` French.txt ```
    ![Image](cd3.png)
   * The cd command with the file French.txt as an argument gave the output expected, and gave us an error that says 'not a directory'.
   *  This is because the cd command is used to access directories not files.
     * Errors were addressed.
     * Directory - messages
       
   ## ``` ls ```, ``` lecture 1 ```, ``` /messages ```, ``` French.txt ```
   ![Image](ls3.png)
   * The ls command is a listing command and when used here with French.txt as the argument, gave us French.txt as output
   * Directory- messages
   * No errors
     
   ## ``` cat ```, ``` lecture 1 ```, ``` /messages ```, ``` French.txt ```
   ![Image](cat3.png)
   * The cat command used on a file argument will read the data from that file specified.
   *  Here the French.txt file was used so Bonjour monde! was printed.
   * Directory- messages
   * No errors. 
   
