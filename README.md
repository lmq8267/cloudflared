# cloudflared - mipsel (mipsle)

<p align="center">
  <img alt="" src="https://img.shields.io/github/created-at/lmq8267/cloudflared?logo=github&label=%E5%88%9B%E5%BB%BA%E6%97%A5%E6%9C%9F">
<a href="https://github.com/lmq8267/cloudflared/releases"><img src="https://img.shields.io/github/downloads/lmq8267/cloudflared/total?logo=github&label=%E4%B8%8B%E8%BD%BD%E9%87%8F"></a>
<a href="https://github.com/lmq8267/cloudflared/releases/"><img src="https://img.shields.io/github/release/lmq8267/cloudflared?logo=github&label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC"></a>
<a href="https://github.com/lmq8267/cloudflared/issues"><img src="https://img.shields.io/github/issues-raw/lmq8267/cloudflared?logo=github&label=%E9%97%AE%E9%A2%98"></a>
<a href="GitHub repo size"><img src="https://img.shields.io/github/repo-size/lmq8267/cloudflared?logo=github&label=%E4%BB%93%E5%BA%93%E5%A4%A7%E5%B0%8F"></a>
<a href="https://github.com/lmq8267/cloudflared/actions?query=workflow%3ABuild"><img src="https://img.shields.io/github/actions/workflow/status/lmq8267/cloudflared/build.yml?branch=main&logo=github&label=%E6%9E%84%E5%BB%BA%E7%8A%B6%E6%80%81" alt=""></a>
</p>

CI参考：https://github.com/minetaro12/cloudflared-mipsle


官方项目：https://github.com/cloudflare/cloudflared

https://github.com/lmq8267/cloudflared/releases/latest/download/cloudflared

## 🎁 cloudflared 命令帮助（简体中文版）

> 以下为 `cloudflared -h` 的完整输出翻译。

```text
# ./cloudflared -h

名称:
   cloudflared - Cloudflare 的命令行工具和代理

用法:
   cloudflared [全局选项] [命令] [命令选项]

版本:
   2026.7.3 (构建于 2026-07-06 08:17 UTC)

描述:
   cloudflared 将您的机器或用户身份连接到 Cloudflare 的全球网络。
     您可以使用它来通过 Cloudflare Access 对某个 API 进行身份认证以便触达，将 Web 流量路由到这台机器，
     并配置访问控制。

     更多深入文档，请参阅 https://developers.cloudflare.com/cloudflare-one/connections/connect-apps

命令:
   update     如果存在新版本，则更新程序（mipsle不支持）
   version    打印版本
   proxy-dns  dns-proxy 功能已不再支持
   tail       从远程 cloudflared 输出日志流
   service    管理 cloudflared 系统服务
   help, h    显示命令列表或某个命令的帮助

   Access:
     access, forward  access 子命令

   Tunnel:
     tunnel  使用 Cloudflare Tunnel 将内网服务穿透到公网，或暴露给已接入 Cloudflare 的私有网络用户

全局选项:
   --output value                               日志输出格式（default, json，默认: "default"）[$TUNNEL_MANAGEMENT_OUTPUT, $TUNNEL_LOG_OUTPUT]
   --proxy-dns                                   作为本地 DNS 代理（默认: false）
   --proxy-dns-port value                        DNS 代理监听端口（默认: 0）
   --proxy-dns-address value                     DNS 代理监听地址
   --proxy-dns-upstream value                    上游 DNS 服务器（可接受多个输入）
   --proxy-dns-max-upstream-conns value          单个上游 DNS 的最大连接数（默认: 0）
   --proxy-dns-bootstrap value                    引导（Bootstrap）DNS 服务器（可接受多个输入）
   --credentials-file value, --cred-file value   读取/写入隧道凭据的文件路径 [$TUNNEL_CRED_FILE]
   --region value                                要连接的 Cloudflare Edge 区域。留空或设为空值则连接全球区域。[$TUNNEL_REGION]
   --edge-ip-version value                       要使用的 Cloudflare Edge IP 地址版本。{4, 6, auto}（默认: "auto"）[$TUNNEL_EDGE_IP_VERSION]
   --edge-bind-address value                    绑定用于出站连接到 Cloudflare Edge 的 IP 地址。[$TUNNEL_EDGE_BIND_ADDRESS]
   --label value                                 使用此选项为特定的连接器（Connector）赋予一个有意义的标签。连接器启动时，会生成一个该连接器唯一标识。这是一个 uuid。为了更容易识别某个连接器，我们通常会使用运行连接器的机器主机名再加上连接器 ID。如果您希望对自己某个连接器的命名拥有更多控制权，就可以使用此选项。
   --post-quantum, --pq                          启用后创建实验性的后量子安全隧道（默认: false）[$TUNNEL_POST_QUANTUM]
   --management-diagnostics                      是否开放可通过管理服务访问的诊断路由（/debug/pprof、/metrics 等）（默认: true）[$TUNNEL_MANAGEMENT_DIAGNOSTICS]
   --overwrite-dns, -f                           用此主机名覆盖现有 DNS 记录（默认:   false）[$TUNNEL_FORCE_PROVISIONING_DNS]
   --help, -h                                    显示帮助（默认: false）
   --version, -v, -V                             打印版本（默认:   false）

版权:
   (c) 2026 Cloudflare Inc.
   您安装 cloudflared 软件即表示您已签署签名，同意以下条款
   的 Apache License Version 2.0（https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/license）、
   服务条款（https://www.cloudflare.com/terms/）以及隐私政策（https://www.cloudflare.com/privacypolicy/）。
```

