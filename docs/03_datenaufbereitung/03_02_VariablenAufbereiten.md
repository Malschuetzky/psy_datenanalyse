---
layout: default
title: Variablenansicht aufbereiten
nav_order: 2
has_children: false
parent: Datenaufbereitung
---

# Variablenansicht aufbereiten
{: .no_toc }

<details open markdown="block">
  <summary>
    Inhalt
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Name, Beschreibung, Skalenniveau und Faktorstufen verändern

{: .info }
>Die folgenden Aktionen können entweder im Tab "Variablen" oder in den Menüpunkten "Daten" oder "Analysen" durchgeführt werden. Die Funktionsweise unterscheidet sich nicht.

Über einen Doppelklick auf den Variablennamen öffnet sich eine Ansicht, in der die Variable bearbeitet werden kann. Hier können Name, Beschreibung, Skalenniveau und Faktorstufen eingestellt und verändert werden.

<a href="./pics/03_02_01.png" target="_blank">
  <img src="./pics/03_02_01.png"/>
</a>

Bei den Skalenniveaus "Nominal" und "Ordinal" werden die in den Daten vorkommenden Faktorstufen automatisch in die Liste der Faktorstufen eingefügt. Weitere Faktorstufen können händisch hinzugefügt werden.
<br>Hierzu muss man das Plus-Icon anklicken, im sich öffnenden Feld den Wert der neuen Faktorstufe eintragen und auf "OK" klicken.

<a href="./pics/03_02_02.png" target="_blank">
  <img src="./pics/03_02_02.png"/>
</a>

Wenn die hinzugefügte Faktorstufe ein Zahlenwert ist, kann man anschließend die Faktorstufe per Doppelklick auf den neuen Eintrag benennen.

{: .info }
>Setzt man den Haken bei "Ungenutzte Faktorstufen in Analyse einschließen", werden in Auswertungen auch Faktorstufen, die nicht im Datensatz vorkommen, mit einbezogen. (Beispielsweise, wenn auf einer Likert-Skala der Wert 3 kein einziges Mal als Antwort ausgewählt wurde.)

## Fehlende Werte identifizieren und ausschließen
<a href="./pics/03_02_03.png" target="_blank">
  <img src="./pics/03_02_03.png"/>
</a>

Fehlende Werte wie "0" oder "99" werden in der Liste der Faktorstufen aufgeführt. Um sie aus Auswertungen auszuschließen, müssen sie als "Fehlende Werte" eingetragen werden.

<a href="./pics/03_02_04.png" target="_blank">
  <img src="./pics/03_02_04.png"/>
</a>

Dies tut man im Feld "Fehlende Werte" über "Fehlenden Wert hinzufügen". Mithilfe von Operatoren können hier entweder einzelne Werte oder Wertebereiche als fehlende Werte definiert werden.

<a href="./pics/03_02_05.png" target="_blank">
  <img src="./pics/03_02_05.png"/>
</a>
<a href="./pics/03_02_06.png" target="_blank">
  <img src="./pics/03_02_06.png"/>
</a>
<a href="./pics/03_02_07.png" target="_blank">
  <img src="./pics/03_02_07.png"/>
</a>

{: .info }
> Die Bedeutung der Operatoren wird im Dropdown erklärt, wenn man mit der Maus darüber fährt. `==` entspricht dem Eintragen der Zahl. <br>Beispiel: `wenn $source == -99` definiert -99 als fehlenden Wert.

Besonders praktisch: Durch Markieren mehrerer Variablen können Fehlende Werte für mehrere Variablen gleichzeitig definiert werden.

<a href="./pics/03_02_08.png" target="_blank">
  <img src="./pics/03_02_08.png"/>
</a>

## Items umpolen/umcodieren
Es gibt zwei Möglichkeiten zum umcodieren von Items: Das Berechnen einer neuen Variable, oder die Nutzung einer Transformation.
### Berechnen neuer Variable
Bei der Berechnung einer neuen Variable wird eine neue Variable erstellt. Hierfür wird der Name der neuen Variable festgelegt, und die Formel zur Berechnung definiert.

