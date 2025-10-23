# Limitar uso de procesador
Limitar la cantidad de núcleos de CPU:
```
--cpus=<número de núcleos>
```

Asignar núcleos de CPU específicos:
```
--cpuset-cpus=<lista de núcleos>
```

**¿Como saber el numero de procesadores virtuales que tiene una máquina?**
## COMPLETAR
Ya que el número de procesadores virtuales de una máquina se corresponde con el número de procesadores lógicos detectados por el sistema operativo.
Se puede usar los siguientes comandos:<br>
Muestra cuántos núcleos físicos y cuántos procesadores lógicos tiene.
```
wmic cpu get NumberOfCores,NumberOfLogicalProcessors
```
O también, el siguiente comando que devuelve directamente el número total de procesadores lógicos.
```
echo %NUMBER_OF_PROCESSORS%
```

## Ejemplos
_Puedes copiar y ejecutar directamente cada uno de los comandos_

Limitar el uso de CPU a 1.5 núcleos
```
docker run -d --name server-nginx --cpus="1.5" nginx:alpine
```

Restringir el contenedor para que use los núcleos de CPU 0 a 2:
```
docker run -d --name server-nginx --cpuset-cpus="0-2" nginx:alpine
```

Restringir el contenedor para que use los núcleos de CPU 1 y 3:
```
docker run -d --name server-nginx --cpuset-cpus="1,3" nginx:alpine
```
