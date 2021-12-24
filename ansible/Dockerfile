FROM ubuntu:20.04

LABEL maintainer=""

ARG DEBIAN_FRONTEND=noninteractive

ENV ANSIBLE_HOST_KEY_CHECKING=False

# Update and install required software and tools
RUN echo "***** Updating and installing required software and tools" && \
    apt --assume-yes update && \
    apt --assume-yes install ansible \
                             sshpass

# Cleanup
RUN echo "***** Cleaning up" && \
    apt --assume-yes clean && \
    apt --assume-yes autoclean && \
    apt --assume-yes autoremove && \
    rm -rf \
           /tmp/* \
           /var/lib/apt/lists/* \
           /var/tmp/*
