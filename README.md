# jellyfin-plugin-isomounter

**ARCHIVED**: Functionality moved to core server.

This implements two core interfaces: IIsoManager and IIsoMount.

## IIsoManager

The manager class can be used to create a mount, and also determine if the mounter is capable of mounting a given file.

## IIsoMount

IIsoMount then represents a mount instance, which will be unmounted on disposal.

This Linux version uses sudo, mount, and umount.

You need to add this to your sudo file via visudo.

```sh
Defaults:jsmith !requiretty
jsmith ALL=(root) NOPASSWD: /bin/mount
jsmith ALL=(root) NOPASSWD: /bin/umount
```
