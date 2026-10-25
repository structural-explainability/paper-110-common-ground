# Neutral Substrates

<!-- CUSTOM: arXiv badge is static by design to avoid Shields/arXiv API lag and cache failures -->

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)
[![arXiv](https://img.shields.io/badge/arXiv-2601.14271-b31b1b.svg)](https://arxiv.org/abs/2601.14271)

[![Build PDF](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/build-latex.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/build-latex.yml)
[![Check Links](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/links.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/links.yml)

[![ArXiv Prep](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/arxiv-prep.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/arxiv-prep.yml)
[![DOI](https://img.shields.io/badge/DOI-10.48550/arXiv.2601.14271-blue)](https://doi.org/10.48550/arXiv.2601.14271)

> Defines neutral substrates that preserve shared reference
> without adopting contested interpretations.

## Paper Overview

Neutral Substrates: A Design Constraint for Shared Records
Under Persistent Interpretive Disagreement

- [arXiv](https://arxiv.org/abs/2601.14271)
- [SciX](https://scixplorer.org/abs/2026arXiv260114271C/abstract)

## Main Contribution

This paper addresses a practical problem in shared records
where parties persistently disagree about interpretation.

Simply omitting contested information can undermine accountability,
because records should preserve what parties claim
along with the provenance of those claims.
But adopting one contested interpretation as the shared foundation
can compromise neutrality.

The paper establishes a sufficient condition for semantic neutrality.
If the shared referential commitments, taken as a whole,
are compatible with every admissible framework,
then limiting the foundation to those commitments
and to attribution statements grounded in them
is enough to preserve neutrality.

Contested causal and normative claims can still be represented
as attributed assertions tied to an identified framework,
source, agent, or record.
The shared system records who asserted what, with provenance,
without endorsing the asserted claim.

Guaranteeing neutrality by design requires additional justification.
The paper establishes one sufficient approach to semantic neutrality,
not the only possible way to build a neutral system.

## Scope

The result does not apply when the shared referential information,
or the basis for attributing claims to sources,
conflicts with an admissible framework.
Disagreement about interpretation alone does not trigger this.

## Basis

- [Lean basis summary](se110-lean-basis.md)
- Lean 4 formalization:
  [se-theory-neutral-substrate](https://github.com/structural-explainability/se-theory-neutral-substrate)

## Building Locally

- On Windows, install Strawberry Perl and MiKTeX.

<!--
On Windows (MiKTeX):

- Download from <https://miktex.org/download>.
- Suggested options during installation:
  - Install for current user only
  - Leave paper size at A4 (default is fine)
  - Install missing packages on the fly = Yes
  - Add MiKTeX to PATH = Yes
-->

Requires a LaTeX distribution with `latexmk` (MiKTeX, TeX Live, or MacTeX):

```bash
latexmk -pdf se110-common-ground.tex

texcount -inc -sum -total se110-common-ground.tex
```

Windows:

```pwsh
# build
.\tools\build\build.ps1

# update ps1 as needed and calculate the basis (defs, etc.)
.\basis.ps1
```

Validate with:

```shell
uvx cffconvert --validate
uvx se-manifest-schema validate-manifest --strict
```

## References

1. Case, D. M. (2026).
   "Neutral substrates: A design constraint for shared records under persistent
   interpretive disagreement."
   Preprint.
   <https://arxiv.org/abs/2601.14271>

1. Craig, W. (1957).
   "Three uses of the Herbrand–Gentzen theorem in relating model theory and
   proof theory."
   _The Journal of Symbolic Logic_, 22(3):269–285.
   <https://doi.org/10.2307/2963594>
   <https://en.wikipedia.org/wiki/Craig_interpolation>

1. Cuenca Grau, B., Horrocks, I., Kazakov, Y., and Sattler, U. (2008).
   "Modular reuse of ontologies: Theory and practice."
   _Journal of Artificial Intelligence Research_, 31:273–318.
   <https://doi.org/10.1613/jair.2375>

1. Robinson, A. (1956).
   "A result on consistency and its application to the theory of definition."
   _Koninklijke Nederlandse Akademie van Wetenschappen, Proceedings, Series A_,
   59:47–58; also _Indagationes Mathematicae_, 18:47–58.
   <https://en.wikipedia.org/wiki/Robinson%27s_joint_consistency_theorem>

## Related and Adjacent Work

Selected papers from the
[Harvard SciX similar-papers search](https://ui.adsabs.harvard.edu/abs/2026arXiv260114271C/similar)
for _Common Ground_.

## Annotations

[Annotations](./.annotations/annotations.md)

## Changelog

[CHANGELOG.md](./CHANGELOG.md)

## Citation

[CITATION.cff](./CITATION.cff)

## License

[CC BY 4.0](./LICENSE)

## Repository Manifest

[SE_MANIFEST.toml](./SE_MANIFEST.toml)
