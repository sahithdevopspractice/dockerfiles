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

How to push docker image into docker hub?
Step1:- Buld an image by using the command "docker build -t sample:v1 ."
Here -t is for tagging
sample is image name
:
v1 is version
.---present working directory
Output:- docker images
[ centos@ip-172-31-23-251 ~/dockerfiles/FROM ]$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
sample       v1        6677f032afc5   2 years ago   231MB

Step2:- Now login into your docker hub account using your credentials like username and password.

Step3:- Retag the build image
docker tag sample:v1 sahith9/sahith9:sampleimage
Here sample:v1 is image name and tag
sahith9/sahith9 is mydockerhub username/repository name
sampleimage is retagged image

Step 4:- Push the image to docker hub
docker push sahith9/sahith9:sampleimage
