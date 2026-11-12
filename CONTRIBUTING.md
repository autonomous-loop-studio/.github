# Contributing

This is the organization-wide default. A repository that has its own `CONTRIBUTING.md` takes
precedence — for the app, read
[Autonomous/CONTRIBUTING.md](https://github.com/autonomous-loop-studio/Autonomous/blob/master/CONTRIBUTING.md).

Thanks for looking. Bug reports and pull requests are both welcome.

## The quick version

- **Open an issue before a large change**, so the same thing does not get built twice.
- **Keep the project's constraint.** The app stays plain PHP: no build step, no runtime
  dependency install, no `composer.json` at runtime, no `package.json` for the app. Node is only
  ever needed to run the JavaScript tests.
- **Run the suite** — `node tests/run.mjs` (PHP first, then JavaScript). A change that touches
  the sandbox, the guards, the harness, the routing engine or the update installer should come
  with a test. A suite that cannot run fails the command rather than passing quietly.
- **Match the surrounding style.** Comments say *why*, not *what*. New code should read like the
  code next to it.
- **Do not add a dependency the host has to install.** If a feature needs a library, it goes in
  the tree or it does not go in.

## Licensing and sign-off

Contributions are accepted under the project's license, **Apache-2.0**. By contributing you
certify the Developer Certificate of Origin 1.1 and agree the work is licensed under Apache-2.0.

Add a sign-off to each commit:

```bash
git commit -s -m "your message"
```

which appends:

```
Signed-off-by: Your Name <you@example.com>
```

### Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.

## What happens after you open a pull request

It gets read, and it gets run — the suite and, for guard changes, the failure case it claims to
fix. Small, focused pull requests land quickly. A large one is easier to accept when it comes
with an issue explaining the problem first.
