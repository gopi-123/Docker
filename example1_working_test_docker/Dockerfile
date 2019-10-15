FROM ubuntu:latest


#RUN apt-get update \
#  && apt-get install -y python3-pip python3-dev \
#  && cd /usr/local/bin \
#  && ln -s /usr/bin/python3 python \
#  && pip3 install --upgrade pip
#"""
#RUN apt install -y docker.io
#RUN usermod -a -G docker $USER
#RUN docker pull continuumio/anaconda3
#RUN docker run continuumio/anaconda3 /bin/bash
#RUN pip3 install matplotlib

RUN apt-get update
RUN apt-get install -y wget
RUN wget https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh
RUN bash Anaconda3-5.0.1-Linux-x86_64.sh -b
RUN rm Anaconda3-5.0.1-Linux-x86_64.sh



# Set path to conda
ENV PATH /root/anaconda3/bin:$PATH

# Updating Anaconda packages
#RUN conda update conda
RUN conda update anaconda


ADD hello.py /
CMD 'chmod 755 hello.py'
CMD  "./hello.py"
