# B.A.B.I

**Beyond AI, Build for Individuals.**

B.A.B.I is a desktop assistant for Windows that works on your own machine: it
sees your projects, reads and writes your files, runs commands, watches your
screen, listens and answers out loud. It runs on **your** Claude account — you
sign in, and every answer it gives is your own subscription at work. This repo
holds the installer and nothing else; the app's brain and memory live in your
account, not here.

## Download

Latest installer:

> **https://github.com/motta22/babi-releases/releases/latest**
>
> Download `BABI-Setup-<version>.exe` — for example `BABI-Setup-1.0.0.exe`.

Nothing else on that page is needed. `latest.yml` and the `.blockmap` files are
there so the app can update itself later.

## Windows will warn you. Here is exactly what to click.

The installer is **not code-signed** yet, so Windows SmartScreen stops it the
first time. This is expected and we would rather say so than hide it.

1. Run `BABI-Setup-<version>.exe`.
2. A blue window appears: **"Windows protected your PC"**.
3. Click **More info** — the small link, under the message.
4. A line appears naming the app and "Unknown publisher".
5. Click **Run anyway**.

If your browser blocks the download first, open the downloads list, find the
file, and choose **Keep** (Edge may ask twice: **Keep anyway**).

Your antivirus may also look hard at it. B.A.B.I types, clicks and takes
screenshots, which is what you installed it for, and which is also what malware
does. If you are not comfortable with an unsigned installer, do not install it.

## What you need

- **Windows 10 or 11, 64-bit.** No macOS, no Linux, English only.
- **A Claude account** (claude.ai), and the Claude desktop app. B.A.B.I uses
  your account for everything it thinks; there is no account from us.
- **About 15 minutes.** The installer is the quick part. The app then walks you
  through the rest out loud: dependencies, your Claude account, publishing your
  own Command Center, your projects, the voice, the ears.
- **About 1 GB of disk**, including the ~330 MB of speech models the app
  downloads on the first run. You can skip the models and use the Windows voice.

Nothing needs administrator rights. The app installs for your user only.

## What it does to your PC, honestly

B.A.B.I installs itself under your user profile and creates a folder at
`%USERPROFILE%\Dev\BABI` for its own files; your projects stay where they are
and are never moved. With your permission it can read, write and delete files,
run commands, install the tools it needs through `winget` (Python, Git, and Node
only if you ask for the agent features), click and type in any window, and take
screenshots to answer questions about what is on screen. Everything it does sits
behind three permission tiers that it explains before the first action: the safe
things happen quietly, the risky things ask you out loud and wait, and the
dangerous things it refuses and tells you how to do yourself. It talks to
Anthropic through your own Claude account and to GitHub to check for updates, and
to nothing else — no data is sent to the author or to any server of ours, there
is no telemetry, and there never will be without being asked first, in plain
words, off by default. Every answer, screenshot read and agent run spends **your**
Claude subscription usage. Uninstalling removes the app and leaves your projects
completely alone.

## Updates

The app updates itself, like Windows does. Most updates install quietly when you
quit. An important one asks and counts down. A rare one stops and updates
immediately, and says so before it does.

One part cannot be pushed: your Command Center page lives in your Claude account,
so when a new version needs a new page, B.A.B.I tells you and gives you the one
line to paste that republishes it. It checks by itself and clears the notice when
you are done.

## Something broke

Open an issue: **https://github.com/motta22/babi-releases/issues**

Please include:

- what you were doing, and what happened instead;
- the version, from the app's header or `%USERPROFILE%\Dev\BABI\VERSION`;
- the diagnostics bundle — **Send diagnostics** in the SETUP panel puts a zip on
  your Desktop with the log, the self-test result and your settings, with your
  artifact URL removed. Nothing is uploaded anywhere; you attach it yourself, or
  not.

This is a small project shared with friends and testers. There is no support
commitment, no warranty, and answers come when they come.
