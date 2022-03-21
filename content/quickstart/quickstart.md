---
title: 快速开始
weight: 2
---

{{< toc >}}

## 1. 说明

本文将从零开始，让您快速的部署**上菜**并更新一个 [rauc](https://rauc.io/) 升级包。

本文主要目的是让您快速体验**上菜**，希望在短时间内，可以说服您这个项目对于终端 OTA 升级管理是有用的。

详细的使用说明请参考后续文章，里面会更加详细的介绍上菜所有的功能以及您最好掌握的相关知识说明。

## 2. 安装

### 2.1 安装准备

目前，上菜已经在 Windows (Win10 & Win11) 和 Linux (Ubuntu, Fedora, CentOS 8) 环境下完成测试。你可以选择你习惯的操作系统环境作为 Docker 主机， 请根据如下官方文档安装 Docker & Docker-Compose

[docker 安装说明](https://docs.docker.com/engine/install/)

[docker-compose 安装说明](https://docs.docker.com/compose/install/)

### 2.2 安装

1. 下载项目
    
   ```sh
   $ git clone https://github.com/dianshao-embedded/dishes-admin.git && cd ./dishes-client
   ```

2. Docker 镜像编译
   ```sh
   $ sudo docker-compose build
   ```

   *注意：Docker 构建默认使用国内镜像源*

3. Docker 容器启动
   ```sh
   $ sudo docker-compose up
   ```

## 3. 创建产品

1. 创建产品，产品为相同终端的集合

1. 目前仅支持创建 Linux 类终端，RTOS 终端待开发
2. 目前仅支持更新 rauc 升级包，swu 及其他升级包待开发
3. 更新方式可选自动或者手动，自动和手动仅代表 PROD 固件是否自动更新
4. 网络连接方式支持 http 和 mqtt， 目前只支持 http

![product-screenshot](/dishes-docs/images/product.png)

## 4. 创建设备

1. 完成产品创建后，点击每行右侧设备按钮进入设备界面

2. 创建设备，输入序列号、设备名、选择终端阶段
3. 终端阶段分为 dev, test, prod，其中 dev 阶段为研发人员开发阶段，test 阶段为测试阶段，prod 阶段为产品生产阶段，每个阶段的更新策略不同
4. 目前仅支持 dev 阶段更新，其他两个阶段更新逻辑待开发
   
![device-screenshot](/dishes-docs/images/device.png)

## 5. 添加固件

1. 点击产品行右侧固件按钮，进入固件页面，在其中添加更新固件包
2. 目前只支持 rauc 更新包，rauc 更新框架请参考 https://rauc.io/
3. 需要选择固件版本号与阶段 (dev, test, prod)，会根据阶段自动更新该阶段所有终端
4. dev 阶段设备无需考虑版本号是否适配，直接更新
   
5. test 与 prod 终端则会检查版本号是否适配

![firmware-screenshot](/dishes-docs/images/firmware.png)


## 6. 查看更新状态

上述添加更新包操作完成后，平台通知终端进行固件更新操作，终端更新完成后会显示更新状态

![update-screenshot](/dishes-docs/images/update.png)

## 7. 与 CI/CD 工具及开发工具配合使用

用户可以通过 dishes-agent 将上菜集成到 CI/CD 工具及开发工具中

可以参考颠勺中如何集成，实现在开发平台中一键部署固件到终端




