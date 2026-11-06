# Unit 4 — Physical Chemistry
## Complete explained study notes: partial molar properties, fugacity and statistical thermodynamics

**Source basis:** the 19-page handwritten Unit 4 notebook scan supplied for this project. The original order and all five original numerical questions are retained. Supplementary explanations and scientific clarifications are explicitly labelled.

> **Reading convention.** “Source record” identifies a statement, equation or drawing retained from the handwritten notes. “Explanation” expands the idea for learning. “Scientific clarification” flags notation that needs care; it does not erase what was written in the source.

## Contents
1. Learning objectives and notation
2. Partial molar properties (source pp. 1–5)
3. Fugacity (source pp. 5–8)
4. Statistical thermodynamics and distributions (source pp. 8–10)
5. Maxwell–Boltzmann distribution and partition function (source pp. 10–13)
6. Molecular partition functions (source pp. 13–14)
7. Translational partition function (source pp. 14–15)
8. Rotational partition function (source pp. 16–18)
9. Vibrational partition function (source p. 18)
10. Original numerical questions (source p. 19)
11. Formula reference
12. Common conceptual difficulties
13. Final chapter revision sheet
14. Scientific clarification log
15. Source figure inventory
16. Answers to supplementary checkpoints

## 1. Learning objectives and notation

After studying this unit, you should be able to explain why mixture properties depend on composition; define and calculate partial molar properties; derive the Gibbs–Duhem relation; distinguish fugacity from pressure; connect a microscopic energy-level picture to macroscopic thermodynamics; identify the three standard ensembles and the Maxwell–Boltzmann, Bose–Einstein and Fermi–Dirac cases; derive the Boltzmann population law and molecular partition functions; and use translational, rotational and vibrational partition functions in the five supplied problems.

### Symbols used repeatedly

- **T, P:** absolute temperature and pressure. Units: kelvin (K) and pascal (Pa), unless another pressure unit is stated.
- **nᵢ, Nᵢ:** amount of component i in moles, or number of particles in an energy level, depending on context.
- **U, H, A, G:** internal energy, enthalpy, Helmholtz energy and Gibbs energy. Unit: joule (J).
- **S, V:** entropy and volume. Units: joule per kelvin (J K⁻¹) and cubic metre (m³).
- **μᵢ:** chemical potential of component i. Unit: joule per mole (J mol⁻¹).
- **X̄ᵢ:** partial molar property of component i; units are the corresponding property per mole.
- **R, k, Nₐ:** gas constant, Boltzmann constant and Avogadro constant.
- **h, ℏ:** Planck constant and reduced Planck constant, with ℏ = h/(2π). Unit: joule second (J s).
- **q, Q:** single-molecule and whole-system partition functions; conventions vary between textbooks. They are dimensionless.
- **gᵢ:** degeneracy, or number of states having energy level i. It is a dimensionless count.
- **β:** inverse thermal energy. Its mathematical definition is given in the Maxwell–Boltzmann section; its unit is J⁻¹.
- **Z:** compressibility factor in the fugacity section; some statistical-mechanics texts use Z for a partition function.
- **φ:** fugacity coefficient; dimensionless.
- **f:** fugacity; it has the same units as pressure.

**Notation warning:** the same letter may have different meanings in different sections. In the fugacity section, \(Z\) denotes compressibility factor. In statistical mechanics, many books use \(Q\) or \(\mathcal Z\) for the canonical partition function. This chapter uses lowercase \(q\) for the molecular/single-particle partition function to follow the notebook.

## 2. Partial molar properties (source pp. 1–5)

### 2.1 Extensive and intensive properties

An **extensive property** changes with the amount of material. The notebook lists internal energy \(U\), entropy \(S\), Helmholtz energy \(A\), Gibbs energy \(G\), enthalpy \(H\), and volume \(V\). For a homogeneous system, doubling the amount at unchanged state and composition doubles an extensive property.

An **intensive property** does not scale with the total amount. Temperature, pressure, density and composition expressed as mole fraction are common examples. An extensive property divided by total amount is generally an intensive molar property.

### 2.2 Closed systems and composition variables

A closed system exchanges no matter with its surroundings. It may still exchange energy. Its total amount of each component remains fixed during a process, although composition is a state variable when comparing different closed-system preparations.

For a mixture property \(X\), the notebook writes

\[
X=X(T,P,n_1,n_2,\ldots,n_j).
\]

The total differential follows from the multivariable chain rule. Each partial derivative is written as a true fraction, and the expression is split across aligned lines:

\[\begin{gathered}
dX=\left(\frac{\partial X}{\partial T}\right)_{P,n_i}dT\\[5pt]
\quad+\left(\frac{\partial X}{\partial P}\right)_{T,n_i}dP\\[5pt]
\quad+\sum_i\left(\frac{\partial X}{\partial n_i}\right)_{T,P,n_{j\ne i}}dn_i.
\end{gathered}\]

Here the subscript states which variables are held constant while taking the partial derivative. The composition term for component \(i\) holds all other component amounts fixed.

### 2.3 Definition of a partial molar property

The partial molar property of component \(i\) is the change in the total extensive property when an infinitesimal amount of component \(i\) is added at constant temperature and pressure, with all other component amounts fixed:

\[
\boxed{\bar X_i=\left(\frac{\partial X}{\partial n_i}\right)_{T,P,n_{j\ne i}}.}
\]

Important examples retained from the first page are

\[
\bar V_i=\left(\frac{\partial V}{\partial n_i}\right)_{T,P,n_{j\ne i}},\qquad
\bar G_i=\left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_{j\ne i}},
\]

\[
\bar U_i=\left(\frac{\partial U}{\partial n_i}\right)_{T,P,n_{j\ne i}}.
\]

For Gibbs energy, \(\bar G_i\) is the **chemical potential** \(\mu_i\). It measures how the Gibbs energy changes when a small amount of that component is added under the stated constraints.

### 2.4 Partial molar volume and the water–ethanol illustration

The partial molar volume is

\[
\boxed{\bar V_i=\left(\frac{\partial V}{\partial n_i}\right)_{T,P,n_{j\ne i}}.}
\]

It is not necessarily the pure-component molar volume. It describes the incremental volume contribution of component \(i\) in the mixture at the mixture's current composition.

**Source illustration (p. 2).** The notebook sketches one mole of water added to water and one mole of water added to ethanol. It records a volume increase of about \(18\,\mathrm{cm^3}\) for the water-in-water case and about \(14\,\mathrm{cm^3}\) for water added to ethanol. The physical lesson is that the same added component can produce a different volume increment in a different molecular environment.

