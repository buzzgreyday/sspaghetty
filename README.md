# SSpagheTTY 🍝
SSpagHeTTY is a Digital Ocean CLI based bash automation script for automatic firewall whitelisting of IPs and ports (when your IP changes). Easy as real spaghetti.

## Install
1. Download the sspaghetti
2. Make executable
   `chmod +x spaghetti`
3. Create an API access token on DO
4. Install
   `sspaghetti install`

The script will encode the API access token for safe usage and remember your connection values.

## Connect
1. Connect `sspaghetti connect`

The script will check if your IP has changed and automatically whitelist the new IP in you DO firewall.

## Update
1. Reinstall
   `sspaghetti install`

## Uninstall
1. Uninstall
   `sspaghetti uninstall`
