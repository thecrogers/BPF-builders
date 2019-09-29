from ubuntu:16.10

RUN echo "deb http://llvm.org/apt/$VER/ llvm-toolchain-$VER-3.7 main
RUN deb-src http://llvm.org/apt/$VER/ llvm-toolchain-$VER-3.7 main" | \
  sudo tee /etc/apt/sources.list.d/llvm.list
Run wget -O - http://llvm.org/apt/llvm-snapshot.gpg.key | sudo apt-key add -
RUN sudo apt-get update

# For other versions
RUN sudo apt-get -y install bison build-essential cmake flex git libedit-dev \
  libllvm3.7 llvm-3.7-dev libclang-3.7-dev python zlib1g-dev libelf-dev

# For Lua support
RUN sudo apt-get -y install luajit luajit-5.1-dev
