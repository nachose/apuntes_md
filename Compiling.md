## Compiling commands

python cdpi-main/NSTdpifws/dpiregressionfw/bin/scripts/regression.py --dpisim-package buildout/dpisim_epg_package.tgz -p CUPS cdpi-main/NSTtests/dpiregression/suites/suite_cups_appID_rule_interaction.xml 

### 1. Compiling EPG

https://wiki.lmera.ericsson.se/wiki/EPG/Infrastructure/BuildSystem/Overview


"build -c lin up/all"  --> Compilar el user plane
"build -c lin.debug up/all -r " --> Compilar up en debug y correr los tess

build -c lin data-plane_upf_DPI_2_UPSFTSUITE --> Compilar un test case


./build/Linux_x86_64/bin/data-plane_upf_DPI_2_UPSFTSUITE/data-plane_upf_DPI_2_UPSFTSUITE_Linux_x86_64.elf -vvv TC21922  --> ver la salida del comando


### 2. Compile DPI

From a dpi shell, execute the following.

Create a dir cmake_build dentro de cdpi-main

Cd and execute 
$  cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRID=ON -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -GNinja ..


Inside.

Execute ninja: $ ninja

#### 2.1 Debug version

Same, substituing type with Debug

cmake -DCMAKE_BUILD_TYPE=Debug -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRID=ON -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -GNinja ..

#### 2.2 Compiling the EPG part

cd $repo/epg

setup_workspace make -C 3pp CONFIG=Linux_x86_64 openssl

cd /repo/esecjos/cdpi-main/cmake_build

cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRIND=OFF -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -DUSE_CLANG_COVERAGE=OFF -DUSE_ASAN=OFF -DBUILD_TEST_HEUR=OFF -DBUILD_TEST_TOOLKIT=OFF -DHEURPACKAGE_SCOPE= -GNinja /repo/esecjos/cdpi-main
 
 #### 2.3 Almost all alfred does.
 
 mkdir cdpi-main/cmake_build
 
 cd $repo/epg
 
setup_workspace make -C 3pp CONFIG=Linux_x86_64 openssl

cd /repo/esecjos/cdpi-main/cmake_build

cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRIND=OFF -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -DUSE_CLANG_COVERAGE=OFF -DUSE_ASAN=OFF -DBUILD_TEST_HEUR=OFF -DBUILD_TEST_TOOLKIT=OFF -DHEURPACKAGE_SCOPE= -GNinja /repo/esecjos/cdpi-main

ninja

ninja install





### 3. PCG

See Bob.md