---
title: "⚡ Impact Ionization Rate and Ionization Integral"
date: 2026-01-24
# star: false
draft: false
categories:
  - Semiconductor Physics
tags:
  - BSIM model
description: Introduced to impact ionization
---

{{< katex >}}

## Impact ionization

Consider a diode junction with applied the reverse bias, the built in electric field is constructed and forms the depletion region. We will expect that the charged particles are accelerated within this strong field region undergoing the scatter process when the applied voltage is high enough. Charged particles possess high energy that can collide to other bonded particles, to transfer excess energy to knock it into the conducting or valence band to create the electron-hole pair. This a serial of chain reaction can happen so that leads to the carrier multiplication and the avalanche breakdown. This scattering phenomenon is so-called impact ionization which can generate more carriers and amplify the current in the device.

![](./ionization.png "Moving electron collides the bonded particle to create the eletron-hole pair[1].")

## Ionization Rate and Ionization Integral

As we quantifying the impact ionization of the system, ionization rate should be introduced which can be defined as the number of the carrier is generated per unit distance within two collide, which can be expressed as[2]:

$$
\alpha_n = \frac{1}{n} \frac{dn}{d(tv_n)} = \frac{1}{nv_t}\frac{dn}{dt}
$$

Accounting for the creation of the electron-hole pair, the creation of the number of hole during the collision is same as electron ones as:

$$
G^{II} = \frac{dn}{dt} =\frac{dp}{dt}= nv_n \alpha_n = pv_p\alpha_p
$$

During the _impact ionization_ process, we can analyze variance of the current density flow from the one end of the depletion region to the another. Then, we define \\(M\\) the multiplication factor to describe the change of the current density.
First, let's define the total current in the steady state as follows:
$$
J=J_n + J_p
$$

which should be constant value along the device. Thence, assume the width of depletion region is \\(W\\), the current density at the one end of position \\(x=0, J_p(0)=J_{p0}\\). Consider the impact ionization process occurs within the depletion region, the current density at x=W should be
$$
J_p(W)=J_{p0}M_p=J.
$$

For the change of the current density \\(J_p\\) during the collision which can be evaluated as
$$
dJ_p = J_p \alpha_pdx+J_n\alpha_ndx
$$
which can reformulate as the first order differential equation[2]
$$
\frac{dJ_p}{dx}= J_p\alpha_p+(J-J_p)\alpha_n.
$$

We can turn this differential equation into a general form as
$$
y' + Py = Q
$$
where \\(P = (\alpha_p -\alpha_n)\\) and \\(Q = \alpha J\\). The homogeneous solution can be obtained easily as 
$$
y_h = C \exp(-\int^x_0 P dx')
$$
where C is the integral constant. For the inhomogeneous one, we can differentiate the homogeneous one first,
$$
y'_p = C' \exp(-\int^x_0 Pdx') - P y_p.
$$
Then, we put it into our equation that we have 
$$
Q = C' \exp(-\int^x_p P dx) \Rightarrow C = \int^x_0 Q \exp(\int^{x'}_p P dx'') dx'.
$$
Therefore, the inhomogeneous solution can be expressed as
$$
y_p =  \exp(-\int^x_0Pdx') [\int^x_0 Q \exp(\int^{x'}_0Pdx'')dx].
$$

Finally, the general solution is obtained as
$$
y = y_h+y_p=\exp(-\int^x_o P dx' ) [\int^x_0 Q \exp (\int^{x'}_0 P dx'')dx' + C].
$$

Applying the boundary condition, \\(J_p(0) = J_{p0} \\) and \\( J_p(W) = J = M_p J_{p0} \\), the current density has the forms as

$$
J_{p}(x) = J \exp(-\int^x_0 (\alpha_p - \alpha_n) dx') [\int^x_0 \alpha_n  \exp( \int^{x'}_0 -(\alpha_p - \alpha_n) dx'') dx' +\frac{1}{M_p} ].
$$

To simplified the solution above, we consider the current density \\(J_p(W) = J\\) and use the integration by part for the integral on the exponential which refers to
$$
\int^W_0 (\alpha_p - \alpha_n) \exp(\int^{x''}_0 -(\alpha_p - \alpha_n) dx'') dx' = -\exp(\int^W_0 -(\alpha_p - \alpha_n ) dx') + 1.
$$
The final becomes as
$$
1 = \int^W_0 \alpha_p \exp(-\int^x_0 (\alpha_p-\alpha_n)dx')dx \Rightarrow 1 = \int^W_0 \alpha dx
$$
where \\(M_p \rightarrow \infty \\) when avalanche occurs and assumes that \\(\alpha = \alpha_p = \alpha_n\\). The integral is so called the ionization integral, here, we should notice that once we know the form of the ionization rate \\(\alpha\\) as function of electric field, we can easily derive the breakdown voltage from the ionization integral. 




## References

[1] https://en.wikipedia.org/wiki/Impact_ionization

[2] https://www.iue.tuwien.ac.at/phd/triebl/node20.html
