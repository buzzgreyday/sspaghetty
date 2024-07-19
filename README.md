![Cable Spaghetti](https://helios-i.mashable.com/imagery/articles/05Iodbvms58ia2wLGLaBa0C/hero-image.fill.size_1248x702.v1623387584.jpg)
# Sspaghetty

> [!IMPORTANT]
> This script currently has limited functionality. 
> * Only support for Ubuntu.
>   Windows users can use WSL (how to below)
> * Only support for maximum one project, server and firewall.
> * Only support for either Digital Ocean *or* Hetzner

This is an early stage script. Please read the sections below.

This script will automatically handle ssh connection to your Constellation Validator Node if the client IP changes (dynamic IP, travel, work, etc.) If the client IP changes, the script will automatically update the Digital Ocean or Hetzner firewall rules and establish connection.

### Requirements

* __**Ubuntu PC/Mac or WSL**__
* __**Digital Ocean or Hetzner server**__

### 1. Getting Started

+ **Digital Ocean**

Setup your Digital Ocean project, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

+ **Hetzner**

Setup your Hetzner project __**name (or rename) the project `Constellation`**__, deploy your server and __**setup the firewall rules. Create an API token with read and write permissions.**__

### 2. Download and Install

> [!IMPORTANT]
> If you're on Windows 10 or above, you can use WSL (Windows Subsystem for Linux). Here's how:
> 1. Open a new PowerShell: `ctrl+x`
> 2. In PowerShell input: `wsl --install`
> 3. Restart your PC
> 4. Open PowerShell and input: `wsl`

This step only has to be done once. Make sure you have `PATH="$PATH:~./local/bin"` among your Ubuntu paths.

```
mkdir -p ~/.local/bin && wget https://raw.githubusercontent.com/buzzgreyday/sspaghetty/main/sspaghetty -P ~/.local/bin && chmod 700 ~/.local/bin/sspaghetty
```
+ **Digital Ocean**
```
sspaghetty install doctl
```
+ **Hetzner**
```
sspaghetty install hcloud
```
### 3. Connect to Server

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