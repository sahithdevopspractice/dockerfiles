LABEL IS A indtruction in docker,
which will provide the metadata of the container
so that it will be easy to identify,
format is key=value pair

docker build -t label:v1

labels are helpful in filteration of images
docker images --filter label=TRAINER=SIVA
