![Cable Spaghetti](https://helios-i.mashable.com/imagery/articles/05Iodbvms58ia2wLGLaBa0C/hero-image.fill.size_1248x702.v1623387584.jpg)
# Sspaghetty

This is an early stage script. Please read the sections below.

This script will automatically handle ssh connection to your Constellation Validator Node if the client IP changes (dynamic IP, travel, work, etc.) If the client IP changes, the script will automatically update the Digital Ocean or Hetzner firewall rules and establish connection. This is very useful if you're using an Ubuntu PC/Mac to handle node operations. Support for more operative systems might follow (depending on interest). 

## Requirements

* __**Ubuntu PC/Mac**__
* __**Max one Digital Ocean or Hetzner server**__

### Getting started

The script is in an early stage. Therefore, __**the script will most likely not behave as expected if you have multiple projects, servers and/or firewalls on Digital Ocean and/or Hetzner.**__ Support for multiple projects, server and/or firewalls will likely follow in the future.

**1a. Digital Ocean**

Setup your Digital Ocean project, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

**1b. Hetzner**

Setup your Hetzner project __**name (or rename) the project `Constellation`**__, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

### 2. Download and Install
```
wget https://raw.githubusercontent.com/buzzgreyday/sspaghetty/main/sspaghetty && chmod +x sspaghetty && mkdir -p ~/.local/bin && mv sspaghetty ~/.local/bin
```
**Install for Digital Ocean**
```
sspaghetty install doctl
```
**Install for Hetzner**
```
sspaghetty install hcloud
```
### 3. Connect to server

These commands are used to connect to your node via ssh.

**Connect to Digital Ocean**
```
sspaghetty connect doctl
```
**Connect to Hetzner**
```
sspaghetty connect hcloud
```
### Uninstall
**Uninstall for Digital Ocean**
```
sspaghetty uninstall doctl && rm -f ~/.local/bin/sspaghetty
```
**Uninstall for Hetzner**
```
sspaghetty uninstall hcloud && rm -f ~/.local/bin/sspaghetty
```