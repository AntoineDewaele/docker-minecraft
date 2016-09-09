# minecraft-server

[![Docker Pulls](https://img.shields.io/docker/pulls/dewaela/minecraft-server.svg)](https://hub.docker.com/r/dewaela/minecraft-server/)
[![Docker Stars](https://img.shields.io/docker/stars/dewaela/minecraft-server.svg?maxAge=2592000)](https://hub.docker.com/r/dewaela/minecraft-server/)

This docker image provides a Minecraft server with several basic command you can execute.

To simply run the container : 
  ```
  docker run -d -p 25565:25565 --name minecraft-server dewaela/minecraft-server
  ```
where the standard server port, 25565, will be exposed on your host machine.

## Commands

To execute a command on the container :
```
docker exec -it minecraft-server [command]
```
For each command, you can see usage with ```[command] --help```

Here's the list of commands :
  - start : start minecraft server
  - stop : stop minecraft server
  - reboot : reboot minecraft server
  - ban : ban a player
  - banip : ban a player with ip
  - whitelist : add player to the whitelist
  - ops : add op privileges to a player
  - properties : set server properties

## Java Configuration

### Memory limit

To adjust the java memory limit, you have to set the ```MIN_MEM``` and ```MAX_MEM``` :
``` docker run -e 'MIN_MEM=1024' ... ```


