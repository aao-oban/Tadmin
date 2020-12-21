# Tadmin Mutator for AAO 2.8.5 servers

Tadmin was originally designed as a tool that allows any player to change the server map without needing to be an admin or PlayerAdmin. Now the Tadmin has become more than a map changer.

Currently, the Tadmin allows the following functions to be carried out without the need to be an Admin or Playeradmin:

- change server map
- enable or disable cheats in the server
- set the duration of the game
- set the number of rounds per game
- enable or disable respawn in the server
- swap teams
- change class without using cheats
- have infinite ammo without using cheats
- get medical packages without using cheats

Tadmin can also help players to find the correct map that is running on the server and thus avoid the DCDS message. This works in conjunction with the DODGE download system.

With tadmin, administrators do not lose control of their server.

# TADMIN COMMANDS FOR PLAYERS

## Help command

displays the list of all available commands that a player can use. To use this command open the command console and type:

	mutate help

## Commands to be and stop being TADMIN

Are commands that are used to self-assign the role of TADMIN or stop being TADMIN

	mutate beadmin (command to auto-assign the role of TADMIN)
	mutate quitadmin (command to leave the TADMIN role)

##Commands to change the map

	mutate switchcoop [x] (command to switch to a cooperative map)
	mutate switchpvp [x]  (command to switch to a player vs player map)

Where **[x]** can be the name of the map or the index number of the list map

Example:mutate switchcoop 13(change to the map CARTEL which is number 13 on the list)
