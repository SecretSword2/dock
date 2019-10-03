FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y curl gnupg
RUN curl https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -
RUN apt-get -y install clang-8 lldb-8 lld-8
RUN apt-get -y install make
RUN apt-get -y install xxd
ENV CXX /usr/bin/clang++-8
RUN mkdir /wksp

WORKDIR /wksp

ENTRYPOINT ["/bin/bash"]