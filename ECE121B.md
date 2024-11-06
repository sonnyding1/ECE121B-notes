## week 0 lecture 1

Silicon is cheap to fabricate because its melting point is low. In contrast, the melting point of gallium nitride is much higher and requires more pressure and temperature, therefore much more expensive to fabricate.

In the battle between silicon and germanium, silicon won because its oxide is super stable, while germanium oxide breaks down at high temperatures or when it meets water.

Semiconductors of different materials have different band gaps, which then is correlated to the breakdown field or the max voltage until it breaks. Diamond is considered an excellent semiconductor because it has the highest band gap, and it is very thermally conductive. But due to scarcity it cannot be used at a larger scale.

## week 1 lecture 1

Semiconductors are special because we may control if it conducts or not. Conductivity $\rho$ ranges from 0.001 to 10000 $\Omega\cdot cm$.

Grain boundaries in polycrystalline produce current leakage, therefore we prefer **crystalline** structure where there is no leakage in dielectric.

If we were to make a transistor out of silicon, then from the TEM view, the crystalline one is semiconductor, the amorphous one is insulator, the polycrystalline poly-silicon one is conductor. But IRL we just use metals for conductor.

**Lattice constant** is a parameter that describes the geometry of a semiconductor crystal. For silicon it is a single number $0.543Å$, but for $GaN$ there are 2 numbers. Atoms with smaller radius, when they form crystals, their lattice constant is also smaller.

Some common cubic crystal structures are **simple cubic**, **body centered** and **face centered**.

![[Pasted image 20241001104931.png]]

Simple cubic contains 1 atom per cube since each one on the edge is shared by 8 cubes, BCC contains 2 atoms, FCC contains 4 atoms.

There is also **diamond** or **zinc blende** crystal structure, which is like 2 FCC latices, the second is shifted $(\frac{a}{4}, \frac{a}{4}, \frac{a}{4})$ from the first lattice. For zinc blende we can call one lattice the V sides, the other lattice the III sides. What about $\text{InGaAs}$? Given the proportion between $\text{In}$ and $\text{Ga}$, for example 30 70, the crystal structure still holds, because the overall proportion between III group and V group is still 50 50. So we can mix stuff together to reach desired behaviors.

From calculations, we obtain that there are $5\times 10^{22}$ silicon atoms per $\text{cm}^2$. The impurity level is usually below $10^{9} / \text{cm}^2$.

$\text{InGaAs}$ is an example of **alloying**, which means we control the ingredients to put in, and can actually change the bandgaps. **Doping** is different, it may be either injecting impurities, or replacing existing atoms. But the main point is that impurities in terms of amount are negligible compared to the main materials. Of course, if you dope too hard you can change the bandgap a little too.

When you cut silicon wafers, there may be different orientations, and different orientations lead to different shapes and different electrical properties. **Miller indices** follow right hand coordinates. Miller indices must be integers. Use `()` for plane, and `[]` for vectors.

![[Pasted image 20241001113557.png]]

**Conductivity** is defined as $\sigma = nq\mu$, where $n$ is the concentration of mobile electrons per volume, $q$ is charge, $\mu$ is the mobility or electron speed in materials. Now, using the equation, the conductivity of aluminum is $\sigma\approx3\times10^{5} / (\Omega \cdot \text{cm})$, which matches reality. For silicon, $\sigma\approx3.2\times10^{5} / (\Omega \cdot \text{cm})$, even more conductive than metal, which doesn't match the reality of $10^{-4}$ to $10^{3}$. This example shows that the conductivity equation works well for conductors, but not so well with semiconductors. For semiconductors, we need quantum mechanics.

## week 1 discussion

There are 7 3D lattice systems, and a total of 14 **Bravais lattice**.

For a hexagonal unit cell, we may have 4 unit vectors, 3 of them on the same plane, separated by 120 degrees, the 4th one going perpendicular. In this way, it is easy to specify any plane or vector in a hexagonal cell. Of course, 2 vectors are sufficient to describe anything on a plane, but by introducing a 3rd one it would just be much easier to represent things.

