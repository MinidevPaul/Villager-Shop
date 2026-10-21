# VillagerShop

A Paper plugin that runs a player shop through Minecraft's own villager trade
screen. No economy plugin, no Vault, and no NPC villager to place.

Players open the shop with `/shop` and trade through the vanilla merchant UI.
Admins add and remove trades in game through chest GUIs. Trades are stored in
YAML and survive restarts.

## Features

- Uses the vanilla merchant GUI, so there is no custom interface
- Trades are created and deleted in game, without editing config files
- The delete GUI is paginated, five trades per page
- Admin commands are permission gated and work with LuckPerms
- Tab completion offers subcommands only to admins
- Physical items are the only currency
- Trades never lock: unlimited uses, discounts disabled

## Commands

| Command | Description | Permission |
|---|---|---|
| `/shop` | Open the shop | Everyone |
| `/vs create` | Open the trade creator GUI | `villagershop.admin` |
| `/vs delete` | Open the trade deletion GUI | `villagershop.admin` |
| `/vs info` | Show command help | `villagershop.admin` |

`/villagershop` is a full alias for `/vs`.

## Permissions

| Node | Default | Description |
|---|---|---|
| `villagershop.admin` | OP | Access to all `/vs` admin commands |

LuckPerms: `/lp group admin permission set villagershop.admin true`

## Installation

1. Drop `VillagerShop-x.x.x.jar` into your server's `plugins/` folder
2. Restart the server
3. Use `/vs create` in game to add your first trade

## Usage

### Creating a trade

1. Run `/vs create`
2. Place your input item or items in the left slots and your output item in the
   center slot
3. Click Confirm. The trade is saved straight away.

### Deleting a trade

1. Run `/vs delete`
2. Browse your trades, five per page
3. Click the red Delete Trade button beside any trade to remove it

## Requirements

- Paper 1.21.4+
- Java 21+
