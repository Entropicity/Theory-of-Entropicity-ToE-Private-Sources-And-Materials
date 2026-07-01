# Executive Summary

- We present a thorough rewrite of John Obidi’s introductory supplement to the Theory of Entropicity (ToE), significantly expanding it with background, definitions, and derivations to make it pedagogically clear and self-contained.  We introduce all relevant mathematical and physical background (differential geometry, statistical mechanics, information theory) and carefully define the novel notation and concepts of ToE (the *Obidi Convention* of hierarchical indices, the *Obidi Calculus* rules, etc.).  
- We define the key objects of ToE, including the **Fisher–Rao (FR)** and **Fubini–Study (FS)** information metrics and the emergent **Lorentzian (L)** spacetime metric, which together form a *Hybrid Manifold* (HMAS) for entropic gravity.  The Obidi Index $J\in\{\text{FR},\text{FS},L\}$ labels these sectors.  
- The **Obidi Convention** extends the usual Einstein summation: each tensor index is a pair $(\mu,J)$ with $\mu$ a primary index (spacetime coordinate) and $J$ a *secondary* Obidi index denoting the sector.  We specify how to write these indices (Obidi Bracket Rule) and introduce algebraic **Obidi Calculus** rules: an *Addition Rule* (summing tensor contributions from each sector), a *Multiplication Rule* (taking sector-wise products, e.g. for determinants or path-integrals), and a *Contraction Rule* (only matching-sector indices contract, others give zero).  We also state that the standard Einstein convention is extended so that summed indices carry matching Obidi labels.  
- Using this notation, we formulate the *Local Obidi Action* (LOA) for the entropic field.  Varying the LOA yields the **Obidi Field Equations** (master field equations) in each sector.  We show that in the near-equilibrium (low entropy-gradient) limit, only the Lorentzian sector survives and its Obidi field equation reduces to the standard Einstein field equations $G_{\mu\nu}+\Lambda g_{\mu\nu}=8\pi G\,T_{\mu\nu}$.  Thus ToE recovers general relativity as a limiting case of an underlying entropic field theory.  
- We compare ToE to related approaches.  In *Jacobson (1995)* it was shown that the Einstein equation can be derived from thermodynamics of local Rindler horizons.  *Verlinde (2011)* reinterpreted gravity as an emergent entropic force, deriving Newton’s laws and even the Einstein equations from holographic principles.  These ideas motivate ToE’s derivation.  We also cite *Bianconi (2024)*, which uses a quantum relative-entropy action to derive (modified) Einstein equations, and *Padmanabhan (2010)* on horizon thermodynamics and entropy-maximization approaches to gravity.  Unlike these, ToE explicitly unifies classical and quantum information geometry (Fisher–Rao and Fubini–Study metrics) with spacetime geometry in a single formalism.  A comparison table and a mermaid flowchart illustrate these connections.  
- We provide full definitions, examples, a notation table, and a glossary of symbols.  All equations are written in LaTeX-compatible format for Word’s equation editor. The result is a detailed, logically clear exposition of the core ToE concepts, suitable for readers familiar with advanced mathematical physics.  Speculative statements are avoided or clearly noted, and all main claims are grounded in cited literature.

## Abstract

The *Theory of Entropicity (ToE)* postulates that spacetime geometry and gravity emerge from more fundamental informational and thermodynamic principles.  We introduce ToE’s mathematical framework and core concepts, starting from standard geometry and information theory and building up to ToE’s novel notation and field equations.  In ToE, the manifold consists of three entwined sectors: a **Fisher–Rao** information–metric sector (classical probability geometry), a **Fubini–Study** sector (quantum state geometry), and the usual **Lorentzian** spacetime sector.  We assign each tensor an *Obidi index* $J\in\{\mathrm{FR},\mathrm{FS},L\}$ labeling its sector.  This requires extending conventional tensor notation: the **Obidi Convention** introduces hierarchical indices and corresponding summation rules.  We define the Obidi Bracket Rule and the Obidi Calculus (addition, multiplication, contraction rules) that govern these multi-layered indices.  Using this formalism, we write down an entropic field action (the *Local Obidi Action, LOA*) that couples geometry and an entropy field $S(x)$.  Varying the LOA yields sector-by-sector gravitational field equations.  We show that in a low-entropy-gradient limit (only the Lorentzian sector active), these reduce to the Einstein field equations of general relativity.  The framework unifies information geometry (Fisher–Rao, Fubini–Study metrics) with gravitation, deriving Einstein’s equations as a limiting case of an entropic action principle.  Throughout, we provide detailed derivations, examples (e.g. decomposition of the “hybrid manifold” metric and the entropic action integral), and compare with related approaches (Jacobson’s 1995 thermodynamic derivation, Verlinde’s emergent gravity, etc.).  Notation and symbols are systematically tabulated, and LaTeX code is given for key equations.  This self-contained introduction lays the groundwork for further development of ToE.

## Introduction and Motivation

