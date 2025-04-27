## Description

This tool generate prebuilt versions (or latest version by default) of:
1. TCC from git://repo.or.cz/tinycc.git
2. libgc from https://github.com/ivmai/bdwgc/.

for [vlang](https://github.com/vlang/v), something like [tccbin](https://github.com/vlang/tccbin).

## Pre-Install 

1. windows : `git`, [`Visual Studio Build Tools​`](https://visualstudio.microsoft.com/zh-hans/downloads/)(include `nmake`, `cl`)
2. nix : `git`, `automake`, `libtool`, `gmake`
3. ubuntu : `libgc-dev` 
3. freebsd : `boehm-gc-threaded-8.2.8`
4. openbsd : `boehm-gc`

## Usage

Simply run it:
```
v run updater.v
```

## Config

There is a config file `updater.toml`, it provide a easy way develop 
config for different platform/system.

1. [global] provide global config for the `updater`.
2. [tools_need] config tools need for different system(`nix` or `windows`).
3. [download] provide the git url and commit settings.
4. Then different platform/system configs. Such as [windows] is for `windows`, 
   [aarch64] is for `aarch64` platforms.

## Tested on

1. Windows 10 LTSC
2. Ubuntu 24.04.2 LTS amd64
3. OpenBSD 7.6 amd64
4. FreeBSD 14.2 amd64
5. Ubuntu 22.04.5 LTS aarch64