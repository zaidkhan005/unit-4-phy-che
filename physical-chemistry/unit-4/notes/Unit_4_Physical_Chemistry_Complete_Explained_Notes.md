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
11. Formula reference and symbol glossary
12. Common conceptual difficulties and revision sheet
13. Scientific clarification log

## 1. Learning objectives and notation

After studying this unit, you should be able to explain why mixture properties depend on composition; define and calculate partial molar properties; derive the Gibbs–Duhem relation; distinguish fugacity from pressure; connect a microscopic energy-level picture to macroscopic thermodynamics; identify the three standard ensembles and the Maxwell–Boltzmann, Bose–Einstein and Fermi–Dirac cases; derive the Boltzmann population law and molecular partition functions; and use translational, rotational and vibrational partition functions in the five supplied problems.

### Symbols used repeatedly

| Symbol | Meaning | Usual unit |
|---|---|---|
| \(T\), \(P\) | absolute temperature, pressure | K, Pa (or stated pressure unit) |
| \(n_i\), \(N_i\) | amount/number of particles of species or energy level \(i\); context matters | mol, or count |
| \(U,H,A,G\) | internal energy, enthalpy, Helmholtz energy, Gibbs energy | J |
| \(S,V\) | entropy and volume | J K\(^{-1}\), m\(^3\) |
| \(\mu_i\) | chemical potential of component \(i\) | J mol\(^{-1}\) |
| \(\bar X_i\) | partial molar property of component \(i\) | property per mole |
| \(R,k,N_A\) | gas constant, Boltzmann constant, Avogadro constant | SI constants |
| \(h,\hbar\) | Planck constant and reduced Planck constant \(h/(2\pi)\) | J s |
| \(q,Q\) | single-molecule and whole-system partition functions; conventions vary | dimensionless |
| \(g_i\) | degeneracy of energy level \(i\) | dimensionless count |
| \(\beta\) | inverse thermal energy, \(1/(kT)\) | J\(^{-1}\) |
| \(Z\) | compressibility factor in fugacity section; partition function in some texts | dimensionless |
| \(\phi\) | fugacity coefficient | dimensionless |
| \(f\) | fugacity | pressure unit |

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

The total differential follows from the multivariable chain rule:

\[
\begin{aligned}
dX={}&\left(\frac{\partial X}{\partial T}\right)_{P,n_i}dT
+\left(\frac{\partial X}{\partial P}\right)_{T,n_i}dP\\
&+\sum_i\left(\frac{\partial X}{\partial n_i}\right)_{T,P,n_{j\ne i}}dn_i.
\end{aligned}
\]

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

**Source illustration (p. 2).** The notebook sketches one mole of water added to water and one mole of water added to ethanol. It records a volume increase of about \(18\,\mathrm{cm^3}\) for the water-in-water case and about \(14\,\mathrm{cm^3}\) for water added to ethanol. The physical lesson is that the same added component can produce a different volume increment in a different molecular environment. The neighbouring molecular sketch represents unlike-molecule interactions in the mixed liquid.

The source also contains a hand-drawn composition graph for the partial molar volumes of water and ethanol against ethanol mole fraction. The curves vary with composition and are not horizontal; this is the visual statement that partial molar volumes are composition-dependent.

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
\boxed{\sum_i n_i\,d\mu_i=0}\qquad (T,P\text{ constant}).
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

\[
\mu_i=\left(\frac{\partial U}{\partial n_i}\right)_{S,V,n_{j\ne i}}
=\left(\frac{\partial H}{\partial n_i}\right)_{S,P,n_{j\ne i}}
\]

\[
=\left(\frac{\partial A}{\partial n_i}\right)_{T,V,n_{j\ne i}}
=\left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_{j\ne i}}.
\]

**Why the conditions matter:** a partial derivative is not fully defined unless the fixed variables are stated. Use the natural variables of the thermodynamic potential: \(U(S,V,n_i)\), \(H(S,P,n_i)\), \(A(T,V,n_i)\), and \(G(T,P,n_i)\).

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
G_m(P_f)=G_m(P_i)+\int_{P_i}^{P_f}V_m\,dP.
\]

For an ideal gas, \(V_m=RT/P\), hence

\[
G_m(P_f)=G_m(P_i)+RT\int_{P_i}^{P_f}\frac{dP}{P}
=G_m(P_i)+RT\ln\frac{P_f}{P_i}.
\]

Choosing the standard pressure \(P^\circ\) as the reference and writing the final pressure as \(P\),

\[
\mu=\mu^\circ+RT\ln\frac{P}{P^\circ}\quad\text{(ideal gas)}.
\]

