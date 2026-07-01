# Mathematical Appendix for the ToE Derivation of Einstein Geometry and the Entropic Source Tensor

## Placement within Letter III

Section 6 of *Letter III* explicitly identifies the decisive unfinished task of the ToE program: not merely to entropically reinterpret spacetime curvature, but to derive **both** the geometric tensor on the left-hand side of Einstein’s equations and the source tensor on the right-hand side from a single entropic-information substrate. It also states, correctly, that pressure, radiation, momentum flow, and stress must be understood as tensorial embodiments of organized entropy rather than as primitives external to the theory. The appendix below is written to complete that program in a mathematically explicit way, without repeating the expository material already present in the body of the monograph. fileciteturn0file0

The strategy is to introduce two precise mathematical devices that are not yet isolated sharply enough in the current draft. The first is an **Obidi Lorentzian Lift**, which turns positive-definite information geometry into Lorentzian spacetime geometry by selecting the entropy gradient as the preferred causal direction. The second is an **Entropic Moment Map**, which turns localized information distributions into a symmetric rank-two tensor whose perfect-fluid, dust, radiation, and anisotropic-stress limits reproduce the Einstein stress-energy tensor. These two devices make the ToE claim exact in form: entropy appears on the left as information curvature after Lorentzian lifting, and on the right as localized, transported, and constrained information after moment-taking and metric variation. Earlier information-geometric and entropic-gravity programs already show parts of this pathway, including information-geometric reconstructions of spacetime, Fisher-metric derivations of Einstein-type tensors, and entropic actions reducing to Einstein gravity in low-coupling limits; the present appendix is designed so that ToE derives *both sides together* from one parent framework. citeturn16view3turn16view4turn16view2

## Core operators and foundational definitions

Let \(\mathcal M_N\) be an \(N\)-dimensional statistical manifold coordinatized by \(\Theta^A\), with \(A,B,\ldots=1,\dots,N\), and let \(p(y\mid \Theta)\) be a smooth family of probability densities. The Fisher information metric is

\[
I_{AB}(\Theta)
=
\int d\mu(y)\,
p(y\mid\Theta)\,
\partial_A \ln p(y\mid\Theta)\,
\partial_B \ln p(y\mid\Theta).
\qquad (A.1)
\]

The associated Amari–Čencov cubic tensor is

\[
C_{ABC}(\Theta)
=
\int d\mu(y)\,
p(y\mid\Theta)\,
\partial_A \ln p\,
\partial_B \ln p\,
\partial_C \ln p,
\qquad (A.2)
\]

and, with the Levi–Civita connection of \(I_{AB}\) denoted by \(\Gamma^{(0)A}{}_{BC}\), one may write the \(\alpha\)-connection family as

\[
\Gamma^{(\alpha)A}{}_{BC}
=
\Gamma^{(0)A}{}_{BC}
-
\frac{\alpha}{2}\,
I^{AD} C_{DBC}.
\qquad (A.3)
\]

The relevance of these structures is standard in information geometry: the Fisher metric is the unique symmetric two-tensor, up to scale, characterized by invariance under sufficient statistics, and the Amari–Čencov tensor is the canonical cubic companion to that geometry. Precisely because the Fisher metric is positive definite, it cannot by itself produce a Lorentzian causal structure. That obstruction is the mathematical reason ToE needs a controlled deformation beyond untouched Čencov invariance. citeturn15view1turn19academia0

Introduce now the ToE entropy field \(S(\Theta)\). Define

\[
Q(\Theta)
=
I^{AB}\,\partial_A S\,\partial_B S,
\qquad
n_A
=
\frac{\partial_A S}{\sqrt{Q}},
\qquad
I^{AB}n_A n_B = 1.
\qquad (A.4)
\]

The **Obidi Lorentzian Lift** is then the map