## week 1 lecture 2

**Wave-particle duality** means that waves show particle-like behavior (photon-light), and particles show wave-like behavior (electron-wave). The equation the connects them is **de Broglie wavelength**:

$$\lambda = \frac{h}{p}$$

**Uncertainty principle** means that you may not know exactly the position and the velocity, or the energy and time, of the particle at the same time:

$$
\begin{align*}
\Delta p \Delta x &\ge \frac{\hslash}{2}\\
\Delta E \Delta t &\ge \frac{\hslash}{2}
\end{align*}
$$

**Energy quanta** states emitted radiation takes on discrete energies. This is because the energy states of atoms are discrete, like 1s, 2p and so on. 

Here is **Schrödinger's equation**:

$$\left(- \frac{\hslash^{2}}{2m}\nabla^{2}+U(r)\right)\psi = E\psi$$

For different elements, their energy states are different, because they have different $U(r)$. Nature tends to want to go to a state that is stable with the minimum amount of energy, so given say a bunch of silicon, they will decrease their interatomic distance until it forms a valence band and a conduction band, with bandgap in between.

![[Pasted image 20241003112708.png]]

![[Pasted image 20241003112804.png]]

**Electron affinity** is the amount of energy needed to remove electron from conduction band to vacuum.

Thermal energy can help electrons to move from valence band to conduction band.

For insulator, the bandgap is very large, therefore it is not easy to move to conduction band. For conductor, the bandgaps are either very close or they are overlapped and reversed. To be honest, the line between insulator and semiconductor can be blurry. The bandgap for diamond is 5eV, which can be used as an insulator. For reference, at room temperature, the thermal energy $k_{B}T$ is 25meV.

## week 2 lecture 1

### continuation of energy states

**Brillouin zone** is the unit cell for reciprocal k space. K space is obtained using Fourier transform, so transforming from time domain to frequency domain.

![[Pasted image 20241008100908.png|300]]

An **E-k diagram** describes the momentum at each energy level. Note that in classic physics, kinetic energy is $\frac{1}{2}mv^{2}=\frac{p^{2}}{2m}$. Now, in terms of quantum mechanics, we may write $p=\hslash k$, so

$$E=\frac{\hslash^{2}k^{2}}{2m} = \frac{p^{2}}{2m}$$

The previous E-k diagram is for electron in free space, it is also 1D. Now, we have a 3D example:

![[Pasted image 20241008103104.png]]

In this diagram, we are again producing 1D plots, by traveling in lines from $L$ to $\Gamma$ to $X$ and so on. Since this is a 3D space, we have 3 $k$ as well. So the x axis is a combination of the $k_{x}, k_{y}, k_{z}$.

We can also connect E-k diagram with the band gap diagram. E-k diagram simply adds a dimension that describes the momentum at each energy state. There may be up to 2 momentums in each energy level, since each energy level may contain up to 2 electrons.

But that E-k diagram was too complicated! In electronic devices, we are mostly concerned with the electrons near minima. Then, we may approximate the electrons in this region as different parabolic functions, just like in free space.

![[Pasted image 20241008104630.png|300]]

And so we create a parameter **effective mass**. 

$$
\begin{align*}
E &= \frac{\hslash^{2}k^{2}}{2m_{e}^{*}} \\
\frac{d^{2}E}{dk^{2}} &= \frac{\hslash^{2}}{m_{e}^{*}} \\
m_{e}^{*} &= \frac{\hslash^{2}}{\frac{d^{2}E}{dk^{2}}}
\end{align*}
$$

Among $AlN, GaN, InN$, we could tell that $InN$ has the largest lattice constant, $AlN$ has the smallest lattice constant, due to their different atomic radii. From there, 

*Larger the lattice constant, thinner/sharper the E-K curve, how did this conclusion arrive?*

