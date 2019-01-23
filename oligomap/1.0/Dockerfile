##### BASE IMAGE #####
FROM ubuntu:18.04

##### METADATA #####
LABEL base.image="ubuntu:18.04"
LABEL version="1"
LABEL software="oligomap"
LABEL software.version="1.0"
LABEL software.description="Oligomap"
LABEL software.website=""
LABEL software.documentation=""
LABEL software.license=""
LABEL software.tags="Genomics,Transcriptomics"
LABEL maintainer="foivos.gypas@unibas.ch"
LABEL maintainer.organisation="Biozentrum, University of Basel"
LABEL maintainer.location="Klingelbergstrasse 50/70, CH-4056 Basel, Switzerland"
LABEL maintainer.lab="Zavolan Lab"
LABEL maintainer.license="https://spdx.org/licenses/Apache-2.0"

COPY oligomap $HOME

RUN apt-get update \
  && apt-get install -y tzdata \
  && ln -fs /usr/share/zoneinfo/Europe/Berlin /etc/localtime \
  && dpkg-reconfigure --frontend noninteractive tzdata \
  && cp oligomap /usr/local/bin/ \
  && apt-get autoremove --purge --yes
