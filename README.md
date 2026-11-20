# Projective Information Loss and Fibre Erasure in Admissible Non-Injective Projection

This repository contains the source of the **Fibre Erasure** Cosmochrony paper
*Projective Information Loss and Fibre Erasure in Admissible Non-Injective Projection*.

This work establishes a conditional **fibre-erasure theorem** for the admissible
coarse-graining hierarchy of the Cosmochrony spectral programme. Version 2.0
corrects the rank-level proposition, removes attributions to the withdrawn O31
results, and restates the O12 application after O32 2.0: for that observable the
label carries no information at any depth, so the theorem gives only $0 \le 0$.

## Quick Summary

The non-injective projection $\Pi : \Omega \to \mathcal{O}$ defines a residual
fibre-information functional $I(c;\sigma(\ell))$, where $c$ is a Weil-block
fibre label and $\sigma_c(\ell)$ is the BFS capacity profile at
coarse-graining depth $\ell$.

Conditional on the structural sufficiency hypothesis **[H-suff]**, the
data-processing inequality implies that $I(c;\sigma(\ell))$ is
non-increasing in $\ell$:

> **Under [H-suff], fibre information cannot increase under admissible coarse-graining.**

[H-suff] is proved at the level of the BFS rank observable: for the uniform
seed of the O12 pipeline the rank is $\min(2\ell+1, q)$, the number of distinct
second coordinates in the ball, independent of $c$. For the O12 three-character
capacity under the campaign sampling law, O32 2.0 proves that the distribution of
the profile does not depend on the label, so $I(c;\sigma(\ell)) = 0$ at every
depth and [H-suff] holds. This is independence in law, not equality of profiles
for each draw of the auxiliary characters. It shows that the label is absent from
that observable; it demonstrates no erasure mechanism.

## Core Result

The fibre-erasure theorem states: under [H-suff] and [H-sg]
(semigroup property, redundant at the rank level), for any $\ell' > \ell$,
$$
I(c;\sigma(\ell')) \le I(c;\sigma(\ell)).
$$

For the O12 observable the bound reads $0 \le 0$: no non-trivial erasure is
established. The inter-sector variance $\mathrm{Var}_c(\sigma_c(\ell))$ of mean
profiles measures finite-sample dispersion, and its restriction to cube-root
orbits carries no colour content.

## Conceptual Structure

This paper connects the qualitative ENI no-go theorem with the BFS
capacity profiles of the spectral programme:

- **ENI** establishes $S_\Pi > 0$ but does not order information loss
  across resolutions.
- **Fibre Erasure** introduces the coarse-graining axis $\ell$ and turns
  ENI into a monotone, measurable hierarchy via the data-processing
  inequality.

Three orthogonal axes are disambiguated:

| Axis | Parameter | Role |
|------|-----------|------|
| Coarse-graining / resolution | $\ell$ (BFS depth) | this paper, carries $I(c;\sigma(\ell))$ |
| Thermodynamic / continuum | $q \to \infty$ | large-$q$ behaviour of the common expected profile |
| Temporal / cascade | $n$ (cascade step) | projective time, handled by PTO |

## Strict Disclaimer

This result is **not** a $c$-theorem. It does not count effective
degrees of freedom. A $c$-theorem-type statement would require an
additional counting principle, listed as open problem [O-2].

## What This Paper Establishes

Conditional on [H-suff] and [H-sg]:

- a monotone information functional $I(c;\sigma(\ell))$ for the BFS
  coarse-graining hierarchy;
- its non-increase under depth-increment, via the data-processing
  inequality;
- the identification of $I(c;\sigma(\ell)) = 0$ as the fibre-erasure
  equilibrium condition;
- for the O12 capacity under the campaign sampling law, $I(c;\sigma(\ell)) = 0$
  at every depth (from O32 2.0), which settles [O-1a$'$] in law.

## What This Paper Does Not Establish

- a $c$-theorem or analogue (open problem [O-2]);
- [H-suff] for observables other than the O12 capacity under the campaign
  sampling law;
- any non-trivial erasure for the O12 observable, or any colour statement
  (the leave-triplet-out scores are unexplained measurements, not support for
  [H-color]);
- the full capacity-level form of [H-sg] (proved at the rank level and
  there redundant; capacity-level residue open as [O-1b]).

## Position in the Programme

Fibre Erasure occupies a **hub position** between the foundational
papers and the spectral admissibility programme:

- inputs: **ENI** (non-injective projection, projection entropy $S_\Pi$)
  and **Foundation** (Weil-fibre realisation);
- inputs: spectral programme (BFS capacity profiles $\sigma_c(\ell)$,
  numerical campaigns, the O32 unit-scaling invariance);
- output: information-theoretic monotone connecting them.

Together with the **PTO** paper (which handles the orthogonal temporal
axis $n$), it constitutes the information-theoretic architecture of the
admissibility cascade.

## Build

```bash
bash compile.sh
```

Output: `out/FibreErasure.pdf`.

## Keywords

Non-injective projection; fibre erasure; admissible coarse-graining;
data-processing inequality; information monotone; BFS capacity;
spectral admissibility; projective information loss; Weil
representation; Heisenberg group.

## Citation

If you reference this work, please cite:

> J. Beau, *Projective Information Loss and Fibre Erasure in Admissible Non-Injective Projection*, Zenodo, 2026.

## Acknowledgements

Portions of the formal development, numerical validation, and editorial
refinement benefited from iterative interactions with large language
models, used as analytical assistants for testing internal consistency
and exploring alternative formulations. All theoretical results and
interpretations remain the sole responsibility of the author.

## Contributions

This repository is intended as a research reference. Critical feedback,
mathematical scrutiny, and independent analyses are welcome. Please open
an issue to discuss conceptual points or technical details.