$AlN$ also has the largest bandgap, because its bond is the strongest, and so it would be more difficult for electrons to escape.

![[Pasted image 20241008110235.png]]

Left is E-k diagram, right is band diagram, their difference is that E-k diagram's x-axis is $k$, while band diagram's x-axis is $x$. If it is just a pure material, the band diagram should not have any energy change along $x$.

We don't say the conduction band is full of holes.

### density of states

Near band edge, we approximate $m_{e}^{*}$ and $m_{p}^{*}$.

After some derivations, we obtain the equation for **density of states**,

$$g(E) dE = \frac{m^* \sqrt{2 m^* E}}{\pi^2 \hslash^3} dE$$

The equation itself is not so relevant, but there are 2 takeaways:

1. Density of states increases with respect to $\sqrt{E}$.
2. Higher effective mass means more density of states.

![[Pasted image 20241008113136.png|300]]

Both takeaways can be shown in the diagram above.

![[Pasted image 20241008114025.png|300]]

We prefer smaller effective masses.

## week 2 lecture 2

### continuation of density of states

Fermi Dirac statistics.

Common statistical distributions: 

- Maxwell Boltzmann: applies for particles distinguishable by number, with no limit on number of particles in each energy state.
- Bose-Einstein: applies for particles that are indistinguishable, with no limit on number of particles in each energy state.
- Fermi-Dirac: applies for particles that are indistinguishable, with only one particle in each energy state.

For electrons in semiconductor, we follow **Fermi-Dirac distribution**, due to Pauli exclusion principle:

$$
f(E) = \frac{1}{1+\text{exp}\left(\frac{E-E_{F}}{kT}\right)}
$$

Where $f(E)$ stands for the probability that a state with energy $E$ is occupied by an electron. The **Boltzmann constant**, $k$ or $k_{B}$, is $1.381\times10^{-23} \frac{J}{K} = 8.617\times10^{-5} \frac{eV}{K}$. Also, $k_{B}T=0.0259eV$ at $T=300K$.

![[Pasted image 20241010102613.png|300]]

As shown, the electron distribution equation is sensitive to temperature. Also, for intrinsic materials, **Fermi level** $E_{f}$ is always in the middle.

**Hole distribution equation** is simply $1-f(E)$.

If $E-E_{F} >> 3k_{B}T$, we may make the **Boltzmann approximation**:

$$
f(E) \approx \frac{1}{\text{exp}\left(\frac{E-E_{F}}{kT}\right)} = \text{exp}\left(-\frac{E-E_{F}}{kT}\right)
$$

![[Pasted image 20241010104131.png|300]]

So density of states tells how many states are there at an energy level, carrier density equation tells if there is a state at this energy level what is the probability of it being filled with carriers. We need to use the 2 equations together to obtain the actual concentration of carriers.

![[Pasted image 20241010104436.png]]

So we find carrier densities:

$$
\begin{align*}
n &= \int_{E_{C}}^{\infty} g_c(E)f(E)\,dE \\
p &= \int_{-\infty}^{E_{V}} g_v(E)[1-f(E)]\,dE
\end{align*}
$$

By applying Boltzmann's approximation, we have:

$$
\begin{align*}
n &= 2 \left( \frac{m_n^* k_B T}{2\pi \hslash^2} \right)^{3/2} \exp \left( \frac{E_F - E_C}{k_B T} \right)\\
p &= 2 \left( \frac{m_p^* k_B T}{2\pi \hslash^2} \right)^{3/2} \exp \left( \frac{E_V - E_F}{k_B T} \right)
\end{align*}
$$

If we define 

$$
\begin{align*}
N_{C} &= 2 \left( \frac{m_n^* k_B T}{2\pi \hslash^2} \right)^\frac{3}{2}\\
N_{V} &= 2 \left( \frac{m_p^* k_B T}{2\pi \hslash^2} \right)^\frac{3}{2}
\end{align*}
$$

We can write 