\[
\mathcal L_S[I]_{AB}
:=
\hat G_{AB}
=
\Omega^2(\Theta)\,
\bigl(I_{AB}-\sigma\, n_A n_B\bigr),
\qquad
\sigma>1.
\qquad (A.5)
\]

This is a gradient-dependent disformal deformation in the sense of Bekenstein, but here its distinguished direction is not an arbitrary scalar field: it is the ToE entropy gradient itself. The condition \(\sigma>1\) is the minimal condition ensuring one and only one timelike direction. citeturn15view0turn15view1

A short proof is immediate. Any vector \(v^A\) decomposes uniquely as \(v^A=v_\perp^A+\lambda n^A\), with \(n_A v_\perp^A=0\). Then

\[
\hat G_{AB}v^A v^B
=
\Omega^2
\left(
I_{AB}v_\perp^A v_\perp^B
+
(1-\sigma)\lambda^2
\right).
\qquad (A.6)
\]

Because \(I_{AB}\) is positive definite and \(1-\sigma<0\), the quadratic form has exactly one negative eigendirection and \(N-1\) positive eigendirections. Hence \(\hat G_{AB}\) has Lorentzian signature \((-+\cdots +)\). By the matrix-determinant lemma,

\[
\det \hat G
=
\Omega^{2N}(1-\sigma)\det I,
\qquad (A.7)
\]

so the sign flip is explicit at the level of the determinant as well. This is the precise mathematical step by which ToE converts statistical distinguishability into causal geometry.

Let \(X:\,M_4\hookrightarrow \mathcal M_N\) be a smooth coarse-grained four-dimensional section, with spacetime coordinates \(x^\mu\), \(\mu,\nu=0,1,2,3\). The emergent spacetime metric is the pullback

\[
g_{\mu\nu}(x)
=
\partial_\mu X^A\,
\partial_\nu X^B\,
\hat G_{AB}(X(x)).
\qquad (A.8)
\]

This is the exact place where physical spacetime appears in the construction. The move from information manifold to spacetime by pullback is structurally consonant with earlier information-geometric constructions of geometrodynamics, but ToE’s distinct move is to insert the entropy-selected Lorentzian lift *before* the reduction, not after it. citeturn16view3turn16view4

The second new operator is the **Entropic Moment Map**. Let \(f_q(x,p)\) be a nonnegative local information distribution on the future mass shell \(\mathcal P_x\subset T_xM_4\), written in ToE’s non-extensive sector as

\[
f_q(x,p)
=
Z_q^{-1}(x)\,
\exp_q\!\bigl[-\alpha(x)-\beta_\mu(x)p^\mu\bigr],
\qquad
\exp_q(z):=\bigl[1+(1-q)z\bigr]^{1/(1-q)}.
\qquad (A.9)
\]

The invariant mass-shell measure may be taken as

\[
dP
=
\frac{d^4p}{(2\pi)^3}\,
\delta\!\bigl(g_{\mu\nu}p^\mu p^\nu + m^2 c^2\bigr)\,
\Theta(p^0).
\qquad (A.10)
\]

Then define, for each \(n\ge0\),

\[
\mathfrak M_n[f_q]^{\mu_1\cdots\mu_n}
:=
\int_{\mathcal P_x}
p^{\mu_1}\cdots p^{\mu_n}
f_q(x,p)\, dP.
\qquad (A.11)
\]

The zeroth, first, and second moments are respectively the local information density, flow, and source tensor; in particular,

\[
N^\mu_{\mathrm{ent}}
=
\mathfrak M_1[f_q]^\mu
=
\int dP\, p^\mu f_q,
\qquad
\Theta_{\mathrm{ent}}^{\mu\nu}
=
\mathfrak M_2[f_q]^{\mu\nu}
=
\int dP\, p^\mu p^\nu f_q.
\qquad (A.12)
\]

