---
tags:
aliases: ["R-Quadrat"]
---

# Determinationskoeffizient
Den Determinationskoeffizient $R^2$ berechnet man, wenn man herausfinden will, ob die Berechnung einer [[Lineare Regression|linearen Regression]] zu einem besseren Schätzwert geführt hat. 
Der Determinationskoeffizient $R^2$ sagt aus, *wie viel Prozent der [[Gesamtvarianz]] wir durch die [[unabhängige Variable (UV)|unabhängigen Variablen (UV)]] erklären können*. Wichtiger ist aber das [[Adjustiertes R^2|adjustierte R^2]] (s.u.).

Also: Wie gut ist mein Modell? –> [[Modellgüte]]
> [!example]-
>   Wie viel Prozent der Unterschiedlichkeit der Einkommen, lassen sich dadurch erklären, dass Menschen unterschiedlich viel arbeiten, unterschiedliche Geschlechter haben, unterschiedliche Staatsbürgerschaften haben und unterschiedlich viel Schulbildung haben?

Der Determinationskoeffizient hat einen Wertebereich von $0$ bis $1$. $0$ bedeutet dann, dass keine [[Varianz]] erklärt wird und bei $1$ wurde die gesamte Varianz erklärt.

Der Determinationskoeffizient ist ein [[PRE-Maß]], man drückt damit also aus, wie viel besser die Vorhersage wird.

Meistens ist das eine Prozentzahl, die dann angibt, wie viel Prozent der Varianz erklärt werden kann. Wenn es keine Prozentzahl ist, dann nimmt man das Ergebnis $*100$ und erhält eine Prozentzahl.

### Das adjustierte $R^2$
> [!danger]
> Wenn man neue [[unabhängige Variable (UV)|unabhängige Variablen (UV)]] hinzufügt, dann verbessert sich *automatisch* die Vorhersage!  Der Determinationskoeffizient hat an sich also keine sehr große Aussagekraft.

Wichtiger bei der Verwendung ist daher das [[Adjustiertes R^2|adjustierte R^2]]. *Das adjustierte $R^2$ berechnet den Effekt der Varianzerklärung durch zusätzliche Variablen mit ein.*

### Was genau berechnet der Determinationskoeffizient?
Definieren wir die Elemente, die wir uns bei der Berechnung eines Determinationskoeffizienten anschauen:
- *Gesamtvarianz*: Der Abstand zwischen dem tatsächlichen Wert $Y$ und dem [[Arithmetisches Mittel|Mittelwert]]
- *Erklärte Varianz*: Der Abstand zwischen dem Schätzwert $\hat Y$  und dem [[Arithmetisches Mittel|Mittelwert]]. 
- *Unerkärte Varianz*: Der Abstand zwischen dem Schätzwert $\hat Y$ und dem tatsächlichen Wert $Y$ – die [[Residualgröße]].
	![[Pasted image 20220617165501.png|400]]
Der Mittelwert ist hier nicht eingezeichnet, wäre aber parallel zur x-Achse, der Schätzwert $\hat Y$ ist die gestrichelte blaue Gerade und der tatsächliche Wert $Y$ ein blauer Punkt. 

Mit diesen Elementen können wir den Determinationskoeffizienten erklären:
> [!summary]
> Determinationskoeffizient = Anteil der erklärten Varianz an der Gesamtvarianz
> $$R^2 =\frac{erklärte\ Varianz}{Gesamtvarianz}$$