# clash for OpenWrt

## 介绍

- [Clash][c]

  A rule-based tunnel in Go.

## 编译

- 从 OpenWrt 的 [SDK][s] 编译

  ```bash
  # 以 ar71xx 平台为例
  tar xJf openwrt-sdk-18.06.1-ar71xx-tiny_gcc-7.3.0_musl.Linux-x86_64.tar.xz
  cd openwrt-sdk-*-ar71xx-*
  # 获取 clash Makefile
  git clone https://github.com/honwen/openwrt-clash.git package/clash
  # 选择要编译的包 Network -> clash
  make menuconfig
  # 开始编译
  make package/clash/compile V=99
  ```

[s]: https://openwrt.org/docs/guide-developer/using_the_sdk#obtain_the_sdk
[c]: https://github.com/Dreamacro/clash
