---
tags:
aliases: ["Multiple Regressionsanalyse", "Multiple Regression", "Multivariate Regressionsanalyse"]
---

# Multivariate lineare Regression
Eine multivariate lineare Regression funktioniert wie eine [[Lineare Regression|bivariate lineare Regression]], nur dass wir es mit mehr [[unabhängige Variable (UV)|unabhängigen Variablen (UV)]] zu tun haben.

Aus der alten Gleichung: $\hat{Y} = b_0 + b_1x$ wird dann:
$$ \hat{Y}= b_0 + b_1x_{1i} + b_2x_{2i}$$
Wir können dabei so viele unabhängige Variablen mit einbeziehen, wie wir wollen.
$$\begin{aligned} \hat{Y}&= b_0 + b_1\ x_{1i} + b_2\ x_{2i} + b_3\ x_{3i}
\\
\hat{Y}&= b_0 + b_1\ x_{1i} + b_2\ x_{2i} + b_3\ x_{3i} + b_4\ x_{4i} 
\\
\hat{Y}&= b_0 + b_1\ x_{1i} + b_2\ x_{2i} + b_3\ x_{3i} + b_4\ x_{4i} + ... + b_n\ x_{ni}  
\end{aligned}$$
Jede [[Variable]] bekommt also ihren eigenen [[Regressionskoeffizient|Steigungskoeffizient]]en.

### Ziel der multiplen Regression
Man kann dadurch den *Effekt der ersten unabhängigen Variable $x_1$ analysieren, während die anderen $x_2$, $x_3$, ... $x_i$ konstant* gehalten werden.
Das ist also eine Form der [[Drittvariablenkontrolle]] (vgl. [[ceteris paribus]]).
> [!example]
> Wie groß ist der Effekt von Körpergröße *und* Geschlecht auf das Gewicht?
> Gegeben sei folgende Gleichung:
> $\hat{Y} = −62,27 + 0,706 ∗ cm + 6,363 ∗ 𝐺eschlecht$
> Damit können wir dann folgende Fragen beantworten:
> - Wie schwer ist ein 1,85cm großer Mann, oder eine X cm große Frau?
> - Was hat den stärkeren Effekt auf $\hat{Y}$

#### Dummy-Variablen – um Variablen mit nicht geeigneten Ausprägungen nutzen zu können
Bei multivariaten linearen Regressionen kann man auch [[dichotom]]e Variablen nutzen. Dafür arbeiten wir mit dem [[numerisches Relativ|numerischen Relativ]].
Man kann auch [[Ordinalskala|ordinal skalierte]] Variablen umwandeln in [[Dummy-Variable]]n – damit kann man dann anhand des Steigungskoeffizienten ablesen, wie viel mehr oder weniger von der [[abhängige Variable (AV)|abhängigen Variable (AV)]] eine Gruppe hat.
> [!example]
> Wenn ich bei der oben genannten Gleichung also folgende numerische Relative hätte:
> ![[Pasted image 20220608165554.png|300]]
> Dann würde ich bei $Geschlecht$ für Mann eine $2$ einsetzen und für Frau eine $1$


### Welche Variable hat den stärkeren Effekt?
Wir können von der bloßen Gleichung einer trivariaten linearen Regression **nicht** ablesen, welche Variable den stärkeren Effekt auf $\hat{Y}$ hat.
> [!danger]
> *Niemals die Regressionskoeffizienten der Variablen miteinander vergleichen*, um herauszufinden, welche den stärkeren Effekt auf die abhängige Variable hat!!!

Es mag zwar ein [[Regressionskoeffizient]] größer sein als der andere, doch die können [[Skalenniveau|unterschiedlich skaliert]] sein und haben beide einen Wertebereich von $-\infty$  bis $+\infty$.
Also:
#### Der standardisierte Regressionskoeffizient
Trotzdem kann man messen, welche der Variablen einen stärkeren Effekt hat!
Dafür muss man den sogenannten [[standardisierter Regressionskoeffizient|standardisierten Regressionskoeffizienten]]  $\beta$ berechnen.
Der hat nur einen Wertebereich von $-1$ bis $+1$ und bildet damit einen Standard, mit dem man die Regressionskoeffizienten miteinander vergleichen kann.

### Hat das alles jetzt was gebracht? – Die Modellgüte
Um herauszufinden, wie viel besser meine Schätzung durch die Berechnung der linearen Regression geworden ist, also wie die [[Modellgüte]] ist, kann ich den [[Determinationskoeffizient]]en $R^2$ berechnen.
Der Determinationskoeffizient sagt aus, wie viel Prozent der [[Gesamtvarianz]] wir durch die unabhängigen Variablen erklären können.

