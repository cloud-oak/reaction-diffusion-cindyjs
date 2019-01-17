## Reaction-Diffusion Systems

---

<section data-background-iframe="examples/diffusion.html">

## Diffusion

Differentalgleichung
$$\dot y = d \cdot \nabla^2 y $$

<!-- <iframe width="540px" height="280px" data-src="examples/diffusion.html"> -->

---

<section data-background-iframe="examples/diffusion.html">

## Reaction-Diffusion
Zwei Diffusions-Komponenten mit Interaktionsterm

###### Gray-Scott Modell

$$\partial_t a = d_a \nabla^2 a - ab^2 + f (1 - a)$$
$$\partial_t b = d_b \nabla^2 b + ab^2 - (f + k) b$$

<iframe width="540px" height="280px" data-src="examples/reactiondiffusion.html">

---

## Ziel

Volumetrisches Rendern von 3D Reaction-Diffusion

---

### Euler-Methode

$\dot{y} = f(y), \quad y_0$ gegeben

###### Iteration

$y_{n+1} = y_n + h \cdot f(y_n)$

---

<section data-background-iframe="examples/integrationmethods.html"></section>

---

### Runge-Kutta

$\dot{y} = f(y), \quad y_0$ gegeben

###### Iteration

* $k_1 = f(y_n)$
* $k_2 = f(y_n + \frac{h}{2} k_1)$
* $k_3 = f(y_n + \frac{h}{2} k_2)$
* $k_4 = f(y_n + h k_3)$
* $y_{n+1} = y_n + \frac{h}{6} \cdot (k_1 + 2 k_2 + 2 k_3 + k_4)$

---

<section data-background="calculation.svg" data-background-size="contain"></section>
### Berechnungsschritte

---


---

Space

---

<section data-background-iframe="../3dgol_rungekutta.html"></section>
