---
hide:
  - navigation
  - feedback
  - footer
---

> 如果您觉得这个项目不错对您有所帮助的话，请点击仓库右上角的 Star 并分享给更多的朋友 :octicons-heart-fill-24:{ .heart style="color: red" }

## :fontawesome-brands-docker:{style="color: #086dd7"} Docker 安装脚本

<table>
<tr>
    <td><a href="https://www.debian.org" target="_blank"><img src="/assets/images/icon/debian.svg" width="16" height="16" style="vertical-align: -0.35em"></a> Debian</td>
    <td><a href="https://access.redhat.com/products/red-hat-enterprise-linux" target="_blank"><img src="/assets/images/icon/redhat.svg" width="16" height="16" style="vertical-align: -0.1em"></a> Red Hat Enterprise Linux</td>
</tr>
<tr>
    <td><a href="https://cn.ubuntu.com" target="_blank"><img src="/assets/images/icon/ubuntu.svg" width="16" height="16" style="vertical-align: -0.15em"></a> Ubuntu</td>
    <td><a href="https://fedoraproject.org/zh-Hans" target="_blank"><img src="/assets/images/icon/fedora.ico" width="16" height="16" style="vertical-align: -0.2em"></a> Fedora</td>
</tr>
<tr>
    <td><a href="https://www.kali.org" target="_blank"><img src="/assets/images/icon/kali-linux.svg" width="16" height="16"></a> Kali Linux</td>
    <td><a href="https://www.centos.org" target="_blank"><img src="/assets/images/icon/centos.svg" width="16" height="16" style="vertical-align: -0.2em"></a> CentOS</td>
</tr>
<tr>
    <td><a href="https://linuxmint.com" target="_blank"><img src="/assets/images/icon/linux-mint.ico" width="16" height="16" style="vertical-align: -0.15em"></a> Linux Mint</td>
    <td><a href="https://rockylinux.org" target="_blank"><img src="/assets/images/icon/rocky-linux.svg" width="16" height="16" style="vertical-align: -0.25em"></a> Rocky Linux</td>
</tr>
<tr>
    <td><a href="https://www.deepin.org" target="_blank"><img src="/assets/images/icon/deepin.png" width="16" height="16" style="vertical-align: -0.3em"></a> Deepin（深度）</td>
    <td><a href="https://almalinux.org/zh-hans" target="_blank"><img src="/assets/images/icon/almalinux.svg" width="16" height="16" style="vertical-align: -0.15em"></a> AlmaLinux</td>
</tr>
<tr>
    <td><a href="https://zorin.com/os" target="_blank"><img src="/assets/images/icon/zorin-os.png" width="16" height="16" style="vertical-align: -0.3em"></a> Zorin OS</td>
    <td><a href="https://www.openeuler.org/zh" target="_blank"><img src="/assets/images/icon/openeuler.ico" width="16" height="16" style="vertical-align: -0.2em"></a> openEuler（开源欧拉）</td>
</tr>
<tr>
    <td><a href="https://www.armbian.com" target="_blank"><img src="/assets/images/icon/armbian.png" width="16" height="16" style="vertical-align: -0.2em"></a> Armbian</td>
    <td><a href="https://www.opencloudos.org" target="_blank"><img src="/assets/images/icon/opencloudos.png" width="16" height="16" style="vertical-align: -0.25em"></a> OpenCloudOS（鸥栖）</td>
</tr>
<tr>
    <td><a href="https://www.proxmox.com" target="_blank"><img src="/assets/images/icon/proxmox.svg" width="16" height="16" style="vertical-align: -0.2em"></a> Proxmox</td>
    <td><a href="https://openanolis.cn" target="_blank"><img src="/assets/images/icon/anolis.png" width="16" height="16" style="vertical-align: -0.1em"></a> Anolis OS（龙蜥）</td>
</tr>
</table>

=== ":octicons-globe-16: 官网（推荐）"

    ``` bash
    bash <(curl -sSL https://linuxmirrors.cn/docker.sh)
    ```

=== ":simple-github: GitHub"

    ``` bash
    bash <(curl -sSL https://raw.githubusercontent.com/SuperManito/LinuxMirrors/main/DockerInstallation.sh)
    ```

