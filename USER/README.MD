ps -ef | grep sleep
sudo kill -9 process id

docker run -d user:v1
docker exec -it imageid bash

Every docker container is a process inside operating system.

your not supposed to run the docker container as a root user, if you do so it a security leakage, anybody can get the underline complete storage.
Docker containers are running in host vm, so here docker containers are not supposed to access each other, it's called isolated process, if you give root access to the container apudu em ayithadi ante user can login as root user can access the operating system, can access the storage.

So to disable this we have to add a user before atleast cmd instruction,

FROM almalinux:8
RUN adduser sahith--- to run this command we need root access
USER sahith-- if we place user before cmd command, we can ristrict the root access, comands which you will place after user will run with user access.
CMD ["sleep", "100"], 
