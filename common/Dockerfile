# common image for some bioshop images
# sthysel/bioshopcommon
FROM ubuntu:14.04
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-06-28.b

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y --no-install-recommends \
  ca-certificates \
  apt-transport-https \
  build-essential \
  git \
  wget
