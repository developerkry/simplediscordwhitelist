# DiscordWhitelistPlugin

A simple PaperMC plugin to whitelist Minecraft players based on their Discord roles using EssentialsX Discord Link.

## Features
- Only allow players with a specific Discord role to join your server
- Customizable kick messages and log prefix
- Bypass permission for staff or trusted users
- Easy configuration

## Requirements
- [PaperMC](https://papermc.io/) 1.21+
- [EssentialsX Discord Link](https://essentialsx.net/downloads.html)
- Java 17+

## Installation
1. Download `SimpleDiscordWhitelist-1.0.0.jar` and place it in your server's `plugins` folder.
2. Make sure EssentialsX Discord Link is installed and configured.
3. Start your server to generate the default `config.yml`.
4. Edit `plugins/SimpleDiscordWhitelist/config.yml`:
   - Set `required-discord-role-id` to your Discord role's ID.
   - Optionally set custom messages and other options.

## Example config.yml
```yaml
required-discord-role-id: "YOUR_ROLE_ID_HERE"
# Optional: required-discord-role-name: "RoleNameHere"
# Message shown if player is linked but does not have the required Discord role
kick-no-role: "You are linked to a Discord account, but you do not have the required role to join this server."
# Message shown if there was an error verifying the Discord role
kick-error: "Could not verify your whitelist. Try again later or contact staff."
# Message shown if the plugin is not configured correctly
kick-not-configured: "Plugin not configured correctly. Contact server staff."
# Message shown if the player is not linked to Discord
kick-not-linked: "Please link using EssentialX."
bypass-permission: "discordwhitelist.bypass"
log-prefix: "[DiscordWhitelist] "
```

## Permissions
- `discordwhitelist.bypass` — Allows a player to bypass the Discord whitelist check.

## Support
If you need help, open an issue on GitHub or ask in the EssentialsX Discord.

## License
MIT
