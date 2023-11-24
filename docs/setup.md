# Setup

```sh
add-apt-repository ppa:git-core/ppa
apt update
apt install -y git
```

```sh
apt-get update
apt-get install git wget
wget https://github.com/Kitware/CMake/releases/download/v3.28.0-rc5/cmake-3.28.0-rc5.tar.gz
cd cmake-3.28.0-rc5

./bootstrap -- -DCMAKE_USE_OPENSSL=OFF
make && make install
cd ..
rm -r cmake-3.28.0-rc5
```
