FROM almalinux:8
RUN cd /tmp
RUN echo "Hello Docker" > hello.txt
CMD ["sleep","100"]

so here when you built and run the above container RUN cd /tmp will not work,
we have to set it by using workdir instruction.
FROM almalinux:8
WORKDIR cd /tmp
RUN echo "Hello Docker" > hello.txt
CMD ["sleep","100"]

so here whathappens is you will directly launch into mentioned workdir folder, and what all are the instructions which you have mentioned after workdir will run in the mentioned folder