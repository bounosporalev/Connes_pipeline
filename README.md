A Relational Observable Substrate & its NCG Realization

This repository contains the numerical prototypes and theoretical framework for realizing Noncommutative Geometry (NCG) on coordinate-free relational networks and curved lattices.

Theoretical Core: The Relational Substrate (relational_substract.pdf)

The framework formulated in "A Relational Observable Substrate and its NCG Realization" moves away from standard "spectral-first" setups. It constructs a coordinate-free physical theory using an algebraic, sheaf-theoretic foundation:

$x$ — Relational Foundations & Strict Descent (Algebraic Layer): Rather than pre-selecting a Hilbert space or state projection, the theory starts with a flat sheaf of local $C^*$-algebras $\mathcal{A}(U_i)$. Overlapping patches are glued via strict comparison $*$-isomorphisms $\alpha_{ij}$ satisfying the cocycle condition:

$$\alpha_{ij}\alpha_{jk} = \alpha_{ik}$$

$y$ — One Spectral Injection (The NCG Realization): Geometry is injected globally at exactly one step. A realization functor $\mathbb{A}_{NCG}$ maps the abstract comparison site to a single global Hilbert space $\mathcal{H}$ and a single global Dirac operator $D$, avoiding coordinate and local Dirac ambiguities.

$z$ — Physical Readout, Curvature, and Crystalline Defects: Local physics is reconstructed by choosing a local Fermi projection $P_i$ within each patch's represented algebra. This defines the connection $a_{ij} = [D, V_{ij}]$, yielding a localized curvature:

$$F = P(d_D P)^2$$

which satisfies an automatic Bianchi identity ($\tilde{\delta}F = 0$). Topological disclinations are measured via the Connes-Chern character and mapped to relational topological classes ($c_1^{rel} \in \tilde{H}^2(\mathbb{Z})$).

Exploratory Prototypes (Jupyter Notebooks)

These computational sandboxes were built to test discrete NCG pipeline behaviors, lattice disorder, and curvature effects prior to the formalization of the relational substrate.

1. Flat-Space Pipeline (Connes_Pipeline (1).ipynb)

Implements a discrete spectral triple pipeline on a flat torus:

Extracts topological invariants from operator variations $dO_i = [D, O_i]$ and relational complex cochains $\omega_{ij} = \mathrm{Tr}(P [D, O_i] [D, O_j])$.

Executes Anderson localization sweeps (varying disorder strength $W$) to test the stability of computed Chern numbers under spatial degradation.

2. Hyperbolic Haldane Pipeline (Hyperbolic_Haldane_Connes_Pipeline.ipynb)

Ports the pipeline onto a negatively curved space to test structural independence from Euclidean translation:

Replaces flat metrics with graph geodesic distances $d_G$ on an order-3 heptagonal tiling $\{7,3\}$ of the Poincaré disk.

Models a closed, genus-3 hyperbolic surface (the Klein Quartic) to supply six independent Wilson loops to test non-contractible transport in negative curvature.
