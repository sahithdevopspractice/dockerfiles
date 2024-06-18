ARG VS ENV
ARG instruction can provide values to the Dockerfile only at buildtime.
ENV variables have access in the container as well.

FROM almalinux:8
ARG username
RUN adduser $username
USER $username
CMD ["sleep","100"]

docker build -t arg:v1 --build-arg username=sivakumar .

Once you done the above step do build the following dockerfile

How do I use ARG Variables inside containers?
Assign the values of ARG to ENV varibles so that you can access them inside container as well.

FROM almalinux:8
ARG username
RUN adduser $username
USER $username
ARG COURSE
ARG TRAINER
RUN echo "course: ${COURSE}, Trainer: ${TRAINER}"
ENV COURSE=${COURSE}
ENV TRAINER=${TRAINER}
CMD ["sleep","100"]

So here what happens, dockerfile build chesetapudu arg lo pass chesina values, image build ayyaka env variables ki pass chesthundi.

docker build -t arg:v1 --build-arg username=sahith --build-arg COURSE=DevOps --build-arg TRAINER=Sahith .
After building the image check values are added in the container.
docker run -d arg:v1
docker exec -it imageid bash

Note:- Regarding Using ARG inthe dockerfile at first line
ARG version
FROM almalinux:${version}
ARG username
RUN adduser $username
USER $username
ARG COURSE
ARG TRAINER
RUN echo "course: ${COURSE}, Trainer: ${TRAINER}"
ENV COURSE=${COURSE}
ENV TRAINER=${TRAINER}
CMD ["sleep","100"]

### So here there is only one execption using ARG instruction at first line:-
you can use AGR instruction before FROM instruction to provide the version. So whathappens now so here we can provide the version at the run time.

ARG instruction can be used before FROM instruction to provide values to FROM instruction.
ARG value defined before FROM will not be acessed after FROM