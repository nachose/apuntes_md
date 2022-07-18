## Valgrind

valgrind --leak-check=full --track-origins=yes --suppressions= $WS_ROOT/tools/test/valgrind.supp [binario]

valgrind --tool=memcheck executable</br>
valgrind --tool=helgrind executable