# Analysis I

${n\choose k} = \frac{n!}{k!(n-k)!}$  
${(n+1)\choose k} = {n \choose (k-1)} + {n\choose k}$  
${n\choose n}={n\choose 0} = 1$

$\lim_{n\rightarrow \infty} \left(1+\frac{1}{n}\right)^n = \sum_{k=0}^{\infty}\frac{1}{k!} = e$
$\lim_{n\rightarrow \infty} \left(1+\frac{x}{n}\right)^n = \sum_{k=0}^{infty}\frac{x^k}{k!} = e^x$

## Sums

$\sum_{k=1}^{n}k=\frac{1}{2}n(n+1)$  
$\sum_{k=0}^{n}q^k = \frac{q^{n+1}-1}{1-q}$  
$\sum_{k=0}^{n}{{n}\choose{k}}x^{k} y^{n-k} = (x+y)^k$


## Abbildungen

Injektiv: $(a_n \neq a_m\Rightarrow f(a_n)\neq f(a_m))\Rightarrow (f(a_n) = f(a_m) \Rightarrow a_n = a_m)$  
Es existiert für jedes Element im Bildbereich *höchstens* 1 Element im Definitionsbereich  
Keine Elemente im Bildbereich werden doppelt getroffen

Surjektiv: $\forall b\in B: \exists a\in A \text{with} b = f(a), f: A\rightarrow B$  
Es existiert für jedes Element im Bildbereich mindestens 1 Element im Definitionsbereich  
Alle Elemente im Bildbereich werden getroffen

Bijektiv: Injektiv $\wedge$ Surjektiv

Bijektiv Vorraussetzung für Umkehrfunktion

$(f\circ g)^{-1} = g^{-1} \circ f^{-1}$

## Mengen

Mächtigkeit einer Menge ist die Anzahl der Elemente $|A|$  

Gleiche mächtigkeit zu $\mathbb{N}$ *abzählbar unendlich* ($\mathbb{Q}$, $\mathbb{Z}$)

## Reelle Zahlen
Alle Intervalle in $\mathbb{R}$ sind gleich mächtig

$||x| - |y|| \leq |x\pm y| \leq |x| + |y|$  


Supremum: kleinste obere Schranke von einer Menge
Infinum: größte untere Schranke von einer Menge
sind nicht in der Menge enthalten, sind ansonsten Max und Min

$\epsilon$-Umgebung: $K_{\epsilon}(x) = (x-\epsilon, x+\epsilon)=\{ y\in \mathbb{R}: |y-x|<\epsilon \}$

x ist  
- innerer Punkt von $A$, wenn gilt$\exists \epsilon: K_{\epsilon}(x) = A$
- äußerer Punkt von $A$, wenn kein Innerer Punkt
- Randpunkt, wenn $A=[a, b]$ und $x=a \vee x=b$
- Häufungspunkt, wenn in einem $\epsilon$-Gebiet unendlich viele Werte sind


## Konvergenzwert

Reihe: $a=\lim_{n\rightarrow\infty} a_n = \lim_{n\rightarrow\infty}a_{n\pm 1}$  
Geometrische Reihe: $\sum_{k=0}^{\infty}r^k = \frac{1}{1-r}:~0<r<1$  

Quotientenkriterium: $p = \left|\frac{a_{k+1}}{a_k}\right|$
- $p \leq q < 1$: Absolut konvergent
- $p \geq 1$: divergent  
- $p \leq 1 \wedge \not \leq q < 1$: keine allgemeine Aussage

Quotientenkriterium 2: $r := \lim{k\rightarrow \infty \left| \frac{a_{k+1}}{a_l}\right|}$  
- $r < 1$: absolut konvergent 
- $r > 1$: divergent  
- $r = 1$: keine allgemeine Aussage

Wurzelkriterium: $r:= \lim_{k\rightarrow \infty}\sqrt[k]{|a_k|}$ 
- $r < 1$: absolut konvergent  
- $r > 1$: divergent  
- $r = 1$: keine Aussage

## Konvergenz

Grenzwert eindeutig bestimmbar  
Cauchyfolge: $\forall \epsilon>0 \exists N=N(\epsilon)\forall n,m \in \mathbb{N}\wedge n,m \geq N(\epsilon) |a_m-a_n|<\epsilon$


Seien $a_n$ und $b_n$ konvergente Folgen, mit den Werten $a$ und $b$, 
    ist auch $c_n = a_n\pm b_n$ konvergent,
    mit den Wert $c = a \pm b$  
gleiches mit $a_n/b_n
und bei multiplikation mit skalar$  

Teilfolge: Folge $a_n$ mit weiterer folge $0<n_1<n_2<...$ dann ist a_{n_{k}} eine Teilfolge

Konvergiert eine Folge konvergiert auch jede Teilfolge

Jede Folge hat eine Konvergente Teilfolge

Monoton wachsend $\wedge$ von oben Beschränkt $\Rightarrow$ konvergent
Monoton fallend $\wedge$ nach unten Beschränkt $\Rightarrow$ konvergent

absolut Konvergent wenn gilt $\sum_{k=0}^{\infty}|a_k| =a$  

Umordnung kann konvergenz verändern: unbedingt Konvergent: jede Umordnung konvergent zum selben Wert sonst bedingt  
unbedingt konvergent $\equiv$ absolut konvergent  

$\sum_{k=0}^{\infty} a_k\cdot \sum_{k=0}^{\infty} b_k = \sum_{k=0}^{\infty} \sum_{l=0}^{k}a_{k-l}\cdot b_l$  

## Funktionen
