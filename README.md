# ruyi-bin-builds

如果你的发行版不被 [ruyi-builds](github.com/weilinfox/ruyi-builds) 源支持，那么可以使用该单二进制打包源。

经过测试的发行版列表

| 发行版 | x86\_64 | aarch64 | riscv64 |
| :--: | :--: | :--: | :--: |
| Debian Bookworm | x | x | x |
| Debian Trixie | x | x | x |
| Ubuntu Jammy | x | x | x |
| Ubuntu Noble | x | x | x |
| Fedora 38 | x | x | x |
| Fedora 39 | x | x | x |
| Fedora 40 | x | x | x |
| Fedora 41 | x | x | x |
| openEuler 23.09 | x | x | x |
| openEuler 24.03 | x | x | x |
| openKylin 1.0 | x | x | x |
| openKylin 2.0 | x | x | x |

## deb 系

在 ``/etc/apt/sources.list`` 中添加

```
deb [trusted=yes] https://github.com/weilinfox/ruyi-bin-builds/raw/master/bin-deb/ stable main
```

保存后运行

```bash
sudo apt-get update
sudo apt-get install ruyi
```

## rpm 系

建立 ``/etc/yum.repos.d/ruyi.repo`` 配置并键入如下内容

```
[ruyi-bin]
name=ruyi-bin
baseurl=https://github.com/weilinfox/ruyi-bin-builds/raw/master/bin-rpm/
enabled=1
gpgcheck=0
```

保存后运行

```bash
sudo dnf update
sudo dnf install ruyi
```