$$
\begin{align*}
n &= N_{C} \exp \left( \frac{E_F - E_C}{k_B T} \right)\\
p &= N_{V} \exp \left( \frac{E_V - E_F}{k_B T} \right)
\end{align*}
$$

Note that for intrinsic materials, $n=p$, since electron moved to conduction band is equivalent to hole moved to valence band.

Also, n and p concentrations can related to **intrinsic concentration** with

$$np = n_{i}^{2} = N_{C}N_{V}\exp(\frac{E_{C}-E_{V}}{k_{B}T})$$

### free carriers, dopants

We can dope material to make its Fermi level move closer to conduction band or valence band. To make Fermi level closer to conduction band, dope **shallow donors** with donor states right below the conduction band, now the material is **n-type**. To make Fermi level closer to valence band, dope **shallow acceptors** with acceptor states right above the valence band, now the material is **p-type**.

![[Pasted image 20241010114639.png]]

A **donor state** is neutral when it is occupied, and is positively charged when it is empty. An **acceptor state** is neutral when it is empty, and is negatively charged when it is occupied.

But things aren't always as we wish. Donor states and acceptor states can be anywhere really, it depends on the material and in which way are they inserted into the material. Sometimes a material only exhibits 1 state, sometimes 3. 

**Deep donors** are close to valence band, they trap holes and prevent them from leaving, so they are known as **hole traps**.
**Deep acceptors** are close to conduction band, they trap electrons and prevent them from leaving, so they are known as **electron traps**.

## week 3 lecture 1

### continuation on free carriers and dopants

By the way, we determine if some dopant is shallow or not based on $k_{B}T$, which is $25meV$. If it is that close to conduction or valence band, then it is shallow enough.

At $0K$, the dopants are in their neutral states. As temperature increases, some of them become ionized. There is an equation that describes the number of carriers with respect to temperature:

$$
\text{fraction of dopants ionized} = \frac{1}{1+\frac{g_{D,A}N_{D,A}}{N_{C,V}}\exp(\frac{E_{B}}{k_{B}T})}
$$

$g_{D}$ stands for degeneracy factor, which is 2.

$N_{D}^{+}$ stands for density of donors that have ionized.

$$
N_{D}^{+} = \frac{N_{D}}{1+2 e^{E_{B}/kT}}
$$

$$
N_{A}^{-} = \frac{N_A}{1+4e^{E_D/kT}}
$$

Both $E_{B}$ and $E_{D}$ are **binding energy**, just different values since measuring from valence band and conduction band. The bind energy depends on the material of dopant and the material of the semiconductor, and is not dependent on temperature.

![[Pasted image 20241015105159.png]]

The left part is called **freeze out** because temperature isn't high enough for the dopants to become ionized, so they are kind of just frozen in place. The right part is where silicon become ionized, and since the number of silicon overwhelms number of dopants, the material behavior is then dominated by silicon, therefore semiconductor behaves intrinsic again.

Note that all the equations in this section are assuming Boltzmann's approximation. Use **Joyce-Dickson** for more accurate results. Boltzmann approximation is valid if the Fermi level is not so heavily doped so that it is within $3kT$ distance to valence or conduction band. If Fermi level is within $3kT$, then we call the material **degenerately doped**. There is another definition of **degenerate**, which means "relating to two or more quantum states that share the same energy level".

**Charge neutrality** states that within a semiconductor at equilibrium, the net charge must be zero, no matter if the material is doped or not:

$$
q(p+N_{D}^{+}) = q(n+N_{A}^{-})
$$

$p, n$ are mobile, $N_{D}^{+}, N_{A}^{-}$ are immobile. 

If we assume 1. total ionization, and 2. non-degeneracy, then we may find the carrier densities equations

$$
\begin{align*}
n &=  \frac{N_D - N_A}{2} + \sqrt{\left( \frac{N_D - N_A}{2} \right)^2 + n_i^2}\\
p &=  \frac{n_i^2}{n} = \frac{N_A - N_D}{2} + \sqrt{\left( \frac{N_A - N_D}{2} \right)^2 + n_i^2}
\end{align*}
$$