This second moment is the mathematically exact answer to the question posed in Section 6 of *Letter III*: a scalar or probability density does not go directly onto the right-hand side of Einstein’s equation; rather, its **second covariant moment** does. That is how localized information becomes a rank-two source tensor. In relativistic kinetic theory, these fibre integrals define the particle current and the stress-energy tensor and, when the kinetic equation holds with collision invariants, they are divergence-free in exactly the sense required by the Bianchi identity. citeturn16view0

## Derivation of the geometric side

The parent information-gravity action is taken in \(N\) dimensions to be

\[
A_{\mathrm{IG}}
=
\frac{1}{2\kappa_I}
\int_{\mathcal M_N}
d^N\Theta\,
\sqrt{|\hat G|}
\left(
\mathcal R[\hat G]-2\Lambda_I
\right)
+
A_{\mathrm{src}}^{(N)}[\hat G,S,f_q,\zeta_I],
\qquad (A.13)
\]

where \(\kappa_I\) is the information-gravitational stiffness, \(\Lambda_I\) is the parent vacuum term, and \(\zeta_I\) denotes whatever additional internal information variables are needed to describe localization, binding, or structural constraints.

Assume that, on the coarse-grained sector, the lifted information metric admits a block form

\[
\hat G_{AB}\,d\Theta^A d\Theta^B
=
g_{\mu\nu}(x)\,dx^\mu dx^\nu
+
h_{ab}(x,y)\,
\bigl(dy^a+A^a_{\mu}dx^\mu\bigr)
\bigl(dy^b+A^b_{\nu}dx^\nu\bigr),
\qquad (A.14)
\]

with \(a,b=1,\dots,N-4\). Then the measure factorizes as

\[
\sqrt{|\hat G|}
=
\sqrt{-g}\,\sqrt{h},
\qquad h:=\det(h_{ab}),
\qquad (A.15)
\]

and, after integrating over the internal information fibre \(F\), one gets the four-dimensional effective action

\[
A_{\mathrm{eff}}
=
\frac{1}{2\kappa_{\mathrm{eff}}}
\int_{M_4}
d^4x\,
\sqrt{-g}\,
\bigl(
R[g]-2\Lambda_{\mathrm{ent}}
\bigr)
+
A_{\mathrm{src}}^{(4)}
+
A_{\mathrm{corr}}.
\qquad (A.16)
\]

Here

\[
\kappa_{\mathrm{eff}}^{-1}
=
\kappa_I^{-1}
\int_F d^{N-4}y\,\sqrt{h},
\qquad
\Lambda_{\mathrm{ent}}
=
\Lambda_I
-
\frac{1}{2}
\left\langle
\mathcal R_{\mathrm{int}}
+
\mathcal R_{\mathrm{mix}}
\right\rangle_F,
\qquad (A.17)
\]

where \(\mathcal R_{\mathrm{int}}\) is the internal information-fibre curvature and \(\mathcal R_{\mathrm{mix}}\) is the fibre/base mixing curvature. The correction action \(A_{\mathrm{corr}}\) collects heavy information modes, higher-derivative terms, and non-adiabatic residues. At this point the Einstein–Hilbert sector is not postulated; it has been isolated as the infrared part of the lifted information action. This is exactly the sort of low-coupling Einsteinian limit that already appears in neighboring entropic-gravity constructions, but here its origin is the Lorentzian lift of information geometry plus fibre reduction. citeturn16view2turn16view3turn16view4

Now vary \(A_{\mathrm{eff}}\) with respect to \(g^{\mu\nu}\). Using the Palatini identity in the standard form,

\[
\delta(\sqrt{-g}\,R)
=
\sqrt{-g}\,
\bigl(
G_{\mu\nu}\,\delta g^{\mu\nu}
+
\nabla_\alpha V^\alpha
\bigr),
\qquad (A.18)
\]

and discarding the total divergence by the usual boundary prescription, one obtains

