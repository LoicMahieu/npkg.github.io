---
layout: default
title: npkg - packages for node-os, powered by npm
---

> npm packages designed for [node-os](http://node-os.com/)

## core packages

unless otherwise noted, packages here should be treated as <span class="label label-default">experimental</span>

### command-line

- [bin-npkg](https://github.com/NodeOS/node-npkg) &mdash; the official node-os package/service binary
- [bin-nsh](https://github.com/jacobgroundwater/node-bin-nsh) &mdash; simple node shell
- [wssh](https://github.com/jacobgroundwater/node-wssh) &mdash; websocket powered remote shell client
- [bin-man](https://github.com/jacobgroundwater/node-bin-man) &mdash; `man` command that uses README.md files
- [bin-term-extras](https://github.com/jacobgroundwater/node-bin-term-extras) &mdash; shell goodies like `clear`
- [bin-ifconfig](https://github.com/jacobgroundwater/node-bin-ifconfig) &mdash; `ifconfig` replacement
- [bin-fs](https://github.com/jacobgroundwater/node-bin-fs) &mdash; common shell goodies like `ls`, `rm`, and `mv`
- [bin-route](https://github.com/jacobgroundwater/node-bin-route) &mdash; set the default IP route
- [bin-shutdown](https://github.com/jacobgroundwater/node-bin-shutdown) &mdash; issue system shutdown and reboot commands
- [bin-mount](https://github.com/jacobgroundwater/node-bin-mount) &mdash; mount file systems
- [bin-getty](https://github.com/jacobgroundwater/node-bin-getty) &mdash; getty replacement
- [findmynode](https://github.com/jacobgroundwater/node-findmynode) &mdash; mDNS service discovery for wssh

### services

- [svc-init](https://github.com/NodeOS/node-init) &mdash; the official node-os init daemon
- [wssh](https://github.com/jacobgroundwater/node-wssh) &mdash; websocket powered remote shell server

### libraries

- [lib-supervise](https://github.com/jacobgroundwater/node-lib-supervise) &mdash; child-process supervision library
- [lib-config](https://github.com/jacobgroundwater/node-lib-config) &mdash; hierarchical config file loading
- [lib-cmdparse](https://github.com/jacobgroundwater/node-lib-cmdparse) &mdash; parse shell commands
- [lib-pathsearch](https://github.com/jacobgroundwater/node-lib-pathsearch) <span class="label label-primary">stable</span> &mdash; return all the files available in a series of paths
- [lib-pathcomplete](https://github.com/jacobgroundwater/node-lib-pathcomplete) <span class="label label-primary">stable</span> &mdash; help auto-complete file paths
- [node-pathchop](https://github.com/jacobgroundwater/node-pathchop) <span class="label label-primary">stable</span> &mdash; better dirname/basename

### sources

- [src-ifaddrs](https://github.com/jacobgroundwater/node-src-ifaddrs) &mdash; network interface syscalls
- [src-mount](https://github.com/jacobgroundwater/node-src-mount) &mdash; mount syscalls
- [src-ioctl](https://github.com/jacobgroundwater/node-src-ioctl) &mdash; ioctl interface
- [src-errno](https://github.com/jacobgroundwater/node-src-errno) &mdash; errno interface
- [src-reboot](https://github.com/jacobgroundwater/node-src-reboot) &mdash; reboot and shutdown syscalls

## community packages

> cool npm packages to try on node-os

- [st](https://github.com/isaacs/st) &mdash; serve static files
- [tetris](https://github.com/mafintosh/tetris) &mdash; tetris
- [hipster](https://github.com/dominictarr/hipster) &mdash; the text editor you've probably never heard of
