---
layout: page
title: 支持
ref: support
lang: 中文
---

如果您在使用宁芙时遇到任何问题或请求，请联系[问题跟踪器](https://github.com/cogniti/nimf/issues)。

## 如何构建deb软件包

首先，安装`devscripts`，`build-essential`，`debhelper`.

```
username:~$ sudo apt install devscripts build-essential debhelper
```

安装`devscripts`之后，`build-essential`执行以下命令。

```
username:~$ cd
username:~$ mkdir tmp-build
username:~$ cd tmp-build
username:~/tmp-build$ wget https://github.com/cogniti/nimf/archive/master.tar.gz
username:~/tmp-build$ tar zxf master.tar.gz
username:~/tmp-build$ cd nimf-master
username:~/tmp-build/nimf-master$ dpkg-checkbuilddeps
```

您可能会看到：

> dpkg-checkbuilddeps: Unmet build dependencies: some-package1 some-package2 ...

安装所有相关软件包并执行以下命令。

```
username:~/tmp-build/nimf-master$ debuild
username:~/tmp-build/nimf-master$ cd ..
username:~/tmp-build$ ls
master.tar.gz                    nimf_YYYY.mm.dd.dsc
nimf_YYYY.mm.dd_amd64.build      nimf_YYYY.mm.dd.tar.xz
nimf_YYYY.mm.dd_amd64.buildinfo  nimf-dbgsym_YYYY.mm.dd_amd64.deb
nimf_YYYY.mm.dd_amd64.changes    nimf-dev_YYYY.mm.dd_amd64.deb
nimf_YYYY.mm.dd_amd64.deb        nimf-master
```

如上所述，自己做包。 否则，请求您的Linux发行版打包宁芙。

### 不是宁芙错误，而是你的应用程序错误

向应用程序项目报告错误。 **不要请求我修复您的应用程序错误。**
