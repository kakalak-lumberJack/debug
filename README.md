# Debug

## Description
A minetest mod that allows in-game debugging/monitoring of the minetest logfile (default: /home/minetest/.minetest/debug.txt).

## Features
Adds in-game commands to read/search logfiles in chat for players with ban priv:
Return the last 100 entries from the logfile.
	
	/debug 
Return the last 100 entries from logfile containing the search term 		
	
	/grep <searchterm>
In-game command to shutdown the server with 10 second delay. 
	
	"/shutdown" 		
Automates keeping logfile at a managable size by archiving (tar format) the logfire in the same folder and creating a new debug.txt on shutdown when the file reaches about 30MB.
	
## Requirements
This mod was developed/tested on Debian 8. may need some tweaking to work on other operating systems. 
	
Requires Lua Filesystem. You can inntall via [Luarocks]https://luarocks.org/modules/hisham/luafilesystem : 
	
	luarocks install luafilesystem 	
Requires tar on operating system
Mod must be listed in minetest.conf under trusted mods:

	secure.trusted mods = debug
The *init.lua* file must be configured to the path of your log file. See comments in the file for more info. 	
	
No other mod dependencies.
		
## License
MIT --See license.txt
