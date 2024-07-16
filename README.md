![Cable Spaghetti](https://helios-i.mashable.com/imagery/articles/05Iodbvms58ia2wLGLaBa0C/hero-image.fill.size_1248x702.v1623387584.jpg)
# Sspaghetty

## Requirements

* __**Ubuntu PC/Mac**__
* __**Max one Digital Ocean or Hetzner server**__

## Getting started

The script is in an early stage. Therefore, __**the script will most likely not behave as expected if you have multiple projects, servers and/or firewalls on Digital Ocean and/or Hetzner.**__ Support for multiple projects, server and/or firewalls, and different Operative systems, will likely follow in the future.

### 1a. Digital Ocean Server

Setup your Digital Ocean project, deploy your server and setup the firewall rules. Create an API token with read and write permissions.

### 1b. Hetzner Server

Setup your Hetzner project __**name (or rename) it `Constellation`**__, deploy your server and setup the firewall rules. Create an API token with read and write permissions.

### 2. Download and Install
```
wget https://raw.githubusercontent.com/buzzgreyday/sspaghetty/main/sspaghetty && chmod +x sspaghetty && mkdir -p ~/.local/bin && mv sspaghetty ~/.local/bin
```
*Digital Ocean Server*
```
sspaghetty install doctl
```
*Hetzner Server*
```
sspaghetty install hcloud
```
### 3. Connect to server
*Digital Ocean Server*
```
sspaghetty connect doctl
```
*Hetzner Server*
```
sspaghetty connect hcloud
```
### 4. Uninstall
*Digital Ocean Server*
```
sspaghetty uninstall doctl && rm -f ~/.local/bin/sspaghetty
```
*Hetzner Server*
```
sspaghetty uninstall hcloud && rm -f ~/.local/bin/sspaghetty
```