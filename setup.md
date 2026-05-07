---
layout: default
title: Setup
description: First-time setup guide for server owners deploying VerifyBot.
permalink: /setup/
---

## First-Time Setup (Server Owners)

### Step 1. Invite VerifyBot

Use the official invite link from the project README:

<https://discord.com/api/oauth2/authorize?client_id=1325944440778657873&permissions=8&scope=applications.commands+bot>

### Step 2. Position the Bot Role

Move the VerifyBot role above any roles it must assign.

Why this matters:
- Discord blocks role assignment when the bot role is lower than target roles.

### Step 3. Configure Verification Roles

1. Create your public verification role (for example `Verified`).
2. Add it to VerifyBot allowlist with `/addverifyrole`.
3. Confirm with `/listverifyroles`.

### Step 4. Configure Logs

Set a log target:

- Channel logging: `/setlogs channel:#verify-logs`
- Webhook logging: use your server webhook target if enabled

### Step 5. Choose Verification Mode

- Manual flow: `/verify @member role:Verified`
- Reaction flow: `/setreactionverify channel:#verify role:Verified emoji:✅`

### Step 6. Test the Workflow

1. Test verification on a non-staff account.
2. Confirm role assignment works.
3. Confirm logs post correctly.
4. Confirm slash commands are visible to moderators.

## Quick Validation Checklist

- Bot can see and send messages in verify and log channels.
- Bot role is above verification role(s).
- Verification role is in allowlist.
- Slash commands are synced in server.
- Log target is configured and writable.
