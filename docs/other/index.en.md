---
hide:
  - navigation
  - footer
---

???+ question "Why do you see this notice?"

    The script of this project currently mainly serves Simplified Chinese users, but from the very beginning it was defined as a universal mirror switching script, providing many command options for customization, which is also one of the reasons why this project is now available to users of other languages. The script output is currently fixed in Simplified Chinese. With feedback and usage from users of other languages, the script may support Traditional Chinese and English in the future.

    The documentation is translated with tools, and some professional terms below may be inaccurate. Corrections are welcome.

## :simple-docker:{style="color: #1d63ed"} Docker Installation & Mirror Switching Script

=== "Install"

    !!! quote ""

        === ":linuxmirrors: Official Site (Recommended)"

            ``` bash
            bash <(curl -sSL https://linuxmirrors.cn/docker.sh)
            ```

        === ":simple-github: GitHub"

            ``` bash
            bash <(curl -sSL https://raw.githubusercontent.com/SuperManito/LinuxMirrors/main/DockerInstallation.sh)
            ```

        === ":simple-gitee: Gitee"

            ``` bash
            bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/DockerInstallation.sh)
            ```
            > Real-time sync, no delay. Recommended for use in mainland China network environments.

        === ":gitcode: GitCode"

            ``` bash
            bash <(curl -sSL https://raw.gitcode.com/gh_mirrors/li/LinuxMirrors/raw/main/DockerInstallation.sh)
            ```
            > This project has joined the GitHub acceleration plan, with a 1-hour sync delay.

        === ":simple-jsdelivr: jsDelivr (CDN)"

            ``` bash
            bash <(curl -sSL https://cdn.jsdelivr.net/gh/SuperManito/LinuxMirrors@main/DockerInstallation.sh)
            ```

        === ":tencent-cloud: Tencent Cloud EO (CDN)"

            ``` bash
            bash <(curl -sSL https://edgeone.linuxmirrors.cn/docker.sh)
            ```
            > Not supported in mainland China network environments.

        Integrates installation of [`Docker Engine`](https://docs.docker.com/engine) and [`Docker Compose`](https://docs.docker.com/compose), supports selecting or switching software sources and registry mirrors, installing specific versions, reinstalling, and supports ARM architecture.

        The script refers to the [official documentation](https://docs.docker.com/engine/install) and uses the system package manager for installation. There are no compatibility or security issues. The available versions are determined by the Docker CE repository.

=== "Only Switch Registry Mirror"

    !!! quote ""

        === ":linuxmirrors: Official Site (Recommended)"

            ``` bash
            bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --only-registry
            ```

        === ":simple-github: GitHub"

            ``` bash
            bash <(curl -sSL https://raw.githubusercontent.com/SuperManito/LinuxMirrors/main/DockerInstallation.sh) --only-registry
            ```

        === ":simple-gitee: Gitee"

            ``` bash
            bash <(curl -sSL https://gitee.com/SuperManito/LinuxMirrors/raw/main/DockerInstallation.sh) --only-registry
            ```
            > Real-time sync, no delay. Recommended for use in mainland China network environments.

        === ":gitcode: GitCode"

            ``` bash
            bash <(curl -sSL https://raw.gitcode.com/gh_mirrors/li/LinuxMirrors/raw/main/DockerInstallation.sh) --only-registry
            ```
            > This project has joined the GitHub acceleration plan, with a 1-hour sync delay.

        === ":simple-jsdelivr: jsDelivr (CDN)"

            ``` bash
            bash <(curl -sSL https://cdn.jsdelivr.net/gh/SuperManito/LinuxMirrors@main/DockerInstallation.sh) --only-registry
            ```

        === ":tencent-cloud: Tencent Cloud EO (CDN)"

            ``` bash
            bash <(curl -sSL https://edgeone.linuxmirrors.cn/docker.sh) --only-registry
            ```
            > Not supported in mainland China network environments.

!!! tip "Docker Compose no longer needs to be installed separately"

    Starting from V2, Docker Compose is part of the Docker CLI. The script integrates the installation of this [plugin](https://docs.docker.com/compose/install/linux) by default. Please use the `docker compose` command instead of `docker-compose`.

!!! node "About Software Sources"

    <div class="grid cards" markdown>

    -   __Docker CE Software Repository__

        ---

        Docker CE stands for Docker Community Edition, which is another name for Docker Engine. This repository is used to download and install Docker-related packages.

    -   __Docker Registry Mirror__

        ---

        Used to control the default source repository for pulling images, also known as a registry accelerator. The default is the official container registry [Docker Hub](https://hub.docker.com).

    </div>

    Due to certain uncontrollable factors, Docker Hub is generally inaccessible in mainland China, making it impossible to pull images. It is recommended to use the domestic registry mirrors listed below.

    Note: The specified WEB protocol in the script is only for controlling the `Docker CE` software source. `Docker Registry` always uses the `HTTPS` protocol.


!!! quote "Built-in Registry Mirrors"

    <div style="text-align: center" markdown>
    <div style="font-size: 0.8rem"><strong>Available in Mainland China</strong></div>

    | Site Name | Address | Description |
    | :--: | :--: | :-- |
    | 1ms Mirror | [docker.1ms.run](https://1ms.run "docker.1ms.run") | Enterprise mirror, CDN smart distribution, extremely fast, supports paid customization, recommended |
    | Docker Proxy | [dockerproxy.net](https://dockerproxy.net "dockerproxy.net") | Created by ghproxy, highly available but slow, supports paid enterprise acceleration |
    | DaoCloud | [docker.m.daocloud.io](https://docker.m.daocloud.io "docker.m.daocloud.io") | Well-known enterprise mirror, highly available and fast, now whitelist only |
    | 1Panel Mirror | [docker.1panel.live](https://1panel.cn "docker.1panel.live") | Enterprise product self-use mirror |

    <blockquote style="border-left: none !important">This open source project is not suitable for collecting personal self-built registry accelerators. If needed, you can use command options to specify your own.</blockquote>

    <div style="font-size: 0.8rem; margin-top: 1rem"><strong>Others</strong></div>

    | Site Name | Address | Site Name | Address |
    | :- | :-: | :- | :-: |
    | Alibaba Cloud (Hangzhou) | [registry.cn-hangzhou.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-hangzhou.aliyuncs.com") | Alibaba Cloud (Japan - Tokyo) | [registry.ap-northeast-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.ap-northeast-1.aliyuncs.com") |
    | Alibaba Cloud (Shanghai) | [registry.cn-shanghai.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-shanghai.aliyuncs.com") | Alibaba Cloud (Singapore) | [registry.ap-southeast-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.ap-southeast-1.aliyuncs.com") |
    | Alibaba Cloud (Qingdao) | [registry.cn-qingdao.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-qingdao.aliyuncs.com") | Alibaba Cloud (Malaysia - Kuala Lumpur) | [registry.ap-southeast-3.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.ap-southeast-3.aliyuncs.com") |
    | Alibaba Cloud (Beijing) | [registry.cn-beijing.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-beijing.aliyuncs.com") | Alibaba Cloud (Indonesia - Jakarta) | [registry.ap-southeast-5.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.ap-southeast-5.aliyuncs.com") |
    | Alibaba Cloud (Zhangjiakou) | [registry.cn-zhangjiakou.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-zhangjiakou.aliyuncs.com") | Alibaba Cloud (Germany - Frankfurt) | [registry.eu-central-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.eu-central-1.aliyuncs.com") |
    | Alibaba Cloud (Hohhot) | [registry.cn-huhehaote.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-huhehaote.aliyuncs.com") | Alibaba Cloud (UK - London) | [registry.eu-west-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.eu-west-1.aliyuncs.com") |
    | Alibaba Cloud (Ulanqab) | [registry.cn-wulanchabu.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-wulanchabu.aliyuncs.com") | Alibaba Cloud (US West - Silicon Valley) | [registry.us-west-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.us-west-1.aliyuncs.com") |
    | Alibaba Cloud (Shenzhen) | [registry.cn-shenzhen.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-shenzhen.aliyuncs.com") | Alibaba Cloud (US East - Virginia) | [registry.us-east-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.us-east-1.aliyuncs.com") |
    | Alibaba Cloud (Heyuan) | [registry.cn-heyuan.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-heyuan.aliyuncs.com") | Alibaba Cloud (UAE - Dubai) | [registry.me-east-1.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.me-east-1.aliyuncs.com") |
    | Alibaba Cloud (Guangzhou) | [registry.cn-guangzhou.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-guangzhou.aliyuncs.com") | Google Cloud (North America) | [gcr.io](https://cloud.google.com/artifact-registry/docs/transition/gcr-repositories?hl=zh-cn "https://gcr.io") |
    | Alibaba Cloud (Chengdu) | [registry.cn-chengdu.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-chengdu.aliyuncs.com") | Google Cloud (Asia) | [asia.gcr.io](https://cloud.google.com/artifact-registry/docs/transition/gcr-repositories?hl=zh-cn "https://asia.gcr.io") |
    | Alibaba Cloud (Hong Kong) | [registry.cn-hongkong.aliyuncs.com](https://help.aliyun.com/zh/acr/user-guide/accelerate-the-pulls-of-docker-official-images "https://registry.cn-hongkong.aliyuncs.com") | Google Cloud (Europe) | [eu.gcr.io](https://cloud.google.com/artifact-registry/docs/transition/gcr-repositories?hl=zh-cn "https://eu.gcr.io") |
    | Tencent Cloud | [mirror.ccs.tencentyun.com](https://cloud.tencent.com/document/product/1207/45596 "https://mirror.ccs.tencentyun.com") | Docker Hub | [registry.hub.docker.com](https://hub.docker.com/ "registry.hub.docker.com") |

    <blockquote style="border-left: none !important">Note: Registry mirrors from domestic cloud computing companies are only for their own business. Instances in mainland China may still not be able to access Docker Hub.</blockquote>

    </div>

- ### Command Options (Advanced Usage)

    | Name | Meaning | Value |
    | :-: | :-: | :-: |
    | `--source` | Specify `Docker CE` source address (domain or IP) | `address` |
    | `--source-registry` | Specify registry mirror address (domain or IP) | `address` |
    | `--branch` | Specify Docker CE repository | `repo name (see docs below)` |
    | `--codename` | Specify Debian-based OS codename | `codename` |
    | `--designated-version` | Specify `Docker CE` installation version | `version (see docs below)` |
    | `--protocol` | Specify WEB protocol for `Docker CE` source | `http` or `https` |
    | `--use-intranet-source` | Prefer intranet Docker CE mirror address | `true` or `false` |
    | `--install-latest` | Whether to install the latest Docker Engine | `true` or `false` |
    | `--close-firewall` | Whether to disable the firewall | `true` or `false` |
    | `--clean-screen` | Whether to clear the screen before running | `true` or `false` |
    | `--only-registry` | Only switch registry mirror mode | none |
    | `--ignore-backup-tips` | Ignore backup overwrite prompt (do not backup) | none |
    | `--pure-mode` | Pure mode, minimal output | none |

    > Full source format: `<WEB protocol>://<source address (domain or IP)>/<repository path>`

    - #### Specify Docker CE Source Address

        ``` { .bash .no-copy }
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --source mirror.example.com/docker-ce
        ```
        > Note: The address path must include the Docker CE repository path, i.e., `docker-ce`.

    - #### Specify Registry Mirror Address

        ``` { .bash .no-copy }
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --source-registry registry.example.com
        ```

    - #### Only Switch Registry Mirror

        === "Use Script for One-Click Replacement"

            Only switches the registry accelerator. If Docker is not installed, an error will be reported and exit.

            ``` bash
            bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --only-registry
            ```

        === "Manual Replacement"
        
            - Install the `jq` package

                === "Debian-based / openKylin"

                    ``` bash
                    apt-get install -y jq
                    ```

                    > `Debian` &nbsp; `Ubuntu` &nbsp; `Kali` &nbsp; `Linux Mint` &nbsp; `Deepin` &nbsp; `Zorin OS` &nbsp; `Armbian` &nbsp; `Proxmox VE` &nbsp; `Raspberry Pi OS` &nbsp; `openKylin`

                    For new systems, run `apt-get update` first.

                === "RedHat-based / openEuler / OpenCloudOS / Anolis OS"

                    ``` bash
                    dnf install -y jq || yum install -y jq
                    ```

                    > `Red Hat Enterprise Linux` &nbsp; `CentOS` &nbsp; `Rocky Linux` &nbsp; `AlmaLinux` &nbsp; `Fedora` &nbsp; `openEuler` &nbsp; `OpenCloudOS` &nbsp; `Anolis OS`

            - Specify registry mirror address

                > Manually replace `<example.registry.com>` with the registry address. See the address column in the "Built-in Registry Mirrors" table above.

                ``` bash
                SOURCE_REGISTRY='"https://<example.registry.com>"'
                ```
                You can also specify multiple registry mirrors, e.g., `SOURCE_REGISTRY='"https://example.registry.com","https://test.registry.com"'`, separated by commas.

            - Replace registry mirror address

                ``` bash
                [ -s "/etc/docker/daemon.json" ] || echo "{}" >/etc/docker/daemon.json
                jq '.["registry-mirrors"] = ['"${SOURCE_REGISTRY}"']' /etc/docker/daemon.json >/etc/docker/daemon.json.tmp && mv /etc/docker/daemon.json.tmp
                ```

            - Restart Docker service

                ``` bash
                systemctl daemon-reload
                [[ $(systemctl is-active docker) == "active" ]] && systemctl restart docker || systemctl enable --now docker
                ```

    - #### Specify Docker CE Repository

        The script will automatically detect this in most cases. Specify only if you have special requirements.

        ``` { .bash .no-copy }
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --branch centos
        ```
        > Repository names are fixed: `centos`, `debian`, `fedora`, `raspbian`, `rhel`, `sles`, `static`, `ubuntu`  
        > See [official installation docs](https://docs.docker.com/engine/install) and [Docker CE official repo](https://download.docker.com/linux) for details.

    - #### Specify Docker CE Installation Version

        When specifying a version, the "install latest" option is ignored. Format: `major.minor.patch`, e.g., `27.4.1`.

        ``` { .bash .no-copy }
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --designated-version 27.0.0
        ```
        > If the specified version does not exist or is not supported on your system, the script will report an error and exit.

        ??? quote "How to view available versions"

            === "Debian-based"

                ``` bash
                apt-cache madison docker-ce | awk '{print $3}' | grep -Eo "[0-9][0-9].[0-9]{1,2}.[0-9]{1,2}" | sort -t '.' -k1,1nr -k2,2nr -k3,3nr
                ```

                > `Debian` &nbsp; `Ubuntu` &nbsp; `Kali` &nbsp; `Linux Mint` &nbsp; `Deepin` &nbsp; `Zorin OS` &nbsp; `Armbian` &nbsp; `Proxmox VE` &nbsp; `Raspberry Pi OS`

            === "RedHat-based / openEuler / OpenCloudOS / Anolis OS"

                ``` bash
                dnf list docker-ce --showduplicates | sort -r | awk '{print $2}' | grep -Eo "[0-9][0-9].[0-9]{1,2}.[0-9]{1,2}" | sort -t '.' -k1,1nr -k2,2nr -k3,3nr
                ```

                > `Red Hat Enterprise Linux` &nbsp; `CentOS` &nbsp; `Rocky Linux` &nbsp; `AlmaLinux` &nbsp; `Fedora` &nbsp; `openEuler` &nbsp; `OpenCloudOS` &nbsp; `Anolis OS`

            Versions not listed are not supported by this script. If you cannot get the version list, your system environment has not been properly configured for the Docker CE repository (this will not happen when running the script).


    - #### Unattended (Automation)

        To perform installation without interaction, use at least the following options. Recommended for experienced users.

        ``` { .bash .no-copy title="Example Command" }
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) \
          --source mirror.example.com/docker-ce \
          --source-registry registry.hub.docker.com \
          --protocol http \
          --use-intranet-source false \
          --install-latest true \
          --close-firewall true \
          --ignore-backup-tips
        ```
        > If you get an "invalid option" error, check the option validity and whitespace encoding. Each option is written on a separate line for readability.

    - #### Pure Mode

        This feature is introduced to facilitate developers. After it is enabled, the script content output will be simplified. It is recommended to use it with other command options without interaction.

        ``` bash
        bash <(curl -sSL https://linuxmirrors.cn/docker.sh) --pure-mode
        ```

        !!! tip "Scrolling command logs may have unpredictable display issues, but no problems have been found so far."

- ### FAQ

    - #### About Service Startup Errors

        !!! quote ""

            In non-fresh environments, you may encounter `Docker` service startup failures after running the script. It is recommended to reinstall to resolve this. Uninstalling will not delete local images or container data.

            Uninstall commands:

            === "Debian-based"

                ``` bash
                apt-get remove -y docker* containerd.io runc && apt-get autoremove
                ```

                > `Debian` &nbsp; `Ubuntu` &nbsp; `Kali` &nbsp; `Linux Mint` &nbsp; `Deepin` &nbsp; `Zorin OS` &nbsp; `Armbian` &nbsp; `Proxmox VE` &nbsp; `Raspberry Pi OS`

            === "RedHat-based / openEuler / OpenCloudOS / Anolis OS"

                ``` bash
                yum remove -y docker* containerd.io podman* runc
                ```

                > `Red Hat Enterprise Linux` &nbsp; `CentOS` &nbsp; `Rocky Linux` &nbsp; `AlmaLinux` &nbsp; `Fedora` &nbsp; `openEuler` &nbsp; `OpenCloudOS` &nbsp; `Anolis OS`

            After uninstalling, simply rerun the script to install.

    - #### About unsupported operating systems

        If it prompts that it is not supported, please use the system's own package management tool to install it. Because these packages are built and maintained by the Linux distribution's package maintainers and may have differences in configuration or are built from modified source code.

        You can also use [Docker Desktop](https://www.docker.com/products/docker-desktop)
