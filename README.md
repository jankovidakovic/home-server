# home-server
Home server setup

## Wishlist

1. Plex server
2. Minecraft server
3. file server (like a personal cloud)
4. music server (FLAC audio files) -> requires good soundcard
5. deep learning (nothing major, just experimenting)
6. self-hosted git (probably gitlab)
7. self-hosted docker registry

## Tech requirements

### Hardware

- lets keep it simple -> consumer-grade PC
- cpu and ram-heavy (must be able to transcode 4k videos)
- storage: ssd for OS, hdd for big files
- probably 10TB HDD is enough for starters
- might need a gigabit switch, not sure yet

### Infrastructure

- linux
    - headless vs headful - unless clear benefits of headless, go with manjaro-desktop
     (i really dont care about 5% performance or some bullshit like that)
- everything in docker (also look into podman/buildah maybe)
- observability (grafana, influxdb, telegraf)
- storage: look into brtfs instead of ext4 for media storage drives (HDDs)

### Networking

- nginx for serving (altho maybe look into alternatives)
- docker networks for subnet isolation
- maaybe VPN
- also might need a gigabit switch for pi-hole (not sure yet)
- cloudflare for DNS entries
- auth server? idk if needed, nginx can probably handle it

### Software

- pi-hole (network-wide ad blocking)
- wireguard for the VPN (if needed)
- torrent client (for downloading movies, tv shows, and music)
- plex server (docker image)
- minecraft server (docker image)
