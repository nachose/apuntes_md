## Cores

### PCG


 docker run --rm -it --entrypoint /usr/bin/gdb --volume $PWD:$PWD --workdir $PWD selndocker.mo.sw.ericsson.se/proj-pc-upf-dev/eric-pc-up-data-plane.debug:1.101.167-1 --ex "file /usr/local/sbin/data-plane" --ex "core-file core3"

--> Desde bash. </br>Es muy sensible a los espacios, así que es mejor copiar de aquí directamente.

-->Desde tcsh:</br>
Debería ser igual, pero poniendole {} a las env variables.


Para lanzar solamente una bash en ese contenedor.
 docker run --rm -it --entrypoint /bin/bash --volume $PWD:$PWD --workdir $PWD selndocker.mo.sw.ericsson.se/proj-pc-upf-dev/eric-pc-up-data-plane.debug:1.101.167-1


More complete command, also from bash:

docker run -e COLUMNS=`tput cols` -e LINES=`tput lines` -e TERM=${TERM} --rm -it --init --entrypoint /usr/bin/gdb --volume $PWD:$PWD --workdir $PWD selndocker.mo.sw.ericsson.se/proj-pc-upf-dev/eric-pc-up-data-plane.debug:1.101.167-1 --ex "file /usr/local/sbin/data-plane" --ex "core-file core3"
 
 For tcsh:
 
docker run -e COLUMNS=`tput cols` -e LINES=`tput lines` -e TERM=${TERM} --rm -it --init --entrypoint /usr/bin/gdb --volume ${PWD}:${PWD} --workdir ${PWD} selndocker.mo.sw.ericsson.se/proj-pc-upf-dev/eric-pc-up-data-plane.debug:1.103.155-0 --ex "file /usr/local/sbin/data-plane" --ex "core-file core3"


print $_siginfo --> Print info of the last signal sent.

### Ways to find executable

Other ways to find which executable generated a core --> https://stackoverflow.com/questions/13308922/find-which-program-caused-a-core-dump-file