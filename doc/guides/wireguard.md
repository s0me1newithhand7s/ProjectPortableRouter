<h1 align="center"> guide/Wireguard </h1>

to be complietly fair - this is really easy, and "guide" but

```Sh
# ssh to your router:
$ ssh root@192.168.1.1 -p 22

# inside router's shel:
opkg update
opkg install kmod-wireguard \
wireguard-tools luci-proto-wireguard
reboot -f
```

now inside LuCI you can manage `Wireguard` as Interface. or with `wg` command in router's shell.

there also packages like:
`prometheus-node-exporter-ucode-wireguard, rpcd-mod-wireguard, wg-installer-client, wg-installer-server, wg-installer-server-hotplug-babeld, wg-installer-server-hotplug-olsrd, wgsd-client, wgsd-coredns`

but for general WG usage `wireguard-tools` and `luci-proto-wireguard` are enough.