---
title: Git commands worth keeping
aliases: [Git reference]
tags: [git, reference, sample]
---
# Git commands worth keeping

A small personal reference for inspecting a notebook repository. These commands read local Git state; they do not publish changes.

## Where am I?

```sh
git branch --show-current
git status --short
```

The first command names the current branch. The second gives a compact view of changed and untracked files.

## What changed?

```sh
git diff --stat
git diff -- "Engineering/Keep a useful offline copy.md"
```

The first command summarizes tracked, unstaged changes. The second shows those changes for one note. Neither includes untracked files. Use `git diff --cached` for staged changes. ^changed

## When did we last touch this note?

```sh
git log -5 --oneline -- "Engineering/Keep a useful offline copy.md"
```

Read the recent history of a decision before revisiting it. The rationale itself lives in [[Engineering/Keep a useful offline copy]].

## The one to remember

When a command contains spaces in a filename, quote the entire path. Keep `--` between options and paths so Git can tell them apart.

[Back to the sample notebook](../README.md)