The original page also contains the beaker sketches and a small molecular arrangement sketch. Their labels and the two recorded volume increments are retained in the figure below.

![Figure 1. Complete source sketch: one mole of water added to water and to ethanol, including the volume increments and molecular arrangement.](assets/figures/figure-01.png)

The page also plots the partial molar volumes of water and ethanol against the mole fraction of ethanol. The two curves change with composition, showing that a partial molar volume is not generally a constant over the full composition range.

![Figure 2. Original partial-molar-volume composition graph from source page 2.](assets/figures/figure-02.png)



### 2.5 Binary solution and total volume

For a binary mixture A–B, a small change in volume is

\[
dV=\left(\frac{\partial V}{\partial n_A}\right)_{T,P,n_B}dn_A
+\left(\frac{\partial V}{\partial n_B}\right)_{T,P,n_A}dn_B.
\]

Recognising the derivatives as partial molar volumes gives

\[
dV=\bar V_A\,dn_A+\bar V_B\,dn_B.
\]

For a homogeneous mixture, the Euler relation for an extensive property gives

\[
\boxed{V=n_A\bar V_A+n_B\bar V_B.}
\]

This is a composition-dependent sum. It does not assert that the volume of mixing is zero. The volume change on mixing is assessed by comparing the actual mixture volume with the sum of the pure-component volumes at the same temperature and pressure.

### 2.6 Chemical potential and Gibbs energy

The chemical potential is the partial molar Gibbs energy:

\[
\boxed{\mu_i=\bar G_i=\left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_{j\ne i}}.}
\]

For a mixture whose Gibbs energy is an extensive property, Euler's theorem gives

\[
\boxed{G=\sum_i n_i\mu_i.}
\]

At constant temperature and pressure, differentiating this expression gives

\[
dG=\sum_i n_i\,d\mu_i+\sum_i\mu_i\,dn_i.
\]

But the fundamental composition differential at constant \(T,P\) is

\[
(dG)_{T,P}=\sum_i\mu_i\,dn_i.
\]

Comparing the two expressions yields the **Gibbs–Duhem equation**:

\[
\boxed{\sum_i n_i\,d\mu_i=0}\qquad (T,P\text{ fixed}).
\]

For a binary mixture,

\[
n_A d\mu_A+n_B d\mu_B=0,
\qquad d\mu_A=-\frac{n_B}{n_A}d\mu_B.
\]

The relation says that the chemical potentials in a mixture cannot change independently when temperature and pressure are fixed. A change in one is constrained by the others.

The notebook lists analogous Gibbs–Duhem forms for partial molar entropy, enthalpy, Gibbs energy, volume and internal energy. In general, for an extensive property \(M\),

\[
\sum_i n_i\,d\bar M_i=0
\]

when the appropriate natural variables of \(M\) are held fixed.

### 2.7 Closed-system thermodynamic relations and chemical-potential forms

For a closed, fixed-composition simple compressible system,

\[
dG=V\,dP-S\,dT.
\]

Thus,

\[
\left(\frac{\partial G}{\partial T}\right)_P=-S,
\qquad
\left(\frac{\partial G}{\partial P}\right)_T=V.
\]

The notebook then uses the Legendre-transform definitions

\[
G=H-TS=U+PV-TS,
\qquad U=G+TS-PV.
\]

Differentiating the second relation and substituting the mixture differential for \(dG\) gives

\[
dU=\sum_i\mu_i\,dn_i+T\,dS-P\,dV.
\]

At constant entropy and volume, the coefficient of \(dn_i\) is the partial molar internal energy in the corresponding natural-variable description. The standard chemical-potential identities are

\[\begin{gathered}
\mu_i=\left(\frac{\partial U}{\partial n_i}\right)_{S,V,n_{j\ne i}}\\[5pt]
\mu_i=\left(\frac{\partial H}{\partial n_i}\right)_{S,P,n_{j\ne i}}\\[5pt]
\mu_i=\left(\frac{\partial A}{\partial n_i}\right)_{T,V,n_{j\ne i}}\\[5pt]
\mu_i=\left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_{j\ne i}}.
\end{gathered}\]

**Why the conditions matter:** a partial derivative is not fully defined unless the fixed variables are stated. Use the natural variables of the thermodynamic potential: \(U(S,V,n_i)\), \(H(S,P,n_i)\), \(A(T,V,n_i)\), and \(G(T,P,n_i)\).


### Check your understanding: partial molar properties

1. How is a partial molar volume different from the molar volume of a pure liquid?
2. Why must the amounts of all other components be held fixed when defining \(\bar V_A\)?
3. Starting from \(V=n_A\bar V_A+n_B\bar V_B\), explain what the two terms contribute to the total mixture volume.
4. At constant temperature and pressure, what does the binary Gibbs–Duhem equation tell you about changes in \(\mu_A\) and \(\mu_B\)?

**Numerical practice.** A binary mixture contains \(1.50\,\mathrm{mol}\) of A and \(0.50\,\mathrm{mol}\) of B. At the stated composition, \(\bar V_A=20.0\,\mathrm{cm^3\,mol^{-1}}\) and \(\bar V_B=16.0\,\mathrm{cm^3\,mol^{-1}}\). Calculate the total volume using the Euler relation.

*Try the four questions and the numerical before checking Section 16.*

## 3. Fugacity (source pp. 5–8)

### 3.1 Meaning

Fugacity is an effective pressure that allows the chemical potential of a real gas to be written in a form resembling the ideal-gas equation. Real gases deviate from ideal behaviour because molecules interact and occupy finite volume. Fugacity incorporates these deviations into a pressure-like quantity.

The notebook introduces

\[
\boxed{f=\phi P,}
\]

where \(f\) is fugacity and \(\phi\) is the dimensionless fugacity coefficient. In the ideal-gas limit, \(\phi\to1\), so \(f\to P\).

### 3.2 Pressure dependence of Gibbs energy

For a pure substance at constant temperature,

\[
dG=V\,dP.
\]

For one mole,

\[
dG_m=V_m\,dP.
\]

Integration between initial pressure \(P_i\) and final pressure \(P_f\) gives

\[
G_m(P_f)-G_m(P_i)=\int_{P_i}^{P_f}V_m(P)\,dP.
\]

For an ideal gas, \(V_m=RT/P\), hence

\[
G_m(P_f)-G_m(P_i)=RT\int_{P_i}^{P_f}\frac{1}{P}\,dP.
\]

Evaluating the integral gives