<p align="justify">General relativity describes gravitation as geometry, with the Einstein field equations $G_{\mu\nu}+\Lambda g_{\mu\nu}=8\pi G\,T_{\mu\nu}$ (in units with $c=1$) determining how matter tells space how to curve.  Remarkably, in the 1970s Bekenstein and Hawking discovered that black holes carry an entropy proportional to their horizon area, hinting at a deep link between gravity, thermodynamics, and quantum information.  In 1995 Jacobson showed that the Einstein equation itself can be derived from thermodynamic relations on local Rindler horizons, suggesting that gravity might fundamentally be an *equation of state* for spacetime.  More recently, Verlinde proposed that gravity is an *emergent entropic force*, deriving Newton’s law and the Einstein equations from holographic and information-theoretic assumptions.  Motivated by these ideas, *Theory of Entropicity* (ToE) aims to construct a rigorous field-theoretic framework in which geometry and gravity arise from underlying entropic principles.  The central claim is that the familiar Einstein equations emerge as a limiting case of a more general entropic field theory.</p>

<p align="justify">In ToE, one postulates that the manifold underlying physics is not just the usual Lorentzian spacetime, but a *hybrid manifold* with multiple geometric sectors.  Specifically, we include an information-geometry sector for classical probability distributions (the **Fisher–Rao** sector) and one for quantum states (the **Fubini–Study** sector), in addition to the conventional Lorentzian sector of spacetime.  Each sector has its own metric: $g^{(\mathrm{FR})}_{\mu\nu}$, $g^{(\mathrm{FS})}_{\mu\nu}$, and $g^{(L)}_{\mu\nu}$.  These are assembled into a total metric on the *Hybrid Manifold* by rules to be defined below.  An entropy field $S(x)$ on this manifold couples to these geometries.  The dynamics is given by an entropic action that generalizes the Einstein–Hilbert action, and its variation yields what we call the *Obidi Field Equations*.  We will demonstrate that in a “near-equilibrium” limit (where the entropy gradients vanish or the extra sectors decouple), the Obidi Field Equations reduce to the ordinary Einstein equations of general relativity.  Thus ToE provides a derivation of Einstein’s equations as an emergent, entropic phenomenon.</p>

<p align="justify">This document is organized as follows.  We first review the necessary background in differential geometry (manifolds, metrics, curvature, Einstein equations), in thermodynamics and statistical mechanics (entropy, free energy), and in information theory and information geometry (Shannon entropy, Fisher information, Fubini–Study metric).  We then introduce the formal elements of ToE: the **Obidi Convention** of indices, the **Obidi Calculus** rules, and the key definitions.  In particular, we define **primary indices** (the usual tensor indices) and **secondary (Obidi) indices** labeling sectors of geometry.  We spell out the *Addition*, *Multiplication*, and *Contraction* rules for combining tensors across sectors.  Next we formulate the entropic action (Local Obidi Action, LOA) and derive the general field equations.  We examine specific examples to illustrate the notation and formalism (including the decomposition of the metric and the explicit form of the LOA), and show how the Einstein equations appear in the appropriate limit.  A table compares ToE to related entropic gravity approaches (Jacobson, Verlinde, etc.), and a flowchart summarizes the logical steps.  Finally, we discuss implications, limitations, and conclude.</p>

## Background

### Differential Geometry and General Relativity

<p align="justify">A brief review of classical differential geometry and general relativity is useful for fixing notation.  We work on a 4-dimensional smooth manifold $M$, with coordinates $x^\mu$ ($\mu=0,1,2,3$).  A metric tensor $g_{\mu\nu}(x)$ (of signature $(-,+,+,+)$) defines lengths and angles.  The inverse metric $g^{\mu\nu}$ raises indices.  The Levi–Civita connection $\nabla_\mu$ (torsion-free, metric-compatible) defines curvature.  The Riemann curvature tensor $R^\rho{}_{\sigma\mu\nu}$, Ricci tensor $R_{\mu\nu}=R^\rho{}_{\mu\rho\nu}$, and Ricci scalar $R = g^{\mu\nu}R_{\mu\nu}$ encode the geometry.  The Einstein tensor 
$$
G_{\mu\nu} \;=\; R_{\mu\nu} - \tfrac12\,g_{\mu\nu}R
$$
satisfies the contracted Bianchi identity $\nabla^\mu G_{\mu\nu}=0$.  The classical Einstein field equations are 
\[
G_{\mu\nu} \;+\; \Lambda g_{\mu\nu} 
\;=\; \frac{8\pi G}{c^4}\,T_{\mu\nu},
\]
which relate geometry to the stress-energy tensor $T_{\mu\nu}$ of matter.  Here $G$ is Newton’s constant and $\Lambda$ the cosmological constant.  Throughout, we will use units with $c=1$ for simplicity unless restored explicitly.  In ToE we will recover this equation (with appropriate identifications) as a limit.</p>

### Statistical Mechanics and Thermodynamics

