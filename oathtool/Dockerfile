FROM ubuntu:20.10

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update -qqy \
    && apt install apt-transport-https curl build-essential -qqy

RUN curl -sL https://download.savannah.nongnu.org/releases/oath-toolkit/oath-toolkit-2.6.7.tar.gz | tar xz

RUN cd oath-toolkit-2.6.7 && ./configure && make check install

RUN ldconfig

ENTRYPOINT [ "oathtool" ]
