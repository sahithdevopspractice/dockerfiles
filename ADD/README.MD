ADD VS COPY:-
Both are used to copy the files from local to image but ADD have two extra capabilities 
ADD can directly download files from internet
ADD can directly untar the tar files.

docker buld -t add:v1 .
docker run -d -p 80:80 add:v1
to check if the file is added or not
docker exec -it imageid bash

added a tar file manually, to check if it's gets untat ot not,
make sure every time you make changes rebuilt the image again.