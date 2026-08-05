# SignUpBreeze Documentation

Source for the SignUpBreeze documentation site, published at
**[docs.signupbreeze.com](https://docs.signupbreeze.com)**.

SignUpBreeze helps organizers create events, coordinate shifts, and manage volunteer
signups — without making volunteers create an account. Learn more at
[signupbreeze.com](https://signupbreeze.com).

## What's here

| Path | Contents |
|------|----------|
| `getting-started/` | Introduction, key concepts, and quickstart |
| `organizers/` | Organizer Guide — events, shifts, signups, sharing |
| `volunteers/` | Volunteer Guide — signing up, magic links, registrations |
| `account/` | Account & Settings — profile, signing in, billing, notifications |
| `changelog.mdx` | Release notes |
| `images/` | Screenshots referenced by the pages |
| `docs.json` | Site configuration and navigation |

Pages are [MDX](https://mdxjs.com) with YAML frontmatter, built with
[Mintlify](https://mintlify.com).

## Preview locally

Install the Mintlify CLI, then run the dev server from the repository root:

```bash
npm i -g mint
```

```bash
mint dev
```

The site is served at `http://localhost:3000` and reloads as you edit.

Check for broken links before opening a pull request:

```bash
mint broken-links
```

## Contributing

Corrections and improvements are welcome — typos, unclear steps, missing detail, anything
that made the docs harder to use than they should be.

1. Open an [issue](https://github.com/SignUpBreeze/docs/issues) to discuss anything
   substantial, or go straight to a pull request for a small fix.
2. Edit the relevant `.mdx` file. Adding a new page? Add it to `navigation` in `docs.json`
   too, or it won't appear.
3. Read [`AGENTS.md`](AGENTS.md) first — it covers terminology, voice, and what must not be
   published. The screenshot rules in particular matter: never capture real names, real email
   addresses, or a local dev host.
4. Run `mint broken-links` and open the pull request.

Found a security or disclosure problem? Don't open a public issue — see
[`SECURITY.md`](SECURITY.md).

## License

Documentation content is licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See [`LICENSE.md`](LICENSE.md).

The SignUpBreeze name and logo are trademarks of SignUpBreeze and are not covered by that
license.