Remember, $n_{i}$ changes as temperature changes. $N_{A}, N_{D}$ also change with temperature.

But the equation is a bit too complicated. We may consider 4 situations to hopefully simplify the calculations given constraints.

Situation 1. Intrinsic semiconductor. In this case, $N_{D}=N_{A}=0$. And $n=p=n_{i}$.

Situation 2. Extrinsic or doped semiconductor, given that $N_{D} \gg N_{A}, N_{D}\gg n_{i}$ for n-type, and $N_{A} \gg N_{D}, N_{A}\gg n_{i}$ for p-type. For n-type, then $n\approx N_{D}, p=\frac{n_{i}^{2}}{n}$. For p-type, then $p\approx N_{A}, n= \frac{n_{i}^{2}}{p}$.

Situation 3. Extrinsic semiconductor at high enough temperature, just like intrinsic semiconductor.

Situation 4. Compensated semiconductor. This is when $N_D$ and $N_A$ are comparable, or when $N_{D}$ and $n_{i}$ are comparable... In this case, just use the entire equation.

![[Pasted image 20241015115327.png|300]]

The figure above shows how at low temperatures, Fermi levels are primarily influenced by the doped materials and are closer to the valence or conduction band, and at high temperatures, silicon dominates so Fermi level moves back towards the intrinsic level. Also, note how since the band gap for $GaAs$ is larger than the band gap for $Si$.

## week 3 discussion

In this lecture, we will talk about:

- examples of dopants in Si and GaN
- concentrations

When temperature increases, the lattice constant also changes, so the Fermi level doesn't stay constant, it rises a bit as temperature increases.

## week 3 lecture 2

### drift and diffusion current

Free electrons can be moved by:

- electric field
- carrier gradient
- recombination

There are 2 types of charges:

- free carriers (electrons and holes)
- fixed charges (polarization charge, ionized impurities, ionized traps)

But only free carriers contribute to current.

### drift current

**Drift current density** is defined as 

$$
J = -e\sum\limits_{i=1}^{n} v_{i}
$$

![[Pasted image 20241017101657.png]]

So it is the sum of the velocities or momentums. At equilibrium, although there are electrons moving in the positive direction and negative direction, they sum up to 0, therefore no drift current.

Electrons move in random directions, they would accelerate until a scattering event occurs, maybe after hitting a wall, and then its direction will change and speed will decrease too.

$$
\begin{align*}
\vec{F} &= m_{e}^{*}\vec{a}\\
q\vec{E} &= \frac{m_{e}^{*}v_{avg}}{\tau}\\
v_{avg} &= \frac{q\tau}{m_{e}^{*}}\vec{E}\\
v_{avg} &= \mu \vec{E}
\end{align*}
$$

Where $\mu$ is known as the electron **mobility**.

Notice how we used effective mass to define this, that's why we try to model density of states and stuff first before discussing current.

$$
\begin{align*}
v_{drift,n} &= - \frac{q\mathcal{E}\tau_{n}}{m_{e}^{*}}\\
v_{drift,p} &= + \frac{q\mathcal{E}\tau_{p}}{m_{n}^{*}}
\end{align*}
$$

![[Pasted image 20241017103141.png|300]]

The figure above is true to a certain extent. It will soon slow down to a saturation voltage.

Every single thing that disrupts the perfect periodicity of crystal structure is considered a **scattering mechanism**. Some scattering mechanisms are:

- dopants
- temperature, as it causes jiggle and disrupt periodicity
- defects
- alloy scattering

We may use **Mathieson's rule** to calculate the net scattering time:

$$
\frac{1}{\tau_{tot}} = \sum\limits_{i} \frac{1}{\tau_{i}}
$$

Where each scattering mechanism is given a scattering constant.

But by increasing dopant concentration, you also increase carrier concentration, despite mobility decreases. So there is probably a sweet spot.

