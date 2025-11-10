[comment]: <> (SPDX-License-Identifier: AGPL-3.0)

[comment]: <> (-------------------------------------------------------------)
[comment]: <> (Copyright © 2024, 2025  Pellegrino Prevete)
[comment]: <> (All rights reserved)
[comment]: <> (-------------------------------------------------------------)

[comment]: <> (This program is free software: you can redistribute)
[comment]: <> (it and/or modify it under the terms of the GNU Affero)
[comment]: <> (General Public License as published by the Free)
[comment]: <> (Software Foundation, either version 3 of the License.)

[comment]: <> (This program is distributed in the hope that it will be useful,)
[comment]: <> (but WITHOUT ANY WARRANTY; without even the implied warranty of)
[comment]: <> (MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the)
[comment]: <> (GNU Affero General Public License for more details.)

[comment]: <> (You should have received a copy of the GNU Affero General Public)
[comment]: <> (License along with this program.)
[comment]: <> (If not, see <https://www.gnu.org/licenses/>.)

# Ahsi

An hello world program to show how to write
a program using the
[Crash JavaScript](
  https://github.com/themartiancompany/crash-js)
and the
[Crash Bash](
  https://github.com/themartiancompany/crash-bash)
libraries together to write a program
which runs both in node.js and
in a browser console.

```bash
# In the terminal
ahsi \
  -p \
    "node" \
  "hello" \
  "mars"

# In the browser
ahsi \
  -p \
    "browser" \
  "hello" \
  "venus"
```

That's significant because it can be noted programs
written using either one of the Crash libraries
are quite similar in their structure and
function names and because there is support
for file system function both on browser
and locally.

Depending on how your Node.js installation
is configured, you may need
The program of course requires
[`node-run`](
  https://github.com/themartiancompany/node-run)
because it is what it is needed to run
system-wide installed programs reliably with node.

Upon installation manual can be accessed with

```console
$ man \
    "ahsi"
```

## How does it work

At build time the 'ahsi' node module is bundled
with its dependencies into `ahsi.js` by

```bash
webpack \
  --mode \
    "production"
```

it can be run in a browser by
accessing the `index.html` file
after running a web server on
the directory.

So for example on
[localhost:3000](
  http://localhost:3000)
with Serve:

```console
$ serve \
    "$(pwd)"
```

This library is being used by most of
Human Instrumentality Project
[(HIP)](
  https://github.com/themartiancompany)
JavaScript programs.

## Installation

The program in this source repo
can be installed from source without any
extra dependencies using GNU Make

```console
$ make \
    all
# make \
    install-npm
```

If you do not wish to install browser
compatibility you can simply run instead

```console
# make \
    install
```

The node module can also be installed
from the
[NPM Registry](
  https://www.npmjs.com/package/ahsi)

```bash
npm \
  install \
    "ahsi"
```

or from the uncensorable
[Ur](
  https://github.com/themartiancompany/ur)
user repository and application store.
The source code is published on the
[Ethereum Virtual Machine File System](
  https://github.com/themartiancompany/evmfs)
so it can't possibly be taken down.

To install it from there just type

```bash
ur \
  ahsi
```

A censorable HTTP Github mirror of the recipe published there
is hosted on
[ahsi-ur](
  https://github.com/themartiancompany/ahsi-ur).
Be aware it could go offline any time.

## License

Ahsi is released by Pellegrino Prevete
under the terms of the GNU Affero General Public License version 3.
