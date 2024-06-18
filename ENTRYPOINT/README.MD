CMD VS ENTRYPOINT
cmd and entrypoint both will run at container creation time only, but there is slightly difference between them, 

bult the image:- docker build -t entry:v1 .
docker run entry:v1:- When you run this command after building the image you can see command is hitting goole.com
docker ps -a:- 
docker run entry:v1 ping yahoo.com now it will ping yahoo.com repetedly until you stop
docker ps -a :- here you can check  which command is ececuting


Conclusion:-
1-- cmd command can be overwritten by another cammand at run time
2-- Entrypoint command can't be overwritten, if you try to do so, the command you are entering at run time will go and append to entrypoint.
3-- we can use CMD and Entrypoint for best results, you can use CMD instructions to supply default arguments to ENTRYPOINT
4-- User can always override CMD arguments from run time 



to check what command is running:- docker ps -a --no-trunc
