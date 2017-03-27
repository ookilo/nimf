---
layout: page
title: サポート
ref: support
lang: 日本語
---

Nimfを使用しているときに問題や要望がある場合は、[issue tracker](https://github.com/cogniti/nimf/issues)に連絡してください。

## debパッケージをビルドする方法

まず、`devscripts`、`build-essential`、`debhelper`をインストールします。

```
username:~$ sudo apt install devscripts build-essential debhelper
```

`devscripts`、`build-essential`をインストールした後、以下のコマンドを実行します。

```
username:~$ cd
username:~$ mkdir tmp-build
username:~$ cd tmp-build
username:~/tmp-build$ wget https://github.com/cogniti/nimf/archive/master.tar.gz
username:~/tmp-build$ tar zxf master.tar.gz
username:~/tmp-build$ cd nimf-master
username:~/tmp-build/nimf-master$ dpkg-checkbuilddeps
```

あなたは次のようなものを見るかもしれません：

> dpkg-checkbuilddeps: Unmet build dependencies: some-package1 some-package2 ...

すべての依存パッケージをインストールし、次のコマンドを実行します。

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

上記のように、自分でパッケージを作る。 それ以外の場合は、LinuxディストリビューションにNimfパッケージを要求してください。

### Nimfのバグではなく、アプリケーションのバグ

アプリケーションプロジェクトにバグを報告してください。 **あなたのアプリケーションのバグ修正を私に要求しないでください。**
