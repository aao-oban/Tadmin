# Tadmin Mutator for AAO 2.8.5 servers

## Tadmin = Temporary administrator

Tadmin was originally designed as a tool that allows any player to change the server map without needing to be an admin or PlayerAdmin. Now the Tadmin has become more than a map changer.

Currently, the Tadmin allows the following functions to be carried out without the need to be an Admin or Playeradmin:

- change server map
- enable or disable cheats
- set the duration of the game
- set the number of rounds per game
- enable or disable respawn
- swap teams
- change class without using cheats
- have infinite ammo without using cheats
- get medical packages without using cheats
- warn inactive players to move
- randomly assign ammo when picking up enemy weapons

Tadmin can also help players to find the correct map that is running on the server and thus avoid the DCDS message. This works in conjunction with the DODGE download system.

With Tadmin you can set a default map to which your server will automatically switch every time your server empties of players (this is configurable, you can activate or deactivate it)

**In fact all the features of Tadmin are configurable you can activate and deactivate the ones you like from its ini configuration file**

## How does it work?

Any player that connects to a server that has the TADMIN running has the possibility to become TADMIN. To do so, just open the command console(press ~key) and type the command **"mutate beadmin"** If no player is self-assigned the role of TADMIN all players can administer the server with TADMIN commands which is not recommended. Once someone is self-assigned the role of TADMIN with the command **"mutate beadmin"** only this player can use the TADMIN commands to manage the server. If the player who had the role of TADMIN is disconnected from the game, the mutator waits 2 minutes for the player to reconnect, if the player does not reconnect during that time the mutator will automatically remove the role of TADMIN to that player. This way any player that is in the server can self-assign the role of TADMIN with the command "mutate beadmin". 

An Admin or PlayerAdmin can use all the TADMIN commands without needing to have the TADMIN role. they can even use the commands if there is a player who already has the role of tadmin.