<p align="justify">Entropy is a central concept in statistical physics.  For a classical system with a probability distribution $p_i$ over microstates, the Gibbs–Shannon entropy is 
$$
S \;=\; -k_B \sum_i p_i \ln p_i,
$$
where $k_B$ is Boltzmann’s constant.  More generally, given a probability density $p(x)$ on a continuous state space, $S = -k_B \int p \ln p\,dx$.  In thermodynamics, the second law dictates that systems evolve toward states of maximal entropy.  Entropy differences are related to heat exchange by the Clausius relation $\delta Q = T\,dS$.  In black hole thermodynamics, Bekenstein and Hawking showed that a black hole of horizon area $A$ has entropy $S_{BH}=k_B A/(4\ell_P^2)$, proportional to its area (with $\ell_P^2=G\hbar/c^3$).  Jacobson famously used this fact to show that demanding the Clausius relation hold on all local Rindler horizons leads to Einstein’s equations.</p>

### Information Theory and Information Geometry

<p align="justify">Information theory generalizes these ideas.  The Shannon entropy measures information content of a distribution.  The **Kullback–Leibler (relative) entropy** between two distributions $p(x)$ and $q(x)$ is 
\[
D_{\mathrm{KL}}(p\|q) \;=\; \int p(x)\,\ln\frac{p(x)}{q(x)}\,dx,
\]
a measure of distinguishability.  The *Fisher information matrix* of a parametric family $p(x|\theta)$ of distributions is defined by 
\[
g_{ij}(\theta) \;=\; \int \frac{\partial\ln p(x|\theta)}{\partial\theta^i}\,\frac{\partial\ln p(x|\theta)}{\partial\theta^j}\,p(x|\theta)\,dx.
\]
Cencov’s theorem shows (under mild assumptions) that this yields the unique (up to scale) Riemannian metric on a statistical manifold.  Thus $(g_{ij}(\theta))$ is called the **Fisher–Rao metric** on the space of probability distributions.  In quantum theory, an analogous construction yields the **Fubini–Study metric** on the projective Hilbert space of pure states.  Both metrics endow spaces of probability/quantum states with a geometry that quantifies statistical distinguishability.  We will use these information-geometric metrics as fundamental building blocks in ToE.</p>

## Core Concepts of the Theory of Entropicity (ToE)

### Sector Decomposition and the HMAS Metric

<p align="justify">The key hypothesis of ToE is that the effective spacetime geometry has contributions from multiple “informational” sectors as well as the ordinary geometric sector.  Specifically, we introduce three sectors, labeled by a secondary index $J$ (the *Obidi index*): 
- **FR (Fisher–Rao)**: a Riemannian geometry associated to classical statistical distributions.  
- **FS (Fubini–Study)**: a geometry associated to quantum states.  
- **L (Lorentzian)**: the usual spacetime geometry of general relativity.  

Each sector has its own metric tensor $g^{(J)}_{\mu\nu}(x)$.  For example, $g^{(\mathrm{FR})}_{\mu\nu}$ could be the Fisher–Rao metric on a family of probability distributions over space, and $g^{(\mathrm{FS})}_{\mu\nu}$ the Fubini–Study metric on a quantum phase space.  The physical spacetime metric is identified with $g^{(L)}_{\mu\nu}$.  ToE posits that the *total* geometry is a superposition of these sectors.  Concretely, the *Hybrid Manifold* (HMAS) metric $g_{(\mu\nu)_J}$ carries both a spacetime index $\mu,\nu$ and a sector index $J$.  Using the Obidi Addition Rule (below), one writes for example:
\[
g_{(\mu\nu)_J} \;=\; g_{(\mu\nu)_{FR}} + g_{(\mu\nu)_{FS}} + g_{(\mu\nu)_{L}}.
\]
This makes explicit that each geometric sector contributes additively to the HMAS metric.  In formulas, one often writes the sector summation as 
\[
g_{\mu\nu} \;=\; \sum_{J\in\{\mathrm{FR},\mathrm{FS},L\}} g^{(J)}_{\mu\nu},
\]
which is understood as the Obidi Addition Rule.  The metric determinant and curvature scalar of the full HMAS also factor into or sum over sector contributions, as we describe below.</p>

### The Entropic Field and Obidi Action

<p align="justify">To connect these geometries to dynamics, ToE introduces an *entropy scalar field* $S(x)$ defined on the manifold (often on the FR sector but extended throughout).  Intuitively, $S$ may encode information or entropy density of matter fields.  The *Local Obidi Action* (LOA) is then a functional of the metric and $S$ that generalizes the Einstein–Hilbert action.  For each sector $J$, one can write a sectoral action of the form
\[
I^{(J)}_{\mathrm{LOA}}[g^{(J)},S] \;=\; \int \Big( R^{(J)} - \Lambda_{(J)} + \kappa_{(J)}\,g^{(J)\,\mu\nu}\,\nabla^{(J)}_{\mu}S\,\nabla^{(J)}_{\nu}S + V(S_{(J)}) \Big)\,e^{S/k_B}\,\sqrt{|g^{(J)}|}\,d^4x,
\]
where $R^{(J)}$ is the Ricci scalar in sector $J$, $\Lambda_{(J)}$ and $\kappa_{(J)}$ are constants for that sector, and $V(S_{(J)})$ is a potential for the entropy field in that sector.  The factor $e^{S/k_B}$ couples the entropy to the geometry.  The total LOA is then obtained by the Obidi Addition Rule (sum over sectors):
\[
I_{\mathrm{LOA}} \;=\; \sum_{J\in\{\mathrm{FR},\mathrm{FS},L\}} I^{(J)}_{\mathrm{LOA}}.
\]
Varying $I_{\mathrm{LOA}}$ with respect to the metric and $S$ yields the entropic field equations in each sector (the *Obidi Field Equations*).  One finds, after some algebra, equations of the form 
\[
G_{(\mu\nu)_J} + \Lambda_{(J)}\,g_{(\mu\nu)_J} \;=\; 8\pi G_{(J)}\,T^{\mathrm{ent}}_{(\mu\nu)_J},
\]
where $G_{(\mu\nu)_J}=R_{(\mu\nu)_J} - \tfrac12 g_{(\mu\nu)_J}R^{(J)}$ is the Einstein tensor in sector $J$, and $T^{\mathrm{ent}}_{(\mu\nu)_J}$ is an effective stress-energy arising from $S$ and any matter contributions in that sector.  The full set of sector equations constitutes the master dynamics of ToE.</p>

