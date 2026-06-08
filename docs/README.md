# Message Inbox

A local-first Mac tool for measuring and improving text responsiveness from iMessage exports.

## What it does
- identifies 1:1 personal conversations waiting on you
- filters spam, group chats, and automated logistics texts
- computes a responsiveness score and history
- helps users stay on top of replies

## How it works
1. Run the local Mac export script to generate JSON from iMessage data
2. Open the local web app and load the exported JSON
3. Review the action list, score, and trends

## Run the export (new users)
The export script reads your iMessage history on your own Mac and writes a
`miranda2_messages.json` file to your Desktop. The easiest way to run it is to
paste this single line into the **Terminal** app and press Return:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/skbrownvibing/ReplyorDie/MAIN/export.command)"
```

This downloads the script straight from GitHub and runs it in memory — nothing
is saved to disk, so you never hit the macOS "permission denied" or
"unidentified developer" warnings that come from double-clicking a downloaded
`.command` file.

**Before running, give Terminal permission to read Messages** (a one-time step):
1. Open **System Settings → Privacy & Security → Full Disk Access**
2. Turn on the switch for **Terminal**
3. Run the line above

When it finishes you'll have `miranda2_messages.json` on your Desktop — open the
web app and drag that file onto the page.

> Note: the one-liner generates the export only. The optional auto-refresh
> "Refresh button" helper requires the full project folder on disk and is meant
> for repeat/local use, not first-time setup.

## Docs
- Product spec: `docs/prd.md`
- Change history: `CHANGELOG.md`
- Agent instructions: `AGENTS.md`

## Current status
Early-stage learning project. Product logic and UX are evolving quickly.
