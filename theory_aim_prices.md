//here will be thoery aim and prices


* calculations for rocket thrust and velocity (please check this meth)

We are given M, dm, v, dv, z (rate of fuel expulsion), t
where dm is mass of fuel, M is mass of rocket

```math
\vec{\mathbf{F}} = \frac{dP}{dt}
```
```math
\;\;\; P(t) = (M + dm) \cdot \vec{v}
```
```math
P(t + dt) = M(\vec{v} + dv) + dm(v + dv + z)
```
```math
dP = P(t + dt) - P(t) = Mdv + dm(dv + z)
```
```math
\frac{dP}{dt} = M\cdot \frac{d\vec{v}}{dt} + z\frac{dm}{dt}
```
```math
\frac{dP}{dt} = M\frac{d\vec{v}}{dt} - z\frac{dM}{dt}
```

//TODO: where do the external forces go?

```math
\sum_{j=1}^{N} \mathbf{F}_{ext} + \sum_{j=1}^{N} \mathbf{F}_{int} = \sum_{j=1}^{N} m_j\cdot \vec{v}_j
```
since all the internal forces obey Newton's third law, they cancel out and sum to zero.
Therefore, F external is equal to the sum of the momentums?
Therefore, for a rocket in free space:
```math
\frac{dP}{dt}
```
