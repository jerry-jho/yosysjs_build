# yosysjs_build

Walkthrough:

    git clone https://github.com/emscripten-core/emsdk.git
    cd emsdk
    git pull
    ./emsdk install latest
    ./emsdk activate latest
    source ./emsdk_env.sh
    cd ..
    
    git clone https://github.com/YosysHQ/yosys.git
    cd yosys
    make config-emcc
    
Then edit Makefile.conf and set ENABLE_ABC := 1
edit Makefile and set ABCREV = default
edit abc/Makefile and add -std=c++14 to CFLAGS
    
    make