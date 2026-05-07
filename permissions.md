---
layout: default
title: Permissions
description: Required permissions for VerifyBot and why they are needed.
permalink: /permissions/
---

## Permission Model

VerifyBot needs specific Discord permissions to execute verification and logging safely.

## Core Permissions Explained

### Manage Roles

Required for assigning/removing verification roles.

If missing:
- `/verify` and reaction verification cannot update member roles.

### View Channels

Required to read configured verify/log channels and command context.

If missing:
- Slash command behavior appears inconsistent due to inaccessible channels.

### Send Messages

Required to post verification responses and status output.

If missing:
- Verification commands may execute partially without user-visible confirmation.

### Embed Links

Required for rich logs/status messages where embeds are used.

If missing:
- Logs may fail or degrade to plain output.

### Read Message History

Required for some verification or moderation context checks.

If missing:
- Historical context checks can fail or return incomplete results.

### Use Application Commands

Required for slash commands (`/verify`, `/setlogs`, etc.).

If missing:
- Commands are unavailable to users in affected channels.

### Manage Webhooks (Optional)

Required only if webhook logging is used.

If missing:
- Channel logging can still work, webhook mode will not.

## Role Hierarchy Requirement

Discord role hierarchy overrides permissions. Even with `Manage Roles`, the bot cannot assign roles above its own top role.

Best practice:
- Place VerifyBot role above all roles it needs to assign.
- Do not place it above owner or highest staff roles unless necessary.
