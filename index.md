---
layout: default
title: npkg - packages for node-os, powered by npm
---

## core packages

unless otherwise noted, packages here should be treated as <span class="label label-default">experimental</span>

### command-line

> command line modules expose executables placed onto your `PATH`

- [bin-npkg](https://github.com/NodeOS/node-npkg) &mdash; the official node-os package/service binary
- [bin-nsh](https://github.com/groundwater/node-bin-nsh) &mdash; simple node shell
- [wssh](https://github.com/groundwater/node-wssh) &mdash; websocket powered remote shell client
- [bin-man](https://github.com/groundwater/node-bin-man) &mdash; `man` command that uses README.md files
- [bin-term-extras](https://github.com/groundwater/node-bin-term-extras) &mdash; shell goodies like `clear`
- [bin-ifconfig](https://github.com/groundwater/node-bin-ifconfig) &mdash; `ifconfig` replacement
- [bin-fs](https://github.com/groundwater/node-bin-fs) &mdash; common shell goodies like `ls`, `rm`, and `mv`
- [bin-route](https://github.com/groundwater/node-bin-route) &mdash; set the default IP route
- [bin-shutdown](https://github.com/groundwater/node-bin-shutdown) &mdash; issue system shutdown and reboot commands
- [bin-mount](https://github.com/groundwater/node-bin-mount) &mdash; mount file systems
- [bin-getty](https://github.com/groundwater/node-bin-getty) &mdash; getty replacement
- [findmynode](https://github.com/groundwater/node-findmynode) &mdash; mDNS service discovery for wssh

    install command-line executables with `npkg install` e.g.

    ```bash
    $ npkg install wssh
    $ wssh 192.168.2.10
    ```

### services

> services define long-running daemons

- [svc-init](https://github.com/NodeOS/node-init) &mdash; the official node-os init daemon
- [wssh](https://github.com/groundwater/node-wssh) &mdash; websocket powered remote shell server

    install and start services with `npkg install` and `npkg start` e.g.

    ```bash
    $ npkg install wssh
    $ npkg start wssh
    ```

### libraries

> libraries are node modules which get required into other module

- [lib-supervise](https://github.com/groundwater/node-lib-supervise) &mdash; child-process supervision library
- [lib-config](https://github.com/groundwater/node-lib-config) &mdash; hierarchical config file loading
- [lib-cmdparse](https://github.com/groundwater/node-lib-cmdparse) &mdash; parse shell commands
- [lib-pathsearch](https://github.com/groundwater/node-lib-pathsearch) <span class="label label-primary">stable</span> &mdash; return all the files available in a series of paths
- [lib-pathcomplete](https://github.com/groundwater/node-lib-pathcomplete) <span class="label label-primary">stable</span> &mdash; help auto-complete file paths
- [node-pathchop](https://github.com/groundwater/node-pathchop) <span class="label label-primary">stable</span> &mdash; better dirname/basename

    libraries are typical node modules, you require them e.g.

    ```javascript
    var supervise = require('lib-supervise');
    ```

### sources

> sources are compiled module, typically c++ code, with a javascript interface

- [src-ifaddrs](https://github.com/groundwater/node-src-ifaddrs) &mdash; network interface syscalls
- [src-mount](https://github.com/groundwater/node-src-mount) &mdash; mount syscalls
- [src-ioctl](https://github.com/groundwater/node-src-ioctl) &mdash; ioctl interface
- [src-errno](https://github.com/groundwater/node-src-errno) &mdash; errno interface
- [src-reboot](https://github.com/groundwater/node-src-reboot) &mdash; reboot and shutdown syscalls

    sources are also node modules that must be required e.g.

    ```javascript
    var mount = require('src-mount');
    ```

## community packages

> cool npm packages to try on node-os

- [st](https://github.com/isaacs/st) &mdash; serve static files
- [tetris](https://github.com/mafintosh/tetris) &mdash; tetris
- [hipster@0.15.0](https://github.com/dominictarr/hipster) &mdash; the text editor you've probably never heard of
