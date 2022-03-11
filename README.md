# Lenovo_G40_70M EFI for MacOS Monterey

引导为Opencore7.9

### 电脑配置

| 规格     | 详细信息                                                |
| -------- | ----------------------------------------------------- |
| 电脑型号 | Lenovo G40 70M 笔记本电脑                                    |
| 操作系统 | MacOS MacOS Monterey（全版本，除非没更新）                                   |
| 处理器   | Intel Core i5-4258U @ 2.40GHz 双核                   |
| 内存     | 12 GB ( DDR3L 1600MHz ) （加装了一块）                          |
| 硬盘     | SATA 固态硬盘                        |
| 显卡     | Intel HD Graphics 5100  (platform-id:0x0A2E0006)       |
| 声卡     |  Conexant CX20751 (layout-id:3)              |
| 网卡     | AC3160,部分网卡不可用，具体请看[官方文档](https://download.lenovo.com/consumer/mobiles_pub/lenovo_g_z_40_series_hmm.pdf)                     |

### 安装镜像

**将镜像中EFI替换为本仓库的EFI文件夹**

### Opencore

* 支持Monterey
* 睡眠唤醒 无效
* 核显支持，采用`Lilu+WhateverGreen`通过`OC/kext`方式注入
* 声卡为Conexant CX20751 ，使用 `AppleALC` ，layout-id:3，通过`OC/kext`方式注入
* 无线网卡更换为 `AC3160` 使用仓库的脚本安装驱动
* 显示器亮度调节无效，原因未知
* 补丁格式为`.aml`,如有需要请自行处理，要在config.plist中加入
* 电池显示无效，原因未知
* 触摸板手势正常,采用`VoodooPS2`，点击无效
* 注：声卡id需自行尝试.3,21,28三个注入
