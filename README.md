# base-package-pkgm

The package manager: packages as self-contained folders, installed into the host's install folder, tested within the package. Node's built-ins only.

A package: self-contained, its code ready to run, laid out as it is installed. Written by the package manager (`pear-full-square/pkgm-base-manager`) from the development repository; do not edit here.

- requires: nothing
- hash: `5e032e7338ed16e881dfbbbf8cd45bd1379c9b9c9df8e1cf17c3811be8f177cd`

## Kicking the package manager

From a folder of `haiccing` repositories side by side, this one and `base-package-haicc` (whose boot does step 0, the host's prerequisites):

```sh
sh base-package-pkgm/kick.sh   # step 0, then the package manager into ~/.haicc/packages; ~/.haicc/bin/pkgm
```

## From scratch

On a machine with only `curl` and `tar` (Linux x86-64): the repositories fetched as archives and unpacked side by side, then the kick.

```sh
mkdir -p ~/haiccing && cd ~/haiccing
for r in base-package-haicc base-package-pkgm; do
  curl -fsSL https://github.com/haiccing/$r/archive/refs/heads/main.tar.gz | tar -xz && mv $r-main $r
done
sh base-package-pkgm/kick.sh
```

## Holds

- `pear-full-square/pkgm-base-manager`
- `pear-full-square/pkgm-base-boot`

## Installed

By the package manager, into the host's install folder (`~/.haicc/packages`), with the packages it requires; its tests run there:

```sh
node <install folder>/pear-full-square/pkgm-base-manager/cli.js install pkgm --from <folder of haiccing repositories>
node <install folder>/pear-full-square/pkgm-base-manager/cli.js test pkgm
```
