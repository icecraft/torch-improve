# MNIST Example with the PyTorch C++ Frontend

This folder contains an example of training a computer vision model to recognize
digits in images from the MNIST dataset, using the PyTorch C++ frontend.

The entire training code is contained in `mnist.cpp`.

To build the code, run the following commands from your terminal:

## usage 
*  ln -s libtorch header files 
*  put mnist datasets at /mnt/datasets/mnt or just create soft link
*  put libtorch lib at /mnt/workspace/libtorch_lib or just create soft link



```shell
    meson build
    ninja -C build
    build/mnist
