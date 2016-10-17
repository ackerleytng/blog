---
layout: post
title: Allowing container to mount ISOs
description: "Instructions to allow container to mount ISOs"
modified: 2016-10-17
tags: [iso, container, lxd]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true

share: true
---

In the lxd host, suppose you have the following containers

```
$ lxc list
+------------------------+---------+-----------------------+------+------------+-----------+
|          NAME          |  STATE  |         IPV4          | IPV6 |    TYPE    | SNAPSHOTS |
+------------------------+---------+-----------------------+------+------------+-----------+
| base                   | STOPPED |                       |      | PERSISTENT | 0         |
+------------------------+---------+-----------------------+------+------------+-----------+
| mount-cd               | RUNNING | 192.168.64.248 (eth0) |      | PERSISTENT | 0         |
+------------------------+---------+-----------------------+------+------------+-----------+
```

Create a new profile for this container and apply it

```
$ lxc profile copy default nsmount
$ lxc profile device add nsmount fuse unix-char path=/dev/fuse
$ lxc profile device add nsmount loop0 unix-block path=/dev/loop0
$ lxc profile apply mount-cd nsmount
```

Make `mount-cd` a privileged container

```
$ lxc config set mount-cd security.privileged true
```

and get apparmor to allow mounting of `iso9660` filesystems

```
$ lxc config set mount-cd raw.apparmor 'mount fstype=iso9660,'
```
