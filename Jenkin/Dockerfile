FROM ubuntu:latest

EXPOSE 8080
EXPOSE 50000
ENV TZ=Europe/Minsk
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update && apt install sudo -y && apt install wget -y \
&& apt-get install -y software-properties-common && sudo add-apt-repository ppa:deadsnakes/ppa && sudo apt install openjdk-11-jdk-headless -y  && java --version \ 
&& sudo apt-get install python3.8 -y  && python3.8 --version \
&& sudo apt install python3-pip -y && pip --version 
RUN wget http://archives.jenkins-ci.org/war-stable/2.361.1/jenkins.war 
RUN sudo apt-get install git -y && git --version && whereis git 
RUN sudo apt-get install python3.8-venv
CMD java -jar jenkins.war


