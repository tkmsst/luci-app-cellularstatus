# luci-app-cellularstatus

Cellular information for OpenWrt LuCi

## How-to add repositry and compile package

Add next line to feeds.conf.default in OpenWrt Buildroot

```
src-git cellularstatus https://github.com/tkmsst/luci-app-cellularstatus.git
```

Update feeds and compile packages

```
./scripts/feeds update -a; ./scripts/feeds install -a
make menuconfig
make -j$((`nproc` + 1)) package/luci-app-cellularstatus/compile
