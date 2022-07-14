---
tags:
aliases: [""]
---

# Datenaufbereitung
Bei der Datenaufbereitung formatiert man die Daten korrekt, sodass man von da aus mit ihnen weiter arbeiten kann. 

Für die Datenaufbereitung gibt man den [[Variable|Variablen]] einen [[Variablennamen]].
Bei [[empirisches Relativ|empirischen Relativen]] fügt man ein [[Variablenlabel]] und ein [[Wertelabel]] hinzu.

### Missings
Wenn es fehlende Werte gibt, dann nennt man diese [[Missings]]. Missings sind Werte, die keine Informationen über die [[Varianz]] geben, zB *"keine Angabe"*

Den Missings gibt man sehr hohe [[numerisches Relativ|numerische Relative]], damit dann bei den [[Analyseverfahren]] auffällig verzerrte Werte herauskommen, wenn man sie aus Versehen mit einberechnet.
> [!example]-
> -9 keine Angabe
### Metrisierung
Man kann neue Informationen zu den Daten hinzufügen, um sie zu "metrisieren". 
> [!example]-
> Ich habe die Nominalvariable Beruf
> mithilfe der Berufsprestigeskala wird diese Variable zu einer Ordinalvariable
>

> [!caution]
> Wenn ich eine Variable metrisiere, dann führt das zu einem **Informationsverlust der [[Varianz]], der Streuung der Variablen**

Sitzung 02, F.8 ???
### Dummy-Variable
Eine [[Dummy-Variable]] ist eine Dichotomie, eine [[Variable]], die nur zwei Ausprägungen haben, 0 und 1. 
[[polytom|Polytome]] Variablen (zB eine [[Nominalskala|nominale]] oder [[Ordinalskala|ordinale]] Variable) zerlege ich in dichotome Variablen. 

Das macht man, damit man die in der [[Regression]] als [[unabhängige Variable (UV)]] aufnehmen kann.
> [!example]-
> Abschlussvielfalt wird reduziert auf: Hat Abitur/hat kein Abitur
### Wechsel der Analyseebene
Als [[Wechsel der Analysebene]] bezeichnet man das *Erschließen kollektiver Daten mit Individualdaten.*
Aus [[Individualmerkmal|Individualmerkmalen]] ([[Absolute Individualmerkmale]] & [[Relationale Individualmerkmale]]) kann man [[Kollektivmerkmal]] erstellen, indem man sie aggregiert (zu [[Analytische Kollektivvariable]] und [[Strukturelle Kollektivvariable]]). Denn diese beiden Kollektivvariablen basieren ja auf der Aggregation von Individualmerkmalen.

Dazu kann man auch [[Globale Kollektivvariable]] zuspielen ..??? Um Effekte von Kollektivvariablen zu analysieren verwendet man die [[Mehrebenenanalyse]].

Zeitreihenanalysen ??? gibt es im "wide" und "long" Format (Quer/Längsschnitterhebung)
Darstellungsweise von Längsschnittdaten.
Entweder jede Vraiable educ2002-2005 misst jedesmal Bildungsabschluss in spezifischem Jahr. Also extra Variable in jedem Jahr.


### Gewichtung der Daten
Man kann Daten unterschiedlich [[Gewichtung|gewichten]], um die Realität möglichst genau abzubilden. Dafür eignen sich [[geschichtete Zufallsstichprobe|geschichtete Zufallsstichproben]].
Wenn man also zB disproportional geschichtete Zufallsstichprobe hat, passt man die Verhältnisse an die Grundgesamtheit an.

### Imputation
fehlende Werte werden statistisch geschätzt.
Dafür muss man über die [[Randverteilungen]] bescheid wissen. 