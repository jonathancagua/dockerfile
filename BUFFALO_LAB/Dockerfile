FROM ubuntu:22.04
MAINTAINER Jon jonathan.cagua@gmail.com
RUN rm -rf /var/lib/apt/lists/*
RUN apt-get update && \
    apt-get install -y git make ninja-build
RUN rm -rf /var/lib/apt/lists/*
WORKDIR /home/dev
ADD . /home/dev
COPY toolchain_gcc_t-head_linux /home/dev
ENV PATH $PATH:/home/dev/toolchain_gcc_t-head_linux/bin

WORKDIR /home/app

#Bajar:
#git clone https://gitee.com/bouffalolab/toolchain_gcc_t-head_linux
