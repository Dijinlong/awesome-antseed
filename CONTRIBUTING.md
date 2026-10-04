# Contributing to awesome-antseed

Thanks for considering a contribution. This list is meant to be *useful*, which
means it has to be honest about what works and what does not.

## What belongs here

- Tools that help someone run, observe, or debug an antseed node
- Guides that explain something non-obvious about the network
- Notes from production, especially failures that were hard to diagnose

## What does not

- Anything you have not actually tried. A link to a plausible-looking repo you
  have never run is worse than no link.
- Referral links, or anything where you benefit from the click.
- Projects that are abandoned. If the last commit is older than two years,
  leave it out unless it still works and you have verified that.

## Format

The list is generated from `data/projects.json`. Edit that file rather than
hand-editing the README, so the two cannot drift apart.

```json
{
  "name": "project-name",
  "url": "https://github.com/owner/repo",
  "description": "One sentence. What it does, not what it aspires to do.",
  "category": "tools",
  "status": "usable",
  "verified": "2026-10-04"
}
```

### Fields

| Field | Meaning |
|---|---|
| `name` | Repository or project name |
| `url` | Canonical link |
| `description` | One sentence, no marketing |
| `category` | `tools`, `guides`, or `notes` |
| `status` | `usable`, `early`, or `experimental` |
| `verified` | The date you last confirmed it works |

The `status` field matters. Marking something `usable` when it is actually
`early` costs someone an afternoon.

## Notes from production

These are the highest-value entries, because they are the hardest to find.
A good note:

- describes a symptom someone would actually search for
- explains the cause, not just the fix
- says how you know (a command, a log line, a field to look at)

Bad: "make sure your node is configured correctly."

Good: "the process stays healthy and the port stays open while advertising
pauses, so check `providers` in `/metadata` rather than the HTTP status."

## Review

A maintainer will check that:

1. the link works
2. the `status` claim is defensible
3. the description says what the thing does

If any of those cannot be confirmed, the entry gets a comment rather than a
merge. That is not personal -- it is the only way the list stays worth reading.