<a href="./pics/03_02_09.png" target="_blank">
  <img src="./pics/03_02_09.png"/>
</a>
<a href="./pics/03_02_10.png" target="_blank">
  <img src="./pics/03_02_10.png"/>
</a>

{: .info }
> Um ein negativ gepoltes Item einer 5-stufigen Likert-Skala umzucodieren wird die Formel `6 - "Wert der Ursprungsvariable"` gebraucht. 
> So wird von dem Wert 6 der Wert der Likert-Skala abgezogen, wodurch aus einer 5 eine 1 wird, aus einer 4 eine 2, usw. Es ist also nur eine einzige Aktion notwendig, um alle Werte zu verändern.


### Transformieren
Eine Transformation ist besonders dann hilfreich, wenn eine Umcodierung mehrfach gebraucht wird, da sie immer wieder genutzt werden kann.
Es wird eine neue Transformation erstellt und mit einem Namen, einer Beschreibung, einem Suffix und den Umkodierungsbedingungen befüllt.

<a href="./pics/03_02_11.png" target="_blank">
  <img src="./pics/03_02_11.png"/>
</a>
<a href="./pics/03_02_12.png" target="_blank">
  <img src="./pics/03_02_12.png"/>
</a>
<a href="./pics/03_02_13.png" target="_blank">
  <img src="./pics/03_02_13.png"/>
</a>

Das "Variablensuffix" ist eine Buchstabenkombination (z.B. "\_u"), die bei Ausführung der Transformation an den Variablennamen angehängt wird.
Die Umkodierungsbedingung ist die Formel zur Berechnung der neuen Variablen. Sie folgt dem gleichen Prinzip wie bei der Berechnung neuer Variablen.

{: .info }
> Um ein negativ gepoltes Item einer 5-stufigen Likert-Skala umzucodieren wird die Formel `6 - "Wert der Ursprungsvariable"` gebraucht. 
> So wird von dem Wert 6 der Wert der Likert-Skala abgezogen, wodurch aus einer 5 eine 1 wird, aus einer 4 eine 2, usw. Es ist also nur eine einzige Aktion notwendig, um alle Werte zu verändern.

Um eine Variable umzukodieren wird die neu angelegte Transformation im Dropdown ausgewählt. jamovi legt dann automatisch eine korrekt benannte, umkodierte Variable an.

<a href="./pics/03_02_14.png" target="_blank">
  <img src="./pics/03_02_14.png"/>
</a>

Über die Variablenansicht können auch mehrere Variablen auf einmal umkodiert werden:

<a href="./pics/03_02_15.png" target="_blank">
  <img src="./pics/03_02_15.png"/>
</a>
<a href="./pics/03_02_16.png" target="_blank">
  <img src="./pics/03_02_16.png"/>
</a>

## Skalenaggregation – Berechnung neuer Items

Die Funktion "Berechnen" wird zur Berechnung von neuen Items genutzt. Es können zum Beispiel Mittelwerte (MEAN) oder Summen (SUM) gebildet werden. Über den **f<sub>x</sub>**-Knopf kann eine Liste aller verfügbarer Elemente für die Formel angezeigt werden, aus der durch Doppelklicken Elemente eingefügt werden können. 

<a href="./pics/03_02_17.png" target="_blank">
  <img src="./pics/03_02_17.png"/>
</a>

{: .wichtig } 
> Fehlt in einer der eingerechneten Variablen ein Wert, gibt jamovi in der neu berechneten Variablen keinen Wert aus. Um dieses Problem zu lösen, muss `ignore_missing=1` in die Formel eingefügt werden.

<a href="./pics/03_02_18.png" target="_blank">
  <img src="./pics/03_02_18.png"/>
</a>

## Nutzung von Filtern

Über den Button "Filter" können Filter eingestellt werden. Die Bedingungen, welche Werte gefiltert werden, werden über eine Formel definiert, und ein Filter kann mehrere Bedingungen beinhalten. jamovi zeigt in der/den ersten Spalte an, welche Fälle durch den Filter ausgeschlossen werden.

<a href="./pics/03_02_19.png" target="_blank">
  <img src="./pics/03_02_19.png"/>
</a>