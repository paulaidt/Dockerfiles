##### BASE IMAGE #####
FROM python:3.6.5

##### METADATA #####
LABEL base.image="python:3.6.5"
LABEL version="3"
LABEL software="ucsc_pairwise_alignments_custom_scripts"
LABEL software.version="0.1"
LABEL software.description="Custom scripts for ucsc alignments"
LABEL software.website=""
LABEL software.documentation=""
LABEL software.license="link to license(file) of original software"
LABEL software.tags="Genomics, Transcriptomics"
LABEL maintainer="foivos.gypas@unibas.ch"
LABEL maintainer.organisation="Biozentrum, University of Basel"
LABEL maintainer.location="Klingelbergstrasse 50/70, CH-4056 Basel, Switzerland"
LABEL maintainer.lab="Zavolan Lab"
LABEL maintainer.license="https://spdx.org/licenses/Apache-2.0"

##### VARIABLES #####
# Use variables for convenient updates/re-usability
ENV SOFTWARE_VERSION 0.1

RUN apt-get update -y \
  && apt-get autoremove -y && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
  && pip install wget==3.2

COPY *.py /usr/bin/
