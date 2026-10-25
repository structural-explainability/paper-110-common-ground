# SE-110 Lean Formalization Basis

> Exact labeled mathematical environments extracted from the authoritative Paper 110 LaTeX source.

- Source: `se110-common-ground.tex`
- Extracted: 2026-10-25T13:49:09-05:00
- Labeled items: 13

Each item contains the exact LaTeX environment from its opening `\begin{...}` through its matching `\end{...}`.

The items remain in paper order. No mathematical text inside an extracted environment has been rewritten.

## Summary

| Kind | Count |
| --- | ---: |
| definition | 5 |
| proposition | 7 |
| example | 1 |

## Paper-Order Index

| # | Paper ID | Kind | Title | Source lines |
| ---: | --- | --- | --- | ---: |
| 1 | `se110.proposition.SatisfiableUnionOfDisjoint` | proposition | Joint Consistency over Disjoint Vocabularies | 401-406 |
| 2 | `se110.def.ReferentialFragment` | definition | Referential Fragment | 416-425 |
| 3 | `se110.proposition.CompatibleBareIffValid` | proposition | Bare Compatibility | 453-458 |
| 4 | `se110.def.Permits` | definition | Interface Permission | 494-498 |
| 5 | `se110.proposition.SatisfiableUnionIffPermits` | proposition | Compatibility Reduces to the Interface | 505-510 |
| 6 | `se110.def.NeutralOn` | definition | Neutral on a Vocabulary | 522-526 |
| 7 | `se110.def.AvoidsVocabulary` | definition | Avoiding a Vocabulary | 532-536 |
| 8 | `se110.proposition.NeutralOnOfAvoids` | proposition | Avoidance Gives Neutrality | 538-541 |
| 9 | `se110.proposition.NeutralOnIffCompatible` | proposition | Neutrality Characterization | 562-566 |
| 10 | `se110.proposition.Dichotomy` | proposition | Scope Dichotomy | 586-591 |
| 11 | `se110.def.FragmentCommonGround` | definition | Fragment-Relative Common Ground | 610-615 |
| 12 | `se110.proposition.FragmentCommonGroundOfNeutral` | proposition | Common Ground from Neutrality | 623-628 |
| 13 | `se110.example.DecisionRecord` | example | Decision Record | 656-668 |

## Extracted Basis

## 01. `se110.proposition.SatisfiableUnionOfDisjoint` — Joint Consistency over Disjoint Vocabularies

- Kind: `proposition`
- Source lines: `401-406`

```latex
\begin{proposition}[Joint Consistency over Disjoint Vocabularies]
  \label{se110.proposition.SatisfiableUnionOfDisjoint}
  Let $T$ lie in $V$ and $U$ lie in $W$, where $V$ and $W$ have no atom in
  common.
  If $T$ and $U$ are each satisfiable, then $T \cup U$ is satisfiable.
\end{proposition}
```

## 02. `se110.def.ReferentialFragment` — Referential Fragment

- Kind: `definition`
- Source lines: `416-425`

```latex
\begin{definition}[Referential Fragment]
  \label{se110.def.ReferentialFragment}
  A \emph{referential fragment} is a vocabulary $V$ together with a theory $R$
  lying in $V$ such that
  \begin{enumerate}
    \item $R$ is satisfiable;
    \item $R$ is nontrivial: some valuation does not satisfy $R$; and
    \item $V$ is bounded: it is contained in a finite set of atoms.
  \end{enumerate}
\end{definition}
```

## 03. `se110.proposition.CompatibleBareIffValid` — Bare Compatibility

- Kind: `proposition`
- Source lines: `453-458`

```latex
\begin{proposition}[Bare Compatibility]
  \label{se110.proposition.CompatibleBareIffValid}
  In the bare setting, a commitment set $T$ is framework-compatible if and only
  if every valuation satisfies $T$.
  Consequently no referential fragment is framework-compatible.
\end{proposition}
```

## 04. `se110.def.Permits` — Interface Permission

- Kind: `definition`
- Source lines: `494-498`

```latex
\begin{definition}[Interface Permission]
  \label{se110.def.Permits}
  A framework $\Framework$ \emph{permits} a valuation $u$ on $V$ when some
  valuation satisfying $\Framework$ agrees with $u$ on every atom of $V$.
\end{definition}
```

## 05. `se110.proposition.SatisfiableUnionIffPermits` — Compatibility Reduces to the Interface