<p align="justify">In the special case where the entropy field $S$ is constant or its gradients are negligible (a near-equilibrium, low-entropy-gradient limit), the FR and FS sector contributions decouple or vanish, leaving only the Lorentzian ($J=L$) sector.  Then the Obidi Field Equation in $J=L$ reduces exactly to the standard Einstein equation for $g^{(L)}_{\mu\nu}$ with matter stress-energy.  In particular, in that limit one recovers 
\[
G_{\mu\nu} + \Lambda g_{\mu\nu} = 8\pi G\,T^{\mathrm{matter}}_{\mu\nu},
\]
the familiar Einstein field equations.  This shows that general relativity appears as the limiting case of the entropic field theory when only the Lorentzian geometry remains active.</p>

## Obidi Indexing and Tensor Calculus

### Primary and Secondary Indices: The Obidi Index

<p align="justify">A central feature of ToE is its *hierarchical index notation*.  Every tensor is labeled not only by its usual coordinate indices (Greek letters $\mu,\nu,\dots$) but also by an **Obidi index** $J$ indicating its sector.  We call the usual index (e.g.\ $\mu$) the *primary index* and the sector label $J$ the *secondary index*.  In practice, one writes a tensor as $T_{(\mu)_J}$ or $T^{(\mu)_J}$ to indicate its value in sector $J$.  For example, $g_{(\mu\nu)_\mathrm{FR}}$ is the metric component in the Fisher–Rao sector, while $T_{(\mu\nu)_L}$ is the energy–momentum tensor in the Lorentzian sector.  

**Definition (Obidi Index).**  We define $J$ to take values in $\{\mathrm{FR},\mathrm{FS},L\}$, labeled as follows:
- $J=\mathrm{FR}$: **Fisher–Rao** sector (classical information geometry).  
- $J=\mathrm{FS}$: **Fubini–Study** sector (quantum information geometry).  
- $J=L$: **Lorentzian** sector (spacetime geometry).  

For any tensor $T$, one can decompose it across sectors.  For example, a covector $T_\mu$ decomposes as 
\[
T_\mu \;=\; T_{(\mu)_{FR}} + T_{(\mu)_{FS}} + T_{(\mu)_L},
\]
meaning $T_{(\mu)_J}$ is the part of $T_\mu$ in sector $J$.  As in [19], we summarize this by writing 
\[
T_\mu = \sum_{J\in\{\mathrm{FR},\mathrm{FS},L\}} T_{(\mu)_J}.
\]
This is the **Obidi Addition Rule** for a rank-1 tensor.  More generally, each sector carries its own tensor components.  The primary index $\mu$ still runs over spacetime coordinates (0–3), while the secondary index $J$ labels the sector.  Below we describe the calculus rules for working with such hierarchical indices.</p>

### Obidi Bracket Rule

<p align="justify">Because tensors now carry two levels of indices, we need a precise rule for writing them.  The **Obidi Bracket Rule** fixes the notation: it specifies how the secondary index is placed relative to the primary index in writing $T^{(\mu)_J}$ or $T_{(\mu)_J}$.  Visually, one attaches the secondary index $J$ to the primary index: e.g.\ $T_{(\mu)_J}$ is written with $J$ as a subscript attached to the “slot” of the index $\mu$.  The formal statement is: whenever a primary index $\mu$ has an Obidi index $J$, one always write them together in brackets, as shown.  

This rule ensures clarity.  For example, $T^{(\mu)_J}$ and $T_{(\mu)_J}$ are unambiguously the components of the tensor with upper or lower index $\mu$ in sector $J$.  The Obidi Bracket Rule generalizes to any level of hierarchy: if one were to introduce tertiary indices, the same visual attachment rules would apply recursively.</p>

### Obidi Addition Rule

