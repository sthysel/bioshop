FROM ubuntu:14.04
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-06-11

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y --no-install-recommends \
  apt-transport-https \
  build-essential \
  cmake \
  wget \
  python \
  git \
  curl \
  zlib1g-dev

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENV GEMINI_ROOT /gemini

RUN mkdir -p ${GEMINI_ROOT}/{bin, data}
WORKDIR ${GEMINI_ROOT}

RUN wget --no-check-certificate https://raw.github.com/arq5x/gemini/master/gemini/scripts/gemini_install.py \
        && python gemini_install.py ${GEMINI_ROOT} ${GEMINI_ROOT}/data
ENV PATH ${GEMINI_ROOT}/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

