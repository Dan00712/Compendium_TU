# Praktische Mathematik I

## Vektorrechnung und Koordinatengeometrie

Ein Vektor ist ein Element eines Vektorraumes.
Jeder Vektor aus $\mathbb{R}^n$ hat genau $n$-Elemente

e.g 
$$
    \vec{x} = \begin{pmatrix} x_1\\x_2 \end{pmatrix} \in \mathbb{R}^2
    \vec{y} = \begin{pmatrix} y_1\\y_2\\y_3\end{pmatrix} \in \mathbb{R}^3
$$

### Betrag

Der Betrag eines Vektors wird gebildet in dem alle Komponenten Quadriert addiert werden
    und anschließend die Wurzel des Ergebnisses gebildet wird.

$$
    |\vec{v}| = \sqrt{\sum_v v_i^2}
    |\vec{x} = \sqrt{x_1^2 + x_2^2}|
    |\vec{y} = \sqrt{y_1^2 + y_2^2 + y_3^2}|
$$

### Basisdarstellung

Jeder Vektor kann als Linearkombination von Basisvektoren dargestellt werden.
Die bekannteste Basis ist hier die ** kartesische Basis**, welche aus den Vektoren 
$\vec{e}_x$ und $\vec{e}_y$ besteht.

Die kartesiche Basis is also die Menge $\{\vec{e}_x, \vec{e}_y \}$, wobei
$\vec{e}_x = \begin{pmatrix}1\\0\end{pmatrix}$ und
$\vec{e}_y = \begin{pmatrix}0\\1\end{pmatrix}$ sind.

Bzw. im $\mathbb{R}$:  $\{\vec{e}_x, \vec{e}_y, \vec{e}_z\}$, wobei
$\vec{e}_x = \begin{pmatrix}1\\0\\0\end{pmatrix}$ 
$\vec{e}_y = \begin{pmatrix}0\\1\\0\end{pmatrix}$ und
$\vec{e}_z = \begin{pmatrix}0\\0\\1\end{pmatrix}$ sind.

Bei einer Basis ist es wichtig, 
    dass alle Vektoren der Basis Linear unabhängig sind.

### Rechenoperationen

```{note} 
Multiplikation mit Skalar  
Hier wird jede Komponente mit dem Skalar multipliziert  
i.e. $s\cdot\vec{v} = \vec{x} \rightarrow s\cdot v_i = x_i$  
```

```{note}   
Addition  
Hier werden alle Elemente der gleichen Zeile addiert.  
i.e. $\vec{x} + \vec{y} = \vec{z}\rightarrow x_i + y_i = z_i$
```

```{note} 
Skalarprodukt  
$\mathbb{R}^2\times \mathbb{R}^2 \rightarrow \mathbb{R}$  
$\vec{x} \cdot \vec{y} \in \mathbb{R}$  
$\vec{x} \cdot \vec{y} = x_1y_1 + x_2y_2,\qquad \vec{x}, \vec{y} \in \mathbb{R}^2$  
$\vec{x} \cdot \vec{y} = x_1y_1 + x_2y_2 + x_3y_3,\qquad \vec{x}, \vec{y} \in \mathbb{R}^3$  
```

```{note} 
Kreuzprodukt  
Nur in $\mathbb{R}^3$ definiert  
$\times: \mathbb{R}^3\times\mathbb{R}^3\rightarrow\mathbb{R}^3, \vec{c} = \vec{a}\times\vec{b}$  

$$\vec{a}\times{b} = \begin{pmatrix}
    \begin{vmatrix}a_2&b_2\\a_3&b_3\end{vmatrix}\\
    -\begin{vmatrix}a_1&b_1\\a_3&b_3\end{vmatrix}\\
    \begin{vmatrix}a_2&b_2\\a_3&b_3\end{vmatrix}
\end{pmatrix}$$
```

### Koordinatengeometrie

![](/media/Polar_to_cartesian.svg.png)
![](/media/3D_Spherical.svg.png)


