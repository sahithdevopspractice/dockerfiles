RUN VS CMD (command) instruction

When we run the command systmectl start catalouge, it will create one node js process and this process will run for infinite time.
As long as this process is running we can say our application is running, once if it stopped application will stop.

CMD:- this instructoin is to make your container running.
RUN:- Runs at  the time image building
CMD:- Runs at the time of container creation, where container is runiing verion of image, CMD instruction is used to run the container infinite times.

Note:- Systemctl commands will not work in container. Because it has to be a main OS to run systemctl command, here containers are not main OS, Container is a process

CMD ["nginx","-g","daemon off;"]:-- Executable format

docker build -t cmd:v1
docker run -d -p 80:80 cmd:v1

if you want to run your image as a container infinite time, you should keep a command inside, you should run it in background, ["nginx","-g","daemon off;"] a foreground command

So even if in linux also if you want to run a process infinite time, then command should be run foreground and attach to the screen, then you send it into background.
So here we are using "-d" detachmode to send the command from foreground to background.