---
layout: page
title: 지원
ref: support
lang: 한국어
---

님프를 사용하면서 어떤 문제나 요청이 있으면
[이슈 트래커](https://github.com/cogniti/nimf/issues)에 문의해주세요.

## deb 패키지 만드는 법

우선, `devscripts`, `build-essential`, `debhelper`를 설치하세요.

```
username:~$ sudo apt install devscripts build-essential debhelper
```

`devscripts`, `build-essential` 을 설치한 후 다음 명령을 수행하세요.

```
username:~$ cd
username:~$ mkdir tmp-build
username:~$ cd tmp-build
username:~/tmp-build$ wget https://github.com/cogniti/nimf/archive/master.tar.gz
username:~/tmp-build$ tar zxf master.tar.gz
username:~/tmp-build$ cd nimf-master
username:~/tmp-build/nimf-master$ dpkg-checkbuilddeps
```

다음과 같은 것을 볼 수 있습니다:

> dpkg-checkbuilddeps: Unmet build dependencies: some-package1 some-package2 ...

의존 패키지를 모두 설치하고 다음 명령을 수행하세요.

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

위에 말씀드린 대로, 직접 패키지를 만드세요. 아니면 귀하가 사용하는 리눅스
배포판 프로젝트에 님프를 패키지해달라고 요청하세요.

### 님프 버그는 아니지만 애플리케이션 버그인 경우

응용 프로그램 프로젝트에 버그를 보고하세요.
**귀하가 사용하는 응용 프로그램 버그를 저에게 고쳐달라고 하지마세요.**