\[
\delta A_{\mathrm{eff}}
=
\frac{1}{2}
\int d^4x\,\sqrt{-g}\,
\left[
\frac{1}{\kappa_{\mathrm{eff}}}
\bigl(
G_{\mu\nu}
+\Lambda_{\mathrm{ent}} g_{\mu\nu}
\bigr)
-
T_{\mu\nu}^{\mathrm{ToE}}
-
\Delta_{\mu\nu}^{\mathrm{IG}}
\right]
\delta g^{\mu\nu},
\qquad (A.19)
\]

where

\[
T_{\mu\nu}^{\mathrm{ToE}}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta A_{\mathrm{src}}^{(4)}}{\delta g^{\mu\nu}},
\qquad
\Delta_{\mu\nu}^{\mathrm{IG}}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta A_{\mathrm{corr}}}{\delta g^{\mu\nu}}.
\qquad (A.20)
\]

Hence the field equations are

\[
G_{\mu\nu}
+
\Lambda_{\mathrm{ent}} g_{\mu\nu}
=
\kappa_{\mathrm{eff}}
T_{\mu\nu}^{\mathrm{ToE}}
+
\kappa_{\mathrm{eff}}
\Delta_{\mu\nu}^{\mathrm{IG}}.
\qquad (A.21)
\]

If one writes \(\kappa_{\mathrm{eff}} = 8\pi G_{\mathrm{eff}}/c^4\), the left-hand side of Einstein’s equations has now been generated explicitly from information geometry:

\[
G_{\mu\nu}
+
\Lambda_{\mathrm{ent}} g_{\mu\nu}
=
\frac{8\pi G_{\mathrm{eff}}}{c^4}
\left(
T_{\mu\nu}^{\mathrm{ToE}}
+
\Delta_{\mu\nu}^{\mathrm{IG}}
\right).
\qquad (A.22)
\]

The geometric side is therefore the coarse-grained curvature sector of the Lorentz-lifted information manifold. No separate metric postulate is needed at the effective level beyond the existence of the section \(X(M_4)\).

## Derivation of the source side

The right-hand side is where ToE must be strongest. The source tensor cannot be a scalar entropy placed by hand on the RHS; it must emerge as the tensorial embodiment of localized information. The proper four-dimensional source action is therefore decomposed as

\[
A_{\mathrm{src}}^{(4)}
=
A_S
+
A_{\mathrm{kin}}
+
A_{\mathrm{cons}},
\qquad (A.23)
\]

corresponding respectively to the coherent entropy-field sector, the incoherent or kinetic-distribution sector, and the localization/constraint sector.

The coherent sector is

\[
A_S
=
\int d^4x\,\sqrt{-g}\,
\bigl[
K(X,S)-U(S)
\bigr],
\qquad
X:=
-\frac{1}{2}
\nabla_\mu S\nabla^\mu S.
\qquad (A.24)
\]

Its Hilbert stress tensor is

\[
T_{\mu\nu}^{(S)}
=
K_X\,\nabla_\mu S\nabla_\nu S
+
g_{\mu\nu}\bigl[K(X,S)-U(S)\bigr].
\qquad (A.25)
\]

If \(\nabla_\mu S\) is timelike, define

\[
u_\mu
=
\frac{\nabla_\mu S}{\sqrt{2X}},
\qquad
u_\mu u^\mu=-1,
\qquad
h_{\mu\nu}:=g_{\mu\nu}+u_\mu u_\nu.
\qquad (A.26)
\]

Then \(T_{\mu\nu}^{(S)}\) assumes the exact perfect-fluid form

\[
T_{\mu\nu}^{(S)}
=
\rho_S\,u_\mu u_\nu
+
p_S\,h_{\mu\nu},
\qquad
\rho_S = 2XK_X-K+U,
\qquad
p_S = K-U.
\qquad (A.27)
\]

For the canonical choice \(K=X\), this becomes

\[
T_{\mu\nu}^{(S)}
=
\nabla_\mu S\nabla_\nu S
-
g_{\mu\nu}
\left[
\frac{1}{2}\nabla_\alpha S\nabla^\alpha S + U(S)
\right].
\qquad (A.28)
\]

