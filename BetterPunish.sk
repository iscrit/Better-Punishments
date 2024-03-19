#==============================================
# FancyModeration
# Skript Made By Critical
# DO NOT DISTRIBUTE WITHOUT PREMISSION
# This is the main version of the skript, Do not dist!
# DONT TOUCH BELOW THIS LINE KIDDO
# THIS SKRIPT NEEDS THE FOLLOWING PLUGINS TO WORK - Vulcan Anti-cheat | Litebans | Any jail plugin
#==============================================

options:
	noperm: Unknown Command. Type /help for help.
	noperm2: {@prefix} &cNo permission
	credits: &eCritical Made this skript, A low end version will be on spigotmc soon # You can make this blank if you dont want to be nice :(
	helperperms: modgui.helper # {@helperperms}
	modperms: modgui.moderator
	prefix: &8[&9BP&8] &f # {@prefix}


# ^^^^^^^^^^^^^^^ Configure Permissions ^^^^^^^^^^^^^^^

command /punish <player>:    
	usage: {@prefix} &cUsage /punish <someone>
	trigger:
		if arg-1 is set:
			if player has permission "{@helperperms}":
				open chest with 5 rows named "&fPunishments for &a%arg-1%" to player 
				format slot 40 of player with red glass named "&c&lLoading, Do not choose punishment yet!" to close 
				wait 10 tick
				play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 0.5 to arg 1
				format slot 0 of player with piston named "&cBan Player" with lore "&eBan a player with reason templates!" to close then run [execute player command "banishmentlist %arg-1%"]
				wait 20 ticks
				format slot 40 of player with orange glass named "&6&lStill Loading..." to close 
				play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
				format slot 1 of player with iron bars named "&9Jail player ♟" with lore "&fJail a player with reason templates!" to close then run [execute player command "jailtemplates %arg-1%"]
				wait 20 ticks
				format slot 40 of player with lime glass named "&a&lLoaded correctly" to close 
				play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1.5 to arg 1
				format slot 2 of player with ice named "&bFreeze player ☢" with lore "&cVulcan Freeze ☄" to close then run [execute player command "freezetemplates %arg-1%"]
				format slot 3 of player with observer named "&eRuin Players camera ↗" with lore "&cThis will ruin the seleced players" and "&ccamera forcing them to rejoin!" to close then run [execute player command "camera %arg-1%"]
				format slot 4 of player with anvil named "&fAnvil Player" with lore "&eThis will spawn a anvil on the players head" to close then run [execute player command "anvil %arg-1%"]
				format slot 5 of player with paper named "&eWarn Player" with lore "&eWarn players for:" and "&f- Naked Killing" and "&f- Glitch abuse" and "&f- Chat spam" and "&f- Not listening to staff" and "&f- Comunnity distuption" to close then run [execute player command "warntemps %arg-1%"]
				format slot 36 of player with firework named "&eCredits" with lore "{@credits}" to close
				format slot 44 of player with barrier named "&cCancel" to close
			else:
				send "{@noperm2}"
		else:
			if arg-1 is not set:
				send "{@prefix} Please select a player to punish!"


   # # # # # # # ##  # # # # # #  # # # # # # # # # # # ######### # # # # # # # #  # # # # # # # # # # # # # # # # # #  # # # # #             
# These are the commands to open the custom guis please do not touch these unless you know what you are doing! - cwitty         #
# # # # # #  # # # # # ## # # # # # #  # ## #  # # # # # # # # ## # # # # # # # # # ## # # # # # # # # # # # # # # # # # # # # # 
command /banishmentlist <player>:
	usage: {@prefix} &cUsage /banishmentlist <someone>
	permission: {@modperms}
	permission message: {@noperm2}
	trigger:
		wait 2 ticks
		open chest with 3 rows named "&c&lBan &a%arg-1%" to player
		wait 1 tick
		format slot 0 of player with lime wool named "&bXRAY" with lore "&f1d ban" to close then run [execute player command "litebans:ban %arg-1% 1d Cheating/Suspected of cheating."]
		format slot 1 of player with yellow wool named "&eNaked killing (10th warn)" with lore "&f2hr Ban" to close then run [execute player command "litebans:ban %arg-1% 2hr Exsessive Naked killing, Do /nkill"]
		format slot 2 of player with orange wool named "&aSuspected Auto totem" with lore "&f30m Ban" to close then run [execute player command "litebans:ban %arg-1% 30m Suspected of using auto totem"]
		format slot 3 of player with red wool named "&cEnd Greifing" with lore "&f2d Ban" to close then run [execute player command "litebans:ban %arg-1% 2d Greifing base in end"]
		format slot 4 of player with black wool named "&e&nPERM BAN" with lore "&e&nMods if you false perm ban a player you will be striked" and "&f&l&nForever Ban" to close then run [execute player command "litebans:ban %arg-1% PermBan - If you belive this was a mistake contact mods"]
		play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
		format slot 26 of player with barrier named "&cCancel" to run [execute player command "punish %arg-1%"] 