英文原文（供对照）：

```text
NAME:
   cloudflared - Cloudflare's command-line tool and agent

USAGE:
   cloudflared [global options] [command] [command options]

VERSION:
   2026.7.3 (built 2026-08-06-08:17 UTC)

DESCRIPTION:
   cloudflared connects your machine or user identity to Cloudflare's global network.
     You can use it to authenticate a session to reach an API behind Access, route web traffic to this machine,
     and configure access control.

     See https://developers.cloudflare.com/cloudflare-one/connections/connect-apps for more in-depth documentation.

COMMANDS:
   update     Update the agent if a new version exists
   version    Print the version
   proxy-dns  dns-proxy feature is no longer supported
   tail       Stream logs from a remote cloudflared
   service    Manages the cloudflared system service
   help, h    Shows a list of commands or help for one command

   Access:
     access, forward  access <subcommand>

   Tunnel:
     tunnel  Use Cloudflare Tunnel to expose private services to the Internet or to Cloudflare connected private users.

GLOBAL OPTIONS:
   --output value                               Output format for the logs (default, json) (default: "default") [$TUNNEL_MANAGEMENT_OUTPUT, $TUNNEL_LOG_OUTPUT]
   --proxy-dns                                  (default: false)
   --proxy-dns-port value                       (default: 0)
   --proxy-dns-address value
   --proxy-dns-upstream value                   (accepts multiple inputs)
   --proxy-dns-max-upstream-conns value                    (default: 0)
   --proxy-dns-bootstrap value                  (accepts multiple inputs)
   --credentials-file value, --cred-file value  Filepath at which to read/write the tunnel credentials [$TUNNEL_CRED_FILE]
   --region value                               Cloudflare Edge region to connect to. Omit or set to empty to connect to the global region. [$TUNNEL_REGION]
   --edge-ip-version value                     Cloudflare Edge IP address version to connect with. {4, 6, auto} (default: "auto") [$TUNNEL_EDGE_IP_VERSION]
   --edge-bind-address value                     Bind to IP address for outgoing connections to Cloudflare Edge. [$TUNNEL_EDGE_BIND_ADDRESS]
   --label value                                 Use this option to give a meaningful label to a specific connector. When a connector starts up, a connector id unique to the tunnel is generated. This is a uuid. To make it easier to identify a connector, we will use the hostname of the machine the tunnel is running on along with the connector ID. This option exists if one wants to have more control over what their individual connectors are called.
   --post-quantum, --pq                          When given creates an experimental post-quantum secure tunnel (default: false) [$TUNNEL_POST_QUANTUM]
   --management-diagnostics                      Enables the in-depth diagnostic routes to be made available over the management service (/debug/pprof, /metrics, etc.) (default: true) [$TUNNEL_MANAGEMENT_DIAGNOSTICS]
   --overwrite-dns, -f                            Overwrites existing DNS records with this hostname (default: false) [$TUNNEL_FORCE_PROVISIONING_DNS]
   --help, -h                                   show help (default: false)
   --version, -v, -V                            Print the version (default: false)

COPYRIGHT:
   (c) 2026 Cloudflare Inc.
   Your installation of cloudflared software constitutes a symbol of your signature indicating that you accept
   the terms of the Apache License Version 2.0 (https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/license),
   Terms (https://www.cloudflare.com/terms/) and Privacy Policy (https://www.cloudflare.com/privacypolicy/).
```