\[
G_m(P_f)-G_m(P_i)=RT\left[\ln P\right]_{P_i}^{P_f}.
\]

Therefore,

\[
G_m(P_f)-G_m(P_i)=RT\ln\left(\frac{P_f}{P_i}\right).
\]

For an ideal gas, choosing the standard pressure \(P^\circ\) as the reference and writing the final pressure as \(P\),

\[
\mu=\mu^\circ+RT\ln\left(\frac{P}{P^\circ}\right).
\]

For a real gas pressure is replaced by fugacity:

\[
\boxed{\mu=\mu^\circ+RT\ln\left(\frac{f}{P^\circ}\right).}
\]

This is the key practical role of fugacity. The ratio inside the logarithm must be dimensionless; the standard pressure is therefore shown explicitly.

### 3.3 Relating fugacity to the compressibility factor

The compressibility factor is

\[
Z=\frac{PV_m}{RT}.
\]

For an ideal gas, \(Z=1\). Starting with

\[
RT\,d\ln f=V_m\,dP,
\]

and subtracting the ideal-gas contribution \(RT\,d\ln P=RT\,dP/P\),

\[
d\ln\left(\frac{f}{P}\right)=\left(\frac{V_m}{RT}-\frac{1}{P}\right)dP.
\]

Since \(\phi=f/P\) and \(V_m/(RT)=Z/P\), substituting into the difference between the real-gas and ideal-gas expressions gives

\[
d\ln\phi
=\left(\frac{Z}{P}-\frac{1}{P}\right)dP
=\frac{Z-1}{P}\,dP.
\]

Using the ideal-gas limiting condition \(\phi\to1\) as \(P\to0\), integration gives

