here copy is used to copy the files from your local into the Image.
docker build -t copy:v1 .

Command to remove running container:- docker rm -f `docker ps -a -q'

docker run -d -p 80:80 copy:v1