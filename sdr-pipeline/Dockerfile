FROM ubuntu:24.04
RUN apt-get update \
  && DEBIAN_FRONTEND=noninteractive apt-get install -y \
       rtl-sdr sox pulseaudio-utils \
  && rm -rf /var/lib/apt/lists/*
# create pulse socket
RUN mkdir -p /tmp/pulse
