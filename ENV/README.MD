to build the image:- docker build -t env:v1 .
to run and open the ports:- docker run -d -p 8080:80 env:v1
to login and inspect:- docker exec -it imageid bash
Env instruction is used to declare the variables

