# Sspaghetty 🍝
Sspaghetty is a Digital Ocean CLI based bash automation script for automatic firewall whitelisting of IPs and ports (when your IP changes). Easy as real spaghetti.

## Install
1. Download the sspaghetty
2. Make executable
   `chmod +x spaghetty`
3. Create an API access token on DO
4. Install
   `sspaghetty install`

The script will encode the API access token for safe usage and remember your connection values.

## Connect
1. Connect `sspaghetty connect`

The script will check if your IP has changed and automatically whitelist the new IP in you DO firewall.

## Update IP, etc.
1. Reinstall
   `sspaghetty install`

## Uninstall
1. Uninstall
   `sspaghetty uninstall`
