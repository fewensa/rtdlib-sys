rtdlib-sys
===

[![Build Status](https://api.travis-ci.org/fewensa/rtdlib-sys.svg)](https://travis-ci.org/fewensa/rtdlib-sys/)


`rtdlib-sys` can call [td](https://github.com/tdlib/td) for rust.


## How include tdjson

The first you need read [td](https://github.com/tdlib/td#building) know how to build td.

And then, when you have `tdjson` dylib file (.so/.lib/.dll) copy the file to the path of the system `$PATH` variable.

Or set an environment `RUSTFLAGS`, in the development phase, you can set `RUSTFLAGS` environment to you IDE.

### Linux

```bash
export RUSTFLAGS="-C link-args=-Wl,-rpath,/path/to/lib_dir"
cargo run
```

### Windows

**MSVC**

```bash
RUSTFLAGS=-C link-args=-LIBPATH:D:/path/to/lib_dir
```


