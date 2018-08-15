# Make DMG for the Mac NetBeans 9 Incubating Release

## Prerequisites

1. [dmgbuild][] must be available on the system.  One way to get it is to use

```bash
pip install dmgbuild
```

which will install it in `/usr/local/bin/dmgbuild`

2. `/Applications/NetBeans/NetBeans 9.app` which can be made by using the [`netbeans-macos-bundle`][netbeans-macos-bundle] tool by Carl Mosca.

## Usage

Run the command

`dmgbuild -s settings.py  nb9vol   nb9dist.dmg`

to make a `nb9dist.dmg`.  When this dmg is opened, it will present a familar DMG GUI where there will be the NetBeans 9.app that can be drag-n-drop'ed onto a shortcut for the `/Applications` folder.

## Future work

1. Combine the two scripts
2. Fix things so install will be into /Applications/NetBeans directory

## Note

Depends on MacOS program `hdiutil`.


[dmgbuild]: http://dmgbuild.readthedocs.io/en/latest/index.html
[netbeans-macos-bundle]: https://github.com/carljmosca/netbeans-macos-bundle
