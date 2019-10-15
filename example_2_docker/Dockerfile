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

# install deap 
RUN conda install -c conda-forge deap

#install pytorch
RUN conda install -c pytorch pytorch


#ADD hello.py /

#CMD [ "python3", "./hello.py" ]


# add this and below command will run without cache
ARG CACHEBUST=1


# add complete(inside) contents of folder "reinforceml"  to homefolder

ADD reinforceml /


#ADD reinforceml $HOME/src
CMD [ "python", "/experiments/expt_1/classification_expt.py" ]