This is important for ToE because it proves that even a single coherent entropic mode already generates a legitimate covariant source tensor, and that when its gradient is timelike it is indistinguishable from an effective fluid. That is exactly the classical scalar-fluid correspondence known in GR and k-essence. citeturn17view0turn17view1

The incoherent, particulate, radiative, or coarse-grained sector is encoded by the Entropic Moment Map introduced above. Its fundamental source tensor is

\[
\Theta_{\mu\nu}^{\mathrm{ent}}
=
\int_{\mathcal P_x} dP\,
p_\mu p_\nu\, f_q(x,p).
\qquad (A.29)
\]

Choose the Landau velocity \(u^\mu\) by

\[
\Theta^{\mu\nu}_{\mathrm{ent}}u_\nu
=
-\rho_{\mathrm{kin}}u^\mu,
\qquad
u_\mu u^\mu=-1.
\qquad (A.30)
\]

Then the exact \(1+3\) decomposition of the kinetic entropic source is

\[
\Theta_{\mu\nu}^{\mathrm{ent}}
=
\rho_{\mathrm{kin}}u_\mu u_\nu
+
p_{\mathrm{kin}} h_{\mu\nu}
+
2u_{(\mu}q_{\nu)}
+
\pi_{\mu\nu},
\qquad (A.31)
\]

with projected parts

\[
\rho_{\mathrm{kin}}
=
u^\mu u^\nu \Theta_{\mu\nu}^{\mathrm{ent}},
\qquad
p_{\mathrm{kin}}
=
\frac{1}{3}h^{\mu\nu}\Theta_{\mu\nu}^{\mathrm{ent}},
\qquad (A.32)
\]

\[
q_\mu
=
-
h_\mu{}^{\alpha}u^{\beta}\Theta_{\alpha\beta}^{\mathrm{ent}},
\qquad
\pi_{\mu\nu}
=
\left(
h_{(\mu}{}^\alpha h_{\nu)}{}^\beta
-
\frac{1}{3}h_{\mu\nu}h^{\alpha\beta}
\right)
\Theta_{\alpha\beta}^{\mathrm{ent}}.
\qquad (A.33)
\]

This is the mathematically decisive identification for the RHS. In ToE language:

\[
\text{mass density}
\;\equiv\;
\frac{\rho_{\mathrm{kin}}}{c^2}
\quad\text{in the rest frame},
\]

\[
\text{pressure}
\;\equiv\;
\frac{1}{3}h^{\mu\nu}T_{\mu\nu},
\]

\[
\text{momentum flux / heat flow}
\;\equiv\;
q_\mu,
\]

\[
\text{anisotropic stress / shear stress}
\;\equiv\;
\pi_{\mu\nu}.
\]

So pressure, radiation, and stress are not verbal appendages added to entropy; they are **different projections of the same rank-two entropic moment tensor**. This is the cleanest mathematical way to state the intuition already present in *Letter III*: localized information becomes physical matter when it acquires inertia, flow, resistance, and anisotropy under coarse-graining. In relativistic kinetic theory, the tensor in (A.29) is symmetric and conserved whenever the microscopic distribution obeys the Liouville or Boltzmann equation with the usual collision invariants. citeturn16view0

The localization or constraint sector captures bound structure, elastic response, compositional locking, topological storage, and other organizational features of information that are not exhausted by a one-particle distribution. Write

\[
A_{\mathrm{cons}}
=
\int d^4x\,\sqrt{-g}\,
\Lambda_c(n,s,\zeta_I,B_{IJ},\ldots),
\qquad (A.34)
\]

where \(n\) is the local carrier density, \(s\) the entropy per carrier, \(\zeta_I\) internal information labels, and \(B_{IJ}\) any additional strain or organization invariants. Then

