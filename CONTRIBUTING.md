# Contributing to the Prompt Shields documentation

This repository is the source for [docs.promptshields.com](https://docs.promptshields.com).
It contains prose, not product code.

## Before you start

Open an issue first for anything larger than a correction. Documentation
structure is deliberate, and a restructure is worth agreeing before it is
written.

## Development setup

No build step and no dependencies beyond Node.js 18 or later.

```bash
npx mint@latest dev
```

## Checks that must pass

```bash
npx mint@latest broken-links
```

A pull request that adds a link must leave this passing.

## House rules

These are not style preferences. They exist because this documentation is read
by people deciding whether to deploy a security control across a fleet.

- **Never document prompt content flowing anywhere.** It does not, and the
  documentation must not imply otherwise.
- **Mark unreleased integrations *Planned* or *In development*.** Roadmap work
  is never described as shipped.
- **Where the documentation and a client disagree, the client is authoritative**
  and the page is a bug. Fix the page rather than arguing from it.
- **State limits explicitly.** A page that describes only what a control does,
  and never what it does not, is not usable by a security reader.

## Coding conventions

Match the surrounding code. Comment density, naming, and idiom should be
indistinguishable from what is already there. A change that reads as though it
were written by a different person is harder to review, whatever its merits.

## Never commit

- Live credentials, API keys, tokens, or connection strings with real passwords
- Customer data, real prompt text, or anything that identifies a person
- Generated artefacts, build output, or editor and OS scratch files
- Roadmap phases, customer names, pricing strategy, or other internal material.
  This repository is public.

If you believe a credential has been committed, email
**security@promptshields.com** immediately rather than opening a pull request
that removes it — a public commit that deletes a secret advertises the secret.

## Pull requests

- One logical change per pull request.
- Say what you changed and why. If you fixed a defect, say how you reproduced it.
- State what you verified, and how. "Tests pass" is only useful if you ran them.
- If a claim in the README stops being true because of your change, update the
  README in the same pull request.

By contributing you agree that your contributions are licensed under the same
terms as this repository, and you confirm you have the right to grant that
licence.

## Conduct

Participation is governed by [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
Vulnerabilities go to [SECURITY.md](SECURITY.md), never to a public issue.
