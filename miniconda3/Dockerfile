# Source image upon to build
FROM debian

# Standard to define a maintainer of the image
LABEL maintainer=@pwolter

# ARG defines an ENV variable
ARG DEBIAN_FRONTEND=noninteractive

# let's install some software
RUN apt-get update --fix-missing && \
	apt-get install -y \
	wget bzip2 ca-certificates \
	libglib2.0-0 libxext6 libsm6 libxrender1
