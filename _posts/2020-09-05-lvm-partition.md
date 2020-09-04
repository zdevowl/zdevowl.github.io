---
layout: post
title:  "LVM 파티셔닝"
description: Linux에서 LVM 파티션 만들고 파일시스템 마운트
date:   2020-09-05 00:00:00 +0900
categories: RedHat CentOS Fedora
---
DB 엔지니어 업무를 하다보면 테스트를 위해서 VM을 만드는 경우가 생기는데 대부분의 경우 한 개의 DISK로 만들지만, DISK의 I/O분산을 위해 여러개를 사용하기도 한다.

# lsblk
DISK를 정보를 확인하기 위해 사용하는 명령어다. 이전에는 fdisk를 사용했지만, 아래와 같이 출력형태가 좋지않아 전체적인 파악을 위해 자주 쓴다.
OS가 설치된 sda에는 LVM이 생성되어 있으나 sdb, sdc에는 disk만 있다.
```bash
[root@centos7 ~]#lsblk
NAME                     MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda                        8:0    0   32G  0 disk
├─sda1                     8:1    0    1G  0 part /boot
└─sda2                     8:2    0   31G  0 part
  ├─rhel_centos7-root    253:0    0   29G  0 lvm  /
  └─rhel_centos7-swap    253:1    0    2G  0 lvm  [SWAP]
sdb                        8:16   0   20G  0 disk
sdc                        8:32   0   80G  0 disk
sr0                       11:0    1 1024M  0 rom
```