\[
\Sigma_{\mu\nu}
=
-\frac{2}{\sqrt{-g}}
\frac{\delta A_{\mathrm{cons}}}{\delta g^{\mu\nu}}
\qquad (A.35)
\]

is the **entropic constraint stress tensor**. This is the term that allows ToE to describe bound matter, internal stresses, elastic response, and stable macroscopic identity without pretending that all matter is a free gas. It is the rigorous home for “structured information” in the source sector. Fluid and dust actions of this general type are standard in relativistic variational hydrodynamics. citeturn18view0turn16view1

The full ToE source tensor is therefore

\[
T_{\mu\nu}^{\mathrm{ToE}}
=
T_{\mu\nu}^{(S)}
+
\Theta_{\mu\nu}^{\mathrm{ent}}
+
\Sigma_{\mu\nu}.
\qquad (A.36)
\]

Equivalently, relative to the hydrodynamic velocity \(u^\mu\),

\[
T_{\mu\nu}^{\mathrm{ToE}}
=
\rho_{\mathrm{eff}}u_\mu u_\nu
+
p_{\mathrm{eff}}h_{\mu\nu}
+
2u_{(\mu}q_{\nu)}
+
\pi_{\mu\nu},
\qquad (A.37)
\]

with

\[
\rho_{\mathrm{eff}}
=
u^\mu u^\nu T_{\mu\nu}^{\mathrm{ToE}},
\qquad
p_{\mathrm{eff}}
=
\frac{1}{3}h^{\mu\nu}T_{\mu\nu}^{\mathrm{ToE}},
\qquad
q_\mu
=
-h_\mu{}^\alpha u^\beta T_{\alpha\beta}^{\mathrm{ToE}},
\qquad
\pi_{\mu\nu}
=
T_{\langle\mu\nu\rangle}^{\mathrm{ToE}}.
\qquad (A.38)
\]

In this form, every familiar Einstein source sector is already present: dust, radiation, perfect fluids, viscous media, anisotropic stresses, coherent scalar media, and bound organizational matter. The ToE claim is therefore not that scalar entropy equals \(T_{\mu\nu}\); it is that **the entropic field, together with its currents, distributions, and constraints, generates the unique rank-two object that coarse-grains to \(T_{\mu\nu}\)**. That is exactly the source-side completion demanded by Section 6 of *Letter III*. fileciteturn0file0

Conservation now follows in the correct way. If \(f_q\) obeys the relativistic Boltzmann equation,

\[
p^\alpha \nabla_\alpha f_q = C[f_q],
\qquad (A.39)
\]

and the collision term satisfies the moment invariant

\[
\int dP\, p^\nu C[f_q]=0,
\qquad (A.40)
\]

then

\[
\nabla_\mu \Theta^{\mu\nu}_{\mathrm{ent}}=0.
\qquad (A.41)
\]

If the coherent entropy field satisfies its Euler–Lagrange equation and the constraint variables \(\zeta_I\) satisfy their own variational equations, then diffeomorphism invariance of the full action implies

\[
\nabla_\mu T^{\mu\nu}_{\mathrm{ToE}}=0.
\qquad (A.42)
\]

At equilibrium, the same structure can be recovered from a thermodynamic generating functional. In covariant statistical mechanics, the equilibrium stress-energy tensor can be obtained as a functional derivative of the partition functional with respect to the inverse-temperature four-vector, and in relativistic fluid actions the equilibrium Lagrangian may be written in terms of pressure. This gives a second, independent route from entropy to source tensor, now from the partition-functional side rather than the moment side. citeturn16view1turn18view0

Finally, the local second law has its proper place here. The entropy current \(J^\mu_{\mathrm{ent}}\) of the non-equilibrium effective theory satisfies

\[
\nabla_\mu J^\mu_{\mathrm{ent}} \ge 0,
\qquad (A.43)
\]