## Differenzierbare relle Funktionen

```{important}
Definition $f: A\rightarrow B$
Injektiv: für jedes $y\in B$ gibt es höchstens ein $x\in A$, welches zu $y$ abbildet
    $\forall x_1, x_2 \in A\quad x_1\neq x_2 \Rightarrow f(x_1)\neq f(x_2)$

Surjektiv: jedes $y\in B$ ist ein Bild eines $a\in A$
    $\forall y \in B \exists x\in A \text{mit} y = f(x)$

Bijektiv: Injektiv $\vee$ Surjektiv
```

Eine Funktion ist Injektiv, wenn sie streng monoton wachsend oder fallend ist
Eine Funktion ist Surjektiv, wenn $B = f(A)$ gilt

Eine Funktion muss Bijektiv sein damit eine Umkehrfunktion möglich ist

### Stetigkeit

Eine Funktion $f: D\rightarrow\mathbb{R}$ ist an der Stelle $x= a\in D$ stetig, 
    wenn gilt $lim_{x\rightarrow a-} f(x)= lim_{x\rightarrow a+} f(x) = f(a)$

Eine Funktion ist stetig, wenn sie an jeden Punkt stetig ist.  

Nicht stetige Punkte sind Sprungstellen oder Polstellen

### Differenzierbarkeit