=== ":simple-gitee: Gitee 码云"

    ``` bash
    bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/DockerInstallation.sh)
    ```

=== ":simple-jsdelivr: jsDelivr"

    ``` bash
    bash <(curl -sSL https://cdn.jsdelivr.net/gh/SuperManito/LinuxMirrors@main/DockerInstallation.sh)
    ```

支持 `选择或更换软件源以及镜像仓库`、`安装指定版本`、`重装` 等功能，支持 ARM 架构处理器

脚本参考 [官方文档](https://docs.docker.com/engine/install) 使用系统包管理工具安装，集成安装 [`Docker Engine`](https://docs.docker.com/engine) 和 [`Docker Compose (插件)`](https://docs.docker.com/compose/install/linux)

> 注：Docker Compose 自 V2 版本起开始作为 Docker CLI 的一部分，不再需要单独安装，请使用 `docker compose` 命令替代 `docker-compose`

!!! node "软件源说明"

    `Docker CE` 软件仓库，全称 Docker Community Edition（Docker 社区版），用于下载并安装 Docker 相关软件包  
    `Docker Registry` 镜像仓库，用于控制拉取镜像的默认来源存储仓库，又称镜像加速器，默认为官方的 Docker Hub 仓库

    由于一些不可抗力的因素，目前国内网络环境一般无法正常访问 Docker Hub 因此无法拉取镜像，使用推荐的镜像源勉强能够使用不过速度可能会很慢

- ### 命令选项

    | 名称 | 含义 | 选项值 |
    | :-: | :-: | :-: |
    | `--source` | 指定 `Docker CE` 源地址(域名或IP) | 地址 |
    | `--source-registry` | 指定镜像仓库地址(域名或IP) | 地址 |
    | `--codename` | 指定 Debian 系操作系统的版本代号 | 代号名称 |
    | `--install-latest` | 是否安装最新版本的 Docker Engine | `true` 或 `false` |
    | `--close-firewall` | 是否关闭防火墙 | `true` 或 `false` |
    | `--clean-screen` | 是否在运行前清除屏幕上的所有内容 | `true` 或 `false` |
    | `--ignore-backup-tips` | 忽略覆盖备份提示（即不覆盖备份） | 无 |

    > 软件源完整格式 `<WEB协议>://<软件源地址（域名或IP）>/<软件源仓库（路径）>`

- ### 关于服务报错无法启动

    !!! quote ""

        非新装环境可能会在运行脚本后遇到 `Docker` 服务无法启动的情况，建议重新安装来解决，卸载不会删除镜像和容器数据

        卸载命令如下：

        === "Debian 系"

            ``` bash
            apt-get remove -y docker* containerd.io runc && apt-get autoremove
            ```

            > `Debian` &nbsp; `Ubuntu` &nbsp; `Kali` &nbsp; `Linux Mint` &nbsp; `Deepin` &nbsp; `Zorin OS` &nbsp; `Armbian` &nbsp; `Proxmox`

        === "RedHat 系 / openEuler / OpenCloudOS / Anolis OS"

            ``` bash
            yum remove -y docker* containerd.io podman* runc
            ```

            > `Red Hat Enterprise Linux` &nbsp; `CentOS` &nbsp; `Rocky Linux` &nbsp; `AlmaLinux` &nbsp; `Fedora` &nbsp; `openEuler` &nbsp; `OpenCloudOS` &nbsp; `Anolis OS`

        卸载完成后重新执行脚本安装即可

## 其它

提供一些常见服务的一键换源命令，用于备忘

### NPM

适用于 `npm` `yarn` `pnpm` 等

=== "淘宝源"

    ``` bash
    npm config set registry https://registry.npmmirror.com/
    ```

=== "腾讯云"

    ``` bash
    npm config set registry https://mirrors.tencent.com/npm/
    ```

### PYPI

适用于 `pip` `pip3`

=== "阿里云"

    ``` bash
    pip3 config set global.index-url https://mirrors.aliyun.com/pypi/simple/
    ```

=== "腾讯云"

    ``` bash
    pip3 config set global.index-url https://mirrors.tencent.com/pypi/simple/
    ```

=== "中科大"

    ``` bash
    pip3 config set global.index-url https://pypi.mirrors.ustc.edu.cn/simple/
    ```
