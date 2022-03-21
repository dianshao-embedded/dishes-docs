---
title: 欢迎使用上菜
description: 一个物联网终端 OTA 管理平台
geekdocNav: false
geekdocAlign: center
geekdocAnchor: false
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable MD033 -->

<!-- markdownlint-restore -->

上菜是一个物联网终端 OTA 及远程连接管理平台，其提供固件自动更新及远程控制台连接功能，帮助嵌入式开发人员开发、管理、维护设备

{{< button size="large" relref="quickstart" >}}  使用手册  {{< /button >}}
[Github 仓库](https://github.com/dianshao-embedded/dishes-admin)

<br>
<br>

## 项目特点

{{< columns >}}

### 自动化更新

上菜提供标准化的 OTA 更新流程，根据开发阶段可选择 Dev Test Prod 三个不同固件类型，上菜会根据不同类型自动执行终端更新操作

<--->

### 远程连接

针对 Linux 终端，上菜基于 Wireguard VPN 与终端保持连接，可实时通过 ssh 连接控制设备

<--->

### 可被集成

上菜可被集成进 CI/CD 工具 (Jenkins, GitLab CI/CD etc.) 以及开发工具中，实现从开发到部署一站式解决方案 

{{< /columns >}}