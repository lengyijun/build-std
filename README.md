An example to demonstrate build-std in Cargo.

```
# suggested way
rustup component add rust-src
cp -r ~/.rustup/toolchains/nightly-x86_64-unknown-linux-gnu/lib/rustlib/src/rust . 
__CARGO_TESTS_ONLY_SRC_ROOT=`pwd`/rust cargo build --target custom-target.json -Zbuild-std=core,compiler_builtins,alloc,std -vv
```

```
# another approach
rustup update nightly
git clone https://github.com/rust-lang/rust --depth=1
cd rust
git submodule update --init
cd ..
__CARGO_TESTS_ONLY_SRC_ROOT=`pwd`/rust cargo build --target custom-target.json -Zbuild-std=core,compiler_builtins,alloc,std -vv
```
