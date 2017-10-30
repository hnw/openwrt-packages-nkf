# openwrt-packages-nkf [![Build Status](https://secure.travis-ci.org/hnw/openwrt-packages-nkf.svg?branch=master)](https://travis-ci.org/hnw/openwrt-packages-nkf)

This is [nkf](https://osdn.jp/projects/nkf/) package for OpenWrt, tested on OpenWrt 15.05.1 / LEDE 17.01.4.

# How to install binary package

See [hnw/openwrt-packages](https://github.com/hnw/openwrt-packages).

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ echo 'src-git hnw_nkf https://github.com/hnw/openwrt-packages-nkf.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install nkf
$ make packages/nkf/compile
```
