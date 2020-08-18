FROM ubuntu:16.04
WORKDIR /root
RUN apt-get update && apt-get install -y \
  git \
  lzip \
  m4 \
  make \
  libgmp-dev \
  libglib2.0-dev \
  libssl-dev \
  software-properties-common \
  vim \
  wget

ADD cmake-3.18.1-Linux-x86_64.sh . 
RUN echo "yy" | bash cmake-3.18.1-Linux-x86_64.sh && ln -s cmake cmake-3.18.1-Linux-x86_64/bin/cmake /bin/cmake
RUN cmake --version

ADD install.sh .
RUN ["bash", "install.sh"]
CMD ["/bin/bash"]
