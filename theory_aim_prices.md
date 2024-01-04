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
