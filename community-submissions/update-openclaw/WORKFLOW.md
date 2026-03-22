---
name: update-openclaw
emoji: 🔄
description: Daily self-update of OpenClaw — pull latest version and restart.
author: davehappyminion @davehappyminion
schedule: "3am"
---

# Update OpenClaw

Run the OpenClaw self-update process daily.

## 1. Record Current Version

Before updating, check the current version:
```
openclaw --version
```
Save this so you can compare after the update.

## 2. Run Update

Use the OpenClaw CLI to update:

```
openclaw update --yes --no-restart
```

This handles git or npm updates automatically, installs deps, and restarts the gateway.

## 3. Check New Version & Changelog

After restart, check the new version:
```
openclaw --version
```

Then look up what changed between the old and new versions:
- Check the changelog at https://docs.openclaw.ai/changelog or https://github.com/openclaw/openclaw/releases
- Summarize the key changes (new features, bug fixes, breaking changes)

## 4. Notify with Summary

Send a short message to the user with:
- **Old version** → **New version**
- **Key changes** (2-3 bullet points of what's new)
- **Link** to the full changelog/release notes for more details

If there was no update (already on latest), just stay quiet — don't notify.
