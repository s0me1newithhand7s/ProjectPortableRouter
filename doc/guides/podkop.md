<h1 align="center"> guide/Podkop </h1>

`sing-box` / `xray` core utilising front-end with LuCI integration.

> [!WARNING]
> podkop is heavy package due of `sing-box` usage. around 20MB to be exact, be sure to have free space!

```Sh
# ssh to your router:
$ ssh root@192.168.1.1 -p 22

# inside your router's shell:
opkg update

# now we need to install podkop via wget from github
wget -O https://github.com/itdoginfo/podkop/releases/download/v0.4.11/podkop_v0.4.11-r1_all.ipk /tmp/podkop.ipk
wget -O https://github.com/itdoginfo/podkop/releases/download/v0.4.11/luci-app-podkop_v0.4.11-r1_all.ipk /tmp/luci-app-podkop.ipk

# fianlly, installing
opkg install /tmp/podkop.ipk        # REQUIERED TO BE FIRST 
opkg install /tmp/luci-app-podkop.ipk
```

> [!WARNING]
> before ANY openwrt update you need to `service podkop stop` or OpenWRT will break!