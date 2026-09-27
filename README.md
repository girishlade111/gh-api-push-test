# gh-api-push-test

A scratch repository used to test the `gh-api push` workflow — pushing code to GitHub
via the Git Data API (blobs → tree → commit → ref update) from an environment where
SSH and authenticated git-over-HTTPS are blocked.

## Purpose

This repo exists only as a disposable test target for the `github` skill's `gh-api`
CLI (`~/workspace/skills/github/bin/gh-api`). It validates that:

- commits can be created through the Git Data API,
- refs can be updated (non-force) on top of the current remote HEAD,
- small fixture files (`README.md`, `hello.txt`) round-trip correctly.

## Contents

- `README.md` — this file
- `hello.txt` — fixture content used in push tests

## Usage

The repo is not a product, library, or website — there is nothing to install, run,
or deploy. It is referenced by the `gh-api push` tests as the destination repository.

Example from the skill:

```bash
gh-api push ./my-project girishlade111/gh-api-push-test main "test: push via gh-api data api"
```

## Deployment

Not applicable — this is a test/scratch repo with no website. No homepage is set.

---

Built by Girish Lade · https://ladestack.in