Crystal vibration is called **phonon**, as it behaves like waves. **Phonon absorption** means electrons getting affected by the crystal vibration, **phonon emission** means electrons' movement causing crystal to start vibrating.

![[Pasted image 20241017111548.png|300]]

The 2 most dominant scattering mechanisms are phonon scattering and impurity scattering. At low temperature, we are at freeze out, which means less carriers, and not enough carriers to form screening around the dopants, so impurity scattering dominates. At higher temperature, screening effect forms, and high temperature causes lattice vibrations, so phonon scattering d

![[Pasted image 20241017112417.png]]

*Notice how $GaAs$ does some overshoot. This happens because it gains so much energy so that it moves from one valley to another valley, and the effective mass changes.*

$$
\begin{align*}
J_{p,drift} &= +qpv_{drift,p} &&= +qp\mu_{p}\mathcal{E}\\
J_{n,drift} &= -qnv_{drift,n} &&= +qn\mu_{n}\mathcal{E}
\end{align*}
$$

Although electrons and holes move in opposite directions, since they also have opposite charges, the currents do add up. So total current is just the sum of them.

$$
\sigma = q(n\mu_{n}+p\mu_{p})
$$

Where $\sigma$ is known as **conductivity**.

Ohm's law is derived from the drift current equation.

### diffusion current

Particles flow randomly, it just so happens that as time moves on, carriers move from high concentration gradient to low concentration gradient. So we obtain the diffusion current at a point by assessing the current going left vs going right, and then subtract them:

![[Pasted image 20241017114829.png|300]]

$$
\begin{align*}
J &= J_{1}- J_{2}\\
&= \frac{-1}{2}qn(-l)v_{th}- \frac{-1}{2}qn(l)v_{th}\\
&= \frac{-1}{2}qv_{th}[n(-l)-n(l)]\\
&= - \frac{1}{2}qv_{th} \left[\left(n_{0}-l \frac{dn}{dz}\right) - \left(n_{0}+l \frac{dn}{dz}\right)\right]\\
&= qlv_{th} \frac{dn}{dx}\\
&= qD_{n} \frac{dn}{dx}
\end{align*}
$$

Where $D_{n}$ is the **diffusion coefficient**, and $l$ is the electron mean free path, or the distance electron moves before being scattered.

## week 4 lecture 1

### continuation of drift and diffusion current

Adding drift and diffusion current together, 

$$
\begin{align*}
J_{n}&= J_{n,drift} + J_{n,diff} &&= + q\mu_{n}n\vec{E} + qD_{n} \frac{dn}{dx}\\
J_{p}&= J_{p,drift} + J_{p,diff} &&= + q\mu_{p}p\vec{E} - qD_{p} \frac{dp}{dx}
\end{align*}
$$

Steady state is not equilibrium. **Equilibrium** requires both no external stimuli *and* no net current flow. So, a piece of semiconductor can have no net current when light shines on it, but it is only in steady state, not in equilibrium.

$$
\begin{align*}
E &= -qV\\
\mathcal{E} &= -\nabla V = \frac{1}{q} \frac{dE_{C}(x)}{dx}
\end{align*}
$$

Knowing the relationships, we may draw graphs of voltage and field $\mathcal{E}$:

![[Pasted image 20241022104107.png|300]]

Under equilibrium, the following equations hold:

$$
\begin{align*}
J_{total,n} &= +qn\mu_{n}\mathcal{E} + qD_{n}\frac{dn}{dx} = 0\\
n(x) &= n_{i}\exp{\left(\frac{E_{F}(x)-E_i(x)}{k_{B}T}\right)}
\end{align*}
$$

*second equation significance? how is there drift current if no external forces for equation 1?*

Solving derivative of equation 2, and plug into equation 1, we obtain the **Einstein relationship**:

$$
\begin{align*}
\frac{D_{n}}{\mu_{n}} &= \frac{k_{B}T}{q}\\
\frac{D_{p}}{\mu_{p}} &= \frac{k_{B}T}{q}
\end{align*}
$$

