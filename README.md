# Discord Moderation Bot

Powerful, clean and fast moderation bot with advanced lockdown system, automatic strikes, custom GIFs and full logging.

![Discord](https://img.shields.io/discord/YOUR_SERVER_ID?label=Discord&logo=discord&style=flat-square)
![Node.js](https://img.shields.io/badge/node-%3E%3D%2020.0.0-brightgreen)
![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-yellow)

## Features

- Complete slash-command moderation suite
- Smart lockdown with 3 permanently exempt channels
- 3-level automatic strike system with increasing mute duration
- Full mute/unmute (text + timeout + voice)
- Custom animated GIFs for ban/kick/unban/clearchat
- All actions logged with moderator & timestamp
- Auto-deleting replies (12 seconds) — no more 10008 errors
- Duplicate command protection on deploy
- Clean, commented and production-ready code

## All Commands

| Command           | Usage                                                                                 | Permission       |
|-------------------|---------------------------------------------------------------------------------------|------------------|
| `/ban`            | Bans a member + reason + custom GIF                                                   | Staff            |
| `/unban`          | Unbans by user ID + reason + custom GIF                                               | Staff            |
| `/kick`           | Kicks a member + reason + custom GIF                                                  | Staff            |
| `/mute`           | Mutes with role + timeout + optional voice mute                                      | Staff            |
| `/unmute`         | Removes timeout, mute role and voice mute                                             | Staff            |
| `/clearchat`      | Deletes up to 100 messages (optional: only from specific user)                        | Staff            |
| `/strike`         | Adds next strike level (1→2→3) + automatic mute (10/20/60 min)                        | Staff            |
| `/removestrike`   | Removes highest strike + clears any active mute                                       | Staff            |
| `/lockdown`       | Locks **all** text channels except 3 exempt ones — staff can always speak            | Staff            |
| `/unlock`         | Unlocks only channels that were previously locked (exempt channels untouched)        | Staff            |
| `/changegif`      | Changes the GIF for ban/kick/unban/clearchat (admin only)                             | Bot Owner        |

## Special Channels (Never Locked)

These channels stay open during `/lockdown`:


## Required Roles & Channels

**Staff Roles** (can use all commands)  
`1406372261815910481` · `1198728273002234009` · `1198728262638121111`

**Strike Roles**  
`strike 1` · `strike 2` · `strike 3`

**Mute Role**  
`1398540495105298544`

**Log Channel**  
`1398023766449324143`

## Installation (5 minutes)

```bash
git clone https://github.com/Dav1dS1lv4/discord-moderation-bot.git
cd discord-moderation-bot
npm install
cp .env.example .env

```
**Edit .env:**
envDISCORD_TOKEN=your_bot_token_here
CLIENT_ID=your_application_client_id_here
GUILD_ID=your_server_id_here

Deploy commands:
Bashnode deploy-commands.js

Start the bot:
Bashnode index.js

Optional: Custom GIFs
Edit data/gifs.json:
JSON{
  "ban": "https://tenor.com/view/ban-gif.gif",
  "kick": "https://tenor.com/view/kick-gif.gif",
  "unban": "https://tenor.com/view/welcome-back-gif.gif",
  "clearchat": "https://tenor.com/view/clean-gif.gif"
}

Security (IMPORTANT)

Never commit your real .env file!
Keep DISCORD_TOKEN, CLIENT_ID and GUILD_ID only on your local machine or VPS
Role/channel IDs in the code are safe to share (they are public anyway)

Author
Made with passion by David Silva
https://www.instagram.com/daviid_rsilva/
https://www.instagram.com/siltechlabs/
