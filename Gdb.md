## Gdb


ptype --> Print definition of type

ptype /o --> Print type definition with offset of fields

refresh/\<C-l> --> Refresh display

x /20xb address --> Print 20bytes starting from address

p $eax  --> Print eax register, which is also where functions store their return value

\<C-x>a  --> Switch between tui and cui modes

tui-enable --> Enable tui

tui-disable --> Disable tui

x /s ptr --> Display null terminated string pointed by ptr.

whatis variable --> Only show type of variable

### Show a string faithfully

call (void)puts(0x1edbec0)  --> Use the address pointing to the string.






### Signal of a crash

print $_siginfo --> Information about the last signal sent.


### Continuosly display smth

display var --> display value of var each time the program stops

undisplay number --> stop displaying number

