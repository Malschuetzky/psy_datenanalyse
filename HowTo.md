# Anleitung zur Pflege der psy_datenanalyse

## Markdown
Die Seite zum Projekt jamovi ist auf Markdown-Dateien aufgebaut. Mehr zu möglichen Formatierungen kann [hier](https://www.markdownguide.org/cheat-sheet/) nachgelesen werden.

## Bilder
Bilder werden nach den entsprechenden Unterseiten, auf denen sie eingebunden werden, benannt. <br> Bsp. Bilder auf der Unterseite "03_01_DatenEinlesen" werden als "03_01_01.png", "03_01_02.png", etc. gespeichert.

Bilder werden per HTML-Code eingebunden, damit sie durch Klick in einem neuen Tab in Originalgröße geöffnet werden können.
```
<a href="./pics/NAMEDESBILDES.png" target="_blank">
  <img src="./pics/NAMEDESBILDES.png"/>
</a>
```

## Callouts
Zur farbigen Hervorhebung von wichtigen Informationen können sogenannte Callouts genutzt werden.
Es sind folgende Callouts definiert:

```
{: .info }
> Info: Blaues Callout – Wird genutzt um weitergehende Infos darzustellen.

{: .wichtig } 
> Wichtig: Rotes Callout – Wird genutzt für kritische Informationen, wie Warnungen vor potentiellen Fehlern.

{: .hinweis }
> Hinweis: Grünes Callout – Wird genutzt für Hinweise, wie z.B. welcher Übungsdatensatz für die jeweilige Anleitung genutzt wurde.
```

Mehr zu Callouts findet man in der [Dokumentation von JustTheDocs](https://just-the-docs.com/docs/configuration/#callouts).

## Inhaltsverzeichnis auf einer Unterseite
Bei Seiten mit besonders vielen Unterpunkten kann ein Inhaltsverzeichnis eingefügt werden, das am Seitenanfang steht und einklappbar ist.

```
{: .no_toc }

<details open markdown="block">
  <summary>
    Inhalt
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
```

## Zeilenumbrüche forcieren
Zeilenumbrüche können mit `<br>` erzwungen werden.