### generation and recombination

There are multiple R-G (recombination generation) processes.

**Band to band** process means thermal generation directly promotes electrons from valence band to conduction band, recombination is the same but opposite process, might be either thermal or optical.

**R-G center** generation requires electrons to go to trap state first, then go to conduction band. Recombination has 2 possibilities, either recombine at the trap state, or recombine at the valence band.

**Auger** recombination is when a hole and electron recombine, energy is given to another carrier in the conduction band to promote it to higher energy states and cool off and go down bit by bit. The electron that is promoted is called a **hot electron**. Generation is also known as **impact ionization**, which happens when there is a field that causes a slope at the bands, so when an electron travels from lowest energy state at point A to a point B, it actually is considered a hot electron at point B, and will drop down and release its KE, the KE may be used for promoting an electron from valence band to conduction band. When the field is so high, then excess energy can cause more electrons in conduction band to travel and drop and excite more electrons, causing an **avalanche**.

![[Pasted image 20241022114235.png]]

**Low-level injection** means the generation recombination has little effect on majority carrier but has large effect on the minority carrier.

Suppose for a piece of silicon, it is n-type, so electron is majority carrier, hole is minority carrier. 

Now, R-G center recombination rate can be described with

$$
\frac{dp}{dt}\bigg|_{R} = -c_{p}N_{T}p
$$

Where $c_{p}$ is capture coefficient of holes, $N_T$ is the trap concentration, $p$ is the minority carrier concentration, which in this case is holes. Basically, we care about minority concentration only for recombination, because even say there are $10^{16}$ electrons, if there are only $10^4$ holes, then the recombination is capped at $10^4$. And the trap concentration also matters, more traps mean more recombination.

And generation should perfectly balance out recombination, else it will just keep generating or recombinating infinitely.

$$
\frac{dp}{dt}\bigg|_{G} = c_{p}N_{T}p_{0}
$$

As for thermal R-G,

$$
\left.\frac{dp}{dt}\right|_{i-\text{thermal},R-G} = \left.\frac{dp}{dt}\right|_{R} + \left.\frac{dp}{dt}\right|_{G} = -c_{p}N_{T}(p - p_{0}) = -c_{p}N_{T}\Delta p
$$

And we could define minority carrier lifetime, $\tau_{p}= 1/c_{p}N_{T}$, now there is

$$
\left.\frac{dp}{dt}\right|_{i-\text{thermal},R-G} = - \frac{\Delta p}{\tau_{p}}
$$

Generation is just thermal, recombination may be induced by external forces like thermal.

There is also optical generation. Intensity of light in the semiconductor is modeled as $I = I_{0}e^{-\alpha (\lambda)x}$. The generation function is then

$$
G_{L}(x,\lambda) = G_{L0}e^{-\alpha x}
$$

![[Pasted image 20241022155542.png]]

We prefer **direct bandgap** over **indirect bandgap** for optical generation, since indirect bandgap optical generation takes 2 steps, and in terms of quantum mechanics, the chance of this generation happening is much lower.

## week 4 lecture 2

Cheatsheet ok, 1 page

In LED, we don't want Auger recombination, because we want photons emitting instead of exciting another electron in the conduction band.

**Continuity equation** states

$$
\frac{\partial n}{\partial t} A\,dx = \left[\frac{J_{n}(x)A}{-q}-\frac{J_{n}(x+dx)A}{-q}\right] + (G-R)A\,dx
$$

Basically we take a slice of semiconductor, and observe if the current changes with change with carrier concentration or not. When we are not in a steady state, generation and recombination are not cancelling each other out.

And formally, it is

