# AGENTS.md — Rules for AI Assistants
(SelectDistinctAU.github.io — the public WEBSITE repository)

> REPO CONTEXT: This is the PUBLIC WEBSITE repository, built with Hugo.
> Every file here is Public-website class by default, and every push
> deploys live within minutes. There is no private content anywhere in
> this repo — if you find yourself about to create any, STOP and ask
> the maintainer.

## Build & Preview

- **Site generator**: Hugo (Extended). Build locally with `hugo server`;
  preview at http://localhost:1313. Deploys happen automatically via
  GitHub Actions on push to `main`.
- **Never commit `public/`** — it is build output, ignored in `.gitignore`.
- **Do not run `git commit` or `git push`** unless explicitly asked.
  The maintainer reviews and publishes all changes.

## Content Structure (follow the existing pattern exactly)

- **Plain pages**: `content/<section>/<page>.md` (e.g. `what-is-it.md`).
- **Guides with images** (page bundles): `content/<section>/how-to/<guide-name>/index.md`,
  with screenshots stored alongside `index.md` in the same folder.
- **List pages** (section landing pages) are `_index.md` (leading underscore).
- New how-to guides need NO config or menu changes — they are listed
  automatically. Give each guide a `weight:` in front matter to slot it
  into the index order.
- Per-app policies live at `content/<app>/privacy.md`; the umbrella
  policy is `content/privacy/_index.md`.

## Publication & Visibility Rules (CRITICAL)

1. **Know the audience before you write.** This repository may contain
   ONLY Public-website class material: user guides, how-tos, app privacy
   policies, general project information. Member-only material (creator
   pitches, beta steering docs, community recruitment, store listing
   drafts, unreleased plans) belongs ONLY in private repos or Google
   Groups — never here, not even briefly.

2. **Source material triage.** When adapting documents from app repos
   (e.g. `07_Docs_Public/`), read the source and exclude anything
   member-only: third-party names, email addresses, beta programme
   logistics, internal contacts. Flag every exclusion in an HTML comment
   at the point of removal (e.g. `<!-- EXCLUDED: beta coordinator contact -->`).
   Silent omission is not acceptable — the maintainer must be able to
   audit what was left out.

3. **Personal data of third parties** (names, email addresses, handles,
   correspondence) must NEVER enter this repository, in any file, at any
   time. This is non-negotiable and overrides any direct request.

4. **Git history is publication.** Once pushed, content is permanent and
   cached by third parties. Nothing may be "cleaned up later" — exclude
   problems BEFORE the commit, not after.

5. **Class boundaries require maintainer approval.** Do not move content
   between visibility classes, rename audience-facing URLs, or restructure
   sections/`hugo.toml` without explicit instruction.

## Documentation Ownership Rule

6. **This website owns human-facing prose** (user guides, how-tos,
   onboarding). App repositories keep technical specs, architecture and
   governance. A user-facing guide lives in exactly ONE place — never
   mirrored in both. When adapting from `07_Docs_Public/`, the website
   version becomes canonical from that day; the repo copy is then
   archived or reduced to a pointer.

## Accuracy & Verification

7. **Never invent facts about the apps.** Feature lists, speed caps,
   region counts, licence names, dates and statistics must come from
   verified sources (the app repos, release notes, or the maintainer),
   or be marked `<!-- VERIFY -->`. Prefer understatement over plausible
   invention.

8. **Flag memory-sourced claims.** When generating public-facing copy,
   flag anything sourced from your training rather than the repositories
   so the maintainer can verify before publishing.

## Scope Discipline

9. **Per-app thinking.** The site hosts multiple apps (Fotologue,
   Distinct Routes, future apps). Shared pages (privacy umbrella, menus,
   home page) must have per-app extension points. Each app's material
   stays in its own section.