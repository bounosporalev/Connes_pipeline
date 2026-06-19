A Relational Observable Substrate & its NCG Realization

This repository contains the numerical prototypes and theoretical framework for realizing Noncommutative Geometry (NCG) on coordinate-free relational networks and curved lattices.

Theoretical Core: The Relational Substrate (discrete_weil.pdf)

The framework formulated in "A Relational Observable Substrate and its NCG Realization" moves away from standard "spectral-first" setups. It constructs a coordinate-free physical theory using an algebraic, sheaf-theoretic foundation:

Stage 1 & 1.5 — Relational Foundations & Strict Descent (Algebraic Layer): Rather than pre-selecting a Hilbert space or state projection, the theory starts with a flat sheaf of local $C^{\ast}$-algebras $\mathcal{A}(U\_i)$. Overlapping patches are glued via strict comparison $C^{\ast}$-isomorphisms $\alpha\_{ij}$ satisfying the cocycle condition:

$$\alpha_{ij}\alpha_{jk}=\alpha_{ik}$$

Stage 2 — One Spectral Injection (The NCG Realization): Geometry is injected globally at exactly one step via a realization functor $\text{NCG}: \mathcal{R}\_Q \to \text{Hilb}\_{\mathcal{A}}$ that represents the local algebras $\mathcal{A}\_i \mapsto (\pi\_i: \mathcal{A}\_i \to B(H\_i))$ and implements the comparisons $\alpha\_{ij} \mapsto V\_{ij}$. This supplies a global trace $\tau$ and the canonical universal differential calculus $\Omega\_u^\bullet(\mathcal{A}\_G)$ ($da = 1 \otimes a - a \otimes 1$), avoiding coordinate and local Dirac operator ambiguities.

Stage 3 & 4 — Physical Readout, Curvature, and Crystalline Defects: Local physics is reconstructed by choosing a local Fermi projection $P\_i$ within each patch's represented algebra. This defines the connection $a\_{ij}=dV\_{ij}$ using the universal differential, yielding the relational simplicial curvature:

$$F_{ijk}^{rel}=P_i dV_{ij} dV_{jk}$$

which satisfies an automatic Bianchi identity ($\tilde{\delta}F^{rel}=0$). Topological disclinations are measured via the product of the compressed transition determinants $g\_{ij} = \frac{\det(V\_{ij}|\_{E\_i})}{|\det(V\_{ij}|\_{E\_i})|}$ and mapped to the relational topological class $c\_1^{rel} \in \tilde{H}^2\left(N(\mathcal{R}\_Q);\mathbb{Z}\right)$.

Exploratory Prototypes (Jupyter Notebooks)

These computational sandboxes were built to test discrete NCG pipeline behaviors, lattice disorder, and curvature effects prior to the formalization of the relational substrate.

Flat-Space Pipeline (Connes_Pipeline (1).ipynb): Implements a discrete spectral triple pipeline on a flat torus. Extracts topological invariants from operator variations $dO\_i = [D,O\_i]$ and relational complex cochains $\omega\_{ij} = \mathrm{Tr}(P[D,O\_i][D,O\_j])$. Executes Anderson localization sweeps (varying disorder strength $W$) to test the stability of computed Chern numbers under spatial degradation.

Hyperbolic Haldane Pipeline (Hyperbolic_Haldane_Connes_Pipeline.ipynb): Ports the pipeline onto a negatively curved space to test structural independence from Euclidean translation. Replaces flat metrics with graph geodesic distances $d\_G$ on an order-3 heptagonal tiling $\{7,3\}$ of the Poincaré disk. Models a closed, genus-3 hyperbolic surface (the Klein Quartic) to supply six independent Wilson loops to test non-contractible transport in negative curvature.