$$
\begin{align*}
\frac{\partial n}{\partial t} &= \frac{1}{q} \nabla\cdot\vec{J_{n}} + \left.\frac{\partial n}{\partial t}\right|_{thermal R-G} + \left.\frac{\partial n}{\partial t}\right|_{other R-G}\\
\frac{\partial p}{\partial t} &= -\frac{1}{q} \nabla\cdot\vec{J_{p}} + \left.\frac{\partial p}{\partial t}\right|_{thermal R-G} + \left.\frac{\partial p}{\partial t}\right|_{other R-G}
\end{align*}
$$

Here, note that $J$ term is related to drift and diffusion current.

After we make a lot of assumption, such as assume low level injection, equilibrium, no electric field so no drift, thermal R-G center is the main R-G mechanism, only "other" R-G method is light, we then simplify the equations into

$$
\begin{align*}
\frac{\partial \Delta n_p}{\partial t} &= D_n \frac{\partial^2 \Delta n_p}{\partial x^2} - \frac{\Delta n_p}{\tau_n} + G_L \\
\frac{\partial \Delta p_n}{\partial t} &= D_p \frac{\partial^2 \Delta p_n}{\partial x^2} - \frac{\Delta p_n}{\tau_p} + G_L
\end{align*}
$$

Note how we have removed drift current, the only terms left are diffusion, thermal R-G, and optical R-G represented by $G_{L}$.

Now, in steady state, 

$$
\frac{\partial \Delta n_p}{\partial t}\to 0 \text{ and } \frac{\partial \Delta p_n}{\partial t}\to 0
$$

If no minority carrier concentration spatial gradient, no diffusion part. If not thermal R-G, no thermal part. If no light, no light part.

*Solve differential equations*

Fermi distribution is only valid under equilibrium, so say if we shine light, we should no longer be able to use Fermi distribution for the semiconductor. But we can still define **Quasi-Fermi levels**, by grouping electrons and holes separately and get a Quasi-Fermi level for electrons, and a Quasi-Fermi level for holes.

## week 5 lecture 1

Onto PN junctions. The device has a p-type and a n-type connected together, which enables current to flow in one direction but not in the other direction, also known as diode. Under equilibrium, there is no net current and the Fermi level $E_{F}$ is horizontal, but there is voltage difference between the p-type and n-type, known as $V_{bi}$.

$$
V_{bi} = \frac{k_{B}T}{q} \ln\left(\frac{N_{D}N_{A}}{n_{i}^{2}}\right)
$$

![[Pasted image 20241031101912.png]]

Note that $\rho$ is charge density, $\epsilon$ is the permittivity of the material.

Depletion region has charge not because of charge carriers, since charge carriers all go away; rather, it's because of the ionized doped materials that remain.

*missing PN diode electrostatics*

## week 5 lecture 2

### continuation on PN diode electrostatics

If we apply a positive voltage to a piece of semiconductor, it shifts the entire band *down*, because the band diagram is for electrons, positive voltage to electron is decreasing its energy. Also, when applying a voltage, the device is no longer in equilibrium, therefore there is no more Fermi level, only Quasi Fermi level $F_{n}$ or $F_{p}$.

![[Pasted image 20241031105919.png]]

Electric field also change as a result of voltage change. Therefore, depletion region width changes as well.

![[Pasted image 20241031110008.png]]

$$
W = \sqrt{ \frac{2\epsilon_s\epsilon_0(V_{bi} - V_A)}{q} \left( \frac{N_A + N_D}{N_A N_D} \right) }
$$

### PN diodes IV

Real diode IV behavior is more complex than an ideal one, and may be represented using an equation: 

$$
I = I_{0} (e^{\frac{qV_{A}}{k_{B}T}}-1)
$$

![[Pasted image 20241031110358.png|300]]

Under equilibrium, drift and diffusion currents cancel each other out, for each of holes and electrons:

![[Pasted image 20241031112011.png]]

*missing rest of the content*

## week 6 lecture 1

$$
\begin{align*}
n_{i} &= \sqrt{N_{C}N_{V}}\exp(- \frac{E_{q}}{2k_{B}T})\\
n &= n_{i}\exp()
\end{align*}
$$