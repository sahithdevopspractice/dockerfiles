Need some help with pushing an image to docker hub:-

I have tried this steps as mentioned in the Class:-

Step 1 Build the image:- docker build -t from:v1 .
Output:- 
[ centos@ip-172-31-27-132 ~/dockerfiles/FROM ]$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
from         v1        6677f032afc5   2 years ago   231MB
firstimage   v1        6677f032afc5   2 years ago   231MB

Step 2 Retag the image:- docker tag from:v1 sahith9/from:v1
Output:- 
[ centos@ip-172-31-27-132 ~/dockerfiles/FROM ]$ docker images
REPOSITORY     TAG       IMAGE ID       CREATED       SIZE
firstimage     v1        6677f032afc5   2 years ago   231MB
from           v1        6677f032afc5   2 years ago   231MB
sahith9/from   v1        6677f032afc5   2 years ago   231MB

Step3:- I have logged in into my dockerhub account

Step 4 tried to push the image:- [ centos@ip-172-31-27-132 ~/dockerfiles/FROM ]$ docker push from:v1 sahith9/from:v1
Output:- "docker push" requires exactly 1 argument.
See 'docker push --help'.

Usage:  docker push [OPTIONS] NAME[:TAG]

Upload an image to a registry

Queston 1:- How to verify if the image is pushed to docker hub or not?
I logged in into my docker hub account and checked but i did see any images there.

It might be a silly queston but I just now stareted practice so it's looks like a big issue for me, any help is appriciated and thank you.

