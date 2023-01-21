# wasm-c-example

WebAssembly example using C using [Emscripten](https://emscripten.org/).

Activate the Emscripten SDK:

```bash
git clone https://github.com/emscripten-core/emsdk.git
cd emsdk
./emsdk install latest
./emsdk activate latest
source ./emsdk_env.sh # emcc command now on path
```

Recompiling the `hello.wasm` file:

```bash
emcc hello.c -o hello.js
node hello.js
```

Optimise code, and emit HTML:

```bash
emcc hello.c -O3 -o hello.html
```

Serve via HTTP:

```bash
python -m http.server 8000
```

View the output on http://127.0.0.1:8000/hello.html

Based on example provided by Aaron Turner and licensed under the
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/).