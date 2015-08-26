FROM sthysel/bioshopcommon
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-08-26

RUN apt-get install -y --no-install-recommends \
  python3 \
  python3-dev \
  python3-pip \
  unzip \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN env --unset=DEBIAN_FRONTEND

# cost of layering is better than cost of rebuilding
RUN pip3 install numpy

RUN mkdir /src/
WORKDIR /src/
RUN wget https://github.com/biopython/biopython/archive/master.zip
RUN unzip master.zip
RUN cd biopython-master

VOLUME /data
WORKDIR /data

RUN groupadd -r po && useradd -r -g po po

