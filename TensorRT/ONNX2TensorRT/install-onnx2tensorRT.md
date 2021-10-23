## Prerequest
Make sure tensorRT and its dependencies has been installed by following [here](../install_tensorRT.md)

## Install CMake
```bash
sudo apt purge --auto-remove cmake
wget -O - https://apt.kitware.com/keys/kitware-archive-latest.asc 2>/dev/null | gpg --dearmor - | sudo tee /etc/apt/trusted.gpg.d/kitware.gpg >/dev/null
# Ubuntu 20.04
sudo apt-add-repository 'deb https://apt.kitware.com/ubuntu/ focal main'     
# Ubuntu 18.04
sudo apt-add-repository 'deb https://apt.kitware.com/ubuntu/ bionic main'
# Ubuntu 16.04
sudo apt-add-repository 'deb https://apt.kitware.com/ubuntu/ xenial main'

sudo apt update
sudo apt install cmake
```

## Install Protobuf
```bash
sudo apt-get install libprotobuf-dev protobuf-compiler
```

```bash
PATH_TO_TRT='/usr/local/TensorRT-8.0.1.6'
cd onnx-tensorrt
mkdir build && cd build
cmake .. -DTENSORRT_ROOT=$PATH_TO_TRT && make -j
export LD_LIBRARY_PATH=$PWD:$LD_LIBRARY_PATH
```
