FROM ubuntu:22.04
MAINTAINER Jon jonathan.cagua@gmail.com

RUN rm -rf /var/lib/apt/lists/*

RUN apt-get update && \
         apt-get clean && \ 
         apt-get install -y \
             build-essential \
             tar \
             wget \
             libbz2-dev \
             curl
RUN rm -rf /var/lib/apt/lists/*
# Set up a development tools directory
WORKDIR /home/dev
ADD . /home/dev
COPY gcc-arm-none-eabi-10.3-2021.10 /home/dev
ENV PATH $PATH:/home/dev/gcc-arm-none-eabi-10.3-2021.10/bin
WORKDIR /home/app

#Bajar:
#https://developer.arm.com/-/media/Files/downloads/gnu-rm/10.3-2021.10/gcc-arm-none-eabi-10.3-2021.10-x86_64-linux.tar.bz2

#Luego descomprimir ese zip:
#tar -xvf gcc-arm-none-eabi-10.3-2021.10-x86_64-linux.tar.bz2
        
