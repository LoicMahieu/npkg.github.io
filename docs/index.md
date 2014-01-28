---
layout: default
title: npkg documentation
nav_docs: active
---

## quick facts

1. npkg is a command-line utility to assist with npm modules on node-os
2. npkg is *not* a repository; npkg uses npm

## about modules

Most node-os package follow a naming convention,
but it is *not* necessary to follow this convention.

### command-line modules

Command-line modules are prefixed with `bin-`,
and expose new executables.
Most commands you type in the shell are from command-line modules.

To expose executables from your module,
add a `bin` key for each command you want defined.

```json
{
  "name": "bin-curl",
  "bin": {
    "curl": "curl.js"
  }
}
```

After installing with `npkg install` your executables will be linked into `$HOME/bin`.

### system daemons and services

Services are prefixed by `svc-`.
Many npm modules are already proper node-os services.

To create a service, your module must export a `start` script in it's `package.json` file.

```json
{
  "name": "svc-dhcp",
  "scripts": {
    "start": "node ./dhcp.js"
  }
}
```

Packages with start scripts can be managed with `npkg start` and `npkg stop`.

```bash
$ npkg start svc-dhcp
```


### javascript libraries

Javascript libraries are prefixed by `lib-` and contain a `main` key in their `package.json` files.

```json
{
  "name": "lib-coolthing",
  "main": "index.js"
}
```

Javascript libraries should be managed with `npm`, like any other node project
e.g. `npm install lib-coolthing`. 
Once installed load the module with 

```javascript
var cool = require('lib-coolthing')
```

Libraries should be small and composable.
Apply the unix philosophy of doing one thing, and one thing well.

### compiled sources

Not everything can be written in Javascript and node.
Certain system calls cannot be accessed outside of c/c++.
Source modules provide Javascript bindings to the c/c++ layer,
and are prefixed by `src-`.
To trigger the node build process they must contain a `binding.gyp` file.

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

This is the trickiest type of module.