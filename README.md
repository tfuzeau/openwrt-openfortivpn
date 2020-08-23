# openwrt-openfortivpn
OpenWRT package for [openfortivpn: A Fortinet (and Ruijie) compatible client for PPP+SSL VPN tunnel services](https://github.com/adrienverge/openfortivpn)

## Build
Example for ar71xx and trunk.
```
wget https://downloads.openwrt.org/releases/19.07.3/targets/ar71xx/generic/openwrt-sdk-19.07.3-ar71xx-generic_gcc-7.5.0_musl.Linux-x86_64.tar.xz
tar xf openwrt-sdk-19.07.3-ar71xx-generic_gcc-7.5.0_musl.Linux-x86_64.tar.xz
cd openwrt-sdk-19.07.3-ar71xx-generic_gcc-7.5.0_musl.Linux-x86_64/package
git clone https://github.com/tfuzeau/openwrt-openfortivpn openfortivpn
cd ..
./scripts/feeds update base
./scripts/feeds install libopenssl resolveip ppp
make package/openfortivpn/compile V=s
```
