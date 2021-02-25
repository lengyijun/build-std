Port https://github.com/apache/incubator-teaclave-sgx-sdk here

```
__CARGO_TESTS_ONLY_SRC_ROOT=`pwd`/rust cargo b --target x86_64-unknown-linux-sgx.json -Zbuild-std=core,alloc,std
```
