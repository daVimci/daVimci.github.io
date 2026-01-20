---
title: "⚡ Breakdown Voltage Calculation "
date: 2026-01-20
# star: false
draft: true
categories:
  - Semiconductor Physics
tags:
  - BSIM model
description: Breakdown voltage of Junction
---

{{< katex >}}

## Impact ionization

Consider a diode junction with applying the reverse bias, the built in electric field is constructed by the depletion region. We will expect that the charged particles are accelerated within this strong field region undergoing the scatter process when the applied voltage is high enough. Charged particles possess high energy that can collide to other bonded particles, to transfer excess energy to knock it into the conducting or valence band to create the electron-hole pair. This a serial of chain reaction can happen so that leads to the carrier multiplication and the avalanche breakdown. This scattering phenomenon is so-called impact ionization which can generate more carriers and amplify the current in the device.

## Ionization rate and integral

As we quantifying the impact ionization of the system, ionization rate is introduced which can be defined as the number of the carrier is generated per unit distance within two collide, which can be expressed as[1]:

$$
\alpha_n = \frac{1}{n} \frac{dn}{d(tv_n)} = \frac{1}{nv_t}\frac{dn}{dt}
$$

Accounting for the creation of the electron-hole pair, the creation of the number of hole during the collision is same as electron ones as:

$$
G^{II} = \frac{dn}{dt} =\frac{dp}{dt}= nv_n \alpha_n = pv_p\alpha_p
$$

To quantify the _impact ionization_ process, we can analyze variance of the current density flow from the end of the depletion region to the another. We can define _M_ the multiplication factor to describe the change of the current density.
First, we can define the total current in the steady state as follows:

$$
J=J_n + J_p
$$

which should be constant value along the device.

## Breakdown voltage calculation

## RESURF mechanism

## References

[1]

[2]
