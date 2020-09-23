<div align="center">

## Command\-line arguments, how to use them


</div>

### Description

A very basic run-through of how to implement command-line arguments, with code.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Eric Gesinski](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/eric-gesinski.md)
**Level**          |Beginner
**User Rating**    |4.3 (26 globes from 6 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/eric-gesinski-command-line-arguments-how-to-use-them__3-1754/archive/master.zip)





### Source Code

Want to know how to use C++ with arguments? There's not too much code to do it, the basic part of it is adding parameters to your main function.
<BR><BR>
You need two parameters, one for the number of arguments that are entered (argc), and one for the arguments themselves (argv). These are an integer and a two-dimensional character array, respectively. These two dimensions are for 1) an array of characters (a string) and 2) the list of strings. To make it two-dimensional, you can do it in two different ways: either putting **argv or *argv[]. I like the second one, myself.
<BR><BR>
A few other things to know: in C++, the program itself is considered the first argument. So you really always have at least one argument, the program call itself. Also, the argc and argv variables are automatically set when you run the program, and they can be different every time you run it.
<BR><BR>
Here's a little program to show you exactly how to do this:
<BR><BR>
<font color="#AA0000">
// Here's the standard include, you'll need it<BR>
// for the "cout" command.<BR>
</font>
<font color="#0000AA">
#include &lt;iostream.h>
<BR><BR>
<font color="#AA0000">
// Now here's where you need to add<BR>
// the "argc" and "argv" parameters.<BR>
</font>
int main(int argc, char *argv[])<BR>
{<BR>
<font color="#AA0000">
  // Checking to see if there's only one<BR>
  // argument (the program).<BR>
</font>
  if (argc == 1)<BR>
  {<BR>
    cout << "There aren't any arguments!\n";<BR>
    cout << "Just the program, \"" << argv[0] << "\".\n";<BR>
  }<BR>
<font color="#AA0000">
  // Otherwise, there will be arguments.<BR>
</font>
  else<BR>
  {<BR>
    cout << "Here are your arguments:\n";<BR><BR>
<font color="#AA0000">
    // I used a for loop to go through<BR>
    // the list of arguments, starting<BR>
    // with the one after the program.<BR>
</font>
    for (int i = 1; i < argc; i++)<BR>
      cout << "\t" << argv[i] << endl;<BR>
  }<BR><BR>
  return 0;<BR>
}<BR>
</font>
<BR><BR>
This is my first submission, so if the HTML tags are a little messed up, I'm still learning how to submit.<BR><BR>
If you have any questions, or requests, just let me know - I'd be happy to help.

