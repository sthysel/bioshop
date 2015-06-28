# Build documentation:
# https://gemini.readthedocs.org/en/latest/content/installation.html

FROM sthysel/bioshop-common
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-06-11

# jus going with the lastes updates in bioshop-common
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get install -y --no-install-recommends \
  python2.7 \
  curl \
  zlib1g-dev

ENV GEMINI_ROOT /gemini

RUN mkdir -p ${GEMINI_ROOT}/{bin, data}
WORKDIR ${GEMINI_ROOT}

RUN ln -s /usr/bin/python2.7 /usr/bin/python
RUN wget --no-check-certificate https://raw.github.com/arq5x/gemini/master/gemini/scripts/gemini_install.py \
        && python2.7 gemini_install.py ${GEMINI_ROOT} ${GEMINI_ROOT}/data
ENV PATH ${GEMINI_ROOT}/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
