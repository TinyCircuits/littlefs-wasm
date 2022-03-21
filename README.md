# TinyCircuits Fork

To build on Linux, publish to GitHub, and then consume with NPM, do the following
1. `git clone --recursive https://github.com/TinyCircuits/littlefs-wasm.git`
2. `cd littlefs-wasm`
3. `git checkout emulator`
4. `cd emsdk` (https://emscripten.org/docs/getting_started/downloads.html)
5. `git submodule update --init --recursive`
6. `./emsdk install latest`
7. `./emsdk activate latest`
8. `source ./emsdk_env.sh`
9. `cd..`
10. `make`
11. `git push <token:url>`

Now the source is updated and published to GitHub under the emulator branch. Consume/use the JavaScript/WASM file in `dist` by installing through `npm install https://github.com/TinyCircuits/littlefs-wasm.git#emulator`