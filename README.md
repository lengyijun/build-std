An example to demonstrate build-std in Cargo.

```
rustup update nightly
git clone https://github.com/rust-lang/rust --depth=1
cd rust
git submodule update --init
cd ..
__CARGO_TESTS_ONLY_SRC_ROOT=`pwd`/rust cargo build --target custom-target.json -Zbuild-std=core,compiler_builtins,alloc,std -vv
```