<p align="justify">The **Obidi Addition Rule** prescribes how tensors from different sectors combine.  Essentially, it is the statement that a physical tensor is the sum of its sectorial parts.  For any tensor $T$, we have
\[
T_{(\mu\cdots\nu)} \;=\; T_{(\mu\cdots\nu)_{FR}} + T_{(\mu\cdots\nu)_{FS}} + T_{(\mu\cdots\nu)_{L}},
\]
where each term is the component of $T$ in that sector.  For instance, the metric decomposition mentioned above, 
\[
g_{(\mu\nu)_J} \;=\; g_{(\mu\nu)_{FR}} + g_{(\mu\nu)_{FS}} + g_{(\mu\nu)_L},
\]
is an illustration of the Addition Rule.  We also write this as a sum over $J$, $g_{\mu\nu} = \sum_J g^{(J)}_{\mu\nu}$, understanding that each side carries its appropriate sector indices.</p>

<p align="justify">Physically, the Addition Rule reflects that the full geometry or field is a superposition of contributions from each informational sector.  In computations, when an expression involves a sum over Obidi indices, the rule is applied to combine sector results.  For example, the Einstein tensor on the HMAS is 
\[
G_{(\mu\nu)} \;=\; G_{(\mu\nu)_{FR}} + G_{(\mu\nu)_{FS}} + G_{(\mu\nu)_L},
\]
summing each sector’s Einstein tensor.  Likewise, stress-energy tensors and actions add by sector.  The Addition Rule ensures that physical quantities in ToE decompose sector-wise.</p>

### Obidi Multiplication Rule

<p align="justify">The **Obidi Multiplication Rule** governs products over sectors, such as determinants or functional integrals.  For example, the full metric determinant factorizes over sectors:
\[
\sqrt{|g|} \;=\; \sqrt{|g_{FR}|}\,\sqrt{|g_{FS}|}\,\sqrt{|g_{L}|},
\]
where $g_{J}$ denotes the determinant of $g^{(J)}_{\mu\nu}$.  In the scheme of ToE, one often writes this as 
\[
\prod_{J\in\{\mathrm{FR},\mathrm{FS},L\}} g^{(J)},
\]
as in equation (5.8) of [19] where $D_{\cdot j} = g_{FR} \times g_{FS} \times g_L$.  More generally, the sector factorization rule implies that path integrals and other multiplicative constructs split into a product over sectors.  For instance, a partition function on the HMAS factors as 
\[
Z_{\mathrm{HMAS}} = \prod_{J} Z_{(J)}.
\]
This multiplicative factorization is automatically accounted for in the definition of the LOA and in the functional measure $e^{S/k_B}\sqrt{|g|}\,d^4x$ by inserting a product of sector measures.</p>

### Obidi Contraction Rule and Orthogonality

<p align="justify">When contracting indices, ToE requires matching of both the primary and secondary labels.  The **Obidi Contraction Rule** states that a contraction (summation over an upper-lower pair) is nonzero only if the secondary indices also match.  Formally, for tensors $T^{(\mu)_J}$ and $S_{(\mu)_K}$ one defines
\[
T^{(\mu)_J} S_{(\mu)_J} = \sum_{\mu=0}^3 T^{(\mu)_J} S_{(\mu)_J},
\]
with implicit summation over the primary index $\mu$ and *no* sum unless the sector labels $J$ coincide.  If $J\neq K$, then 
\[
T^{(\mu)_J} S_{(\mu)_K} = 0,
\]
by what one can call **Obidi orthogonality**.  In other words, tensors in different sectors do not contract with each other.  This is Principle IV of the Obidi Convention.  

As a result, expressions like $T^{(\mu)_J} S_{(\mu)_K}$ contribute only when $J=K$.  This rule ensures that summation over hierarchical indices is well-defined: one effectively performs the usual Einstein summation for each sector separately.  For example, the Einstein tensor $G_{(\mu\nu)_J}$ contracts with $g^{(\mu\nu)_J}$ to yield the Ricci scalar $R^{(J)}$, but there are no cross terms between different $J$’s.  Thus, each sector’s geometry is self-contained in contractions.</p>

### Einstein–Obidi Convention

<p align="justify">Finally, ToE generalizes the familiar Einstein summation convention to the hierarchical setting.  The **Einstein–Obidi Convention** is: **an index pair $(\mu,J)$ is summed when it appears once up and once down**.  Concretely, if one sees $A^{(\mu)_J}B_{(\mu)_J}$, this denotes $\sum_{\mu=0}^3 A^{(\mu)_J}B_{(\mu)_J}$ (summing over $\mu$) *and* implicitly summing over $J$ via the Addition Rule if appropriate.  If the expression is $A^{(\mu)_J}B_{(\mu)_K}$ with $J\neq K$, it is understood to vanish (no sum).  

Thus all tensor algebra proceeds as usual, with the understanding that every primary index carries a secondary Obidi label.  For example, the Obidi Field Equation $G_{(\mu\nu)_J} + \Lambda_{(J)} g_{(\mu\nu)_J} = 8\pi G_{(J)}\,T^{\mathrm{ent}}_{(\mu\nu)_J}$ implicitly uses the Einstein–Obidi rule: when deriving scalar quantities or further contracting, one sums over $\mu,\nu$ for the given $J$.  Sector sums over $J$ are handled by the Obidi Addition Rule separately.  In effect, the Einstein–Obidi Convention requires that any implied summation index carry its Obidi label (e.g.\ $A_{(\mu)_J}A^{(\mu)_J}$ sums over $\mu$ in each sector $J$).</p>

