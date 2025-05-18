FROM ubuntu:24.04
RUN apt-get update \
  && DEBIAN_FRONTEND=noninteractive apt-get install -y \
       js8call pulseaudio-utils x11-apps \
  && rm -rf /var/lib/apt/lists/*
# User and home
RUN useradd -m js8
USER js8
WORKDIR /home/js8
