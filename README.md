<div align="center">
  <img width="50" height="50" alt="cssharp" src="https://github.com/user-attachments/assets/3393573f-29be-46e1-bc30-fafaec573456" />
	<h3><strong>Custom Menu</strong></h3>
	<h4>a plugin to create customizable menus</h4>
	<h2>
		<img src="https://img.shields.io/github/downloads/exkludera-cssharp/custom-menu/total" alt="Downloads">
		<img src="https://img.shields.io/github/stars/exkludera-cssharp/custom-menu?style=flat&logo=github" alt="Stars">
		<img src="https://img.shields.io/github/forks/exkludera-cssharp/custom-menu?style=flat&logo=github" alt="Forks">
		<img src="https://img.shields.io/github/license/exkludera-cssharp/custom-menu" alt="License">
	</h2>
	<!--<a href="https://discord.gg" target="_blank"><img src="https://img.shields.io/badge/Discord%20Server-7289da?style=for-the-badge&logo=discord&logoColor=white" /></a> <br>-->
	<a href="https://ko-fi.com/exkludera" target="_blank"><img src="https://img.shields.io/badge/KoFi-af00bf?style=for-the-badge&logo=kofi&logoColor=white" alt="Buy Me a Coffee at ko-fi.com" /></a>
	<a href="https://paypal.com/donate/?hosted_button_id=6AWPNVF5TLUC8" target="_blank"><img src="https://img.shields.io/badge/PayPal-0095ff?style=for-the-badge&logo=paypal&logoColor=white" alt="PayPal"  /></a>
	<a href="https://github.com/sponsors/exkludera" target="_blank"><img src="https://img.shields.io/badge/Sponsor-696969?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Sponsor" /></a>
</div>

<br>

> supports ChatMenu/ConsoleMenu/CenterHtmlMenu/WasdMenu/ScreenMenu
>
> permission based or team based menus and commands
>
> every menu and menu option has a bunch of settings, <a href="https://github.com/exkludera-cssharp/custom-menu/tree/main/examples">see examples</a>

## Requirements
- [MetaMod](https://github.com/alliedmodders/metamod-source)
- [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp)
- [CS2MenuManager](https://github.com/schwarper/CS2MenuManager)

## Showcase
<details>
	<summary>content</summary>
	<video src="https://github.com/user-attachments/assets/07574910-1b56-48e4-90de-39342743bdaa">
</details>

## Config
<a name="config"></a>

<details>
<summary>CustomMenu.json</summary>
  
**Message** - Default: `true` (sends no permission & selecting message) <br>

**Type** - Default: `"CenterHtmlMenu"` (ChatMenu/ConsoleMenu/CenterHtmlMenu/WasdMenu/ScreenMenu) <br>
**Command** - Defualt: `[""]` (you can use multiple by splitting them with `,`) <br>
**Permission** - Default: `[""]` (empty for no check, also support groups) <br>
**Team** - Default: `""` (T for Terrorist, CT for CounterTerrorist or empty for both) <br>
**ExitButton** - Default: `true` (if false menu wont have exit button) <br>
**DisplayTime** - Default: `0` (time in seconds menu will be open, 0 = no limit) <br>

**Sound** - Default: `""` (use vsnd like sounds/buttons/blip1.vsnd) <br>
**CloseMenu** - Default: `false` (close the menu on select) <br>
**Confirm** - Default: `false` (opens a confirmation menu on select) <br>
**Message** - Default: `false` (sends message with which option player selected) <br>
**Disabled** - Default: `false` (disables the option in menu) <br>
**Cooldown** - Default: `0` (how many seconds until the command can be used again) <br>

```json
{
  "Prefix": "{green}[Menu]{default}",
  "Menus": {
    "Example Menu 1": {
      "Type": "ChatMenu",
      "Command": ["css_menu1"],
      "Options": {
        "Example Option": {
          "Command": ["say test"]
        }
      }
    },
    "Example Menu 2": {
      "Type": "CenterHtmlMenu",
      "Command": ["css_menu2"],
      "Permission": ["@css/reservation"],
      "Team": "T",
      "ExitButton": false,
      "DisplayTime": 10,
      "Options": {
        "Example Option 1": {
          "Command": ["say test"]
        },
        "Example Option 2": {
          "Command": ["css_example2"],
          "Permission": ["@css/root"],
          "Team": "T",
          "SoundEvent": "UIPanorama.inventory_item_pickup",
          "CloseMenu": true,
          "Confirm": true,
          "Message": true,
          "Disabled": false,
          "Cooldown": 5
        }
      }
    }
  }
}
```
</details>