- Kind: `proposition`
- Source lines: `505-510`

```latex
\begin{proposition}[Compatibility Reduces to the Interface]
  \label{se110.proposition.SatisfiableUnionIffPermits}
  Let $R$ lie in $V$.
  Then $R \cup \Framework$ is satisfiable if and only if $\Framework$ permits
  some valuation that satisfies $R$.
\end{proposition}
```

## 06. `se110.def.NeutralOn` — Neutral on a Vocabulary

- Kind: `definition`
- Source lines: `522-526`

```latex
\begin{definition}[Neutral on a Vocabulary]
  \label{se110.def.NeutralOn}
  A framework $\Framework$ is \emph{neutral on} $V$ when it permits every
  valuation of $V$.
\end{definition}
```

## 07. `se110.def.AvoidsVocabulary` — Avoiding a Vocabulary

- Kind: `definition`
- Source lines: `532-536`

```latex
\begin{definition}[Avoiding a Vocabulary]
  \label{se110.def.AvoidsVocabulary}
  A framework $\Framework$ \emph{avoids} $V$ when it lies in some vocabulary
  $W$ with no atom in common with $V$.
\end{definition}
```

## 08. `se110.proposition.NeutralOnOfAvoids` — Avoidance Gives Neutrality

- Kind: `proposition`
- Source lines: `538-541`

```latex
\begin{proposition}[Avoidance Gives Neutrality]
  \label{se110.proposition.NeutralOnOfAvoids}
  A satisfiable framework that avoids $V$ is neutral on $V$.
\end{proposition}
```

## 09. `se110.proposition.NeutralOnIffCompatible` — Neutrality Characterization

- Kind: `proposition`
- Source lines: `562-566`

```latex
\begin{proposition}[Neutrality Characterization]
  \label{se110.proposition.NeutralOnIffCompatible}
  A framework $\Framework$ is neutral on $V$ if and only if $R \cup \Framework$
  is satisfiable for every satisfiable theory $R$ lying in $V$.
\end{proposition}
```

## 10. `se110.proposition.Dichotomy` — Scope Dichotomy

- Kind: `proposition`
- Source lines: `586-591`

```latex
\begin{proposition}[Scope Dichotomy]
  \label{se110.proposition.Dichotomy}
  For every framework $\Framework$ and vocabulary $V$, either $\Framework$ is
  neutral on $V$, or some satisfiable theory $R$ lying in $V$ is such that
  $R \cup \Framework$ is not satisfiable.
\end{proposition}
```

## 11. `se110.def.FragmentCommonGround` — Fragment-Relative Common Ground

- Kind: `definition`
- Source lines: `610-615`

```latex
\begin{definition}[Fragment-Relative Common Ground]
  \label{se110.def.FragmentCommonGround}
  Let $(V,R)$ be a referential fragment and $\mathcal{K}$ a class of frameworks.
  The fragment has \emph{common ground relative to} $\mathcal{K}$ when
  $R \cup \Framework$ is satisfiable for every $\Framework \in \mathcal{K}$.
\end{definition}
```

## 12. `se110.proposition.FragmentCommonGroundOfNeutral` — Common Ground from Neutrality

- Kind: `proposition`
- Source lines: `623-628`

```latex
\begin{proposition}[Common Ground from Neutrality]
  \label{se110.proposition.FragmentCommonGroundOfNeutral}
  Let $(V,R)$ be a referential fragment.
  If every framework in $\mathcal{K}$ is neutral on $V$, then the fragment has
  common ground relative to $\mathcal{K}$.
\end{proposition}
```

## 13. `se110.example.DecisionRecord` — Decision Record

- Kind: `example`
- Source lines: `656-668`

```latex
\begin{example}[Decision Record]
  \label{se110.example.DecisionRecord}
  Consider a decision record with four atoms:
  $\pred{decisionMade}$ (a decision was made),
  $\pred{occurredAt}$ (it occurred at the recorded time),
  $\pred{causedByScore}$ (the denial was caused by the score), and
  $\pred{justifiedByPolicy}$ (the cited policy justified the decision).
  Let $V = \{\pred{decisionMade}, \pred{occurredAt}\}$ and
  $R = \{\pred{decisionMade}, \pred{occurredAt}\}$.
  The theory $R$ is satisfied by the valuation that makes every atom true, and
  not satisfied by the valuation that makes every atom false.
  So $(V,R)$ is a referential fragment.
\end{example}
```

