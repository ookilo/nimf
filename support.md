---
layout: page
title: Support
ref: support
lang: English
---

If you have any problems or requests while you are using Nimf, please contact
[issue tracker](https://github.com/cogniti/nimf/issues).

## How to build deb package

First of all, install `devscripts`, `build-essential`, `debhelper`.

```
username:~$ sudo apt install devscripts build-essential debhelper
```

After installing `devscripts`, `build-essential` perform the following commands.

```
username:~$ cd
username:~$ mkdir tmp-build
username:~$ cd tmp-build
username:~/tmp-build$ wget https://github.com/cogniti/nimf/archive/master.tar.gz
username:~/tmp-build$ tar zxf master.tar.gz
username:~/tmp-build$ cd nimf-master
username:~/tmp-build/nimf-master$ dpkg-checkbuilddeps
```

You may see something like:

> dpkg-checkbuilddeps: Unmet build dependencies: some-package1 some-package2 ...

Install all dependent packages and perform the following commands.

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

As above mentioned, make the package yourself. Otherwise, request your Linux
distribution to package Nimf.

### Not Nimf bugs but your application bugs

Report bugs to your application project. **Do not request me to fix your
application bugs.**