[click here to see a video tutorial on how to use tadmin](https://youtu.be/1NilWoCvryI)

## How to install Tadmin on your server?

- **STEP 1** Get a copy of the Tadmin v1.7 [Here](https://github.com/aao-oban/Tadmin/raw/main/Tadmin%20v%201.7.7z)
- **STEP 2** unzip the file to extract its content
- **STEP 3** Copy the files Tadmin.u, Tadmin.ini to the system folder of your server
- **STEP 4** Stop your server and start it adding the parameter ?Mutator=Tadmin.Tadmin as shown in the following example

EXAMPLE:

	Server.exe LAN Bridge.aao?Mutator=Tadmin.Tadmin log=server.log ini=server.ini

**Note: If you want the Tadmin map change function to be fully functional you must generate the files "tadmin_coop_list.lst" and "tadmin_pvp_list.lst" and copy those files to the System folder of your server. Below you can see the methods to create the lists for the Tadmin**

Any questions you can write to my email oban.bere@gmail.com

## How to generate the PVP and COOP maps lists for Tadmin mutator

There are two methods for creating the lists. the automatic method using a tool and the manual method.

###### Automatic method

For this we are going to use a list generator tool that you can download [Here](https://github.com/aao-oban/Tadmin/raw/main/maplistg.7z)

The file you will download is a compressed file that contains 3 files:

- maplistg.u
- RunTool.bat
- ToMapFolder.bat

To know how to use this tool watch the video tutorial [Here](https://youtu.be/K4GwD25ztRQ)

If an error occurs during the list creation process, watch the video to continue the process [Here](https://youtu.be/_iCUhSC0Dcg)

**IMPORTANT NOTE: Before using this tool, you must have in the "Maps" folder of the game all the maps that your server has. so you can generate lists that reflect the maps of your server.**

###### Manual method

The manual method consists of manually creating the tadmin_coop_list.lst and tadmin_pvp_list.lst files.

for this you must create two text files and rename them tadmin_coop_list.lst and tadmin_pvp_list.lst (it is important that you change the extension to .lst)

then open each of the files with a text editor and begin to add the names of the maps one for each line and always ending the line with ":" as shown in the following example

> armoury_infiltration.aao:

once you finish adding the maps save your files and that's it

Remember the **COOP** maps must go in the **tadmin_coop_list.lst** file and the **PVP** maps must go in the **tadmin_pvp_list.lst** file.

Once you have the files ready, upload them to the system folder of your server.

# TADMIN COMMANDS FOR PLAYERS

## Help command

displays the list of all available commands that a player can use. To use this command open the command console and type:

	mutate help

## Commands to be and stop being TADMIN

Are commands that are used to self-assign the role of TADMIN or stop being TADMIN

	mutate beadmin (command to auto-assign the role of TADMIN)
	mutate quitadmin (command to leave the TADMIN role)

## Commands to change the map

	mutate switchcoop [x] (command to switch to a cooperative map)
	mutate switchpvp [x]  (command to switch to a player vs player map)

Where **[x]** can be the name of the map or the index number of the list map

	Example: mutate switchcoop 13 (change to the map CARTEL which is number 13 on the list)
	
## Command to see the list of maps

	mutate listcoop [x] (shows the list of available COOP maps)
	mutate listpvp [x] (shows the list of available PVP maps)

Where **[x]** is a number that indicates the list that you want to see.

	Example:mutate listcoop 10 (will show the list number 10 of cooperative maps)

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

	Example:mutate listcoop land,snow2 (will show the list number 2of Coop maps with snow and on land)
	
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

## Command to get random ammo when pick up an enemy weapon

prammo [x] (Enable/Disable pickup enemy random ammo)

Where [x] could be 1 or 0

This command causes that when you pick up an enemy weapon a random number of bullets is assigned to the weapon and it can also give you 1 to 3 clips of ammo and occasionally also give you grenades


## Commands for Admin and Players Admins

	tadminon (command that prevents the player with the Tadmin role from using the commands)
	tadminoff (command that enables the player with the Tadmin role to use the commands)


Note:These commands cannot be used by the TADMIN only can be used by an Admin or PlayerAdmin. These commands are used so that an Admin or PlayerAdmin prevent the player who has the Tadmin role from using the Tadmin commands temporarily if he is abusing of his role. Or if the administrators want to take control of the server.

## Commands to configure the Tadmin (only for admins or PlayerAdmins)

	setini cheats [x] (enable or disable the cheats cmd in Tadmin)   
	setini forceall [x] (enable or disable the forceall cmd in Tadmin)
	setini changemap [x] (enable or disable the change map cmds in Tadmin)
	setini settime [x] (enable or disable the settime cmd in Tadmin)
	setini setrounds [x] (enable or disable the setrounds cmd in Tadmin)
	setini respawn [x] (enable or disable the respawn cmd in Tadmin)
	setini endgame [x] (enable or disable the endgame cmd in Tadmin)
	setini changeclass [x] (enable or disable the changeclass cmd in Tadmin)
	setini swapteams [x] (enable or disable the swapteams cmd in Tadmin)
	setini paramsammo [x] (enable or disable the paramsammo cmd in Tadmin)
	setini medic [x] (enable or disable the medic cmd in Tadmin)
	setini s_changeclass [x] (server start with changeclass cmd enabled in Tadmin)
	setini s_paramsammo [x] (server start with paramsammo cmd enabled in Tadmin)
	setini s_cheats [x] (server start with cheats cmd enabled in Tadmin)
	setini default_map [x] (enables or disables the server to switch to a default map when the server is empty in Tadmin)
	setini prammo [x] (enable or disable the prammo cmd in Tadmin)
	setini warnidle [x] (enable or disable idle warnings in Tadmin)
	

	Where [x] could be 1 or 0, 1 is to enable 0 to disable

	setini setmap [x]  (set the default map of the server in Tadmin)
	
	where [x] is the name of the map 
	
	setini getmap (shows which is the default map established in Tadmin)



