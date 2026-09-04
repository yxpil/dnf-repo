# BIT DNF 源（Fedora / RHEL / openSUSE 等）

自托管 RPM 仓库，由 CI 从 [BIT Releases](https://github.com/yxpil/bit/releases) 自动同步。

```bash
sudo dnf config-manager addrepo --from-repofile=https://yxpil.github.io/dnf-repo/bit.repo
sudo dnf install bit
```

- 架构: x86_64 / aarch64
- 元数据: repodata/primary.xml.gz（由 [gen_repos.py](https://github.com/yxpil/bit/blob/main/packaging/repos/gen_repos.py) 生成）
