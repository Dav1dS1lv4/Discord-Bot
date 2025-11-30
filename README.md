# Discord-Bot
A clean, fast, simple and professional moderation bot for Discord servers.

## Features

- `/lockdown` → Locks all text channels (3 channels permanently exempt)
- `/unlock` → Unlocks only the channels that were locked
- `/mute` & `/unmute` → Full mute system (role + timeout + optional voice mute)
- `/strike` → Automatic 3-strike system with increasing mute duration
- `/removestrike` → Removes the highest strike from a user
- `/ban`, `/kick`, `/unban`, `/clearchat`
- Custom GIFs via `/changegif`
- Full moderation logging
- Auto-deleting replies (no more 10008 errors)
- Duplicate command protection on deploy

## Setup (5 minutes)

### 1. Clone the repo
```bash
git clone https://github.com/Dav1dS1lv4/discord-moderation-bot.git
cd discord-moderation-bot
