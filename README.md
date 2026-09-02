# dnf 软件源（BIT）

Fedora / RHEL / CentOS Stream / openSUSE 等可直接添加本源安装 BIT。

```bash
sudo tee /etc/yum.repos.d/bit.repo <<'EOF'
[bit]
name=BIT
baseurl=https://yxpil.github.io/dnf-repo
enabled=1
gpgcheck=0
EOF
sudo dnf install bit
```

> 说明：本源未做 GPG 签名（`gpgcheck=0`）；RPM 包与 GitHub Release 的 .rpm 完全一致（SHA256 相同），HTTPS 传输保证完整性。

支持的架构：

| 架构 | 芯片 |
|---|---|
| x86_64 | Intel / AMD / 兆芯 / 海光 |
| aarch64 | 飞腾 / 鲲鹏 / 麒麟 |

升级：`sudo dnf upgrade bit`

卸载：`sudo dnf remove bit`

各架构 RPM 也可从 [Releases](https://github.com/yxpil/bit/releases) 直接下载。
