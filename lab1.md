# Eric Bolander 
Professor Politz
Lab 1 - CSE 15L
Today in lab we learned how to navigate different commands within the Ed Workspace. Given a directory through GitHub called lecture 1, we were first able to clone the directory into our workspace using git 
clone command. 
We then used cd, ls, and cat commands to navigate the directory and the files within:
1. Example using these commands with no arguments
   ## cd command: ![Image](cd command no arg.png)
   * This command when used from outside of a directory produced no output, however when used from inside the directory took us back out of the directory.
   
   ## ls command: ![Image](ls command no arg.png)
*  This command produced the output with all the files in the directory that is on the left.
*  No Errors
*  Directory- lecture1
   ## cat command: ![Image](cat command no arg.png)
    *  The cat command shows a files contents, so with no command it prompts you to give it content, I wrote hello and it printed out hello
    *  Directory- lecture1
    *  Used control D to end. 
3. Example using commands with directory argument
   ## cd: ![Image](cd command directory arg.png)
    * The cd command with the directory as an argument gave the output expected where it navigated to the directory specified 'messages' and now allows us to access any files inside.
    * Directory- lecture1
    * No errors
   ## ls: ![Image](ls command with directory arg.png)
   * The ls command is a listing command and when used here with messages as an argument it listed all the files inside 'messages'
   * Directory-lecture1
   * no errors 
   ## cat: ![Image](cat command directory arg.png)
   * The cat command is used for files, so when used with a directory as an argument the output was simply 'lecture1 is a directory'.
   * Directory- lecture1 
5. Example using commands with file argument
   ## cd: ![Image](cd command file arg.png)
   * The cd command with the file French.txt as an argument gave the output expected, and gave us an error that says 'not a directory'. This is because the cd command is used to access directories not files.
     * Errors were addressed.
     * Directory - messages
   ## ls: ![Image](ls command file arg.png)
   * The ls command is a listing command and when used here with French.txt as the argument, gave us French.txt as output
   * Directory- messages
   * No errors
   ## cat: ![Image](Cat arg with file arg.png)
   * The cat command used on a file argument will read the data from that file specified. Here the French.txt file was used so Bonjour monde! was printed.
   * Directory- lecture1
   * No errors. 
   
