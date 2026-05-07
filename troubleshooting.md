---
layout: default
title: Troubleshooting
description: Fix common VerifyBot setup and operation issues.
permalink: /troubleshooting/
---

## Troubleshooting

### Slash commands not showing

Checks:
1. Confirm bot has `Use Application Commands`.
2. Wait for Discord command propagation after invite/update.
3. Re-invite with correct scopes (`bot` + `applications.commands`).

### Bot cannot assign roles

Checks:
1. Bot has `Manage Roles`.
2. Target verification role is below bot role.
3. Role is allowlisted via `/addverifyrole`.

### Verification message not working

Checks:
1. Verify channel permissions (`View`, `Send`, `Embed Links`).
2. Confirm `/setreactionverify` targets correct channel/role/emoji.
3. Recreate verification message after role or emoji changes.

### Logs not posting

Checks:
1. Confirm `/setlogs` is configured.
2. Confirm bot can post in log channel.
3. If using webhooks, verify webhook URL and permissions.

### Role hierarchy problems

Symptoms:
- Verification command runs but role is not applied.

Fix:
1. Move VerifyBot role above the verification role.
2. Re-test with `/verify`.
3. Audit all role ordering in server settings.

## Still Stuck?

- Support server: <https://discord.gg/BusuZp2G8w>
- Include: command used, expected result, actual result, and screenshots of role order + channel permissions.
