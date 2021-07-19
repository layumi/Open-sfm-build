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
             -DPYBIND11_PYTHON_VERSION=3.6 \
             -DPYTHON_INSTALL_DIR=/home/zzd/anaconda3/lib/python3.6/site-packages \
             && \
    sudo make install   
```

```
conda config --add channels conda-forge
```

```
    conda install exifread gpxpy networkx pyproj python-dateutil xmltodict loky repoze.lru
```
