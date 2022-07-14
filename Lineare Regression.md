---
tags:
aliases: ["Ordinary-Least-Squares Regression", "OLS-Regression", "Kleinste-Quadrat-Regression", "bivariate lineare Regression"]
---

# Lineare Regression
Eine lineare Regression nutzt man, um mithilfe [[Stichprobe|der erhobenen Daten]] *Schätzwerte für die [[Grundgesamtheit]]* zu erhalten. 
Es ist ja ohnehin das Ziel so einer [[Datenerhebung|Erhebung]], dass man dadurch A4ussagen über die Grundgesamtheit treffen kann. Mit der linearen Regression also kann man dem ein Stückchen näher kommen.
> [!question] Die Hauptfrage lautet:
> Wie viel [[Varianz]] (also Streuung) der [[abhängige Variable (AV)|abhängigen Variable (UV)]] können wir erklären, mithilfe der [[unabhängige Variable (UV)|unabhängigen Variable (UV)]]?

Bei diesem Verfahren möchte man die Summe der Abstände zwischen den quadrierten und addierten einzelnen Werten und [[Regressionsgeraden]] minimal halten -> "Kleinste-Quadrat-Regression"

![[Pasted image 20220608162507.png|400]] 
Als Basis einer linearen Regression hat man also unabhängige Variablen $x_1, x_2, x_3$.
Mit denen berechnet man *Schätzwerte* für die abhängige Variable $y$.
Man kann damit bestimmen: 
- hat die Variable einen *positiven oder negativen Effekt* auf die abhängige Variable?
- wie viel Prozent der Varianz der abhängigen Variable können wir mit der UV erklären?
- Welche Drittvariablen einen Einfluss haben ([[Drittvariablenkontrolle]])

### Begrifflichkeiten
Neben den Komponenten der Geradengleichung (s.u.) gibt es Bezeichnungen für die Variablen.
Die *unabhängige Variable X* bezeichnet man dabei auch als [[unabhängige Variable (UV)|Regressor]], oder Prädiktor.
Die *abhängige Variable Y* als [[abhängige Variable (AV)|Regressand]].

### Arten der linearen Regression
Man unterscheidet diese Arten der linearen Regression je nach der Anzahl der UVs:
- [[Lineare Regression|bivariate lineare Regression]] – dafür nutzt man die allg. Geradengleichung (s.u.) und metrische Variablen. Es gibt nur die Variablen X und Y, das wird hier erklärt
- [[trivariate lineare Regression]] – hier nutzt man metrische und [[dichotom]]e Variablen. Zusätzlich zu Y gibt es standardisierte und unstandardisierte X
- [[Multivariate lineare Regression]] – hier nutzt man metrische, dichotome *und* [[Ordinalskala|ordinale]] Variablen. Varianzaufklärung: Determinationskoeffizient $R^2$ ?????

### Allgemeine Geradengleichung
$$\hat{Y} = b_0 + b_1x$$
$\hat{Y} =$ *Schätzung* der abhängigen Variablen Y 
$b_0=$ [[Regressionskonstante]] – "Y-Achsenabschnitt", *Sockelbetrag*, niedrigster Wert von allen
$b_1=$ [[Regressionskoeffizient]] – *Steigung und Stärke des Zusammenhangs*; Steigung der [[Regressionsgeraden]]
$x=$ unabhängige Variable
![[Pasted image 20220605144227.png|400]]

$\hat{Y}$ ("Y Dach") ist die *Schätzung*. Der tatsächliche Wert der Realität ist $Y$ ohne Dach! Den Unterschied zwischen beiden nennt man die [[Residualgröße]].
Dafür ergibt sich:
$$\begin{aligned}
Y &= \hat{Y} +e \\
 &= b_0 + b_1X+e
\end{aligned}$$
$e=$ [[Residualgröße]]
$Y=$ exakte Messung der AV Y


### Voraussetzungen
Meine [[Variable|Variablen]] müssen auf bestimmte Art und Weise vorliegen, damit ich mit denen eine lineare Regression machen kann.

- UVs und AVs
	- Die [[abhängige Variable (AV)|abhängigen Variablen (AV)]] **müssen** ein [[Metrische Skala|metrisches Messniveau]] haben.
	- Die [[unabhängige Variable (UV)|unabhängigen Variablen (UV)]] können jedes [[Skalenniveau]] haben, sie müssen aber, wenn sie nicht metrisch sind, in eine [[Dummy-Variable]] umgewandelt werden.
- Die UVs *und* AVs müssen (näherungsweise) [[Normalverteilung|normalverteilt]] sein.

> [!example]
> ##### Fragestellung
In einer [[Stichprobe]] erhalten wir eine unterschiedliche Lesekompetenz, also eine unterschiedliche [[Varianz]]. Warum?
Welche Variablen können erklären, warum manche SchülerInnen besser und andere schlechter lesen können?
Idee: Vielleicht liegt es an sozio-ökonomischen Ressourcen? Die Korrelation zwischen der Lesekompetenz und den Ressourcen ist mit 0.4057 recht stark.  
Wie sieht das grafisch aus?
![[Pasted image 20220603191427.png|300]]
Sowohl Lesekompetenz als auch sozioökonomischer Status sind annähernd gleich verteilt.
>
> ##### Gesamtvarianz
Schauen wir uns die Varianz der Lesekompetenz an in Abhängigkeit vom sozioökonomischen Status an. Wir können einen [[Arithmetisches Mittel|Mittelwert]] berechnen, der bei $520$ Punkten liegt.
![[Pasted image 20220603191642.png|400]]
Die [[Gesamtvarianz]] ist nun der *Abstand zwischen dem Mittelwert der Lesekompetenz der ganzen Stichprobe*, also der roten Linie, *und der Lesekompetenz eines einzelnen Befragten*, also einem blauen Punkt.
>>Mit einer linearen Regression können wir nun einen *besseren Schätzwert* finden als den Mittelwert.
>>Dadurch werden die *Abstände zwischen Schätzwert (roter Linie) und einzelnem Wert (blauer Punkt) kleiner*.
>>Die beste Gerade ist die, bei der die Summe der *quadrierten Abstände der Werte zur Gerade* am kleinsten ist. Deshalb heißt dieses Verfahren der linearen Regression so: *Kleinste-Quadrat-Regression.*
>
Es ergibt sich:     $\hat{Y}=381+40x$ 
![[Pasted image 20220608163333.png|400]]
> #### Interpretation
>  - *Steigung*: Mit jedem Anstieg um eine Einheit auf der X-Achse, steigt die Lesekompetenz um 40 Punkte
>  - *Konstante*: Jemand mit einem sozio-ökonomischen Status von 0, hat eine durchschnittliche Lesekompetenz von 381 Punkten
>
>  Wenn man jetzt einen Wert einsätzt für jemanden, dessen sozio-ökonomischer Status zB bei 1,4 liegt, dann kann man daraus die geschätzte Lesekompetenz berechnen, indem man den Wert für $x$ einsetzt.
>
> Die [[Residualgröße]] beschreibt jetzt die Abstände zwischen dem Schätzwert und dem tatsächlichen Wert, also den Abstand zwischen der blauen Linie und einem höher oder tiefer liegenden blauen Punkt.

> [!success]
> Mit einer linearen Regression trifft man zwar immer noch nicht jeden Wert exakt, doch die Schätzung wird besser als mit dem Mittelwert!

