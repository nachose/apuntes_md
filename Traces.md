## Traces

Traces are not showing output because stdout and stderr have been programatically redirected.

The way out of there is to re-enroute them to the terminal:

> #include \<cstdio>
>
>//freopen("/dev/tty", "w", stdout);</br>
>freopen("/dev/tty", "w", stderr);
>
>fprintf(stderr, "Hola, Optimized xml: %s", optimizedXml);</br>
>fflush(stderr);

