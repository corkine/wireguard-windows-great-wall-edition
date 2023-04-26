# [WireGuard](https://www.wireguard.com/) for Windows (Great Wall Edition)

Wireguard Great Wall Edition 基于 WireGuard for Windows main 分支源码修改，主要增加了 `根据配置文件名称中的 -auto+{BASE_PORT}` 来自动将端口更改为今天是今年的第几天 + 此基础 Port 作为实际下发给 Wireguard 的端口，以避免此端口被长时或短时封锁导致的连通性问题。比如 `hk-tunnel-auto+10086` 会直接使用端口 `10086+{今天是今年的第几天}` 而非 10086。

使用指南：直接执行 `quickinstall.bat` 即可，会自动卸载旧版本的 Wireguard 并安装新版本。 或在这里直接下载预先编译好的二进制安装包：[天翼云盘](https://cloud.189.cn/t/UFnYruuQbUJj)。

This is a fully-featured WireGuard client for Windows that uses [WireGuardNT](https://git.zx2c4.com/wireguard-nt/about/). It is the only official and recommended way of using WireGuard on Windows.

## Download &amp; Install

If you've come here looking to simply run WireGuard for Windows, [the main download page has links](https://www.wireguard.com/install/). There you will find two things:

- [The WireGuard Installer](https://download.wireguard.com/windows-client/wireguard-installer.exe) &ndash; This selects the most recent version for your architecture, downloads it, checks signatures and hashes, and installs it.
- [Standalone MSIs](https://download.wireguard.com/windows-client/) &ndash; These are for system admins who wish to deploy the MSIs directly. For most end users, the ordinary installer takes care of downloading these automatically.

## Documentation

In addition to this [`README.md`](README.md), the following documents are also available:

- [`adminregistry.md`](docs/adminregistry.md) &ndash; A list of registry keys settable by the system administrator for changing the behavior of the application.
- [`attacksurface.md`](docs/attacksurface.md) &ndash; A discussion of the various components from a security perspective, so that future auditors of this code have a head start in assessing its security design.
- [`buildrun.md`](docs/buildrun.md) &ndash; Instructions on building, localizing, running, and developing for this repository.
- [`enterprise.md`](docs/enterprise.md) &ndash; A summary of various features and tips for making the application usable in enterprise settings.
- [`netquirk.md`](docs/netquirk.md) &ndash; A description of various networking quirks and "kill-switch" semantics.

## License

This repository is MIT-licensed.

```text
Copyright (C) 2018-2022 WireGuard LLC. All Rights Reserved.

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
```
