# base-package-pkgm

The package manager: packages as self-contained folders, installed into the host's install folder, tested within the package. Node's built-ins only.

## Installed

By HAICC's boot (`haiccing/boot` in a work folder, from `base-package-haicc`), with its own code, into the work folder's `.haicc/packages`; HAICC is then installed by it. There is no boot of its own: everything starts at HAICC.

## The package

- holds: `pear-full-square/pkgm-base-manager`
- requires: nothing
- hash: `cd28ada5126fe73b792286df80dbd25a74eb5c545a8b6fb6e166a9c80ad010c5`

In a work folder (see [haiccing/base-package-haicc](https://github.com/haiccing/base-package-haicc)), installed by HAICC as a project needs it, or by `./haicc install pkgm`, into `.haicc/packages` with what it requires; tested there, within the package: `./haicc test pkgm`.

Written by the package manager from the development repository ([splectrum/dev-env-2-p2p-cluster](https://github.com/splectrum/dev-env-2-p2p-cluster)): not edited here.
