Expose is an instruction from docker
It is used to know which ports are open in an Image

EXPOSE 80/tcp:- it means port numebr 80 is opened with tcp protocal, this instruction will not add any functionality, this is only for information purpose only,

docker build -t expose:v1 .

docker inspect imageid