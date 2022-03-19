# BetterPlayerXP

A plugin that adds a leveling system to your server. Users start at level 1, and gain experience through doing tasks such as escaping as a classd or scientist, winning the round, killing an SCP, etc.

# Message for people that use this plugin.

I have no time or motivation to maintain this plugin, too many problems exist in this plugin that my brain can't comprehend and read code correctly, since EXILED 3 released this kept happening, though if you want to fix them, make a pull request and I'll push it to main branch.

# READ ME!!!

There are a few issues with the plugin but it is still usable, One issue is with commands not working! If you want to fix it please go ahead and do so. -Denty (I just rebuilt this since Atom was having an issue with their compiler)

# I know this code hurts
Previous owner's fault

# Fork info

This fork is meant to maintain the plugin by the community.

# Installation

**[EXILED](https://github.com/galaxy119/EXILED) 4.1.2+ must be installed**

Place the `BetterPlayerXP.dll` file in your `~/.config/Exiled/Plugins` folder.

# Features
* Grants xp to players for completing game tasks.
* Scale factor for all xp values.
* All xp rates are configurable, as well as all messages displayed to users for gaining xp.
* Players will be given small configurable messages on their screen to notify them when they gain xp, as well as level up.
* Fully configurable karma system.
  * Players will gain karma for doing good deeds
  * Players will lost karma for doing bad deeds such as killing unarmed Class-D or Scientists.
  * Karma is an xp multiplier, all players start with a karma of 1.00
  * Players with karma below a certain amount can be denied the ability to play SCP.
  * This system can be toggled on and off.
* Commands that can be run through RA console **or** client console by using the prefix `.` to check the level, xp, and server ranking of a user, as well as the server leaderboard.
* Commands to calculate a server leaderboard based off a configurable size and check a player's level.
* Levels get increasingly harder to achieve, the amount in which is takes to achieve the next level can be modified.
* When a player is killed, the victim gets a message displaying the killers level.
* All data transfer between servers.

# API
Developers can access and modify data about each player through the API. After referencing this assembly, add the namespace `PlayerXP.API` to your file. You will then be able to access several useful methods to retrieve and modify data through the `PXP` class.

# Commands

**Commands that can be run from both RA console and player console. These commands must use the prefix `.` if they are being run through the player console.**

| Command        | Value Type | Description |
| :-------------: | :---------: | :------ |
| LVL / LEVEL | PLAYER NAME / STEAMID64 | Displays a user's level and xp. Will also display their server ranking. Not specifying a name will default to yourself. |
| LB / TOP | SIZE | Displays the top users in the server. If no size is specified it will output the top 5. Maximum leaderboard size is 15. |

**Commands that can only be run through RA console.**

| Command        | Description |
| :-------------: | :------ |
| XPTOGGLE | Toggles XP gaining/saving. |
| XPSAVE | Forces a file save from the current round cache. |