For a real gas pressure is replaced by fugacity:

\[
\boxed{\mu=\mu^\circ+RT\ln\frac{f}{P^\circ}.}
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
d\ln\left(\frac{f}{P}\right)
=\left(\frac{V_m}{RT}-\frac{1}{P}\right)dP.
\]

Since \(V_m/(RT)=Z/P\),

\[
d\ln\phi=\frac{Z-1}{P}\,dP.
\]

Using the ideal-gas limiting condition \(\phi\to1\) as \(P\to0\), integration gives

\[
\boxed{\ln\phi=\int_0^P\frac{Z-1}{P}\,dP.}
\]

More rigorously the integration variable is a dummy variable, often written \(P'\):

\[
\ln\phi(P)=\int_0^P\frac{Z(P',T)-1}{P'}\,dP'.
\]

### 3.4 Physical interpretation of the sign

The notebook associates \(Z<1\) with attractive interactions and \(Z>1\) with repulsive effects. This is a useful qualitative interpretation in the relevant pressure range, but one should not treat a single value of \(Z\) as a universal interaction label at every pressure. The sign of \(\ln\phi\) depends on the integral over the full pressure interval.

When the integrand remains negative, \(\phi<1\) and therefore \(f<P\); when it remains positive, \(\phi>1\) and \(f>P\). Fugacity is an effective thermodynamic pressure, not a directly measured mechanical pressure.

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

| Ensemble | Fixed quantities | What can vary/exchange? | Typical system |
|---|---|---|---|
| Microcanonical | \(N,V,E\) | no energy or particle exchange | isolated system |
| Canonical | \(N,V,T\) | energy exchange with a heat bath | closed system in thermal contact |
| Grand canonical | \(\mu,V,T\) | energy and particle exchange | open system |

The notebook labels the microcanonical ensemble as isolated, the canonical ensemble as allowing energy exchange, and the grand canonical ensemble as open. The sketches are reproduced in the figures section.

## 5. Maxwell–Boltzmann distribution and partition function (source pp. 10–13)

### 5.1 Energy levels, populations and degeneracy

Suppose \(N\) distinguishable particles are distributed among energy levels \(E_0,E_1,E_2,\ldots\). Let \(N_i\) be the number of particles in level \(i\), and let \(g_i\) be the degeneracy of that level (the number of distinct states having the same energy).

The particle-number and total-energy constraints are

\[
N=\sum_i N_i,
\qquad E=\sum_i N_iE_i.
\]

A **microstate** specifies the detailed state occupied by every particle. A **macrostate** specifies only the occupation numbers \(N_i\). Many microstates may correspond to one macrostate.

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
-\beta\left(E-\sum_iN_iE_i\right).
\]

Differentiating with respect to \(N_i\) and setting the result to zero,

\[
\frac{\partial\ln W}{\partial N_i}-\alpha+\beta E_i=0.
\]

From the logarithmic multiplicity expression,

\[
\frac{\partial\ln W}{\partial N_i}=\ln N+\ln g_i-\ln N_i.
\]

Therefore,

\[
\ln\left(\frac{Ng_i}{N_i}\right)-\alpha+\beta E_i=0,
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
q=\sum_{\text{states }r}e^{-\beta E_r}.
\]

The two forms are equivalent: a level with energy \(E_i\) and degeneracy \(g_i\) contributes \(g_i e^{-\beta E_i}\).

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

This factorisation assumes that the molecular Hamiltonian and accessible states are sufficiently separable; strong coupling between modes can invalidate the simple product approximation. The source writes the product for translational, rotational and vibrational contributions and shows the electronic factor in the energy decomposition.

## 7. Translational partition function (source pp. 14–15)

### 7.1 Particle in a three-dimensional box

The notebook models a particle of mass \(m\) in a rectangular box with sides \(a,b,c\). For quantum numbers \(n_x,n_y,n_z=1,2,\ldots\),

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

## 8. Rotational partition function (source pp. 16–18)

### 8.1 Rigid-rotor model

A diatomic molecule is approximated as two point masses separated by a fixed internuclear distance \(r\). Its moment of inertia about the centre of mass is

\[
I=\mu r^2,
\qquad \mu=\frac{m_1m_2}{m_1+m_2},
\]

where \(\mu\) is the reduced mass.

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

The symmetry number \(\sigma\) corrects for rotations that exchange identical nuclei and leave the molecule physically indistinguishable. In the notebook, homonuclear diatomic molecules such as H\(_2\) have \(\sigma=2\), whereas heteronuclear diatomics such as HCl have \(\sigma=1\).

The notebook also records the rotational constant \(B\), in spectroscopic wavenumber units, and the equivalent form

\[
q_{\mathrm{rot}}\approx\frac{kT}{\sigma h c B},
\]

provided \(B\) is expressed in inverse-length units consistent with \(c\) and \(h\).

## 9. Vibrational partition function (source p. 18)

### 9.1 Simple harmonic oscillator

The source models molecular vibration as a simple harmonic oscillator (SHO). The energy levels are

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

## 10. Original numerical questions (source p. 19)

The following questions are transcribed from the final handwritten page without changing their given values or requested quantities.

**Q1.** Calculate the translational partition function for benzene (molar mass = 78 g/mol) in a volume of 1 m\(^3\) at 25 °C.

**Q2.** Calculate translational partition function for hydrogen atom at 3000 K continued to move in a box volume of \(2.494\times10^5\) cm\(^3\). Also determine the thermal de-Broglie wavelength.

**Q3.** Calculate the characteristic rotational temperature and rotational partition function for H\(_2\) gas at 2727 °C given that the moment of inertia of hydrogen gas molecule at this temperature is \(4.6033\times10^{-48}\) kg m\(^2\).

**Q4.** The rotational constant of gaseous HCl, determined from microwave spectroscopy, is 10.59 cm\(^{-1}\). Calculate the rotational partition function of HCl at (a) 100 K and (b) 500 K.

**Q5.** Calculate the characteristic rotational temperature for N\(_2\) molecule. Given: the internuclear distance of N\(_2\) is 109.76 pm.

### Formula reference for the five questions

- Translational: \(q_{\mathrm{trans}}=V(2\pi mkT/h^2)^{3/2}=V/\Lambda^3\).
- Thermal wavelength: \(\Lambda=h/(2\pi mkT)^{1/2}\).
- Molar mass to molecular mass: \(m=M/N_A\).
- Rotational characteristic temperature: \(\theta_{\mathrm{rot}}=h^2/(8\pi^2Ik)\).
- High-temperature rotational partition function: \(q_{\mathrm{rot}}=T/(\sigma\theta_{\mathrm{rot}})\).
- Diatomic moment of inertia: \(I=\mu r^2\), with \(\mu=m_1m_2/(m_1+m_2)\).
- If the spectroscopic rotational constant \(\tilde B\) is in cm\(^{-1}\), then \(\theta_{\mathrm{rot}}=hc\tilde B/k\), after converting cm\(^{-1}\) to m\(^{-1}\), and \(q_{\mathrm{rot}}\approx T/(\sigma\theta_{\mathrm{rot}})\).

**Data convention:** use SI units throughout a calculation. Convert Celsius to kelvin, cm\(^3\) to m\(^3\), pm to m, and molar mass to kg mol\(^{-1}\) before substituting. No numerical answers are inserted here, because the source asks the questions and does not supply worked solutions.

## 11. Compact formula reference

| Topic | Principal relation |
|---|---|
| Partial molar property | \(\bar X_i=(\partial X/\partial n_i)_{T,P,n_{j\ne i}}\) |
| Mixture volume | \(V=\sum_i n_i\bar V_i\) |
| Chemical potential | \(\mu_i=(\partial G/\partial n_i)_{T,P,n_{j\ne i}}\) |
| Euler relation | \(G=\sum_i n_i\mu_i\) |
| Gibbs–Duhem | \(\sum_i n_i d\mu_i=0\) at constant \(T,P\) |
| Fugacity | \(f=\phi P\) |
| Real-gas chemical potential | \(\mu=\mu^\circ+RT\ln(f/P^\circ)\) |
| Compressibility factor | \(Z=PV_m/(RT)\) |
| Fugacity coefficient | \(\ln\phi=\int_0^P[(Z-1)/P']dP'\) |
| Beta | \(\beta=1/(kT)\) |
| Partition function | \(q=\sum_i g_i e^{-\beta E_i}\) |
| Boltzmann population | \(N_i/N=g_i e^{-\beta E_i}/q\) |
| Molecular factorisation | \(q=q_{tr}q_{rot}q_{vib}q_{elec}\) |
| Translation | \(q_{tr}=V(2\pi mkT/h^2)^{3/2}=V/\Lambda^3\) |
| Thermal wavelength | \(\Lambda=h/(2\pi mkT)^{1/2}\) |
| Rotation | \(E_J=J(J+1)h^2/(8\pi^2I)\) |
| Rotation, high T | \(q_{rot}=T/(\sigma\theta_{rot})\) |
| Rotational temperature | \(\theta_{rot}=h^2/(8\pi^2Ik)\) |
| Vibration | \(E_v=(v+1/2)h\nu\) |
| Vibration, including zero-point energy | \(q_{vib}=e^{-h\nu/(2kT)}/(1-e^{-h\nu/(kT)})\) |

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

| Source location | Source notation or statement | Clarification used in this document | Why it matters |
|---|---|---|---|
| p. 1 | Extensive list includes \(U,S,A,G,H,V\) | Kept; clarified scaling with amount | Distinguishes extensive from intensive quantities |
| pp. 1–2 | Closed-system notation and composition variables | A closed system has no matter exchange in a process; fixed component amounts are not a ban on using composition as a state variable | Avoids conflating system type with mixture-state dependence |
| p. 3 | Binary Gibbs–Duhem boxed as \(d\mu_A=-(n_B/n_A)d\mu_B\) | Retained; shown as a differential relation at fixed T,P | This equation is not an algebraic relation between chemical potentials |
| p. 4 | Chemical-potential derivatives across U,H,A,G | Fixed-variable conditions are aligned to each potential's natural variables | Correct derivative constraints are essential |
| p. 6 | Standard pressure marked as 1 bar | Written as a standard pressure \(P^\circ\), with the dimensionless ratio explicit | Logarithm arguments must be dimensionless |
| pp. 7–8 | \(\ln\phi=\int_0^P (Z-1)/P\,dP\) | Dummy integration variable written as \(P'\) | Avoids using the same symbol as both limit and integration variable |
| pp. 7–8 | \(Z<1\) attractive; \(Z>1\) repulsive | Retained as a qualitative interpretation, not a universal rule at every pressure | Fugacity depends on an integral over pressure |
| p. 9 | FD: only one particle per energy level | Restricted to one particle per complete quantum state; degeneracy/spin states may allow multiple particles at the same energy | Pauli exclusion applies to states, not merely energy values |
| pp. 10–12 | MB multiplicity and Lagrange derivation | Recast with clear constraints and consistent signs; gives \(N_i/N=g_i e^{-\beta E_i}/q\) | Makes normalisation and the role of degeneracy explicit |
| p. 13 | “Corrected Boltzones” expression is difficult to read | The standard degeneracy-corrected MB multiplicity is stated; no unverified alternative formula is attributed to the source | The handwritten line is ambiguous and should not be silently presented as a standard formula |
| p. 14 | Particle-in-box energy and integral | Standard 3-D box energy retained with quantum numbers starting at 1; integral is a high-temperature/macroscopic-box approximation | Shows where the approximation enters |
| p. 17 | Rotational high-temperature integral | Includes symmetry number \(\sigma\) in final result | Corrects indistinguishable orientations for symmetric molecules |
| p. 18 | Vibrational sum and exponential | Geometric-series result given, with and without zero-point reference | Both conventions are common, but must not be mixed without explanation |
| p. 19 | Five numerical problem statements | Transcribed without solving or altering given data | Preserves the original assessment tasks |

## Appendix A. Source figure inventory

| Figure | Source page | Contents preserved | Placement |
|---|---:|---|---|
| F1 | 2 | Two beaker sketches, water/ethanol labels and volume increments, molecular interaction sketch | Section 2.4 |
| F2 | 2 | Hand-drawn composition graph of partial molar volumes versus ethanol mole fraction | Section 2.4 |
| F3 | 9 | Microcanonical ensemble grid, repeated N–V–E labels | Section 4.3 |
| F4 | 9 | Canonical ensemble grid, repeated N–V–T labels and energy-exchange note | Section 4.3 |
| F5 | 10 | Grand-canonical ensemble grid, repeated μ–V–T labels and open-system note | Section 4.3 |
| F6 | 10 | Energy-level population ladder with N0…N4 and E0…E4; microstate/macrostate annotation | Section 5.1 |
| F7 | 14 | Rectangular three-dimensional particle-in-a-box sketch, dimensions a, b, c | Section 7.1 |
| F8 | 16 | Diatomic rigid-rotor spring/axis sketch | Section 8.1 |
| F9 | 17 | Homonuclear H–H and heteronuclear H–Cl symmetry-number sketches | Section 8.4 |
| F10 | 18 | Source page's simple-harmonic-oscillator vibrational section and adjacent equations | Section 9.1 |

**Additional visual source records:** full handwritten pages 1–19 are archived separately in the source-page render directory; pages 1, 3–8, 11–13, 15 and 19 contain boxed equations, derivation annotations, or handwritten material that is retained in the chapter transcription rather than cropped as independent figures. No sketch from these pages was silently replaced by a newly invented scientific figure.