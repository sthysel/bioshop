# this is the official dockerhub OpenJDK java 6,
# not Oracle's more performant and propably more compatible version.
FROM java:6
MAINTAINER sthysel <sthysel@gmail.com>
ENV REFRESHED_AT 2015-06-04

ENV FASTQC_ZIP fastqc_v0.11.3.zip 

RUN mkdir /fastqc
WORKDIR /fastqc
RUN wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/${FASTQC_ZIP} \
    && unzip ${FASTQC_ZIP} \
    && rm ${FASTQC_ZIP}

RUN chmod +x /fastqc/FastQC/fastqc
CMD ["/fastqc/FastQC/fastqc"]


