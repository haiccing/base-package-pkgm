# base-package-pkgm

The package manager: packages as self-contained folders, installed into the host's install folder, tested within the package. Node's built-ins only.

A package: self-contained, its code ready to run, laid out as it is installed. Written by the package manager (`pear-full-square/pkgm-base-manager`) from the development repository; do not edit here.

- requires: nothing
- hash: `0484594baf7aa911a264540fc37ee8c497d3f2caa77f6a5e5df633a99d50e079`

## Installed

By HAICC's boot (`haiccing/boot` in a work folder, from `base-package-haicc`), with its own code, into the work folder's `.haicc/packages`; HAICC is then installed by it. There is no boot of its own: everything starts at HAICC.

## Holds

- `pear-full-square/pkgm-base-manager`

## Installed

By the package manager, into the host's install folder (`~/.haicc/packages`), with the packages it requires; its tests run there:

```sh
node <install folder>/pear-full-square/pkgm-base-manager/cli.js install pkgm --from <folder of haiccing repositories>
node <install folder>/pear-full-square/pkgm-base-manager/cli.js test pkgm
```
