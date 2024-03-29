//here will be thoery aim and prices
[little history](https://www.youtube.com/watch?v=lZRsSd0ismU)
* [rate of change of mass](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/model-rocket-engine-designation/)
* [our rocket model](first.ork)
* [magnificent shroket](shroket.ork)
* [combustion chamber](https://www.youtube.com/watch?v=H4YZxb2E5PA)
* [form of an engine](https://www.youtube.com/watch?v=b9NcdDhhZio)
* [form of an engine #2](https://www.youtube.com/watch?v=sTZhUrflZF4)
* [kerosene rocket engines](http://www.astronautix.com/h/h2o2kerosene.html)


* calculations for rocket thrust and velocity (please check this)

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
Mg + Cv = M\frac{d\vec{v}}{dt} - z\frac{dM}{dt}
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

//please check new formulas!!!

air friction:
 - p - fluid density (air)
 - v2 - speed of object relative to fluid (in our case air)
 - Cdrag - drag coefficient (depends on shape use [this](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D1%8D%D1%84%D1%84%D0%B8%D1%86%D0%B8%D0%B5%D0%BD%D1%82_%D1%81%D0%BE%D0%BF%D1%80%D0%BE%D1%82%D0%B8%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F_%D1%84%D0%BE%D1%80%D0%BC%D1%8B) link)
 - A - Cross sectional area of an object (says for itself)
```math
F_d =\frac{1}{2}\ ∗ p ∗ v_2 ∗ C_d ∗ A
```
So we can assume that we have conical shaped end of rocket, it means according to the table we have Cdrag = 0.75, p = 1.293 kg m−3, A depends on our model, according to current one, it's at most 210 cm^3, and speed of our current engine in maximum state is 219 meters per second, but it's no good for 43-46 seconds (IT'S 46.9 SECONDS BRO), so I changed it a bit, it's really close to requirements but not enough, also if we are going to find "best proportion" I highly doubt we will make it work this way, because of conditions. We have to come up with some system.

Evaluating formula yields: at most 0.1 newtons, (0.05-0.1 around, depending on A, which will change during construction)

update: 2/8/24
for personal rocket, after some calculation we determine the necessary escape velocity is at least
```math
v_{esc} = \sqrt{2gR_e}
```
which is approximately 
```math
1.1 \cdot 10^4
```
