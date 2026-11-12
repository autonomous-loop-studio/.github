# Security policy

## Reporting a vulnerability

**Please do not open a public issue for a security problem.**

Use GitHub's private reporting instead: open the repository's **Security** tab and choose
**Report a vulnerability**. That starts a private advisory that only you and the maintainer
can read, and it keeps the details out of the public issue tracker until a fix exists.

A useful report includes:

- the version (`VERSION` in the app folder) and how it is being served — `php -S`, Apache or nginx
- what an attacker controls: a prompt, a provider response, a page an agent reads, a URL, a file
- the exact request or tool call, and what it did that it should not have
- what you expected instead, and why you think the current behaviour is a flaw

You will get an answer as soon as possible. This is a single-maintainer project, so there is
no guaranteed response time; a clear, reproducible report is answered fastest.

## Supported versions

The latest release only. The project develops on one track and does not backport fixes to older
versions — if you are behind, `Config → Updates` updates in place and keeps `storage/`.

## What this project already assumes

Some behaviour that looks alarming is deliberate, and is worth knowing before you write a report:

- **Every capability that can touch your machine is off until you switch it on** — `exec`,
  `run_code`, the browser and MCP. Off means the tool is not offered to the model at all.
- **`exec` takes an argv array, never a shell string**, and runs only allowlisted binaries.
- **File tools are confined to a jail** (`sandbox/` by default), and every write asks for approval.
- **A token is required to use the app at all.** A fresh copy refuses to serve (503) until a
  token exists, so an exposed install is not an unauthenticated one.
- **The app refuses to serve `storage/` and `tests/`** — under `serve.php`, the shipped Apache
  `.htaccess` and the shipped nginx rules.
- **No telemetry, no phone-home, no account.** Nothing about your use leaves the host.

Two things are documented as expected, not bugs:

- **Turning everything on and auto-approving writes** with the jail pointed at the filesystem
  root gives a language model a very capable shell. That is the operator's choice and the docs
  say so plainly.
- **A provider seeing your prompts.** Any hosted model you point the app at receives the
  conversation; that is what a hosted model is. Use a local model if that matters.

## Scope

In scope: the PHP application, the shipped server configs, the update installer, the token and
session handling, the sandbox and tool guards, and anything that lets a model or a web page an
agent reads reach past those guards.

Out of scope: vulnerabilities in a model provider's service, in PHP itself, or in third-party
tools you install and enable yourself; and anything that requires the operator to have already
handed over control of the machine.
