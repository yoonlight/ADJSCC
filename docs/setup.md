# Setup

- Handle Public GPG Key Error

```sh
# Reference
# https://github.com/NVIDIA/nvidia-docker/issues/1631
rm /etc/apt/sources.list.d/cuda.list
rm /etc/apt/sources.list.d/nvidia-ml.list
apt-key del 7fa2af80
apt-get update
curl -L -O https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-keyring_1.1-1_all.deb
dpkg -i cuda-keyring_1.1-1_all.deb
rm cuda-keyring_1.1-1_all.deb
```

- git install

```sh
add-apt-repository ppa:git-core/ppa
apt update
apt install -y git
```

- Install cmake

```sh
curl -L -O https://github.com/Kitware/CMake/releases/download/v3.28.0-rc5/cmake-3.28.0-rc5.tar.gz
tar -zxvf cmake-3.28.0-rc5.tar.gz
cd cmake-3.28.0-rc5

./bootstrap -- -DCMAKE_USE_OPENSSL=OFF && make && make install
cd ..
rm -r cmake-3.28.0-rc5
```

- pythpn package install

```sh
pip install -r requirements.txt --use-feature=2020-resolver
```
