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
also contains the development checks and build tools. Only the files in
`release.json`'s runtime allowlist enter an installation package.

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

Automated checks cover the count/rhythm helpers, evidence-status reporting, rule
declarations and release packaging. GitHub Actions runs the same entrypoint on
Windows and Linux; see the check results on each PR. The test inventory and its
limits are documented in [tests/COVERAGE.md](tests/COVERAGE.md).

Historical local checker replays retain their mixed statuses: 12 AUTO_PASS,
2 AUTO_FAIL for unmarked explanatory prose, and 3 requiring manual review.
Those private replies are not required by CI or included here. Automated checks
do not certify model behavior, real-score transcription, platform installation
or actual singer performance.

## Development

Use Python 3.10 or newer; these checks need only the standard library:

```sh
python -B -X utf8 tools/build_release.py --check
```

To test packaging without replacing the tracked download:

```sh
python -B -X utf8 tools/build_release.py --output-dir dist/preview
```

Both commands validate source and run the same tests once. CI uses an output
folder outside the checkout. This tooling migration leaves the v1.7.2 runtime,
download ZIP and checksum unchanged. See [CONTRIBUTING.md](CONTRIBUTING.md) for
the PR workflow, release exports and optional local-history checks.

## Working with ROSA

ROSA can assist with theological and contextual review of worship lyrics. This
skill focuses on translation, native Chinese craft and musical allocation. Install
each separately; a link between repositories does not automatically install or run
the companion skill.
