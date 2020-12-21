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
	changeclass [x] (change the weapon of the player who used the command)

Where [x] is the index number of the weapon in the list of weapons

	Example1: mutate forceall 12 (force all players to use the M9 pistol that has the index 12 on the weapon list)
	Example2: mutate giveme 12 (give the players who used the command the M9 pistol)
	Example3: mutate changeclass 12 (give the players who used the command the M9 pistol)

	listw1 (command that shows the list1 of available weapons)
	listw2 (command that shows the list 2 of available weapons)
	
**Important note:** the **giveme** command and the **changeclass** command may or may not be enabled, the Tadmin must use **swgiveme** or **swchangeclass** commands respectively to enable or disable them.

## Commands to have infinite ammunition

	paramsammo [x] (Command to have infinite ammunition)
	
Where [x] could be 1 or 0

**Important note:** the **paramsammo [x]** command may or may not be disabled, to enable or disable it you must use the **swparamsammo** command



## Commands to enable and disable respawn

	respawnon (Command to enable respawn )
	respawnoff (Command to disable respawn)
	endgame (Command to terminate the match)

**Note:** the Tadmin must use the **endgame** command to allow players who joined late to a game to join the game. This is necessary when the respawn is activated in the game. The TADMIN mod will automatically send a message every 20 seconds to the player who has the role of TADMIN to use the command "endgame" when it detects that there are players as spectators waiting to join the game. In coop games it is necessary that there are at least 2 players connected for the respawn to work.Admin or PlayerAdmin. These commands are used so that an Admin or PlayerAdmin disables the player who has the role of TADMIN if he is abusingofhis role. Orif the administrators want to take control of the match.

## Commands for Admin and Players Admins

	tadminon (command to enable the TADMINcommands)
	tadminoff (command to disable the TADMINcommands)


Note:These commands cannotbe used by the TADMIN only can be used by an Admin or PlayerAdmin. These commands are used so that an Admin or PlayerAdmin disables the player who has the role of TADMIN if he is abusingof his role. Or if the administrators want to take control of the match.

## commands to configure tadmin by and admin or PlayerAdmin

	setini cheats [x] (enable or disable the cheats cmd)   
	setini forceall [x] (enable or disable the forceall cmd)
	setini changemap [x] (enable or disable the change map cmds)
	setini settime [x] (enable or disable the settime cmd)
	setini setrounds [x] (enable or disable the setrounds cmd)
	setini respawn [x] (enable or disable the respawn cmd)
	setini endgame [x] (enable or disable the endgame cmd)
	setini changeclass [x] (enable or disable the changeclass cmd)
	setini swapteams [x] (enable or disable the swapteams cmd)
	setini paramsammo [x] (enable or disable the paramsammo cmd)
	setini medic [x] (enable or disable the medic cmd)
	setini s_changeclass [x] (server start with changeclass cmd enabled)
	setini s_paramsammo [x] (server start with paramsammo cmd enabled)
	setini s_cheats [x] (server start with cheats cmd enabled)
	setini default_map [x] (enables or disables the server to switch to a default map when the server is empty)

	Where [x] could be 1 or 0

	setini setmap [x]  (set the default map of the server)
	
	where [x] is the name of the map 
	
	setini getmap (shows which is the default map established)



