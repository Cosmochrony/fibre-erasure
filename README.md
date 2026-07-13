# Projective Information Loss and Fibre Erasure in Admissible Non-Injective Projection

This repository contains the source of the **Fibre Erasure** Cosmochrony paper
*Projective Information Loss and Fibre Erasure in Admissible Non-Injective Projection*.

This work establishes a **fibre-erasure theorem** for the admissible
coarse-graining hierarchy of the Cosmochrony spectral programme.

## Quick Summary

The non-injective projection $\Pi : \Omega \to \mathcal{O}$ defines a residual
fibre-information functional $I(c;\sigma(\ell))$, where $c$ is a Weil-block
fibre label and $\sigma_c(\ell)$ is the BFS capacity profile at
coarse-graining depth $\ell$.

Conditional on the structural sufficiency hypothesis **[H-suff]**, the
data-processing inequality implies that $I(c;\sigma(\ell))$ is
non-increasing in $\ell$:

> **Fibre information is erased, not created, under admissible coarse-graining.**

[H-suff] is proved at the level of the BFS rank observable
(Proposition 3.6, label-blindness from Schur's lemma) and numerically
supported at the full Born--Infeld capacity level for
$q \in \{61, 151, 211\}$.

## Core Result

The fibre-erasure theorem (Theorem 4.1) states: under [H-suff] and [H-sg]
(semigroup property, redundant at the rank level), for any $\ell' > \ell$,
$$
I(c;\sigma(\ell')) \le I(c;\sigma(\ell)).
$$

The inter-sector variance $\mathrm{Var}_c(\sigma_c(\ell))$ serves as a
computable proxy. Its restriction to $\mathrm{SU}(3)$ colour-triplets
connects directly to hypothesis [H-color] of the O31--O32 campaign.

## Conceptual Structure

This paper connects the qualitative ENI no-go theorem with the
quantitative spectral convergence observed numerically across
$q \in \{61, 151, 211, 307\}$:

- **ENI** establishes $S_\Pi > 0$ but does not order information loss
  across resolutions.
- **Fibre Erasure** introduces the coarse-graining axis $\ell$ and turns
  ENI into a monotone, measurable hierarchy via the data-processing
  inequality.

Three orthogonal axes are disambiguated:

| Axis | Parameter | Role |
|------|-----------|------|
| Coarse-graining / resolution | $\ell$ (BFS depth) | this paper, carries $I(c;\sigma(\ell))$ |
| Thermodynamic / continuum | $q \to \infty$ | limit for the universal profile $\sigma^*$ |
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
  equilibrium condition (Corollary 4.4).

## What This Paper Does Not Establish

- a $c$-theorem or analogue (open problem [O-2]);
- the full capacity-level form of [H-suff] (proved at the rank level;
  pointwise Born--Infeld residue open as [O-1a$'$]);
- the full capacity-level form of [H-sg] (proved at the rank level and
  there redundant; capacity-level residue open as [O-1b]).

## Position in the Programme

Fibre Erasure occupies a **hub position** between the foundational
papers and the spectral admissibility programme:

- inputs: **ENI** (non-injective projection, projection entropy $S_\Pi$)
  and **Foundation** (Weil-fibre realisation);
- inputs: spectral programme (BFS capacity profiles $\sigma_c(\ell)$,
  numerical campaigns, [H-color] hypothesis);
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
representation; Heisenberg group; [H-color].

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