Eine Funktion ist Differenzierbar wenn der Grenzwert von
    $lim_{\Delta x \rightarrow 0} \frac{f(x_0+\Delta x) - f(x_0}{\Delta x} = f'(x_0) = \frac{df}{dx}(x_0)$
    existiert.

Die Ableitung zeigt immer die momentan Steigung am Punkt $x_0$.

### Differenzial

```{important}
$f: D\rightarrow \mathbb{R}$ mit der Ableitung $f'$  
$dy = f'(x) dx$
```

### Folgernde Sätze

```{admonition} Ableitung der Umkehrfunktion
$(f^{-1}(x))' = \frac{1}{f'(f^{-1}(x)}$
```

```{admonition} Monotomie
- $f'(x) \geq 0~\forall x \in (a, b) \Rightarrow f$ ist **monoton steigend** auf $[a, b]$  
- $f'(x) > 0~\forall x \in (a, b) \Rightarrow f$ ist **streng monoton steigend** auf $[a, b]$  
- $f'(x) < 0~\forall x \in (a, b) \Rightarrow f$ ist **monoton fallend** auf $[a, b]$  
- $f'(x) \leq 0\forall x \in (a, b) \Rightarrow f $ ist **streng monoton fallend** auf $[a, b]$
```

```{admonition} Taylor Reihen
$$f(x) 
    = \sum_{k=0}^{\infty}\frac{f^{(k)}(x_0)}{k!}\cdot (x-x_0)^k
    = \sum_{k=0}^{n} \frac{f^{(k)(x_0)}}{k!} \cdot (x-x_0)^k + R_{n+1}(x)
$$
```

Taylor reihen werden verwendet um Funktionen um ein $x_0$ anzunähern.
Meistens wird nur das Taylor Polynom $n$-ten Grades gebildet 
    und das Restglied weggelassen.

## Integralrechnung

### Stammfunktion

Für eine Stammfunktion $F(x)$ von $f(x)$ muss gelten $F'(x) = f(x)$.  

Wenn $F(x)$ einen Konstanten Term $C$ hat fällt dieser Weg,
    deshalb muss man diesen bei unbestimmten Integralen berücksichtigenn

$F(x)$ ist deshalb nicht eindeutig bestimmbar, ohne zusätzliche Informationen.


Ein Bestimmtes Integral wird wie folgt berechnet:
$\int_a^b f(x) dx = F(b)-F(a)$, wobei $F(x)$ die Stammfunktion von$f(x)$ ist.  
Bei der Berechnung eines Bestimmten Integrales, 
    fällt der Konstante Term weg und muss deshalb nicht berücksichtigt werden.

### Hauptsatz der Differenzial und Integralrechnung

```{important}
$\int_a^b f(x) dx = F(b)-F(a)$, wobei $F(x)$ die Stammfunktion von$f(x)$ ist.  
```

### Integrationsregeln

```{admonition} Summen und Differenzenregel
$\int f(x) \pm g(x) dx = \int f(x) dx \pm \int g(x) dx$
```

```{admonition} Konstantenregel
$\int k\cdot f(x)dx = k\cdot\int f(x) dx$
```

```{admonition} Aufteilung von Integralen
$\int_a^b f(x) dx = \int_a^c f(x) dx + \int_c^b f(x) dx$
```

```{admonition} Verleiche von Integralen
- $f(x) \leq g(x), x\in [a, b] \Rightarrow \int_a^b f(x) dx \leq \int_a^b g(x) dx$
- Falls $|f(x)|$ integrierbar $\Rightarrow |\int_a^b f(x)| \leq \int_a^b f(x)$
- $|f(x)| \leq M ~\text{auf}~[a, b]\Rightarrow |\int_a^b f(x) dx| \leq M\cdot (b-a)$
```

### Integrationsmethoden

#### Partielle Integration 

$\int f'(x)g(x) dx = f(x)g(x) - \int f(x)g'(x) dx$

Oft ist es hier hilfreich das ganze mittels einer Tabelle zu machen
    und die diagonalen mit alternierenden Vorzeichen zu verwenden.

#### Substitution

$\int f(z) dz = \int f(\varphi(x)) \varphi'(x) dx = F(\varphi(x)) + C$

In der Praxis wird ein Term  $u$ bestimmt, 
    welcher ersetzt wird und anschließend muss das Differenzial ersetzt werden.
Es sollte kein Term mehr direkt von x abhängen sonder nur von $u(x)$

#### Spezielle Substitutionen

| Integral                     | Subsitution                   |
|------------------------------|-------------------------------|
| $\int R(e^{ax}$              | $z = e^{ax}, a\neq 0 $        |
| $\int R(sin(x), cos(x) dx$   | $t = tan(x/2)$                |
| $\int R(x, \sqrt{1+x^2}) dx$ | $x= sinh(t)$                  |
| $\int R(x, \sqrt{x^2-1}) dx$ | $x = cosh(t)$                 |
| $\int R(x, \sqrt{1-x^2})dx$  | $x = cos(t)$ od. $x = sin(t)$ |

#### Flächen 

Der Flächeninhalt $A$, der von der $x$-Achse und der Funktion $f$ eingeschlossen wird,
    wird im Intervall $[a, b]$ wie folgt berechnet

$A = \int_a^b |f(x)| dx$

Der Flächeninhalt zwischen zwei den Graphen der Funktionen $f$ und $g$, 
    wird wie folgt berechnet.
$A = \int_{x_1}^{x_2} |f(x) -g(x)| dx$, wobei das Flächenstück 
    durch die Schnittpunkte $x_1$ und $x_2$ begrenzt wird

#### Volumen

Bei der Rotation des Graphen der Funktion $f$ um die $x$-Achse
    entsteht ein Drehkörper mit dem Volumen 
    $V = \pi \int_a^b y^2 dx= \pi \int_a^b (f(x))^2 dx$

Die Rotation um die $y$-Achse kann Analog mittels der Umkehrfunktion berechnet werden,
    entsprechend muss die Funktion im Rotierenden Bereich Bijektiv sein.

## Komplexe Zahlen und Funktionen

### Grundbegriffe

$\mathbb{C} =  \{z = a + ib: a,b \in \mathbb{R}\}$

$i^2 = -1$

Für jede Komplexe Zahl $z$ existiert eine konjugiert Komplexe Zahl $\overline{z}$,
welche wie folgt gebildet wird.

$z = a + ib = r\cdot\exp(i\cdot \varphi) \Rightarrow \overline{z} = a-ib = r\cdot\exp(-i\cdot\varphi)$


Komplexe Zahlen haben auch einen Betrag und ein Argument.

Der Betrag wird über den Pythagoras gebildet: $|z| = r = \sqrt{a^2 + b^2}$
Das Argument wird auch über das Dreieck gebildet: $tan(\alpha) = \frac{b}{a}$

Beim Argument muss man aufpassen in welchen Quadranten man sich befindet,
    wenn $a < 0$ muss zum $\arctan$ $\pi$ addiert werden, 
    da der Tangens keine Winkel im 2. und 3. Quadranten angeben kann.

Da die Winkel meist im Intervall $[0, 2Pi)$ gefragt sind, 
    muss man $+2\pi$ rechnen, wenn man im 4. Quadranten ist.
Dieser Punkt kann sich aber je nach Aufgabestellung ändern!

| $a=x$ | $b=y$ | Quadrant | $arg(a+ib)$                    |
|-------|-------|----------|--------------------------------|
| $a>0$ | $b>0$ | I        | $arctan(\frac{b}{a})$          |
| $a<0$ | $b>0$ | II       | $arctan(\frac{b}{a}) + \pi$    |
| $a<0$ | $b<0$ | III      | $arctan(\frac{b}{a}) + \pi$    |
| $a>0$ | $b<0$ | IV       | $arctan(\frac{b}{a}) (+ 2\pi)$ |

Für die Komponentendarstellung gelten im Grunde die selben Rechenregeln.

Mit den Besonderheiten:
$z\cdot\overline{z} = |z|^2$


### Polarform

Die Polarform wird mit dem Betrag $r$ und dem Argument $\varphi$ gebildet und sieht wie folgt aus
$z = r\cdot \exp(i\cdot \varphi)$

In der Polarform gelten die Regulären exponential Rechenregeln

Besondere Rechenregeln

- $\exp(0) = 1$
- $\exp(z) \neq 0, \forall z \in \mathbb{C}$
- $\overline{\exp(z)} = \exp(\overline{z})$
- $|\exp(z)| = \exp_{\mathbb{R}}(z), \forall z \in \mathbb{C}$
- $\exp(z)^n = \exp(n\cdot z)$

### Bereichsangaben

Es können einfach Bereiche Definiert werden

Bsp.
$M = \{z \in \mathbb{C}: |z| \leq 1, \frac{\pi}{2} < arg(z) \leq \pi\}$

### Formeln

```{admonition} Formel von Moivre
$z^n=  |z|^n\exp(in\varphi)$
```

### Wurzeln

Eine Zahl $z$ ist die $n$-te komplexe Wurzel von $w$, wenn die Beziehung $z^n = w$ erfüllt ist.

Da, wenn das Argument $+2\pi$ ist, es sich um die selbe Zahl handelt,
    können Zahlen in den Winkelbereich $[0, 2\pi)$ hereinfallen,
    wodurch mehrere Wurzeln entstehen.
Somit gibt es bei der $n$-ten Wurzel n Lösungen, 
    die verschiedenen Lösungen werden mit 
    $z_k = \sqrt[n]{|z|} \exp\left(i \left(\frac{\phi}{n} + k\frac{2\pi}{n}\right)\right)$ 

Der Wert für $k=0$ wird als Hauptwert bezeichnet.

### Quadratische Gleichungen

Das Polynom
$f(z) = az^2 + bz +c $
hat genau zwei Nullstellen

Mit $p,q \in \mathbb{R}$, ergibt sich die Diskriminante $D= \left(\frac{p}{2}\right)^2-q$

Wenn $D>0$ sind die Nullstellen: $x_{1,2} = -\frac{p}{2}\pm\sqrt{\frac{p^2}{4}-q}$  
Wenn $D<0$ sind die Nullstellen: $x_{1,2} = -\frac{p}{2} \pm i\sqrt{q-\frac{p^2}{4}}$

## Kurven und Felder
