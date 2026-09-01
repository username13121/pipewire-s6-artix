# Per-user PipeWire services for s6 on Artix

This repository builds one package, `pipewire-s6`, containing recommended
per-user s6-rc service definitions for:

```text
pipewire
pipewire-pulse
wireplumber
```

Definitions are installed in the Artix package store:

```text
/etc/s6/user/sv
```

The package depends on `pipewire`, `pipewire-pulse`, and `wireplumber`. The
native `elogind-usersv` s6 backend is packaged separately.

Build and install as a normal user:

```sh
makepkg -Csi
```
