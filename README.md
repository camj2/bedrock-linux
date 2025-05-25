# Bedrock

Void Linux Minecraft Bedrock server managed with runit and `screen`.

## Download

[Linux](https://mcpelauncher.readthedocs.io/en/latest/getting_started/index.html)

[Server](https://www.minecraft.net/en-us/download/server/bedrock)

## Install

```
xbps-install flatpak screen

flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

flatpak install --user flathub io.mrarm.mcpelauncher

flatpak update

flatpak run io.mrarm.mcpelauncher
flatpak run io.mrarm.mcpelauncher -p
```

`/etc/nftables.conf`:

```
udp dport 19132 accept
udp dport 19133 accept
```

## Seed

[Map](https://www.chunkbase.com/apps/seed-map)

<!-- -9134377708685086840 -->

## Server

### Documentation

```
bedrock_server_how_to.html
```

### Config

```
server.properties
```

### Launcher

```
~/.var/app/io.mrarm.mcpelauncher/data/mcpelauncher/games/com.mojang
```

### Recommended

```
gamerule spawnradius 0
gamerule playerssleepingpercentage 0
gamerule showcoordinates true
mobevent minecraft:wandering_trader_event false
gamerule recipesunlock false
```

## Usage

### Flags

`-r <path>`: bedrock server path (default: `.`)

<!-- `-S <name>`: server name (default: `bedrock`) -->

`-c`: open the server console (close with: `CTRL + a -> d`)

<!-- `-s`: stop the server (this will restart the runit service) -->

## LICENSE

MIT
