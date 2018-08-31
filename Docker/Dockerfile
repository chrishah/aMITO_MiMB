FROM chrishah/mitobim:latest

MAINTAINER Christoph Hahn <christoph.hahn@uni-graz.at>

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y -q ncbi-blast+ muscle

WORKDIR /home/working
