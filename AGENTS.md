# Documentation project instructions

## About this project

- This is the source of the public SignUpBreeze documentation site, built on [Mintlify](https://mintlify.com) and published at [docs.signupbreeze.com](https://docs.signupbreeze.com)
- Pages are MDX files with YAML frontmatter
- Navigation and configuration live in `docs.json` — a new page is not visible until it is added there
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

**This repository is public.** Anything committed here — including git history — is
permanently visible to everyone. See `SECURITY.md` for how to report a disclosure problem.

## Terminology

- **Organization** — the account that owns events and billing. Use this in user-facing docs.
- **Team** — a group of people collaborating inside an organization. Not a synonym for
  organization. Earlier docs used the two interchangeably; they are distinct. Don't
  reintroduce "team" where "organization" is meant.
- **Event** — the thing an organizer creates. **Shift** — a slot within an event.
  **Registration** — a volunteer's signup for a shift.
- **Organizer** and **volunteer** are the two audiences; the Organizer Guide and Volunteer
  Guide are written for each.
- SignUpBreeze is **passwordless**. Never write about passwords, password resets, 2FA apps,
  TOTP, or recovery codes — none of these exist. Sign-in is a one-time emailed code, or
  Google or Apple. Volunteers use magic links and need no account at all.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

Document what the product *does*, never how its security is *implemented*.

**Do not publish:**

- Token or code formats, lengths, or entropy details
- Expiry windows and TTLs for sign-in codes or magic links — write "expires after a short
  time", never a specific number
- Rate limits, lockout thresholds, or retry counts
- Infrastructure details: internal hostnames, IPs, provider names, queue or database specifics
- Anything about admin-only or internal tooling

**Screenshots** are the most common way this leaks. Before adding one:

- Use seeded demo data. Never real names or real email addresses — including your own.
  A live address in a screenshot on a public site gets scraped.
- Capture from production or a staging host. Never a local dev domain such as `*.test` or
  `localhost` — check the URL bar, share links, and any QR code, which encodes the URL too.
- Check the whole frame, not just the subject: account menus, breadcrumbs, sidebars, and
  notification badges all carry identifying detail.
- Save as `.webp` in `images/`, reference as `/images/<name>.webp`, and always write
  descriptive `alt` text.
