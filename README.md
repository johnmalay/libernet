<p align="center">
  <img src="https://i.ibb.co/TwD8Vyy/Screenshot-from-2021-03-18-21-24-17.png" alt="dashboard" />
</p>

# Libernet
Libernet is open source web app for tunneling internet using SSH, V2Ray, Trojan, Shadowsocks, OpenVPN on OpenWRT with ease.

## Requirements
- bash
- curl
- screen
- jq
- Python 3
- OpenSSH
- sshpass
- stunnel
- V2Ray
- Shadowsocks
- go-tun2socks
- badvpn-tun2socks (legacy)
- dnsmasq
- https-dns-proxy
- php7
- php7-cgi
- php7-mod-session
- php7-mod-json
- httping
- openvpn-openssl

## Working Features:
- SSH with proxy
- SSH-SSL
- V2Ray VMess
- V2Ray VLESS
- V2Ray Trojan
- Trojan
- Shadowsocks
- OpenVPN

## Installation
- If you don't have bash & curl on OpenWRT, please install first:
```sh
opkg update && opkg install bash curl
```
- Run installation script:
```sh
bash -c "$(curl -sko - 'https://raw.githubusercontent.com/johnmalay/libernet/main/install.sh')"
```
- Reboot router, if necessary
- Open Libernet on your browser: http://router-ip/libernet
- Fill your tunnel server, save configuration & run Libernet

## Updating
- Just run updater script:
```sh
bash ~/Downloads/libernet/update.sh
```
- Updater script will updating Libernet to latest version

## Fresh Install / Fresh Update
- Remove Libernet installer directory
```sh
rm -rf ~/Downloads/libernet
```
- Run Libernet online installer
```sh
bash -c "$(curl -sko - 'https://raw.githubusercontent.com/johnmalay/libernet/main/install.sh')"
```
- Latest version Libernet will be installed on your system

## Installation Note
Don't forget to always clear browser cache after installing or upgrading Libernet to prevent unwanted error.

## Default Username & Password
- Username: admin
- Password: libernet

## Additional Information
In home menu, check 'Use tun2socks legacy' to use badvpn-tun2socks or uncheck to use go-tun2socks instead.

## Fix Php Error
wget -O /bin/fixphp "https://raw.githubusercontent.com/helmiau/openwrt-config/main/fix-xderm-libernet-gui" && chmod +x /bin/fixphp && fixphp
