# Source image upon to build
FROM --platform=linux/x86_64 debian

# Standard to define a maintainer of the image
LABEL maintainer=@pwolter

# ARG defines an ENV variable
ARG DEBIAN_FRONTEND=noninteractive

# let's install some software
RUN apt-get update --fix-missing && \
	apt-get install -y \
	wget bzip2 ca-certificates qemu \
	libglib2.0-0 libxext6 libsm6 libxrender1

RUN echo 'export PATH=/opt/miniconda/bin:$PATH' > /etc/profile.d/conda.sh && \
	wget --quiet \
	https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O /tmp/miniconda.sh && \
    /bin/bash /tmp/miniconda.sh -b -p /opt/miniconda && \
    rm /tmp/miniconda.sh

RUN apt-get install -y curl grep sed dpkg tini && \
    apt-get clean 
