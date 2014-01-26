---
layout: default
title: npkg documentation
nav_docs: active
---

## quick facts

1. npkg is a command-line utility to assist with npm packages on node-os
2. npkg is *not* a repository; npkg uses npm

## package conventions

Most node-os package follow a naming convention,
but it is *not* necessary to follow this convention.

### command-line packages

Command-line packages are prefixed with `bin-`,
and expose new executables.
Most commands you type in the shell are from command-line packages.

```json
{
  "name": "bin-curl",
  "bin": {
    "curl": "curl.js"
  }
}
```

### system daemons and services

Services are prefixed by `svc-`.
Many npm packages are already proper node-os services.
To create a service, your module must export a `start` script in it's `package.json` file.

```json
{
  "name": "svc-dhcp",
  "scripts": {
    "start": "node ./dhcp.js"
  }
}
```

### javascript libraries

Javascript libraries are prefixed by `lib-` and contain a `main` key in their `package.json` files.

```json
{
  "name": "lib-coolthing",
  "main": "index.js"
}
```

Libraries should be small and composable.


### compiled sources

Source modules are prefixed by `src-` and contain a `binding.gyp` file.

```
src-module/
  package.json
  binding.gyp
  README.md
  src/
    binding.cpp
```

the `binding.gyp` file:

```
{
  "targets": [
    {
      "target_name": "binding",
      "sources": [ "src/binding.cpp" ]
    }
  ]
}
```
