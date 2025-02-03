FROM ubuntu

RUN apt update && apt install ssh sudo -y

RUN adduser ansible

RUN echo "ansible:123" | chpasswd

RUN usermod -aG sudo ansible


ENTRYPOINT service ssh start && bash


#172.17.0.2