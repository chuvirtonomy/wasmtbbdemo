# Build and test demo project

## Environment
Tested in Ubuntun 20.04

## Pre-requisite
Install latest emcc by following: https://emscripten.org/docs/getting_started/downloads.html

Compile wasmtbb https://github.com/hpcwasm/wasmtbb by:

git clone https://github.com/hpcwasm/wasmtbb

emmake make tbb

## Build demo project

make sure TBB include path correctly points to WASMTBB in cmakelist:
set(TBB_INCLUDE_DIR "/home/ubuntu/wasmtbb/include")

following the commands
mkdir buildwasm
cd buildwasm/
emmake cmake ..
make

## Test demo project
node tbbdemo

Terminal output:

Allocating a new web worker from /home/ubuntu/wasmtbbdemo/buildwasm/tbbdemo.worker.js

Allocating a new web worker from /home/ubuntu/wasmtbbdemo/buildwasm/tbbdemo.worker.js

test

Example::init(2)

0.001

created 64 tasks

0

runParallel done 

7.616

runSerial done 

15.106

threadInit
