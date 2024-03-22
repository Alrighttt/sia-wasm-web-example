# sia-wasm-web-example

https://alrighttt.github.io/sia-wasm-web-example/

A simple demonstration on how to utilize the WASM object outputted by Sia's walletd

## Build

Clone the Sia `web` repo: 

`https://github.com/SiaFoundation/web`

Build the WASM binary:

`~/web/walletd$ GOOS=js GOARCH=wasm go build -o ./bin.wasm ./wasm/`

The above will out a WASM binary, `bin.wasm`.

In order to use this, we must import the go js library of the go version we used to compile this, generally named wasm_exec.js

if using goenv this can be found at: `$(go env GOROOT)/misc/wasm/wasm_exec.js`

if using goenv: `~/.goenv/versions/1.21.7/misc/wasm/wasm_exec.js`

See available methods at:
https://github.com/SiaFoundation/web/blob/3ffeded85d89b1df63782a05c64ad5e026b35700/walletd/wasm/wasm.go#L17
