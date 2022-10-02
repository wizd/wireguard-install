[English](README.md) | [中文](README-zh.md)

# WireGuard VPN Server Auto Setup Script

WireGuard VPN server installer for Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS and Fedora.

This script will let you set up your own VPN server in just a few minutes, even if you haven't used WireGuard before. [WireGuard](https://www.wireguard.com) is a fast and modern VPN designed with the goals of ease of use and high performance.

Video tutorial (Spanish): [Install OpenVPN/WireGuard on Ubuntu 20.04](https://www.youtube.com/watch?v=99qtaJU2E2k).

[**&raquo; See also: OpenVPN Server Auto Setup Script**](https://github.com/hwdsl2/openvpn-install)

## Installation

Run the script on your Linux server\* and follow the prompts.

**Option 1:** Auto install WireGuard using default options.

```bash
wget https://get.vpnsetup.net/wg -O wireguard.sh
sudo bash wireguard.sh --auto
```

<details>
<summary>
List of default options.
</summary>

```
Port: UDP/51820
Client name: client
Client DNS: Google Public DNS
```
</details>

**Option 2:** Interactive install using custom options.

```bash
wget https://get.vpnsetup.net/wg -O wireguard.sh
sudo bash wireguard.sh
```

<details>
<summary>
Alternative commands.
</summary>

You may also use `curl` to download:

```bash
# Download the script
curl -fL https://get.vpnsetup.net/wg -o wireguard.sh
# Option 1: Auto install WireGuard using default options
sudo bash wireguard.sh --auto
# Option 2: Interactive install using custom options
sudo bash wireguard.sh
```

Alternative setup URLs:

```bash
https://github.com/hwdsl2/wireguard-install/raw/master/wireguard-install.sh
https://gitlab.com/hwdsl2/wireguard-install/-/raw/master/wireguard-install.sh
```

If you are unable to download, open [wireguard-install.sh](wireguard-install.sh), then click the `Raw` button on the right. Press `Ctrl/Cmd+A` to select all, `Ctrl/Cmd+C` to copy, then paste into your favorite editor.
</details>

\* A cloud server, virtual private server (VPS) or dedicated server.

## Next steps

After setup, you can run the script again to manage users or uninstall WireGuard.

Get your computer or device to use the VPN. Please refer to:

**[Configure WireGuard VPN Clients](docs/clients.md)**

Enjoy your very own VPN! :sparkles::tada::rocket::sparkles:

<details>
<summary>
Like this project? You can show your support or appreciation.
</summary>

<a href="https://ko-fi.com/hwdsl2" target="_blank"><img height="36" width="187" src="docs/images/kofi2.png" border="0" alt="Buy Me a Coffee at ko-fi.com" /></a> &nbsp;&nbsp;<a href="https://coindrop.to/hwdsl2" target="_blank"><img src="docs/images/embed-button.png" height="36" width="145" border="0" alt="Coindrop.to me" /></a>

Supporter-only content is available. [Click to see details](https://ko-fi.com/hwdsl2).
</details>

## Credits

This script is based on the great work of [Nyr and contributors](https://github.com/Nyr/wireguard-install), with enhancements and changes for compatibility with the [Setup IPsec VPN](https://github.com/hwdsl2/setup-ipsec-vpn) project.

<details>
<summary>
List of enhancements over Nyr/wireguard-install.
</summary>

- Improved compatibility with Setup IPsec VPN
- Improved script reliability, user input and output
- Supports auto install using default options
- Supports listing existing VPN clients
- Supports custom DNS server(s) for VPN clients
- Optimized `sysctl` settings for improved VPN performance
- Improved creation of client config files when using `sudo`

...and more!
</details>

## License

MIT
