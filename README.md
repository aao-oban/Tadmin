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

	Example: mutate switchcoop 13 (change to the map CARTEL which is number 13 on the list)
	
## Command to see the list of maps

	mutate listcoop[x] (shows the list of availableCOOPmaps)
	mutate listpvp[x] (shows the list of available PVP maps)

Where **[x]** is a number that indicates the list that you want to see.

	Example:mutate listcoop10 (will show the list number 10 of cooperative maps)

You can also use Filters in these commands to see lists of maps classified by climate, class, etc.

	listcoop [CLASS],[TOD],[WEATHER],[SF],[OTHERS] [x]
	listpvp [CLASS],[TOD],[WEATHER],[SF],[OTHERS] [x]

where:

	[CLASS] = AIR,LAND,SEA,SPACE

	[TOD] = DAWN,DAY,DUSK,NIGHT

	[WEATHER] = CLOUDY,FOG,HAZY,MIST,RAIN,SNOW,SUNNY,CLEAR

	[SF] = SF,NSF

	[OTHERS] = BETA,NBETA,MOD,NMOD,ES2,NES2

	[x] = x is a number that indicates the list number you want to see

	Example:mutate listcoop land,snow2 (will show the list number 2of Coopmaps with snow and on land)
	
## Commands to enable and disable cheats

	mutate cheatson (command to enable the cheats)
	mutate cheatsoff (command to disable the cheats)
	
**Note:This commands takes effect immediately after executing it.**

## Commands to set the time and number of rounds

	settime [x] (Set the round length in minutes)
	setrounds [x] (Set the number of rounds per match)

	Example:mutate settime 20 (Set the round length of the game to 20 minutes)
	mutate setrounds 3 (Set the rounds per match to 3)
	
**Note:The “settime [x]” command takes effect in the next round.**

## Commands to force weapons

	forceall [x] (command to force all players to have the same weapon)
	giveme[x] (change the weapon of the player who used the command)

Where [x] is the index number of the weapon in the list of weapons

	Example1:mutate forceall12 (force all players to use the M9 pistol that has the index 12 on the weapon list)
	Example2:mutate giveme12 (give theplayerswhoused the command the M9 pistol)

	listw1 (command that shows the list1 of available weapons)
	listw2 (command that shows the list 2 of available weapons)
