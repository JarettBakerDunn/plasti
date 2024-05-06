FROM ubuntu:jammy

RUN apt-get update && \
  DEBIAN_FRONTEND='noninteractive' \
  DEBCONF_NONINTERACTIVE_SEEN='true' \
  apt-get install --yes \
    build-essential \
    git \ 
    gfortran \
    liblapack-dev \
    libopenblas-dev 

RUN useradd \
  --create-home \
  plasti_user 

USER plasti_user

WORKDIR /home/plasti_user

RUN git clone 'https://github.com/geodynamics/plasti'; cd plasti; make FORT="gfortran -fallow-argument-mismatch";

ENV PATH="/home/plasti_user/ellipsis3d:${PATH}"
