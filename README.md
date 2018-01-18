# openwrt-extra

Some extra packages for OpenWrt

## Install

* Add `src-git extra https://github.com/Akagi201/openwrt-extra.git` to `feeds.conf.default`.

```
./scripts/feeds update extra
./scripts/feeds install -a -p extra
```

* Builded opkg feeds: `bin/packages/arm_cortex-a15_neon-vfpv4/extra`

## Online opkg feeds
* Add `src/gz extra http://opkg.ortc.io` to `/etc/opkg/customfeeds.conf`.
* `opkg update`
* `opkg install <extra-package>`

## Package list
* hellocmake - example project for package built with cmake.
* lanc - [Lancaster](https://github.com/Akagi201/lancaster) client.
