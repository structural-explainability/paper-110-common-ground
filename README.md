# Referential Common Ground

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)

[![Build PDF](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/build-latex.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/build-latex.yml)
[![Check Links](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/links.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/links.yml)

[![ArXiv Prep](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/arxiv-prep.yml/badge.svg?branch=main)](https://github.com/structural-explainability/paper-110-common-ground/actions/workflows/arxiv-prep.yml)

> Characterizes conditions under which a bounded referential fragment
> remains compatible with interpretive frameworks,
> without requiring agreement on contested interpretations.

## Paper Overview

**Referential Common Ground**: Conditions for Compatibility
Between a Bounded Referential Fragment and Interpretive Frameworks

This paper investigates the Referential Common Ground assumption
underlying the Neutral Substrate design constraint.

It establishes conditions under which a satisfiable referential
fragment is compatible with a declared class of interpretive frameworks.

The results are developed in classical propositional logic
and checked in Lean 4.

## Main Contribution

The Neutral Substrate result establishes a sufficient condition
for semantic neutrality of a shared foundational layer,
provided its referential commitments are compatible
with every admissible interpretive framework.

Referential Common Ground is an assumption of that result.
This paper investigates when the assumption can be justified.

The paper establishes that admissibility alone does not guarantee
nontrivial common ground.
When admissibility imposes no restrictions beyond consistency,
only commitment sets satisfied by every valuation
are compatible with every admissible framework.

A stronger condition must therefore constrain frameworks.

The paper defines a framework as neutral on a vocabulary
when it permits every valuation of that vocabulary.

It establishes that:

- Compatibility with a theory over a vocabulary depends
  on the valuations that a framework permits on that vocabulary.
- A framework neutral on a vocabulary is compatible
  with every satisfiable theory over that vocabulary.
- Conversely, compatibility with every satisfiable theory
  over a vocabulary characterizes neutrality on that vocabulary.
- Every framework is either neutral on the vocabulary
  or conflicts with some satisfiable theory over it.
- A satisfiable framework whose propositions use only atoms
  outside the vocabulary is neutral on that vocabulary.

These results characterize a class of frameworks
without defining membership through agreement
with a particular referential fragment.

The mathematical ingredients are classical.
The contribution is their formulation as explicit conditions
for fragment-relative Referential Common Ground
in the Neutral Substrate setting.

## Scope

The results are conditional on the stated logical setting,
referential fragment, and framework class.

The formal development uses classical propositional logic.
Referential fragments are satisfiable, nontrivial,
and bounded by a finite vocabulary.

The results do not establish:

- Referential Common Ground for the full class
  of admissible interpretive frameworks.
- That a particular fragment's commitments
  are genuinely referential.
- Uniform compatibility with every satisfiable theory
  over a vocabulary for frameworks that are not neutral on it.
  Such frameworks may still be compatible with particular fragments.
- Corresponding results for first-order logic with equality
  or identity-bearing fragments.
- The scientific adequacy of a particular
  information-system realization.

A concrete realization must independently justify
its referential commitments and the applicable framework class.

## Basis

- [Lean basis summary](se110-lean-basis.md)
- Common Ground Lean 4 formalization:
  [se-theory-common-ground](https://github.com/structural-explainability/se-theory-common-ground)
- Upstream Neutral Substrate formalization:
  [se-theory-neutral-substrate](https://github.com/structural-explainability/se-theory-neutral-substrate)

The Common Ground formalization provides the concrete
propositional instance, vocabulary-interface results,
scope characterization, and independence results.

The Neutral Substrate theory supplies the abstract
consequence and framework systems on which this work builds.

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

The mathematical context includes Robinson's joint consistency
theorem, Craig interpolation, and conservative extensions
in ontology modularity.

The paper distinguishes these established logical results
from its formulation of fragment-relative
Referential Common Ground.

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
