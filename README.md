![Cable Spaghetti](https://helios-i.mashable.com/imagery/articles/05Iodbvms58ia2wLGLaBa0C/hero-image.fill.size_1248x702.v1623387584.jpg)
# Sspaghetty

> [!IMPORTANT]
> This script currently has limited functionality. 
> * Only support for Ubuntu.
> * Only support for maximum one project, server and firewall.
> * Only support for either Digital Ocean *or* Hetzner

This is an early stage script. Please read the sections below.

This script will automatically handle ssh connection to your Constellation Validator Node if the client IP changes (dynamic IP, travel, work, etc.) If the client IP changes, the script will automatically update the Digital Ocean or Hetzner firewall rules and establish connection.

### Requirements

* __**Ubuntu PC/Mac**__
* __**Digital Ocean or Hetzner server**__

### 1. Getting Started

+ **Digital Ocean**

Setup your Digital Ocean project, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

+ **Hetzner**

Setup your Hetzner project __**name (or rename) the project `Constellation`**__, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

### 2. Download and Install

This step only has to be done once. Make sure you have `PATH="$PATH:~./local/bin"` among your Ubuntu paths.

```
mkdir -p ~/.local/bin && wget https://raw.githubusercontent.com/buzzgreyday/sspaghetty/main/sspaghetty -P ~/.local/bin && chmod 700 ~/.local/bin
```
+ **Digital Ocean**
```
sspaghetty install doctl
```
+ **Hetzner**
```
sspaghetty install hcloud
```
### 3. Connect to server

This step is used to connect to the Validator Node and is repeated any time you wish to connect to your Validator Node.

+ **Digital Ocean**
```
sspaghetty connect doctl
```
+ **Hetzner**
```
sspaghetty connect hcloud
```
### Uninstall
+ **Digital Ocean**
```
sspaghetty uninstall doctl && rm -f ~/.local/bin/sspaghetty
```
+ **Hetzner**
```
sspaghetty uninstall hcloud && rm -f ~/.local/bin/sspaghetty
```