# 

command /jailtemplates <player>:
	usage: {@prefix} &cUsage /jailtemplates <someone>
	permission: {@helperperms}
	permission message: {@noperm2}
	trigger:
		wait 2 ticks
		open chest with 3 rows named "&9Jail &f%arg-1%" to player
		wait 1 tick
		format slot 0 of player with lime wool named "&fNaked killing 15M" to close then run [execute player command "jail %arg-1% 15m Please do not naked kill, To see what naked killing is do /nkill"]
		format slot 1 of player with yellow wool named "&fGlitch/Bug abuse 20M" to close then run [execute player command "jail %arg-1% 20m Please do not abuse bugs, report them instead!"]
		format slot 2 of player with orange wool named "&cLAG MACHINE" with lore "&fThis should only be used to jail a player that is using a lag machine!" to close then run [execute player command "jail %arg-1% 10d SUSPECTED LAG MACHINE | JAILED FOR LAG MACHINE ADMINS BEING CONTACTED"]
		format slot 3 of player with black wool named "&fCheater" to close then run [execute player command "jail %arg-1% 1d Cheating | Jailed beacuse helpers cant ban!"]
		play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
		format slot 26 of player with barrier named "&cCancel" to run [execute player command "punish %arg-1%"] 

#

command /freezetemplates <player>:
	usage: {@prefix} &cUsage /freezetemplates <someone>
	permission: {@helperperms}
	permission message: {@noperm2}
	trigger:
		wait 2 ticks
		open chest with 3 rows named "&bFreeze &f%arg-1%" to player
		wait 1 tick
		format slot 0 of player with cyan wool named "&bFreeze" to close then run [execute player command "vulcan freeze %arg-1%"]
		format slot 1 of player with green wool named "&aUnfreeze" to close then run [execute player command "vulcan freeze %arg-1%"]
		play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
		format slot 26 of player with barrier named "&cCancel" to run [execute player command "punish %arg-1%"]

# Ruin Player camera

command /camera <player>:
	usage: {@prefix} &cUsage /camera <someone>
	permission: {@modperms}
	permission message: {@noperm2}
	trigger:
		wait 2 ticks
		open chest with 3 rows named "&cCamera glitch amount" to player
		wait 1 tick
		format slot 0 of player with lime wool named "&fSPIN CAMERA" with lore "&eThere is only 1 mode more coming soon - critical" to close then run [execute player command "camerabug %arg-1%"]	
		play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
		format slot 26 of player with barrier named "&cCancel" to run [execute player command "punish %arg-1%"]

command /camerabug <player>:
	usage: {@prefix} &cUsage /camerabug <someone>
	permission: troll.camera
	permission message: {@noperm2}
	trigger:
		if arg-1 is online:
			set {_x} to x-coordinate of arg-1
			set {_y} to y-coordinate of arg-1
			set {_z} to z-coordinate of arg-1
			set {_world} to world of arg-1
			set {_yaw} to yaw of arg-1
			set {_pitch} to pitch of arg-1
			loop 50 times:
				set {_random} to random integer from 1 to 360
				add {_random} to {_yaw}
				set {_location} to location({_x}, {_y}, {_z}, {_world}, {_yaw}, -89)
				teleport the arg-1 to {_location}
				wait 4 tick
				set {_random} to random integer from 1 to 360
				add {_random} to {_yaw}
				set {_location} to location({_x}, {_y}, {_z}, {_world}, {_yaw}, 89)
				teleport the arg-1 to {_location}
				wait 4 tick
		else:
			stop


# ANVIL PUNSIHMENT 
command /anvil <player>:
	usage: {@prefix} &cUsage /anvil <someone>
	permission: troll.anvil
	permission message: {@noperm2}
	trigger:
		set block 10 meters above the arg 1 to damaged anvil


# Warn punishment

command /warntemps <player>:
	usage: {@prefix} &cUsage /warntemps <someone>
	permission: {@helperperms}
	permission message: {@noperm2}
	trigger:
		wait 2 ticks
		open chest with 3 rows named "&eGive &f%arg-1%&e a warning" to player
		wait 1 tick
		format slot 0 of player with green wool named "&fNaked Killing" with lore "&f1st offense" and "&fJail if 2nd offense" to close then run [execute player command "litebans:warn %arg-1% Naked killing 1st offense (/nkill)"]
		format slot 1 of player with yellow wool named "&fStaff Disrespect" to close then run [execute player command "vulcan freeze %arg-1%"]
		play sound "entity.experience_orb.pickup" with volume 0.5 at pitch 1 to arg 1
		format slot 26 of player with barrier named "&cCancel" to run [execute player command "punish %arg-1%"]
