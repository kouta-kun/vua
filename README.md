# vua
vua is a simple script to build and package vitasdk libraries from their packages repository. The regular vdpm tool
uses precompiled packages, some of which are currently broken and/or outdated (libmathneon).

## usage
Install vua by doing
```
# cp vua $VITASDK/bin
```
and compile and install packages by running
```
# vua PACKAGENAME
```
where `PACKAGENAME` is a subdirectory of github.com/vitasdk/packages. vua downloads the repository for you in
$VITASDK/packages.

Currently, you need to remove $VITASDK/bin/libmakepkg/tidy/strip.sh, since stripping libraries breakes linking them.
I've already submitted a pull-request to vitasdk (https://github.com/vitasdk/vita-makepkg/pull/5) that removes it but
it has not yet been merged.