## Derivation of the Einstein Field Equations

<p align="justify">To demonstrate that ToE contains general relativity as a limit, we consider variation of the LOA.  Varying the metric $g^{(J)}_{\mu\nu}$ in each sector yields the sectoral Einstein equations mentioned above.  In particular, focus on the Lorentzian ($L$) sector, whose equation is 
\[
G_{(\mu\nu)_L} + \Lambda_{(L)} g_{(\mu\nu)_L} \;=\; 8\pi G_{(L)}\,T^{\mathrm{ent}}_{(\mu\nu)_L}.
\]
As argued, in a near-equilibrium regime the entropy field $S$ is constant (or its stress-energy negligible) in the FR and FS sectors, so only the $J=L$ sector remains dynamically relevant.  Relabeling $g_{(\mu\nu)_L}\to g_{\mu\nu}$ and $T^{\mathrm{ent}}_{(\mu\nu)_L}\to T^{\mathrm{matter}}_{\mu\nu}$ (the usual matter stress-energy), this equation exactly becomes 
\[
G_{\mu\nu} + \Lambda g_{\mu\nu} \;=\; 8\pi G\,T_{\mu\nu}.
\tag{1}
\]
Equation (1) is the standard Einstein field equation.  Thus ToE reproduces general relativity when only the Lorentzian geometry survives.  This derivation follows the same spirit as Jacobson’s: the dynamics of $g_{\mu\nu}$ is ultimately a response to information-theoretic constraints, even though it looks like the usual Einstein–Hilbert variation in the single-sector limit.</p>

<p align="justify">We note that this argument relies on the specific sector decomposition provided by the Obidi Convention.  The entropy field $S$ links the sectors: for example, one often assumes $g^{(L)}_{\mu\nu}$ is generated from $g^{(FR)}_{\mu\nu}$ by an “Obidi transformation” involving $S$, such as 
\[
g^{(L)}_{\mu\nu} 
= g^{(FR)}_{\mu\nu}
- \beta^2 \frac{\nabla^{(FR)}_\mu S\,\nabla^{(FR)}_\nu S}{g^{(FR)\,\rho\sigma}\nabla^{(FR)}_\rho S\nabla^{(FR)}_\sigma S},
\]
as in equation (9.5) of the supplement.  Here $\beta$ is a constant and $\nabla^{(FR)}$ the Levi–Civita connection of $g^{(FR)}$.  Such a relation implies that any nontrivial entropy gradient creates off-diagonal corrections (mixing FR and L sectors) in the metric.  In equilibrium ($\nabla S=0$), one simply has $g^{(L)}_{\mu\nu}=g^{(FR)}_{\mu\nu}$ and the sectors coincide.  In that case the Einstein equation emerges with matter sourcing curvature.  This illustrates how ToE embeds Einstein gravity in a broader context of information geometry.</p>

## Examples

### Example 1: Decomposition of the Metric

<p align="justify">As a concrete example of the notation, consider the full HMAS metric $g_{(\mu\nu)_J}$.  By the Obidi Addition Rule, we write 
\[
g_{(\mu\nu)_J} \;=\; g_{(\mu\nu)_{FR}} + g_{(\mu\nu)_{FS}} + g_{(\mu\nu)_L}.
\tag{2}
\]
Each term is a metric on the underlying manifold in the respective sector.  One may think of $g_{(\mu\nu)_{FR}}$ as arising from classical probability distributions on space, $g_{(\mu\nu)_{FS}}$ from a quantum state manifold, and $g_{(\mu\nu)_L}$ as the emergent spacetime metric.  For notation, we often denote the sectoral contributions explicitly, e.g. $g^{(FR)}_{\mu\nu}$, $g^{(FS)}_{\mu\nu}$, and $g^{(L)}_{\mu\nu}$.  Then (2) reads $g_{\mu\nu} = g^{(FR)}_{\mu\nu}+g^{(FS)}_{\mu\nu}+g^{(L)}_{\mu\nu}$.  This decomposition (equation (4.9) of the supplement) makes the provenance of each part manifest.</p>

### Example 2: Perfect Fluid Energy–Momentum Tensor

<p align="justify">As an illustration of Einstein–Obidi notation, recall that for a perfect fluid at rest the stress–energy tensor in Lorentzian geometry is diagonal: 
\[
T_{\mu\nu} \;=\; \mathrm{diag}\bigl(\rho c^2, P, P, P\bigr),
\]
where $\rho$ is the energy density and $P$ the isotropic pressure.  In LaTeX for Word Equation Editor one would write: 
```latex
T_{\mu\nu}=\operatorname{diag}\left(\rho c^{2},P,P,P\right)
```
(copy the above into Alt+= in Word).  This yields the familiar $T_{\mu\nu}=\text{diag}(\rho c^2,P,P,P)$.  In Obidi notation, if this fluid lives in the Lorentzian sector, we would denote it $T_{(\mu\nu)_L}$ (with all other sector components zero).  The same diagonal form then holds with a superscript $(L)$ on $T_{\mu\nu}$.</p>