so the entropic source tensor is not merely conserved; it also carries the irreversible bookkeeping required by ToE’s arrow-of-time sector. Modern non-equilibrium EFT derivations show that local entropy-production positivity follows from symmetry and unitarity assumptions in the hydrodynamic regime. citeturn18view1turn14academia3

## Einstein limit and unification theorem

The low-energy Einstein limit is obtained by taking the simultaneous infrared and local-equilibrium limit

\[
q\to1,
\qquad
\Delta_{\mu\nu}^{\mathrm{IG}}\to0,
\qquad
q_\mu\to0,
\qquad
\pi_{\mu\nu}\to0,
\qquad
\Sigma_{\mu\nu}\to\Sigma_{\mu\nu}^{\mathrm{eq}}.
\qquad (A.44)
\]

Then \(f_q\) reduces to the ordinary Maxwell–Jüttner/Boltzmann sector, the dissipative pieces disappear, the information-geometry corrections decouple, and the full ToE source tensor reduces to the generalized perfect-fluid form

\[
T_{\mu\nu}^{\mathrm{ToE}}
\longrightarrow
(\rho+p)u_\mu u_\nu + p\, g_{\mu\nu}.
\qquad (A.45)
\]

This is the Einstein fluid tensor. The special cases are immediate:

\[
p\ll \rho
\quad\Longrightarrow\quad
T_{\mu\nu}\approx \rho\,u_\mu u_\nu
\qquad\text{(dust / cold matter)},
\qquad (A.46)
\]

\[
m=0,\quad \rho=3p
\quad\Longrightarrow\quad
T_{\mu\nu}= (\rho+p)u_\mu u_\nu + p\,g_{\mu\nu}
\qquad\text{(radiation)},
\qquad (A.47)
\]

\[
K=X
\quad\Longrightarrow\quad
T_{\mu\nu}^{(S)}
=
\nabla_\mu S\nabla_\nu S
-
g_{\mu\nu}
\left[
\frac{1}{2}\nabla_\alpha S\nabla^\alpha S + U(S)
\right]
\qquad\text{(canonical scalar sector)}.
\qquad (A.48)
\]

The scalar-field result is not foreign to Einstein matter; it is one of its standard admissible sectors, and when \(\nabla_\mu S\) is timelike it is already equivalent to a perfect fluid. Thus the Einstein RHS is recovered not by forcing entropy into a pre-existing slot, but by passing from the entropic field, through moment formation and variational projection, into the familiar GR matter classes. citeturn17view0turn17view1turn18view0

The final effective field equation of the completed ToE program is therefore

\[
G_{\mu\nu}
+
\Lambda_{\mathrm{ent}} g_{\mu\nu}
=
\frac{8\pi G_{\mathrm{eff}}}{c^4}\,
T_{\mu\nu}^{\mathrm{ToE}}
+
\frac{8\pi G_{\mathrm{eff}}}{c^4}\,
\Delta_{\mu\nu}^{\mathrm{IG}}.
\qquad (A.49)
\]

In the strict Einstein limit,

\[
G_{\mathrm{eff}}\to G,
\qquad
\Lambda_{\mathrm{ent}}\to \Lambda,
\qquad
\Delta_{\mu\nu}^{\mathrm{IG}}\to0,
\qquad
T_{\mu\nu}^{\mathrm{ToE}}\to T_{\mu\nu}^{\mathrm{Einstein}},
\qquad (A.50)
\]

and one recovers

\[
G_{\mu\nu}
+
\Lambda g_{\mu\nu}
=
\frac{8\pi G}{c^4}\,
T_{\mu\nu}^{\mathrm{Einstein}}.
\qquad (A.51)
\]

A compact theorem may now be stated.

