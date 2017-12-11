FROM drydockaarch64/u16:v5.10.1

RUN sudo apt-get update && sudo apt-get install -yy \
  autoconf \
  automake \
  ccache \
  clang-3.8 \
  gcc-4.8 \
  graphviz \
  kmod \
  libconfig-dev \
  libcunit1-dev \
  libnuma-dev \
  libpcap-dev \
  libssl-dev \
  libtool \
  linux-headers-`uname -r` \
  mscgen \
  ruby-dev \
  xsltproc

RUN wget "https://github.com/Shippable/support/raw/master/bin/reports" && \
    chmod +x reports && \
    rm -f /home/shippable/cexec/bin/reports && \
	mkdir -p /home/shippable/cexec/bin && \
	cp reports /home/shippable/cexec/bin/

RUN sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 10
RUN sudo ln -s /usr/bin/clang-3.8 /usr/bin/clang
