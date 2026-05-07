---
layout: default
title: Commands
description: Command reference for VerifyBot verification and trust workflows.
permalink: /commands/
---

## Command Reference

| Command | Description | Required Permission | Example Usage |
| --- | --- | --- | --- |
| `/verify` | Manually verifies a user with an approved verification role. | Manage Roles | `/verify @member role:Verified` |
| `/setreactionverify` | Creates reaction-based verification in a target channel with role + emoji. | Manage Channels, Manage Roles | `/setreactionverify channel:#verify role:Verified emoji:✅` |
| `/addverifyrole` | Adds a role to the verification role allowlist. | Manage Roles | `/addverifyrole role:Verified` |
| `/removeverifyrole` | Removes a role from the allowlist. | Manage Roles | `/removeverifyrole role:Verified` |
| `/listverifyroles` | Lists allowed verification roles. | Manage Roles | `/listverifyroles` |
| `/setlogs` | Configures logging channel or webhook target. | Manage Channels (or webhook permission) | `/setlogs channel:#verify-logs` |
| `/check` | Runs a verification status check for a user. | Moderate Members | `/check @member` |
| `/crosscheck` | Checks whether a user is recognized in linked trust contexts. | Moderate Members | `/crosscheck @member` |
| `/bancheck` | Checks ban/verification trust state for moderation review. | Ban Members | `/bancheck @member` |
| `/fullscan` | Runs a broader scan to reconcile verification state and logs. | Administrator | `/fullscan` |
| `/stats` | Displays verification statistics. | View Channels | `/stats` |
| `/help` | Shows help categories and quick navigation. | View Channels | `/help` |
| `/support` | Returns support resources. | View Channels | `/support` |

> Command availability can vary by deployment and access scope.