**Theorem.**  
Let \((\mathcal M_N,I_{AB},S)\) be a ToE information manifold with nonvanishing entropy gradient on a smooth four-dimensional coarse-grained section \(X(M_4)\). Let the Fisher metric be Lorentz-lifted by the Obidi map \(\hat G_{AB}=\mathcal L_S[I]_{AB}\) with \(\sigma>1\), let the lifted action reduce to (A.16) after fibre integration, and let the microscopic information content be encoded by the moment-generating distribution \(f_q\) together with coherent and constraint sectors \(A_S\) and \(A_{\mathrm{cons}}\). Then the effective four-dimensional field equation is (A.49). In the infrared local-equilibrium Boltzmann–Gibbs limit, it reduces exactly to the Einstein field equation (A.51).

The proof is the chain already established above: the Lorentzian lift generates the causal metric; the pullback and fibre reduction generate the Einstein tensor; the moment map and Hilbert variation generate the source tensor; and the equilibrium limit suppresses non-Einstein corrections. The geometric side and the source side are thus **two tensorial manifestations of the same underlying entropic-information structure**, which is precisely the monistic claim of ToE, now written in a fully covariant mathematical form. This conclusion is aligned with the ambition announced in *Letter III*, while making explicit the derivational machinery that the main text only sketches. fileciteturn0file0 citeturn16view3turn16view4turn16view2

## References

The references most useful for this appendix, and most directly connected to the derivational architecture just given, are the following.

Obidi, J. O. *Theory of Entropicity Living Review Letters Series — Letter III: From Information Geometry to Information Gravity*. May 2026. fileciteturn0file0

Fisher, R. A. “Theory of Statistical Estimation.” *Proceedings of the Cambridge Philosophical Society* 22 (1925): 700–725.

Rao, C. R. “Information and the Accuracy Attainable in the Estimation of Statistical Parameters.” *Bulletin of the Calcutta Mathematical Society* 37 (1945): 81–91.

Čencov, N. N. *Statistical Decision Rules and Optimal Inference*. American Mathematical Society, 1982.

Amari, S., and H. Nagaoka. *Methods of Information Geometry*. American Mathematical Society and Oxford University Press, 2000.

Ay, N., J. Jost, H. V. Lê, and L. Schwachhöfer. “Information Geometry and Sufficient Statistics.” *Probability Theory and Related Fields* 162 (2015): 327–364. citeturn15view1

Bekenstein, J. D. “The Relation between Physical and Gravitational Geometry.” *Physical Review D* 48 (1993): 3641–3647. citeturn15view0

Jacobson, T. “Thermodynamics of Spacetime: The Einstein Equation of State.” *Physical Review Letters* 75 (1995): 1260–1263. citeturn20academia0

Brown, J. D. “Action Functionals for Relativistic Perfect Fluids.” *Classical and Quantum Gravity* 10 (1993): 1579–1606. citeturn18view0

Becattini, F. “Covariant Statistical Mechanics and the Stress-Energy Tensor.” *Physical Review Letters* 108 (2012): 244502. citeturn16view1

Faraoni, V. “The Correspondence between a Scalar Field and an Effective Perfect Fluid.” *Physical Review D* 85 (2012): 024040. citeturn17view0

Arroja, F., and M. Sasaki. “A Note on the Equivalence of a Barotropic Perfect Fluid with a K-Essence Scalar Field.” *Physical Review D* 81 (2010): 107301. citeturn17view1

Sarbach, O., and T. Zannias. “Relativistic Kinetic Theory: An Introduction.” *AIP Conference Proceedings* 1548 (2013): 134–155. citeturn16view0

Caticha, A. “The Information Geometry of Space-time.” arXiv:1909.09657 (2019). citeturn16view3

Matsueda, H. “Emergent General Relativity from Fisher Information Metric.” arXiv:1310.1831 (2013). citeturn16view4

Bianconi, G. “Gravity from Entropy.” *Physical Review D* 111 (2025): 066001. citeturn16view2

Glorioso, P., and H. Liu. “The Second Law of Thermodynamics from Symmetry and Unitarity.” arXiv:1612.07705 (2016). citeturn18view1