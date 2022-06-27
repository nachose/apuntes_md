## Compiling commands

python cdpi-main/NSTdpifws/dpiregressionfw/bin/scripts/regression.py --dpisim-package buildout/dpisim_epg_package.tgz -p CUPS cdpi-main/NSTtests/dpiregression/suites/suite_cups_appID_rule_interaction.xml 

Compiling EPG

"build -c lin up/all"  --> Compilar el user plane

build -c lin data-plane_upf_DPI_2_UPSFTSUITE --> Compilar un test case


./build/Linux_x86_64/bin/data-plane_upf_DPI_2_UPSFTSUITE/data-plane_upf_DPI_2_UPSFTSUITE_Linux_x86_64.elf -vvv TC21922  --> ver la salida del comando


Compile DPI

From a dpi shell, execute the following.

Create a dir cmake_build dentro de cdpi-main

Cd and execute 
$  cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo -DINTEGRATION_MODE=OFF -DCMAKE_TOOLCHAIN_FILE=/repo/esecjos/BuildAndTools/cmake/linux_x86_64.cmake -DUSE_MEMCHECK_VALGRID=ON -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DUSE_EPG_3PP=ON -GNinja ..

From <https://teams.microsoft.com/multi-window/?agent=electron&version=22050101009> 

Inside.

Execute ninja: $ ninja