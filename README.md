# mongodb_cpp

配置方法
```bash
sudo apt install -y g++ tmux jq
sudo apt install -y cmake wget libmongoc-1.0-0 libbson-1.0 libssl-dev libsasl2-dev doxygen

tar xzf mongo-c-driver-1.23.2.tar.gz
mkdir -p mongo-c-driver-1.23.2/cmake-build
cd mongo-c-driver-1.23.2/cmake-build
cmake -DENABLE_AUTOMATIC_INIT_AND_CLEANUP=OFF ..
sudo make install

tar -xzf mongo-cxx-driver-r3.6.7.tar.gz
cd mongo-cxx-driver-r3.6.7/build
cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_CXX_STANDARD=17 -DBSONCXX_POLY_USE_MNMLSTC=1 -DCMAKE_INSTALL_PREFIX=/usr/local
sudo cmake --build . --target EP_mnmlstc_core
cmake --build .
sudo cmake --build . --target install
```
