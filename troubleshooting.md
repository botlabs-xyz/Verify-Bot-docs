---
layout: default
title: Troubleshooting
description: Fix common VerifyBot setup and operation issues.
permalink: /troubleshooting/
---

## Troubleshooting

### Slash commands are not showing

Try these checks:

1. Open **Server Settings → Integrations → VerifyBot** and confirm the app is installed.
2. Open **Server Settings → Roles → VerifyBot** and make sure command-related permissions are enabled.
3. If you just invited VerifyBot, wait a few minutes and check again. Discord sometimes needs a short delay before new commands appear.
4. If commands still do not appear, re-invite VerifyBot using the official invite link from this docs repo.

### VerifyBot cannot assign roles

Try these checks:

1. Open **Server Settings → Roles**.
2. Drag the **VerifyBot** role above the role you want VerifyBot to give (for example, `Verified`).
3. In the VerifyBot role permissions, make sure **Manage Roles** is enabled.
4. Confirm the target role has been allowed in VerifyBot with `/addverifyrole`.

Plain-English note: Discord only lets a bot assign roles that are below the bot's own role in the role list.

### Verification message is not working

Try these checks:

1. Open the verify channel, then click **Edit Channel → Permissions**.
2. Make sure VerifyBot can:
   - View Channel
   - Send Messages
   - Embed Links
3. Run `/setreactionverify` again and double-check channel, role, and emoji choices.
4. If you recently changed emoji/role settings, create a fresh verification message.

### Logs are not posting

Try these checks:

1. Run `/setlogs` again and select the correct log channel.
2. Open the log channel → **Edit Channel → Permissions** and confirm VerifyBot can send messages there.
3. If you use webhook-based logs, make sure that log destination is still active.

Plain-English note: A webhook is just another way Discord can deliver bot messages to a channel.

### Role order problems

Common sign:
- A verify command says success, but no role appears on the member.

Fix:

1. Open **Server Settings → Roles**.
2. Move the **VerifyBot** role higher than your verification roles.
3. Test again with `/verify` on a test member.

Plain-English note: You may hear this called "role hierarchy". It simply means the top-to-bottom role order in **Server Settings → Roles**.

## What to send support

If you still need help, share this in support:

- server name
- command used
- what you expected
- what happened instead
- screenshot of roles or permissions if relevant

Support server: <https://discord.gg/BusuZp2G8w>