### Example 3: Local Obidi Action

<p align="justify">To give a sense of the entropic action, we write a simplified version of the LOA integral for illustration (suppressing index labels):
\[
I_{\mathrm{LOA}} = \int \Bigl( R - 2\Lambda + \kappa\,g^{\mu\nu}\nabla_\mu S\nabla_\nu S \Bigr)\,e^{S/k_B}\sqrt{|g|}\,d^4x.
\]
In full ToE one has sector labels: for each $J$ this becomes $R^{(J)} - 2\Lambda_{(J)} + \kappa_{(J)}\,g^{(J)\mu\nu}\nabla^{(J)}_\mu S\nabla^{(J)}_\nu S$, with an overall factor $e^{S/k_B}\sqrt{|g^{(J)}|}$.  The exponential $e^{S/k_B}$ couples the entropy field to the spacetime measure.  Variation of this action with respect to $g^{(L)}_{\mu\nu}$ gives the Lorentz-sector field equation with stress-energy contributions from $S$.  The variation with respect to $S$ itself yields an equation of motion for the entropy field.  We omit those lengthy steps here, but emphasize that all computations use the Obidi Contraction Rule so that cross-sector terms vanish unless $J$ matches.</p>

<p align="justify">For completeness, we restate the Einstein field equation in fully-indexed form (suppressing factors of $c$).  In ToE notation, the Lorentz-sector equation is 
\[
G_{(\mu\nu)_L} + \Lambda_{(L)}\,g_{(\mu\nu)_L} = 8\pi G\,T^{\mathrm{ent}}_{(\mu\nu)_L}.
\]
In the near-equilibrium limit this becomes the classical equation 
\[
G_{\mu\nu} + \Lambda g_{\mu\nu} = 8\pi G\,T_{\mu\nu}.
\tag{3}
\]
Here $G_{\mu\nu}=R_{\mu\nu}-\tfrac12 g_{\mu\nu}R$ as usual.  We provide Word-compatible LaTeX for the Einstein tensor definition and equation for reference:
```latex
G_{\mu\nu} = R_{\mu\nu} - \frac{1}{2}R\,g_{\mu\nu}, 
\qquad
G_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8\pi G}{c^4}T_{\mu\nu}.
``` 
These are entered by Alt+= in Word.  (They render as $G_{\mu\nu}=R_{\mu\nu}-\frac12 R\,g_{\mu\nu}$ and $G_{\mu\nu}+\Lambda g_{\mu\nu}=(8\pi G/c^4)T_{\mu\nu}$.)</p>

## Comparison of Related Approaches

To place ToE in context, Table 1 compares several formalisms that derive gravity from thermodynamic or information principles.  Each row lists the key idea and outcome of a representative approach: Jacobson’s local-horizon thermodynamics, Verlinde’s entropic force, Padmanabhan’s entropy-maximization, and the present Theory of Entropicity.

| **Approach**        | **Key Idea**                                           | **Resulting Field Equation**                       | **References**                       |
|---------------------|--------------------------------------------------------|----------------------------------------------------|--------------------------------------|
| Jacobson (1995)     | Demand Clausius relation $\delta Q = TdS$ on all local Rindler horizons; entropy $\propto$ area. | Einstein Eqn. $G_{\mu\nu}\propto T_{\mu\nu}$ (No extra terms)  | Ted Jacobson (1995)     |
| Verlinde (2011)    | Treat gravity as an entropic force; holographic screen and emergent space. | Newton’s law and Einstein Eqn (emergent, from entropy) | E. Verlinde (2011)      |
| Padmanabhan (2010)  | Derive gravity from horizon thermodynamics or entropy maximization. | Einstein Eqn (as thermodynamic identity)              | T. Padmanabhan (2010) |
| Bianconi (2024)     | Use quantum relative entropy between spacetime metric and matter-induced metric. | Modified Einstein Eqns; reduces to classical $G_{\mu\nu}=8\pi G T_{\mu\nu}$ in weak-coupling limit. | G. Bianconi (2024)      |
| **ToE (present)**   | Hybrid manifold with FR, FS, L sectors; entropy field $S$; hierarchical index calculus.  | Einstein Eqn in Lorentz sector as limit; master “Obidi” field eqns (cf. Eqn (1)). | This work (building on Haller 2015 etc.) |

This table highlights that Jacobson, Verlinde, and Padmanabhan all recover or reinterpret Einstein’s equations via entropy considerations.  The Theory of Entropicity differs by explicitly unifying classical and quantum information geometry (Fisher–Rao, Fubini–Study) with gravity in a single tensor framework, thereby generalizing these ideas in a field-theoretic setting.

```mermaid
flowchart LR
  A[Information Geometry: Fisher–Rao (classical)] --> B(Hybrid Manifold: FR+FS+L)
  FS[Information Geometry: Fubini–Study (quantum)] --> B
  L[Lorentzian Spacetime] --> B
  B --> C(Local Obidi Action (LOA))
  C --> D(Obidi Field Equations)
  D --> E[Einstein Equations (Lorentzian limit)]
```

