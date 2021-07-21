Install gcc-7
```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
sudo apt-get install gcc-7 g++-7
cd /usr/bin
sudo rm gcc
sudo ln -s gcc-7 g++
sudo rm g++
sudo ln -s g++-7 g++
```

```
sudo apt-get update \
    && sudo apt-get install -y \
        build-essential \
        cmake \
        git \
        libatlas-base-dev \
        libeigen3-dev \
        libgoogle-glog-dev \
        libopencv-dev \
        libsuitesparse-dev 
        
    curl -L http://ceres-solver.org/ceres-solver-1.14.0.tar.gz | tar xz && \
    cd ceres-solver-1.14.0 && \
    mkdir -p build && cd build && \
    cmake .. -DCMAKE_C_FLAGS=-fPIC -DCMAKE_CXX_FLAGS=-fPIC -DBUILD_EXAMPLES=OFF -DBUILD_TESTING=OFF && \
    sudo make -j4 install 
```


for Ubuntu-16
``` 
wget http://kr.archive.ubuntu.com/ubuntu/pool/universe/e/eigen3/libeigen3-dev_3.3.4-4_all.deb 
sudo dpkg -i libeigen3-dev_3.3.4-4_all.deb 
```


```python
from distutils.sysconfig import get_python_lib
print(get_python_lib())
```

```bash
    git clone https://github.com/paulinus/opengv.git && \
    cd opengv && \
    git submodule update --init --recursive && \
    mkdir -p build && cd build && \
    cmake .. -DBUILD_TESTS=OFF \
             -DBUILD_PYTHON=ON \
             -DPYBIND11_PYTHON_VERSION=3.7 \
             -DPYTHON_INSTALL_DIR=/home/zzd/anaconda3/lib/python3.7/site-packages \
             && \
    sudo make install   
```

```
conda config --add channels conda-forge
```

```
conda install exifread gpxpy networkx pyproj python-dateutil xmltodict loky repoze.lru sphinx fpdf cloudpickle flask joblib matplotlib pytest six wheel
```

```
python setup.py build
```

