<h1 align="center"> guide/Zapret </h1>

> [!NOTE]
> this guide is more useful for CIS citizens 

> [!WARNING]
> zapret is heavy! be sure to have enough ROM for this!

```Sh
# ssh to your router:
$ ssh root@192.168.1.1 -p 22

# inside your router's shell:
mkdir /opt
cd /opt
# now inside /opt
mkdir zapret                            # to create symlinks and to update easily
wget -O https://github.com/bol-van/zapret/releases/download/v71.4/zapret-v71.4-openwrt-embedded.tar.gz
tar -xf zapret-v71.4-openwrt-embedded.tar.gz 
# this ^^^ downloads and unpacks zapret inside /opt but

mv -f zapret-v71.4/* zapret/
rm -rf zapret-v71.4-openwrt-embedded.tar.gz zapret-v71.4/
# this moves zapret inside /opt/zapret 

./install_bin.sh && ./install_easy.sh
# installs zapret itself
```

there is a cool script called `blockcheck.sh` that allows you to create list of suitable strategies. 