\[
\boxed{\ln\phi(P)=\int_0^P\frac{Z(P',T)-1}{P'}\,dP'.}
\]

### 3.4 Physical interpretation of the sign

The notebook associates \(Z<1\) with attractive interactions and \(Z>1\) with repulsive effects. This is a useful qualitative interpretation in the relevant pressure range, but one should not treat a single value of \(Z\) as a universal interaction label at every pressure. The sign of \(\ln\phi\) depends on the integral over the full pressure interval.

When the integrand remains negative, \(\phi<1\) and therefore \(f<P\); when it remains positive, \(\phi>1\) and \(f>P\). Fugacity is an effective thermodynamic pressure, not a directly measured mechanical pressure.

### Check your understanding: fugacity

1. What does the fugacity coefficient \(\phi\) measure?
2. What happens to fugacity as a gas approaches ideal behaviour?
3. Why is the ratio \(f/P^\circ\), rather than a dimensional pressure by itself, placed inside the logarithm for chemical potential?
4. In the pressure range considered, what does \(\phi<1\) indicate about the effective pressure relative to the mechanical pressure?

**Numerical practice.** Suppose a gas is described over a pressure interval by the illustrative model \(Z=1+aP\), where \(a=0.020\,\mathrm{bar^{-1}}\). At \(P=2.00\,\mathrm{bar}\), use the fugacity integral to calculate \(\phi\) and then \(f\).

*Try the questions first. The worked calculation is in Section 16.*

## 4. Statistical thermodynamics and distributions (source pp. 8–10)

### 4.1 What statistical thermodynamics connects

Statistical thermodynamics links microscopic descriptions (molecular energy levels and populations) to macroscopic properties such as internal energy, entropy, enthalpy and Gibbs energy. Classical thermodynamics describes bulk-state relationships; statistical thermodynamics explains how those bulk properties arise from the allowed microscopic states and their probabilities.

### 4.2 Three distribution families

**Maxwell–Boltzmann (MB):** the classical distribution for distinguishable particles in the dilute, classical regime. There is no quantum occupancy restriction that prevents many particles from occupying the same one-particle state.

**Bose–Einstein (BE):** applies to indistinguishable bosons with symmetric many-particle wavefunctions. Any number of bosons may occupy the same single-particle state.

**Fermi–Dirac (FD):** applies to indistinguishable fermions with antisymmetric many-particle wavefunctions. The Pauli exclusion principle permits at most one fermion in each complete single-particle quantum state (with spin states counted separately).

The notebook describes MB particles as distinguishable, BE particles as indistinguishable and symmetric, and FD particles as indistinguishable and antisymmetric. Its shorthand “only one particle can occupy any energy level” for Fermi–Dirac requires the clarification that the restriction is on a quantum state, not necessarily an entire energy level when that level is degenerate.

### 4.3 Ensembles

An ensemble is a conceptual collection of many replicas of a system, all prepared under the same macroscopic constraints. The source drawings show nine cells for each ensemble, with the corresponding fixed quantities marked in each cell.

**Microcanonical ensemble**
- Fixed quantities: N, V and E.
- No energy or particle exchange; the system is isolated.

**Canonical ensemble**
- Fixed quantities: N, V and T.
- Energy can be exchanged with a heat bath; particle number remains fixed.

**Grand-canonical ensemble**
- Fixed quantities: chemical potential μ, V and T.
- Both energy and particles can be exchanged; this represents an open system.

![Figure 3. Source microcanonical ensemble grid, with N, V and E fixed in each replica.](assets/figures/figure-03.png)

![Figure 4. Source canonical ensemble grid, with N, V and T fixed in each replica.](assets/figures/figure-04.png)

![Figure 5. Source grand-canonical ensemble grid, with μ, V and T fixed in each replica.](assets/figures/figure-05.png)

### Check your understanding: statistical thermodynamics and ensembles

1. In one sentence, distinguish a microstate from a macrostate.
2. Which ensemble is appropriate when \(N,V,T\) are fixed but the system can exchange heat with its surroundings?
3. Which quantities can be exchanged in the grand-canonical ensemble?
4. Why can bosons share a single quantum state, whereas fermions are subject to the Pauli exclusion principle?

**Application question.** Classify each situation as microcanonical, canonical or grand canonical: (a) a perfectly isolated rigid container; (b) a sealed container held in a large constant-temperature bath; (c) a small region that can exchange both heat and particles with a reservoir.

*The answers and reasoning are collected in Section 16.*

## 5. Maxwell–Boltzmann distribution and partition function (source pp. 10–13)

### 5.1 Energy levels, populations and degeneracy

Suppose \(N\) distinguishable particles are distributed among energy levels \(E_0,E_1,E_2,\ldots\). Let \(N_i\) be the number of particles in level \(i\), and let \(g_i\) be the degeneracy of that level (the number of distinct states having the same energy).

The particle-number and total-energy constraints are

\[
N=\sum_i N_i,
\qquad E=\sum_i N_iE_i.
\]

A **microstate** specifies the detailed state occupied by every particle. A **macrostate** specifies only the occupation numbers \(N_i\). Many microstates may correspond to one macrostate.

![Figure 6. Source energy-level population ladder showing level labels, populations and the microstate/macrostate note.](assets/figures/figure-06.png)

### 5.2 Multiplicity of a distribution

For distinguishable particles, the number of ways of assigning particles to the levels is

\[
W_0=\frac{N!}{\prod_iN_i!}.
\]

If level \(i\) has degeneracy \(g_i\), each of its \(N_i\) particles has \(g_i\) possible states, so

\[
\boxed{W=\frac{N!}{\prod_iN_i!}\prod_i g_i^{N_i}.}
\]

Taking logarithms,

\[
\ln W=\ln N!+\sum_iN_i\ln g_i-\sum_i\ln(N_i!).
\]

For large numbers, Stirling's approximation is

\[
\ln x!\approx x\ln x-x.
\]

Using \(\sum_iN_i=N\),

\[
\boxed{\ln W=N\ln N+\sum_iN_i\ln g_i-\sum_iN_i\ln N_i.}
\]

This is the same logarithmic multiplicity expression developed over the source's pp. 10–11.

### 5.3 Most probable distribution: Lagrange-multiplier derivation

At equilibrium the overwhelmingly most probable macrostate is the one that maximises \(W\), equivalently \(\ln W\), subject to fixed particle number and total energy. Introduce multipliers \(\alpha\) and \(\beta\):

\[
\mathcal L=\ln W+\alpha\left(N-\sum_iN_i\right)
+\beta\left(E-\sum_iN_iE_i\right).
\]

Here the constraint terms are written with plus signs for both multipliers; differentiating gives the negative energy term needed for a decaying Boltzmann population. Differentiating with respect to \(N_i\) and setting the result to zero,

\[
\frac{\partial\ln W}{\partial N_i}-\alpha-\beta E_i=0.
\]

From the logarithmic multiplicity expression,

\[
\frac{\partial\ln W}{\partial N_i}=\ln N+\ln g_i-\ln N_i.
\]

Therefore,

\[
\ln\left(\frac{Ng_i}{N_i}\right)-\alpha-\beta E_i=0,
\]

which gives

\[
N_i=Ng_i e^{-\alpha}e^{-\beta E_i}.
\]

Apply the number constraint:

\[
N=\sum_iN_i=Ne^{-\alpha}\sum_i g_i e^{-\beta E_i}.
\]

Define the single-particle partition function

\[
\boxed{q=\sum_i g_i e^{-\beta E_i}.}
\]

It follows that \(e^{-\alpha}=1/q\), and hence

\[
\boxed{N_i=N\frac{g_i e^{-\beta E_i}}{q}.}
\]

The population fraction of level \(i\) is therefore

\[
\boxed{\frac{N_i}{N}=\frac{g_i e^{-\beta E_i}}{q}.}
\]

### 5.4 Boltzmann factor and beta

The factor \(e^{-\beta E_i}\) is the **Boltzmann factor**. Lower-energy states receive larger statistical weights; higher-energy states are less populated, with the rate of decrease controlled by temperature.

\[
\boxed{\beta=\frac{1}{kT}.}
\]

At higher temperature, \(\beta\) is smaller and the relative penalty for higher-energy states is weaker. At lower temperature, populations are concentrated more strongly in low-energy states.

When the sum is taken over every individual quantum state rather than over energy levels grouped by degeneracy,

\[
q=\sum_{r\in\mathrm{states}}e^{-\beta E_r}.
\]

The two forms are equivalent: a level with energy \(E_i\) and degeneracy \(g_i\) contributes \(g_i e^{-\beta E_i}\).

### Check your understanding: Maxwell–Boltzmann distribution

1. What physical information is represented by the degeneracy \(g_i\)?
2. Why is the partition function required in the population formula?
3. What happens to the relative population of a higher-energy state when temperature increases?
4. Explain why the Boltzmann factor is smaller for a higher energy when temperature is fixed.

**Numerical practice.** Consider two energy levels with \(E_0=0\), \(g_0=1\), \(E_1=2kT\) and \(g_1=3\). Calculate (a) the partition function considering only these two levels, and (b) the fraction of particles in each level.

*Attempt the normalisation yourself before checking Section 16.*

### 5.5 Corrected Boltzmann counting

The notebook adds a “corrected Boltzmann” expression after introducing degeneracy. The standard Maxwell–Boltzmann multiplicity with degeneracy is the expression above. For quantum BE or FD statistics, the counting formula changes; those distributions are not obtained merely by adding a degeneracy factor to the classical MB formula.

## 6. Molecular partition functions (source pp. 13–14)

### 6.1 Separation of molecular energy

For a molecule whose translational, rotational, vibrational and electronic motions can be treated as separable, the total energy is written

\[
E=E_{\mathrm{trans}}+E_{\mathrm{rot}}+E_{\mathrm{vib}}+E_{\mathrm{elec}}.
\]

The Boltzmann factor then factorises:

\[
e^{-\beta E}=e^{-\beta E_{\mathrm{trans}}}
 e^{-\beta E_{\mathrm{rot}}}e^{-\beta E_{\mathrm{vib}}}
 e^{-\beta E_{\mathrm{elec}}}.
\]

When the state sums are independent products, the molecular partition function is

\[
\boxed{q=q_{\mathrm{trans}}q_{\mathrm{rot}}q_{\mathrm{vib}}q_{\mathrm{elec}}.}
\]

This factorisation assumes that the molecular Hamiltonian and accessible states are sufficiently separable; strong coupling between modes can invalidate the simple product approximation.

### Check your understanding: molecular partition functions

1. Why can the molecular partition function be written as a product when the energy contributions are separable?
2. Name the four molecular contributions shown in the source notes.
3. What physical situation could make the simple product approximation less reliable?

**Numerical practice.** For a simplified molecule, suppose \(q_{\mathrm{trans}}=40\), \(q_{\mathrm{rot}}=5\), \(q_{\mathrm{vib}}=1.2\), and \(q_{\mathrm{elec}}=1\). Calculate the total molecular partition function.

*The worked answer is in Section 16.* The source writes the product for translational, rotational and vibrational contributions and shows the electronic factor in the energy decomposition.

## 7. Translational partition function (source pp. 14–15)

### 7.1 Particle in a three-dimensional box

The notebook models a particle of mass \(m\) in a rectangular box with sides \(a,b,c\).

![Figure 7. Original rectangular three-dimensional particle-in-a-box sketch, showing the side labels a, b and c.](assets/figures/figure-07.png)

The source writes \(g_i=1\) beside this sketch; this notebook notation is retained here for the displayed state.

For quantum numbers \(n_x,n_y,n_z=1,2,\ldots\),

\[
E_{n_xn_yn_z}=\frac{h^2}{8m}
\left(\frac{n_x^2}{a^2}+\frac{n_y^2}{b^2}+\frac{n_z^2}{c^2}\right).
\]

The translational partition function is the sum over all allowed states:

\[
q_{\mathrm{trans}}=\sum_{n_x=1}^{\infty}\sum_{n_y=1}^{\infty}\sum_{n_z=1}^{\infty}
\exp\left[-\frac{E_{n_xn_yn_z}}{kT}\right].
\]

Since the energy is a sum of independent x-, y- and z-contributions, the triple sum separates into a product of three one-dimensional sums.

### 7.2 Continuum approximation and Gaussian integral

At ordinary temperatures and for macroscopic box dimensions, translational energy levels are very closely spaced. The sums may be approximated by integrals. The source uses the Gaussian integral

\[
\int_0^{\infty}e^{-\omega x^2}\,dx
=\frac12\left(\frac{\pi}{\omega}\right)^{1/2},\qquad \omega>0.
\]

For the x direction, the integral gives

\[
\int_0^{\infty}\exp\left(-\frac{h^2n_x^2}{8mkTa^2}\right)dn_x
=\frac{a}{h}\left(2\pi mkT\right)^{1/2}.
\]

The y and z integrals give the same form with \(b\) and \(c\). Multiplying all three contributions and using \(V=abc\),

\[
\boxed{q_{\mathrm{trans}}=V\left(\frac{2\pi mkT}{h^2}\right)^{3/2}.}
\]

### 7.3 Thermal de Broglie wavelength

Define the thermal de Broglie wavelength

\[
\boxed{\Lambda=\frac{h}{(2\pi mkT)^{1/2}}.}
\]

Then

\[
\boxed{q_{\mathrm{trans}}=\frac{V}{\Lambda^3}.}
\]

The partition function per unit volume is

\[
\boxed{\frac{q_{\mathrm{trans}}}{V}=\frac{1}{\Lambda^3}.}
\]

For one mole, use molecular mass \(m=M/N_A\) and \(k=R/N_A\). The molar-volume form can be written

\[
q_{\mathrm{trans}}=V_m\left(\frac{2\pi MRT}{N_Ah^2}\right)^{3/2}.
\]

At fixed particle mass, translational partition function increases linearly with volume and as \(T^{3/2}\) with temperature.

### Check your understanding: translational partition function

1. Why does the three-dimensional translational partition function contain the power \(3/2\)?
2. What does the thermal de Broglie wavelength represent in this model?
3. At fixed mass and volume, by what factor does \(q_{\mathrm{trans}}\) change if the absolute temperature is doubled?

**Numerical practice.** A particle has mass \(m=4.65\times10^{-26}\,\mathrm{kg}\). At \(T=300\,\mathrm{K}\), it moves in a box of volume \(V=1.00\times10^{-3}\,\mathrm{m^3}\). Calculate its thermal de Broglie wavelength and translational partition function. Use \(h=6.62607015\times10^{-34}\,\mathrm{J\,s}\) and \(k=1.380649\times10^{-23}\,\mathrm{J\,K^{-1}}\).

*Work in SI units. The worked calculation is in Section 16.*

## 8. Rotational partition function (source pp. 16–18)

### 8.1 Rigid-rotor model

A diatomic molecule is approximated as two point masses separated by a fixed internuclear distance \(r\). Its moment of inertia about the centre of mass is

\[
I=\mu r^2,
\qquad \mu=\frac{m_1m_2}{m_1+m_2},
\]

where \(\mu\) is the reduced mass.

![Figure 8. Original diatomic rigid-rotor sketch from source page 16.](assets/figures/figure-08.png)

### 8.2 Rotational energy levels and degeneracy

For rotational quantum number \(J=0,1,2,\ldots\),

\[
E_J=\frac{J(J+1)h^2}{8\pi^2I},
\qquad g_J=2J+1.
\]

Therefore,

\[
q_{\mathrm{rot}}=\sum_{J=0}^{\infty}(2J+1)
\exp\left[-\frac{J(J+1)h^2}{8\pi^2IkT}\right].
\]

### 8.3 High-temperature approximation

When the thermal energy is much larger than the rotational level spacing, the sum may be approximated by an integral. The source sets

\[
c=\frac{h^2}{8\pi^2IkT},
\qquad q_{\mathrm{rot}}\approx\int_0^{\infty}(2J+1)e^{-cJ(J+1)}dJ.
\]

Use the substitution

\[
x=J(J+1),\qquad dx=(2J+1)dJ.
\]

The limits remain zero and infinity, so

\[
q_{\mathrm{rot}}\approx\int_0^{\infty}e^{-cx}dx
=\left[-\frac{1}{c}e^{-cx}\right]_0^{\infty}
=\frac{1}{c}.
\]

Thus,

\[
\boxed{q_{\mathrm{rot}}\approx\frac{8\pi^2IkT}{h^2}.}
\]

### 8.4 Rotational characteristic temperature and symmetry number

The characteristic rotational temperature is

\[
\boxed{\theta_{\mathrm{rot}}=\frac{h^2}{8\pi^2Ik}.}
\]

Hence the high-temperature expression is more generally

\[
\boxed{q_{\mathrm{rot}}\approx\frac{T}{\sigma\theta_{\mathrm{rot}}}.}
\]

The symmetry number \(\sigma\) corrects for rotations that exchange identical nuclei and leave the molecule physically indistinguishable. In the notebook, homonuclear diatomic molecules such as \(H_2\) have \(\sigma=2\), whereas heteronuclear diatomics such as HCl have \(\sigma=1\).

![Figure 9. Source sketches comparing H–H and H–Cl and their rotational symmetry numbers.](assets/figures/figure-09.png)

The notebook also records the rotational constant \(B\), in spectroscopic wavenumber units, and the equivalent form

\[
q_{\mathrm{rot}}\approx\frac{kT}{\sigma h c B},
\]

provided \(B\) is expressed in inverse-length units consistent with \(c\) and \(h\).

### Check your understanding: rotational partition function

1. Why does the rotational degeneracy equal \(2J+1\)?
2. What condition allows the rotational sum to be approximated by an integral?
3. Why is the symmetry number 2 for a homonuclear diatomic but 1 for a heteronuclear diatomic?
4. Which physical quantities determine the characteristic rotational temperature?

**Numerical practice.** Use the hydrogen-molecule data from the original Q3: \(I=4.6033\times10^{-48}\,\mathrm{kg\,m^2}\), \(T=2727^\circ\mathrm C\), and \(\sigma=2\). Convert the temperature to kelvin, calculate \(\theta_{\mathrm{rot}}\), and estimate \(q_{\mathrm{rot}}\) using the high-temperature formula. Use the SI values of \(h\) and \(k\) given above.

*Compare your calculated values with the worked answer in Section 16.*

## 9. Vibrational partition function (source p. 18)

### 9.1 Simple harmonic oscillator

The source models molecular vibration as a simple harmonic oscillator (SHO). The source visual is reproduced below.

![Figure 10. Original source-page vibrational section and adjacent oscillator energy equations.](assets/figures/figure-10.png)

The allowed energy levels are

\[
E_v=\left(v+\frac12\right)h\nu,
\qquad v=0,1,2,\ldots
\]

For a non-degenerate vibrational mode, \(g_v=1\). The vibrational partition function is

\[
q_{\mathrm{vib}}=\sum_{v=0}^{\infty}e^{-\beta E_v}
=\sum_{v=0}^{\infty}\exp\left[-\left(v+\frac12\right)\frac{h\nu}{kT}\right].
\]

Factor out the zero-point contribution:

\[
q_{\mathrm{vib}}=e^{-h\nu/(2kT)}
\sum_{v=0}^{\infty}\left(e^{-h\nu/(kT)}\right)^v.
\]

The remaining sum is a geometric series, \(1+x+x^2+\cdots=1/(1-x)\) for \(|x|<1\). Therefore,

\[
\boxed{q_{\mathrm{vib}}=\frac{e^{-h\nu/(2kT)}}{1-e^{-h\nu/(kT)}}.}
\]

If the zero of energy is chosen at the vibrational ground state rather than including zero-point energy, the common expression becomes

\[
q_{\mathrm{vib}}=\frac{1}{1-e^{-h\nu/(kT)}}.
\]

Both conventions give the same energy differences and thermal excitation populations; the partition function itself differs by the energy-reference factor. The source notes that the vibrational sum should not be replaced by an integral when \(h\nu\) is large compared with \(kT\), because the discrete levels remain important.

### Check your understanding: vibrational partition function

1. What does the vibrational quantum number \(v\) represent?
2. Why does the harmonic-oscillator energy contain a one-half term?
3. Why is the vibrational partition function a geometric series?
4. When can the zero-point prefactor be omitted, and what energy reference does that choice imply?

**Numerical practice.** A vibrational mode has \(h\nu/k=1000\,\mathrm K\). At \(T=300\,\mathrm K\), calculate the vibrational partition function (a) including zero-point energy and (b) with the zero of energy at the ground vibrational level.

*The two results and their interpretation are given in Section 16.*

## 10. Original numerical questions (source p. 19)

The following questions are transcribed from the final handwritten page without changing their given values or requested quantities.

**Q1.** Calculate the translational partition function for benzene (molar mass = 78 g/mol) in a volume of 1 m\(^3\) at 25 °C.

**Q2.** Calculate translational partition function for hydrogen atom at 3000 K continued to move in a box volume of \(2.494\times10^5\ \mathrm{cm^3}\). Also determine the thermal de-Broglie wavelength.

**Q3.** Calculate the characteristic rotational temperature and rotational partition function for \(H_2\) gas at 2727 °C given that the moment of inertia of hydrogen gas molecule at this temperature is \(4.6033\times10^{-48}\) \(\mathrm{kg\,m^2}\).

**Q4.** The rotational constant of gaseous HCl, determined from microwave spectroscopy, is 10.59 cm\(^{-1}\). Calculate the rotational partition function of HCl at (a) 100 K and (b) 500 K.

**Q5.** Calculate the characteristic rotational temperature for \(N_2\) molecule. Given: the internuclear distance of \(N_2\) is 109.76 pm.

### Formula reference for the five questions

- Translational: \(q_{\mathrm{trans}}=V(2\pi mkT/h^2)^{3/2}=V/\Lambda^3\).
- Thermal wavelength: \(\Lambda=h/(2\pi mkT)^{1/2}\).
- Molar mass to molecular mass: \(m=M/N_A\).
- Rotational characteristic temperature: \(\theta_{\mathrm{rot}}=h^2/(8\pi^2Ik)\).
- High-temperature rotational partition function: \(q_{\mathrm{rot}}=T/(\sigma\theta_{\mathrm{rot}})\).
- Diatomic moment of inertia: \(I=\mu r^2\), with \(\mu=m_1m_2/(m_1+m_2)\).
- If the spectroscopic rotational constant \(\tilde B\) is in cm\(^{-1}\), then \(\theta_{\mathrm{rot}}=hc\tilde B/k\), after converting cm\(^{-1}\) to m\(^{-1}\), and \(q_{\mathrm{rot}}\approx T/(\sigma\theta_{\mathrm{rot}})\).

**Data convention:** use SI units throughout a calculation. Convert Celsius to kelvin, \(\mathrm{cm^3}\) to m\(^3\), pm to m, and molar mass to kg mol\(^{-1}\) before substituting. No numerical answers are inserted here, because the source asks the questions and does not supply worked solutions.

## 11. Formula reference

Use these as a revision sheet. Fractions are deliberately written as mathematical fractions rather than slash-separated text.

### Partial molar properties and fugacity

\[
\bar X_i=\left(\frac{\partial X}{\partial n_i}\right)_{T,P,n_{j\ne i}},
\qquad
\mu_i=\left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_{j\ne i}}.
\]

\[
V=\sum_i n_i\bar V_i,
\qquad
G=\sum_i n_i\mu_i,
\qquad
\sum_i n_i\,d\mu_i=0\quad(T,P\text{ constant}).
\]

\[
f=\phi P,
\qquad
\mu=\mu^\circ+RT\ln\left(\frac{f}{P^\circ}\right),
\qquad
Z=\frac{PV_m}{RT}.
\]

\[
\ln\phi(P)=\int_0^P\frac{Z(P',T)-1}{P'}\,dP'.
\]

### Statistical thermodynamics and molecular partition functions

\[
\beta=\frac{1}{kT},
\qquad
q=\sum_i g_i e^{-\beta E_i},
\qquad
\frac{N_i}{N}=\frac{g_i e^{-\beta E_i}}{q}.
\]

\[
q=q_{\mathrm{trans}}q_{\mathrm{rot}}q_{\mathrm{vib}}q_{\mathrm{elec}}.
\]

### Translational partition function

\[
\Lambda=\frac{h}{\sqrt{2\pi mkT}},
\qquad
q_{\mathrm{trans}}=\frac{V}{\Lambda^3}
=V\left(\frac{2\pi mkT}{h^2}\right)^{3/2}.
\]

### Rotational partition function

\[
I=\mu r^2,
\qquad
\mu=\frac{m_1m_2}{m_1+m_2},
\qquad
E_J=\frac{J(J+1)h^2}{8\pi^2 I}.
\]

\[
\theta_{\mathrm{rot}}=\frac{h^2}{8\pi^2 I k},
\qquad
q_{\mathrm{rot}}\approx\frac{T}{\sigma\theta_{\mathrm{rot}}}.
\]

### Vibrational partition function

\[
E_v=\left(v+\frac12\right)h\nu,
\qquad
q_{\mathrm{vib}}=\frac{e^{-h\nu/(2kT)}}{1-e^{-h\nu/(kT)}}.
\]

If the ground vibrational level is chosen as zero energy, omit the zero-point prefactor in the partition function.

## 12. Common conceptual difficulties

1. **A partial molar volume is not the pure-component molar volume.** It is a derivative evaluated in the mixture, so it depends on composition.
2. **The chemical potential is a partial molar Gibbs energy.** Its meaning depends on what is held fixed in the derivative.
3. **Gibbs–Duhem is a constraint, not an additional equation of state.** At fixed temperature and pressure, component chemical potentials cannot vary independently.
4. **Fugacity is not simply another name for pressure.** It is a thermodynamic effective pressure; for an ideal gas it approaches pressure.
5. **Degeneracy counts states with the same energy.** It multiplies the Boltzmann weight of an energy level.
6. **A partition function is a weighted sum over states.** The weights depend on energy and temperature; it is not an ordinary count of states.
7. **The continuum approximation needs closely spaced levels.** It is appropriate for translation in a macroscopic box and for rotation at sufficiently high temperature, but not automatically for vibration.
8. **The rotational symmetry number corrects overcounting.** It is 2 for a homonuclear diatomic and 1 for a heteronuclear diatomic.
9. **Zero-point energy is an energy-reference convention.** Including it multiplies the vibrational partition function by a temperature-dependent prefactor.

## 13. Final chapter revision sheet

Use this list as a last-pass recall exercise. Cover the statements and try to explain each one aloud before reading it.

- Partial molar properties describe incremental contributions of mixture components.
- The total differential of an extensive mixture property includes temperature, pressure and composition terms.
- Chemical potential is the partial molar Gibbs energy.
- Euler's equation and Gibbs–Duhem follow from extensivity.
- Fugacity coefficient connects real-gas fugacity and pressure: \(f=\phi P\).
- Statistical thermodynamics connects microscopic states and macroscopic properties.
- MB, BE and FD statistics differ in particle distinguishability and quantum-state occupancy.
- Microcanonical: \(N,V,E\); canonical: \(N,V,T\); grand canonical: \(\mu,V,T\).
- The most probable MB population is proportional to \(g_i e^{-\beta E_i}\).
- The partition function normalises the Boltzmann populations.
- For separable molecular motions, molecular partition functions multiply.
- Translational partition function scales as \(VT^{3/2}\).
- High-temperature rotational partition function scales as \(T/(\sigma\theta_{rot})\).
- Harmonic vibrational levels are equally spaced by \(h\nu\); their partition function is a geometric series.

## 14. Scientific clarification log

The following points are made explicit to protect the scientific meaning while retaining the source statements.

1. **Source p. 1 — extensive properties:** the source list U, S, A, G, H and V is retained; these quantities scale with amount of material.
2. **Source pp. 1–2 — closed system:** a closed system has no matter exchange during a process. Component amounts may still be state variables when comparing different mixture preparations.
3. **Source p. 3 — binary Gibbs–Duhem equation:** the expression is shown as a differential relation at constant temperature and pressure; it is not an algebraic equation between the chemical potentials themselves.
4. **Source p. 4 — chemical-potential derivatives:** the fixed-variable conditions are stated using the natural variables of U, H, A and G.
5. **Source p. 6 — standard pressure:** the standard pressure is written as P° and the dimensionless ratio is shown explicitly inside the logarithm.
6. **Source pp. 7–8 — fugacity integral:** the integration variable is written as P′ to distinguish it from the upper limit P.
7. **Source pp. 7–8 — compressibility factor:** Z below or above unity is retained as a qualitative interpretation of attractive or repulsive effects over the range considered; fugacity depends on an integral over pressure.
8. **Source p. 9 — Fermi–Dirac occupancy:** the one-particle restriction applies to a complete quantum state. A degenerate energy level can contain several distinct states.
9. **Source pp. 10–12 — Maxwell–Boltzmann derivation:** the multiplicity and Lagrange-multiplier steps are written with consistent signs and explicit constraints, leading to the standard population expression.
10. **Source p. 13 — “corrected Boltzones”:** the handwritten expression is difficult to read. The standard degeneracy-corrected Maxwell–Boltzmann multiplicity is given, but no uncertain alternative formula is attributed to the source.
11. **Source p. 14 — particle in a box:** the three-dimensional box expression uses positive integer quantum numbers; the integral is identified as a continuum approximation.
12. **Source p. 17 — rotational partition function:** the symmetry number is included in the high-temperature expression to correct for indistinguishable orientations.
13. **Source p. 18 — vibrational zero-point energy:** expressions with and without the zero-point prefactor are shown, with the energy-reference difference explained.
14. **Source p. 19 — numerical questions:** all five original problems are retained without changing their given values or requested quantities.

## 15. Source figure inventory

1. **F1 — Source p. 2; Section 2.4.** Two beaker sketches, water/ethanol labels, recorded volume increments and molecular interaction sketch.
2. **F2 — Source p. 2; Section 2.4.** Hand-drawn graph of partial molar volumes against ethanol mole fraction.
3. **F3 — Source p. 9; Section 4.3.** Microcanonical ensemble grid with N, V and E fixed.
4. **F4 — Source p. 9; Section 4.3.** Canonical ensemble grid with N, V and T fixed and energy exchange allowed.
5. **F5 — Source p. 10; Section 4.3.** Grand-canonical ensemble grid with μ, V and T fixed and particle exchange allowed.
6. **F6 — Source p. 10; Section 5.1.** Energy-level population ladder with N₀…N₄ and E₀…E₄ and the microstate/macrostate annotation.
7. **F7 — Source p. 14; Section 7.1.** Rectangular three-dimensional particle-in-a-box sketch with dimensions a, b and c.
8. **F8 — Source p. 16; Section 8.1.** Diatomic rigid-rotor sketch.
9. **F9 — Source p. 17; Section 8.4.** Homonuclear H–H and heteronuclear H–Cl symmetry-number sketches.
10. **F10 — Source p. 18; Section 9.1.** Source vibrational section and adjacent simple-harmonic-oscillator equations.

**Additional visual source records:** the complete 19-page scan remains the archival visual source. Pages 1, 3–8, 11–13, 15 and 19 contain boxed equations, derivation annotations or handwritten material represented in the explanatory text. No original sketch was silently replaced by an invented scientific illustration.

## 16. Answers to supplementary checkpoints

These answers are for the newly added practice questions, not replacements for the five original numerical questions on source page 19.

### 16.1 Partial molar properties

1. A pure-component molar volume describes one mole of the pure substance. A partial molar volume describes the incremental volume change when that component is added to a mixture at its current composition.
2. This defines the contribution of A alone. If another component amount also changed, the observed volume change would include more than one composition effect.
3. The terms are the component contributions, each equal to amount multiplied by its partial molar volume at that mixture composition.
4. Their changes are linked; they cannot vary independently at fixed T and P.

For the numerical practice:

\[
V=n_A\bar V_A+n_B\bar V_B.
\]

Substitution gives

\[
V=(1.50)(20.0)+(0.50)(16.0)=38.0\,\mathrm{cm^3}.
\]

### 16.2 Fugacity

1. It measures the departure of fugacity from mechanical pressure: \(\phi=f/P\).
2. \(\phi\to1\) and \(f\to P\).
3. A logarithm must have a dimensionless argument; dividing by standard pressure achieves this.
4. \(\phi<1\) means \(f<P\) for that state.

For the numerical practice, \(Z=1+aP\), so \(Z-1=aP\). Thus:

\[
\ln\phi=\int_0^P\frac{aP'}{P'}\,dP'=\int_0^P a\,dP'=aP.
\]

At the stated pressure,

\[
\ln\phi=(0.020)(2.00)=0.0400.
\]

\[
\phi=e^{0.0400}=1.0408,
\qquad
f=\phi P=(1.0408)(2.00)=2.0816\,\mathrm{bar}.
\]

### 16.3 Statistical thermodynamics and ensembles

1. A microstate specifies the detailed quantum state of every particle; a macrostate specifies the populations of the energy levels.
2. The canonical ensemble.
3. Both energy and particles.
4. Bosons have symmetric many-particle wavefunctions and may share a state. Fermions have antisymmetric wavefunctions, so two identical fermions cannot occupy the same complete quantum state.

Application: (a) microcanonical; (b) canonical; (c) grand canonical.

### 16.4 Maxwell–Boltzmann distribution

1. \(g_i\) is the number of distinct quantum states having the same energy \(E_i\).
2. It normalises the weights so that all population fractions add to one.
3. The relative population of the higher-energy state increases as temperature rises.
4. At fixed T, the exponent \(-E_i/(kT)\) becomes more negative as energy increases.

For the numerical practice:

\[
q=g_0e^{-E_0/(kT)}+g_1e^{-E_1/(kT)}
=1+3e^{-2}=1.4060.
\]

\[
\frac{N_0}{N}=\frac{1}{q}=0.711,
\qquad
\frac{N_1}{N}=\frac{3e^{-2}}{q}=0.289.
\]

The fractions add to 1.000, as required.

### 16.5 Molecular partition functions

1. If the energy is a sum of independent contributions, the Boltzmann exponential becomes a product; independent sums then factor into a product of partition functions.
2. Translational, rotational, vibrational and electronic.
3. Strong coupling between motions or modes.

For the numerical practice:

\[
q=(40)(5)(1.2)(1)=240.
\]

### 16.6 Translational partition function

1. The exponent 3/2 comes from three independent spatial dimensions, each contributing a square-root Gaussian integral.
2. It is the characteristic thermal wavelength associated with a particle of mass m at temperature T.
3. Since \(q_{\mathrm{trans}}\propto T^{3/2}\), doubling T multiplies q by \(2^{3/2}=2.828\).

For the numerical practice:

\[
\Lambda=\frac{h}{\sqrt{2\pi mkT}}
=1.905\times10^{-11}\,\mathrm m.
\]

\[
q_{\mathrm{trans}}=\frac{V}{\Lambda^3}
=\frac{1.00\times10^{-3}}{(1.905\times10^{-11})^3}
\approx1.45\times10^{29}.
\]

### 16.7 Rotational partition function

1. For each J, the magnetic quantum number takes the values \(m_J=-J,-J+1,\ldots,J\), giving \(2J+1\) states.
2. The thermal energy must be large compared with the characteristic spacing of adjacent rotational levels.
3. A 180-degree rotation exchanges the identical ends of a homonuclear diatomic, giving an indistinguishable configuration; heteronuclear ends are different.
4. \(I\) and \(k\) (and the fixed constant h) determine \(\theta_{\mathrm{rot}}\).

For the numerical practice, \(2727^\circ\mathrm C=3000\,\mathrm K\). Using the supplied moment of inertia:

\[
\theta_{\mathrm{rot}}=\frac{h^2}{8\pi^2Ik}
=87.49\,\mathrm K.
\]

For \(H_2\), \(\sigma=2\):

\[
q_{\mathrm{rot}}\approx\frac{T}{\sigma\theta_{\mathrm{rot}}}
=\frac{3000}{2(87.49)}
\approx17.14.
\]

### 16.8 Vibrational partition function

1. The quantum number \(v=0,1,\ldots\) labels the allowed vibrational levels; the lowest level has zero-point energy.
2. Because adjacent levels are equally spaced by \(h\nu\), successive Boltzmann terms have the common ratio \(e^{-h\nu/(kT)}\) and form a geometric series. If the ground level is assigned zero energy, omit the zero-point prefactor.

For the numerical practice, \(h\nu/(kT)=1000/300=3.3333\):

\[
q_{\mathrm{vib,\,with\,ZPE}}
=\frac{e^{-1000/(2\times300)}}{1-e^{-1000/300}}
\approx0.1959.
\]

With the ground vibrational level chosen as zero, the corresponding result is \(q_{\mathrm{vib}}=\frac{1}{1-e^{-1000/300}}\approx1.0370\).
