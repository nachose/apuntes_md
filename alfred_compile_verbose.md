## Alfred compile verbose

·seroiuts02353> alfred -v compile | & tee alfred_compile_verbose.log</br>                                                                                                                                                                        
INFO [CompileCommand]: Creating temporal folder /tmp/tmpd68FMP_aoverifier</br>
DEBUG [root]: Building Command Compiler</br>
INFO [root]: Executing Cmd: setup_workspace make -C 3pp CONFIG=Linux_x86_64 openssl, Folder: /repo/esecjos/epg, Return Code: None</br>
INFO [root]: Executing Cmd: cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRIND=OFF -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -DUSE_CLANG_COVERAGE=OFF -DUSE_ASAN=OFF -DBUILD_TEST_HEUR=OFF -DBUILD_TEST_TOOLKIT=OFF -DHEURPACKAGE_SCOPE= -GNinja /repo/esecjos/cdpi-main, Folder: /repo/esecjos/cdpi-main/cmake_build/epg, Return Code: None</br>
DEBUG [root]: Executing Cmd: echo "cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRIND=OFF -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -DUSE_CLANG_COVERAGE=OFF -DUSE_ASAN=OFF -DBUILD_TEST_HEUR=OFF -DBUILD_TEST_TOOLKIT=OFF -DHEURPACKAGE_SCOPE= -GNinja /repo/esecjos/cdpi-main" > /repo/esecjos/cdpi-main/cmake_build/epg/cmake_compile_dpi_cmd.log, Folder: /repo/esecjos/cdpi-main/cmake_build/epg, Return Code: None</br>
INFO [root]: Executing Cmd: ninja  , Folder: /repo/esecjos/cdpi-main/cmake_build/epg, Return Code: None</br>
DEBUG [root]: Executing Cmd: cp /repo/esecjos/cdpi-main/cmake_build/epg/compile_commands.json ./buildout/, Folder: /repo/esecjos, Return Code: None</br>
INFO [root]: Executing Cmd: ninja install, Folder: /repo/esecjos/cdpi-main/cmake_build/epg, Return Code: None</br>
INFO [root]: Compilation logs in: logs/aoverifier-20220720-173159-599383/cmakeCompile--project=cdpi-main_--platform=epg_--compile-epg-3pp_stdout.log</br>
INFO [CompileCommand]: Removing temporal folder /tmp/tmpd68FMP_aoverifier</br>