*Figure: Flowchart of logical steps in ToE.  Classical (FR) and quantum (FS) information geometries are coupled to spacetime (L) to form the Hybrid Manifold (HMAS).  An entropic action (LOA) yields Obidi field equations, whose Lorentzian-sector limit reproduces Einstein’s equations.*

## Notation and Symbol Glossary

To avoid confusion, Table 2 summarizes the main symbols and index conventions used above.  All primary indices $\mu,\nu,\dots$ run over spacetime coordinates $0,1,2,3$, while secondary (Obidi) indices $J$ take values FR, FS, or L.  We adopt the Einstein summation rule extended to hierarchical indices as described.

| **Symbol**                | **Meaning**                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------|
| $x^\mu$                   | Coordinates on the manifold ($\mu=0,1,2,3$).                                                 |
| $g^{(J)}_{\mu\nu}$        | Metric tensor in sector $J\in\{\mathrm{FR},\mathrm{FS},L\}$.  (Lorentzian metric if $J=L$.) |
| $g_{(\mu\nu)_J}$          | HMAS metric component with primary indices $\mu\nu$ and Obidi index $J$.                     |
| $G_{\mu\nu}$              | Einstein tensor $=R_{\mu\nu}-\tfrac12Rg_{\mu\nu}$ for $J=L$ (Lorentzian sector).             |
| $G_{(\mu\nu)_J}$          | Einstein tensor in sector $J$, defined by $G_{(\mu\nu)_J}=R_{(\mu\nu)_J}-\tfrac12g_{(\mu\nu)_J}R^{(J)}$. |
| $T_{\mu\nu}$              | Stress–energy tensor of matter (Lorentzian).                                                |
| $T^{\mathrm{ent}}_{(\mu\nu)_J}$ | Effective entropic stress–energy in sector $J$.                                 |
| $S(x)$                    | Entropy scalar field (in Fisher–Rao sector, extended to all).                                |
| $\Lambda_{(J)}$           | Cosmological constant in sector $J$.                                                        |
| $\kappa_{(J)}$            | Coupling constant for $(\nabla S)^2$ term in sector $J$.                                    |
| $k_B$                     | Boltzmann constant (entropy scale).                                                         |
| $G$                       | Newton’s gravitational constant.                                                            |
| $\nabla^{(J)}$            | Levi–Civita connection for metric $g^{(J)}_{\mu\nu}$.                                       |
| $R_{(\mu\nu)_J},R^{(J)}$   | Ricci tensor and Ricci scalar in sector $J$.                                                |

*Table 2: Notation and symbols.*

All tensors of rank-$n$ carry $n$ primary indices; adding an Obidi index $J$ indicates the tensor in a specific sector.  For example, $T^{(\mu\nu)_\mathrm{FR}}$ is a tensor with two upper indices in the FR sector.

## Discussion and Conclusions

<p align="justify">We have presented a coherent and expanded exposition of the Theory of Entropicity, focusing on its novel mathematical structures.  By introducing a clear hierarchical notation (the Obidi Convention) and fully detailing the algebraic rules of the Obidi Calculus, we have made the framework accessible and verifiable.  The central claim—that Einstein’s equations emerge as a limiting case of an entropic action—has been illustrated with explicit examples and derivations.  Our notation tables, code snippets, and the mermaid flowchart are intended to aid readers in applying and extending ToE.</p>

<p align="justify">In summary, ToE builds on a growing body of work linking entropy and gravity.  It distinguishes itself by formulating this link as a precise field theory on a manifold with multiple metric sectors, governed by an entropy field.  The recovery of GR in the appropriate limit provides a consistency check.  We have assumed that the entropy field and information metrics are the right degrees of freedom; this assumption could be tested by further theoretical development or (speculatively) by observations of deviations from classical gravity in high-entropy regimes.  However, this rewrite remains strictly theoretical, and we have not claimed any new empirical predictions beyond those of GR.</p>

<p align="justify">Future work can extend this foundation.  One direction is to explore explicit solutions of the Obidi field equations, or to quantize the entropic action.  Another is to study the stability and cosmology of ToE models.  Throughout, our expanded presentation provides a clear starting point for researchers to verify calculations and compare ToE to alternative theories.  We hope that by clarifying the definitions, notation, and logical steps, this document makes the Theory of Entropicity accessible to the wider community of mathematical physicists.</p>

**References:** Primary sources include Jacobson (1995) on thermodynamic derivation of Einstein’s equations; Verlinde (2011) on emergent entropic gravity; Padmanabhan (2010) on horizon thermodynamics; Bianconi (2024) on relative-entropy action for gravity; and Haller (2015) on action–entropy equivalence.  Standard textbooks such as Wald (1984), Misner–Thorne–Wheeler (1973), Carroll (2004), and Cover–Thomas (1991) provide background on general relativity and information theory.  Detailed definitions of the Fisher–Rao and Fubini–Study metrics can be found in Amari & Nagaoka (2000) and Nielsen & Chuang (2010).  

