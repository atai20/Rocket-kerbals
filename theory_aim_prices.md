//here will be thoery aim and prices
[little history](https://www.youtube.com/watch?v=lZRsSd0ismU)
* [rate of change of mass](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/model-rocket-engine-designation/)
* [our rocket model](first.ork)


* calculations for rocket thrust and velocity (please check this [meth](https://www.youtube.com/watch?v=6L3g5LduShM))

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
```math
\sum_{j=1}^{N} \mathbf{F}_{ext} + \sum_{j=1}^{N} \mathbf{F}_{int} = \sum_{j=1}^{N} m_j\cdot \vec{v}_j
```
since all the internal forces obey Newton's third law, they cancel out and sum to zero.
Therefore, F external is equal to the sum of the momentums?
Therefore, for a rocket in free space:
```math
\frac{dP}{dt} = 0
```
and a rocket in constant gravitational field (with air friction of course)
```math
Mg - Cv = M\frac{d\vec{v}}{dt} - z\frac{dM}{dt}
```
for simplicity, because I am not sure how to include air friction right now (i mean to solve the equation), I will only include gravitational field:
dividing by m we have
```math
g + \frac{z}{m}\frac{dM}{dt} = \frac{dv}{dt}
```
then we multiply everything by dt and integrate
```math
\int_{t_0}^{t_f}g\;dt + \int_{m_0}^{m_f} \frac{z}{m}\;dm = \int_{v_0}^{v_f}dv
```
```math
v_f - v_0 = z\cdot\ln{\frac{m_f}{m_0}} + g(\delta t)
```
of course we can assume initial velocity and initial time to be zero
