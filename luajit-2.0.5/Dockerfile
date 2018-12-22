FROM centos:7.5.1804

RUN yum install -y gcc gcc-c++ make git vim gdb \
    && curl -SL http://luajit.org/download/LuaJIT-2.0.5.tar.gz|tar zxf - \
    && cd LuaJIT-2.0.5 \
    && make install \
    && make clean && cd / \
    && curl -fLo /cmake_installer.sh https://cmake.org/files/v3.12/cmake-3.12.4-Linux-x86_64.sh \
    && chmod +x /cmake_installer.sh && mkdir -p /opt/cmake && /cmake_installer.sh --skip-license --prefix=/opt/cmake \
    && rm -f /cmake_installer.sh

ENV PATH /opt/cmake/bin:$PATH

WORKDIR /
