# About
Rust bindings to `libwebp`, `libwebpdemux`, and workarounds for static/inline C functions and some other miscellaneous stuff.

**Much of the API doc comments from the C header files have been included with their rust FFI counterparts.**

## Modules `raw` & `sys`
Raw, unaltered symbols are under the `raw` module. Also most of the `raw` symbols are re-exported under the `sys` module, with more idiomatic rust naming conventions. E.g. the `WebPValidateConfig` function is renamed to `webp_validate_config`.


## llvm

Maybe you need to install llvm first:

```
OS=$(uname)


if [ "$OS" = "Darwin" ]; then
    # brew install llvm@8
    export LLVM_CONFIG_PATH=/usr/local/opt/llvm/bin/llvm-config
    export PATH=/opt/local/llvm/bin:${PATH}
else
    # apt-get install llvm-8
    export LLVM_CONFIG_PATH=/usr/bin/llvm-config-8
    export PATH=/usr/bin:${PATH}
fi
```

