## Complex commands

grep -rI 'ctx_deployment_mcs.csh' . | cut -d ":" -f 1 | xargs sed -i "s,ctx_deployment_mcs.csh,ctx_deployment_mcs.bash,g" --> encontrar los archivos que tienen una cadena, separar el nombre, y realizar una sustitución a todos ellos.
