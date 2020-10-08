[![Python version](https://img.shields.io/badge/python-3.5%2C%203.6%2C%203.7-blue.svg)](https://python.org)

### Setup
Setting up the bot is easy. Here: 
* Install Python 3.7
* During the setup, tick Install launcher for all users (recommended) and Add Python 3.7 to PATH when prompted.
* Install Git for Windows.
* During the setup, tick Git from the command line and also 3rd-party software, Checkout Windows-style, commit Unix-style endings, and Use MinTTY (the default terminal MSYS2).
* Open Git Bash by right-clicking an empty space inside of a folder (e.g My Documents) and clicking Git Bash here.
* Run git clone `https://github.com/Vexvain/Discord-Music-Bot.git DiscordMusicBot -b master` in the command window that opens.
* After doing that, a folder called DiscordMusicBot will appear in the folder you opened Git Bash in. Configure your bot, then run update.bat to update your dependencies, then run.bat to start the DiscordMusicBot.

After that, configure the bot to ensure its connection to Discord.

The main configuration file is `config/options.ini`, but it is not included by default. Simply make a copy of `options.ini` See `options.ini` for more information about configurations.

### Commands

There are many commands that can be used with the bot. Most notably, the `play <url>` command (preceded by your command prefix) will download, process, and play a song from YouTube or a similar site. A full list of commands is available here: 

    !help [command] - Prints a list of commands, or info on a command if one is specified.
    
    !play <URL/query> - Plays audio from a specific URL or searches for a query on YouTube and queues the first result.
    
    !queue - Displays all of the media that is queued.
    
    !np - Displays the media that is currently being played.
    
    !skip - Vote to skip the current media. Required skips/skip ratio is set in the config file. The bot’s owner will instantly skip when using !skip f.
    
    !search [service] [#] <query> - Searches a specific service (default: YT) for a query and returns the first few results (default: 3, limit: 10). The user can then select from the results if they want to add any to the queue.
    
    !shuffle - Shuffles the queue.
    
    !clear - Clears the queue.
    
    !pause - Pauses the current media.
    
    !resume - Resumes the current media
    
    !volume [number] - Sets the volume of the bot for everyone. Should be a number between 1 and 100. Can be relative (e.g +10 to add 10 to current volume). If no parameter is given, it will display the current volume.
    
    !summon - Connects the bot to your current voice channel, if it has permission.
     
     !clean <number> - Searches through the number of messages given and deletes those that were sent by the bot, effectively cleaning the channel. If the bot has Manage Messages on the server, it will delete user command messages too, like !play.

    !blacklist <status> <@user1>... - Add or remove users from the blacklist. Blacklisted users cannot use any bot commands. This overrides any permissions settings set in the permissions file. The owner cannot be blacklisted. Multiple users can be specified in the command. Users must be @mentioned. Status should be either +, -, add, or remove.
    
    !perms - Sends a message to the user with their bot permissions.
    
    !stream <url> - Streams a URL. This can be a Twitch, YouTube, etc livestream, or a radio stream. This feature of the bot is experimental and may have some issues.
    
    !save - Saves the current song to the autoplaylist.
    
    !karaoke - Enables karaoke mode in a server. During karaoke mode, only users with the BypassKaraokeMode permission can queue music.
    
### ADMIN COMMANDS

    !joinserver - Provides the URL that can be used to add the bot to another server. This command is always restricted to the owner of the bot.
    
    !leaveserver <name/id> - Forces the bot to leave a server. You must specify either the server name or id.
    
    !pldump <playlist> - Collects URLs from a YouTube playlist or Soundcloud set and dumps them into a text file that can be copied into the autoplaylist.
    
    !setavatar [url] - Changes the bot’s avatar to the specified URL or uploaded image. A URL does not need to be specified if an image is uploaded with the command as the message (comment).
    
    !setname <name> - Changes the bot’s Discord username (not nickname). Discord limits these changes to 2/hr.
    
    !setnick <nick> - Changes the bot’s nickname on a server, if it has permission to do so.
    
    !disconnect - Disconnects the bot from the voice channel.
    
    !restart - Restarts the bot.
    
    !shutdown - Shuts down the bot and terminates the process.
    
    !option <option> <y/n> - Changes a config option without restarting the bot for the current session. Run !help option for info.
    
    !remove <number> - Removes a song from the queue by its numbered position. Use 
    
    !queue to find out song positions.
