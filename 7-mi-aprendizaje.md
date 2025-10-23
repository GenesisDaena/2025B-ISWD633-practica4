# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Antes de la práctica, no tenía experiencia directa creando Dockerfiles ni comprendía la función específica de cada instrucción y el orden que deben seguir. Después de la práctica, aprendí a escribir Dockerfiles adecuados y a entender cómo cada instrucción (FROM, RUN, COPY, ADD, ENTRYPOINT, ENV, EXPOSE, CMD) impacta el proceso de construcción y el funcionamiento del contenedor. Además aprendí a construir una imagen de Docker a partir de un Dockerfile con un comando específico. Por otro lado, aprendí la manera de calcular la memoria swap máxima disponible y la existencia de healthcheck que permite definir comandos específicos para comprobar si un contenedor se considera saludable.

Durante la práctica, me encontré con un error al intentar construir la imagen con CentOS 7 debido a la desconexión de los repositorios oficiales. Investigando, descubrí que RockyLinux 8 es el sustituto natural y adapté mi Dockerfile usando FROM rockylinux:8 y cambiando el gestor de paquetes a dnf. Esto me permitió continuar y cumplir los objetivos de la práctica.
