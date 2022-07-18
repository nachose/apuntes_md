## Python


### Show lines that are executing


python -m trace -t yourscript.py

will display all lines your program is executing. If you just want to see how python steps through one script you could do.

python -m trace -t yourscript.py | grep yourscript.py

https://stackoverflow.com/questions/60593258/how-do-you-see-the-execution-of-a-programme-line-by-line-in-python



### Debug step by step

https://stackoverflow.com/questions/4929251/how-to-step-through-python-code-to-help-debug-issues

Yes! There's a Python debugger called pdb just for doing that!

You can launch a Python program through pdb by using pdb myscript.py or python -m pdb myscript.py.

There are a few commands you can then issue, which are documented on the pdb page.

Some useful ones to remember are:

b: set a breakpoint

c: continue debugging until you hit a breakpoint

s: step through the code

n: to go to next line of code

l: list source code for the current file (default: 11 lines including the line being executed)

u: navigate up a stack frame

d: navigate down a stack frame

p: to print the value of an expression in the current context
