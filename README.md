# Singable Lyric Translator

Translate English lyrics into natural, singable Chinese while preserving meaning,
repeated hooks and song structure. A companion project to
[ROSA](https://github.com/subverse-rosa/rosa-skill), also usable independently.

## Package

- Version: **1.7.2**, packaged 2026-10-23.
- [Download package](singable-lyric-translator_latest.zip)
- [SHA-256 checksum](SHA256.txt)
- [Read the skill instructions](skill/SKILL.md)

The ZIP is the original supplied release, unchanged. The eight files under
`skill/` are exact readable copies of its contents for review. This repository
contains the packaged runtime; the development master and its tests are maintained
separately.

## Install

For a host that supports this ZIP layout, upload the complete ZIP. For file-based
installation, create a folder named `singable-lyric-translator` and extract all ZIP
contents into it, keeping `SKILL.md`, `references/` and `scripts/` together. Follow
your host's installation procedure; platform acceptance has not been verified here.

On Windows, check the downloaded ZIP with:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath .\singable-lyric-translator_latest.zip
```

Compare the result with `SHA256.txt`. GitHub's automatic Source code archive is a
repository snapshot; use the named package above for installation.

## Workflow and evidence

Adaptive analysis is the default when rhythm evidence is available. Proposed
rhythmic reallocations require explicit user approval before adoption. Deep Review
is on demand; ordinary review targets material improvements.

The local master's 55 automated regression tests and source checks passed before
this upload. Package bytes, the eight-file allowlist and source/manifest hashes
were checked. Historical checker replays retain their explicit mixed statuses:
12 AUTO_PASS, 2 AUTO_FAIL for unmarked explanatory prose, and 3 requiring manual
review. These checks do not certify model behavior, real-score transcription,
platform installation or actual singer performance.

## Working with ROSA

ROSA can assist with theological and contextual review of worship lyrics. This
skill focuses on translation, native Chinese craft and musical allocation. Install
each separately; a link between repositories does not automatically install or run
the companion skill.
