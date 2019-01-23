## Reaction-Diffusion Systems

---

### Hauptziel

Kontinuierliches System simulieren, um Volume Rendering auszureizen

---

<section data-background-iframe="applets/diffusion.html">

## Diffusion

Differentalgleichung
$$\dot y = d \cdot \nabla^2 y $$

Note:

+ "Heat Equation"

---

## Reaction-Diffusion
Zwei Diffusions-Komponenten mit Interaktionsterm

###### Gray-Scott Modell

$$\partial_t a = d_a \nabla^2 a - ab^2 + f (1 - a)$$
$$\partial_t b = d_b \nabla^2 b + ab^2 - (f + k) b$$

<iframe width="540px" height="280px" data-src="applets/reactiondiffusion.html"></iframe>

Note:

+ Zwei Komponenten A, B
+ Interaktionsterm simuliert chemische Reaktion
  + A + 2B -> 3B
  + B -> (Abfall)
+ *Klick*
+ Laplace-Operator einzige räumliche Komponente
  + Laplace-Operator in 3D Schlüssel zum Erfolg

---

## Diskreter Laplace Operator

* **2D**: Konvolution mit $\begin{pmatrix}0&1&0\\\\1&-4&1\\\\0&1&0\end{pmatrix}$ <!-- .element: class="fragment" -->
* **3D**: Konvolution mit $\begin{pmatrix}0&1&0\\\\1&-4&1\\\\0&1&0\end{pmatrix}$ <!-- .element: class="fragment" -->

---

## Ziel

Volumetrisches Rendern von 3D Reaction-Diffusion

---

### Euler-Methode

$\dot{y} = f(y), \quad y_0$ gegeben

###### Iteration

$y_{n+1} = y_n + h \cdot f(y_n)$

---

<section data-background-iframe="applets/reactdiff-euler.html" data-background-size="contain"></section>

---

<section data-background-iframe="applets/integrationmethods.html"></section>

$$\dot{y} = \begin{pmatrix}0&1\\\\ -1&0\end{pmatrix} y$$

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

<section data-background="static/calculation.svg" data-background-size="contain"></section>
### Berechnungsschritte

---

[final](3dgol_rungekutta.html)


---

Space

---

<section data-background-iframe="../3dgol_rungekutta.html" data-background-size="contain"></section>
