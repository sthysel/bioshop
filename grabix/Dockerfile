# https://github.com/arq5x/grabix
FROM sthysel/bioshop-common
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-06-28

RUN apt-get install -y --no-install-recommends \
  zlib1g-dev \
  python

RUN mkdir /src/
WORKDIR /src/
RUN git clone https://github.com/arq5x/grabix.git \
  && cd grabix \
  && make \
