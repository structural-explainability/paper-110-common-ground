# Changelog

<!-- markdownlint-disable MD024 -->

All notable changes to this project will be documented in this file.

The format is based on **[Keep a Changelog](https://keepachangelog.com/en/1.1.0/)**
and this project adheres to **[Semantic Versioning](https://semver.org/spec/v2.0.0.html)**.

---

## [Unreleased]

### Planned

Contestability Clarification - explain why neither
the absence of demonstrated framework variance
nor membership in the undetermined middle
establishes foundational permissibility.

Fixes (after football): Paper 110's metadata still identifies Paper 100.
Its README title, overview, arXiv badge, DOI, and main contribution are copied from Neutral Substrates.
CITATION.cff also identifies the Paper 100 title and DOI,
while SE_MANIFEST.toml still describes Paper 100's neutrality result.
The changelog even instructs replacing arXiv submission 2601.14271.

---

## [0.1.0] - 2026-10-25

### Added

---

## Notes on versioning and releases

- We use **SemVer**:
  - **MAJOR** - breaking changes to the meaning, assumptions, or conclusions
    of existing paper items, or removal or renaming of their identifiers
  - **MINOR** - backward-compatible additions
  - **PATCH** - fixes, documentation, tooling
- Versions are driven by git tags. Tag `vX.Y.Z` to release.

## Release Procedure (Required)

Follow these steps exactly when creating a new release.

### Task 1. Update release metadata (manual edits)

1.1. CITATION.cff: update version and date-released
1.2. CHANGELOG.md: add section, move unreleased entries, update links, update release command

### Task 2. Set up and Validate

```shell
# Update GitHub Actions and pin all action references to immutable SHAs.
uvx gha-tools autoupdate --pin=all --write .github/workflows

# Audit the resulting GitHub configuration for security findings.
uvx zizmor@latest .github/
# some suppressed is still okay

# Validate.
uvx cffconvert --validate
uvx se-manifest-schema validate-manifest --strict

# Format Markdown.
npx markdownlint-cli2 --fix

# Build and inspect
latexmk -pdf se110-common-ground.tex
.\tools\build\build.ps1

texcount -inc -sum -total se110-common-ground.tex
.\basis.ps1
```

Review all generated and modified files before committing.

### Task 3. Commit and Push

```shell
git add -A
git commit -m "Prep X.Y.Z"
git push -u origin main
```

Verify that all required GitHub Actions complete successfully.

### Task 4. Prepare and submit to arXiv

1. As Needed: Run the **Prepare arXiv Source** workflow manually.
2. As Needed: Download `arxiv-source.zip` and the compiled PDF artifact; check the PDF.
3. Replace the existing arXiv submission (2601.14271) with the new source.
4. Update the arXiv abstract field to match the paper's abstract.
5. Summarize the change in the arXiv Comments field.

Verify the updated arxiv step BEFORE tagging.

### Task 5. Tag and Push the Release

After the required GitHub Actions succeed:

```shell
git tag vX.Y.Z -m "X.Y.Z"
git push origin vX.Y.Z
```

After it succeeds, for a major revision, create a release:

```shell
gh release create v0.1.0 --verify-tag --title "v0.1.0" --generate-notes
```

## Only As Needed (delete a tag)

```shell
git tag -d vX.Z.Y
git push origin :refs/tags/vX.Z.Y
```

## Links

[Unreleased]: https://github.com/structural-explainability/paper-110-common-ground/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/structural-explainability/paper-110-common-ground/releases/tag/v0.1.0
