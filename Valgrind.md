## Valgrind

valgrind --leak-check=full --track-origins=yes --suppressions= $WS_ROOT/tools/test/valgrind.supp [binario]</br>

valgrind --leak-check=full --track-origins=yes ./build/Linux_x86_64/bin/up-dp-bsp_SUITE/up-dp-bsp_SUITE_Linux_x86_64.elf

valgrind --tool=memcheck executable</br>
valgrind --tool=helgrind executable
