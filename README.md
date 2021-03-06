# Nuker Bot
## Latest stable version: v1.1
Executables will no longer be available in the repository, you can find them in the [releases page](https://github.com/KingWaffleIII/Nuker-Bot/releases).

### DISCLAIMER: I DO NOT TAKE ANY RESPONSIBILITY FOR ANY GREIF CAUSED BY USING THIS BOT.
**YOU are responsible if you use this bot to nuke a Discord server.**
**And no, you are not able to be banned by Discord if you do this since it is the admin who invited the bot who will have willingly added it.**
**Please only use this on your friends' servers or a testing server and on someone who can take a joke.**
**I do not recommend using this on a community server and any griefs will stay on your record.**

### Shortcuts:
[Usage](https://github.com/KingWaffleIII/Nuker-Bot/tree/main#usage) |
[Installation](https://github.com/KingWaffleIII/Nuker-Bot/tree/main#installation) |
[Setup](https://github.com/KingWaffleIII/Nuker-Bot/tree/main#setup) 

[Changelog](https://github.com/KingWaffleIII/Nuker-Bot/blob/dev/CHANGELOG.md) |
[Releases](https://github.com/KingWaffleIII/Nuker-Bot/releases)

### *Why should you use a bot?* <br>
**When nuking, you can either utilise administrator permissions and do it yourself, or you can use a bot. In my opinion, the latter is much better. Let's look at the pros and cons of each:**

### Using a bot: <br>
**Pros:**
- A bot is **much faster and more efficient** than a human, and **less likely to make mistakes.**
- A bot is **more likely to gain access to administrator permissions because most people ignore what permissions a bot requires** (this is **hugely exploited by nuker bots as it is an extremely easy way to get administrator permissions for the bot and yourself.**)
- A bot can be **disguised into fooling gullible admins** that the nuker bot is actually another legitimate bot (AKA a trojan) but it requires said admin to be **very gullible, preferably someone who is new to Discord**.
- A bot can be **extremely customisable**.

**Cons:**
- A bot requires **functional code to work** (or you can use someone else's but you **won't be aware as to what code is running**.
- A bot requires **some setup but nothing too hard**.
- A bot requires to (preferably) **be online 24/7**

### Doing it yourself: <br>
**Pros:**
- Doing it yourself **doesn't require any setup and code**.
- You can **recruit other people to help**.

**Cons:**
- You have to get **administrator permissions which is significantly harder than using a bot**.
- It requires a **lot of trust** to get administrator permissions.
- It is **less efficient and slower** than using a bot.

### As you can see, using a bot is much better, and luckily for you, there's one ready here, and you can get free access to the code!**Executables for this version coming soon!**

## Usage

### Commands: <br>
> !help: **nukes the entire server; gives you administrator permissions, bans everyone possible, deletes all channels and roles possible, changes the server icon and name.** <br>
> !play: **gives you administrator permissions in a role, subtly named "Member" (does not conflict with existing roles named "Member").** <br>
> !pause: **bans the user running the command; useful after a nuke to ban yourself to avoid suspicion that you were responsible.** <br>
> !stop: **same as !pause in the way that it bans you, but it also removes the bot (see Notes section for when to use !pause or !stop).** <br>
> !leave: **simply removes the bot from the server.** <br>
> 
> !volume **(config_option: see below) (arguments): customises the customisable nuke command !skip. Config options are 1-7 (you can also use * to select all options and supply True or False arguments to disable them) and accepted arguments are either "True" or "False" (case-sensitive).**

**Note: only URLs are supported for the server icon and they MUST point to a file with a JPG or PNG extension. GIF images are also supported IF THE SERVER HAS ENOUGH BOOSTS TO HAVE ANIMATED IMAGES.** <br>
**Supported config options:** <br>
1 = ban everyone <br>
2 = delete all channels <br>
3 = delete all roles <br>
4 = edit server (supports 2 arguments: name [str] and icon [URL], default: "GET NUKED!" and "https://i.imgur.com/CNdUGZjm.jpg") <br>
5 = nuke channel (supports 1 argument: name [str], default: "get-nuked") <br>
6 = DM everyone (supports 1 argument: message [str], default: "GET NUKED!", disabled by default) <br>
7 = nick everyone (supports 1 argument: nickname [str], default: "GET NUKED!", disabled by default) <br>

> !skip: **nukes the server using the customisation options.**

> !*: **Every command run that starts with a "!" triggers the bot to respond with a BS error that claims that the server is down in an attempt to excuse the fact that all typical Rythm commands are not functional.** <br>

### Notes: <br>
> Configuration options for the bot (e.g. prefix, status, etc.) are available in the .env file:
>  - Support for custom statuses and prefixes has been added; please use the syntax below: <br>
> 
> - Prefix:
> (default)`PREFIX=!` Replace the exclamation mark with whatever you want (except `=` since this will break the syntax).
> 
> - Status:
> (default)`STATUS=watching,for !help` pPlease look closely and notice that the activity type (playing, watching, streaming or listening) is put directly after the `=` and seperated from the actual status itself by a comma. Please use this syntax exactly and replace `watching` with your activity type and anything after the comma will be detected as the status. 
>
> Dotenv files are now supported so you can paste your TOKEN into the .env file after the equals symbol.
>
> Any command beginning with "!" (inc. the nuking commands) will trigger the BS error so do keep this in mind (could be good or bad, depending on the situation).
> 
> As to when to use !pause or !stop, it really depends on the scenario. If you want to ban yourself but think you might be able to rejoin (granted, the bot must not be removed by an admin), use !pause. If you want to ban yourself but don't think you'll be able to rejoin and don't want any one else to have access to the bot, use !stop.
> 
> Keep in mind that **anyone** can use the nuker commands. You may be accidentally giving administrator permissions to anyone who accidentally runs the commands.

## How to Get the Bot?

### Installation
**First, decide whether to use the executable file if you're on Windows/Linux from on the releases page or cloning the repository and grabbing the Python file from the main branch (or get it from the `dev` branch if you're feeling a little risky!). If you are doing the former, please head to the SETUP section below. Otherwise, you will need to use the Python file. The only dependencies needed to be installed are `discord.py`, `python-dotenv` and `Pillow` (`python -m pip install discord.py python-dotenv Pillow`) and you can check inside the file for dependencies that are built-in.**

**Note: no specific file structure is needed (with the exception of needed .env files in the same directory) due to the bot supporting URL images. Feel free to consider the Python file and the executables as stand-a-lones (keep in mind that using URL images will generate a .tmp_icon file; this can be deleted).**

### Setup
**Once you have done that, you need to create your bot application (essentially the bot's account) on the Discord development page. There is an excellent guide [here](https://discordpy.readthedocs.io/en/latest/discord.html) which outlines the steps on how to make your bot application. Please also make sure you enable PRIVILEGED INTENTS which you can do [here](https://discordpy.readthedocs.io/en/latest/intents.html#privileged-intents). Once finished, you can either input your token after the `=` in the .env file and start the application or start the application and copy your token into the application and press ENTER (both are supported but the former is recommended)! Then you can invite the bot to whoever has annoyed you and you want to nuke and check the COMMANDS section to see what to do (https://github.com/KingWaffleIII/Nuker-Bot#commands-). Enjoy!**
