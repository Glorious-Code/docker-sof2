# docker-sof2
A docker container for Soldier of Fortune 2

Build: 
```bash
docker build -t sof2-gold .
```

Run:
```bash
docker run -it --name sof2-gold --rm -p 20100/udp -e "SOF2_GAME={MOD}" -e "SOF2_CONFIG={Config}" -v /your/path/to/mod:/home/docker/{MOD}:rw -v /your/path/to/base:/home/docker/base:rw sof2-gold
```

For example:
```bash
docker run -it --name sof2-gold --rm -p 20100/udp -e "SOF2_GAME=1fx" -e "SOF2_CONFIG=Config.cfg" -v /home/noah/mods/1fx:/home/docker/1fx:rw -v /home/noah/mods/base:/home/docker/base:rw sof2-gold
```