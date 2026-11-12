# Organization profile and shared files

This repository is not the app. It holds the files GitHub reads across the
**Autonomous Loop Studio** organization.

| file | what it does |
|---|---|
| [`profile/README.md`](profile/README.md) | Renders on [github.com/autonomous-loop-studio](https://github.com/autonomous-loop-studio) — the first thing a visitor reads |
| [`SECURITY.md`](SECURITY.md) | The vulnerability-reporting policy, inherited by every repository in the organization that does not define its own |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | The default contribution guide, inherited the same way |

Nothing here ships in a release and nothing here is served to anyone using the app.
It exists so the organization page has content and so a new repository starts with
the right rules instead of none.

## The app

**[Autonomous](https://github.com/autonomous-loop-studio/Autonomous)** — a self-hosted
AI agent console in plain PHP. No Docker, no Node, no build step, no account.
[Landing page](https://autonomous-loop-studio.github.io/Autonomous/) ·
[Releases](https://github.com/autonomous-loop-studio/Autonomous/releases) ·
[Roadmap](https://github.com/autonomous-loop-studio/Autonomous/discussions/1)

## Changing the organization page

Edit `profile/README.md` and push to `main`. The page updates within a minute or two;
GitHub caches the render briefly, so a hard refresh may be needed. Images are linked by
absolute URL from the app repository's `screenshots/` folder, so they never need copying
here.

Repository settings that live on the web and cannot be set from this folder: the avatar,
the display name, the website link, pinned repositories, and the public email.
