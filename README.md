# Bedrock

Void Linux Minecraft Bedrock server managed with runit and `screen`.

## Download

[Linux](https://github.com/minecraft-linux/appimage-builder/releases)

[Server](https://www.minecraft.net/en-us/download/server/bedrock)

## Setup

```
xbps-install screen
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

### Recommended

```
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
