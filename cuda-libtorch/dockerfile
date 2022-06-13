FROM archlinux:latest

RUN pacman -Syyu --noconfirm cuda cudnn wget unzip cmake make gcc

RUN wget https://download.pytorch.org/libtorch/cu113/libtorch-cxx11-abi-shared-with-deps-1.11.0%2Bcu113.zip \
	&& unzip libtorch-cxx11-abi-shared-with-deps-1.11.0+cu113.zip \
	&& rm libtorch-cxx11-abi-shared-with-deps-1.11.0+cu113.zip \
	&& mv libtorch /usr/include/libtorch
