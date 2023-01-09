---
layout: post
title: "Why do antiparticles have the opposite helicity?"
date: 2023-01-03
---

This is a very common question when learning particle physics. We learn that antiparticles arise due to the incorporation of relativity into quantum mechanics causing both a positive and negative solution for energy to appear. Antiparticles are those negative energy solutions. Negative energy is a bit difficult to deal with so we abstract this out using different spinor bases, using $$u_1$$ and $$u_2$$ spinors for the particles and the $$v_1$$ and $$v_2$$ spinors for the antiparticles rather than using all 4 in the same basis. The result of this is that the helicity, the spin in the direction of the particle's velocity, gets flipped. The following is a foray into how this comes about, created for the audience of the Part III/Masters Particle Physics course and based on the notes from [https://www.hep.phy.cam.ac.uk/~lester/teaching/partIIIparticles/welcome.html](https://www.hep.phy.cam.ac.uk/~lester/teaching/partIIIparticles/welcome.html).

Just to make sure we are on the same page here, let us define two different quantities: **"mathematical momentum"** $p_m$ (i.e. the momentum directly from the wave-equation if we are ignorant to the fact that anti-particles exist), and **"practical momentum"** $p_p$ (i.e. the momentum we would actually observe in real life).

When Schroedinger defined his equation, and therefore when Dirac defined his equation, and therefore all the formulas in quantum mechanics were defined, he used the convention of the plane wave that was used in EM, $$\psi=e^{i(\vec{r}\cdot\vec{p}_m-E_mt)}=\cos(\vec{r}\cdot\vec{p}_m-E_mt)+i\sin(\vec{r}\cdot\vec{p}_m-E_mt)$$. 

Let us assume $E_m$ is +ve and understand why this is chosen this way. The reason why the $E_mt$ term has to be the opposite sign is such that if $$\vec{p}_{m}$$ is +ve, the wave moves in the +ve direction with that momentum. Whether the entire exponent was negated was simply a matter of convention, since that would only change the sign of the imaginary sine term, and back then in EM you always took the real part only so it didn't matter. The energy and momentum we observe in particles is exactly the same as the energy and momentum defined in this equation so the wavefunction is still $$\psi=e^{i(\vec{r}\cdot\vec{p}_{p,u}-E_{p,u}t)}$$.

However, the issue arises when $E_m$ is -ve. If $E_m$ is -ve, then if $\vec{p}_m$ is +ve, the wave actually in practice will move in the -ve direction! (You can confirm this yourself by playing around with this plot [https://www.desmos.com/calculator/bujsvobpeb](https://www.desmos.com/calculator/bujsvobpeb)). As particle physicists, this is doubly annoying, since in practice we want to measure things. In real life, regardless of whether or not they are "anti-particles" or "particles", in experiments we see both as just little things moving with a definite momentum (which points in the direction the thing is actually going) and positive energy that we can measure. And therefore, we would like to deal with both particles and anti-particles in terms of "observable" or "practical" energy and momenta. 

For anti-particles, the "practical" energy would need to be positive, so if $E_m$ is -ve, $E_{p,v}=-E_m$. Similarly, to make the particle move in the correct direction again, we set $$\vec{p}_{p,v}=-\vec{p}_m$$. Therefore, the wavefunction can be more practically written as $$\psi=e^{-i(\vec{r}\cdot\vec{p}_{p,v}-E_{p,v}t)}$$.

In all of the formulas in this course, we always use $E\equiv E_{p,v},E_{p,u}$ and $$\vec{p}\equiv \vec{p}_{p,v},\vec{p}_{p,u}$$, i.e. to be the "practical momenta", even though mathematically behind the scenes they may be technically different things.

Recall that your spin will affect your (classical) energy as $$\Delta T_m=-\frac{q}{m}\vec{B}\cdot\vec{s}$$ (taking the classical case and ignoring the other terms just to understand this). Let's simplify that and assume that the magnetic field and the spin are aligned. Therefore in the particle and antiparticle cases respectively we get that:

$$
\begin{cases}
|\vec{s}_u|=-\Delta T_m\frac{m}{q|\vec{B}|}\\
|\vec{s}_v|=-\Delta T_m\frac{m}{q|\vec{B}|}\\
\end{cases}$$

$$\begin{cases}
|\vec{s}_u|=-\Delta T_{p,u}\frac{m}{q|\vec{B}|}\\
|\vec{s}_v|=+\Delta T_{p,v}\frac{m}{q|\vec{B}|}\\
\end{cases}$$

since spin is a measurable quantity, for the same "observed" energy difference the spin-quantum numbers are opposite, and therefore we can define $$\vec{S}_{p,v}=-\vec{S}_{p,u}$$.

The helicity and spins are measurable quantities. The spin can be physically measured in the lab, and we would need to measure it with respect to the **"practical"** momenta, since we in the lab would **physically measure the actual direction of travel and take the spin with respect to that**.


Therefore, we would need to define it using the "practical" quantities as (for particles, anti-particles respectively) where 
$$\vec{S}_{p,u}\equiv \vec{\Sigma}|\vec{S}_{p,u}|$$ 
where $$\vec{\Sigma}$$ is as defined in the notes. 

$$h \equiv \frac{\vec{S}_p\cdot \vec{p}_{p}}{|\vec{S}_p||\vec{p}_{p}|}$$

$$=\begin{cases}
\frac{\vec{S}_{p,u}\cdot \vec{p}_{p,u}}{|\vec{S}_{p,u}||\vec{p}_{p,u}|}\\
\frac{\vec{S}_{p,v}\cdot \vec{p}_{p,v}}{|\vec{S}_{p,v}||\vec{p}_{p,v}|}
\end{cases}$$

$$=\begin{cases}
\frac{\vec{\Sigma}\cdot \vec{p}_{p,u}}{|\vec{p}_{p,u}|}\\
\frac{-\vec{\Sigma}\cdot \vec{p}_{p,v}}{|\vec{p}_{p,v}|}
\end{cases}$$

which in the notes is defined as:

\begin{equation}
\boxed{
h=\begin{cases}
\frac{\vec{\Sigma}\cdot \vec{p}}{|\vec{p}|}\\
\frac{-\vec{\Sigma}\cdot \vec{p}}{|\vec{p}|}
\end{cases}
}
\end{equation}