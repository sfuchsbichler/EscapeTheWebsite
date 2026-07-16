# Escape the Website

Ein browserbasiertes Escape-Room-Rätselspiel (HTML, CSS, JavaScript). Die Besucher lösen nacheinander mehrere Rätsel-Runden mit je vier Fragen, um "aus der Website zu entkommen".

## Funktionen

- **Namensabfrage zu Beginn** mit Wiederholungsaufforderung, falls kein Name eingegeben wird
- **Mehrere Rätsel-Runden** mit je vier Fragen, die dynamisch nachgeladen werden
- **Automatische Auswertung** der Antworten (Groß-/Kleinschreibung wird ignoriert), inklusive visueller Rückmeldung (grün/rot) direkt im Eingabefeld
- **Wiederholungsmöglichkeit** bei falschen Antworten, ohne das Spiel neu starten zu müssen
- **Abschluss-Screen** mit Weiterleitung nach erfolgreichem Lösen aller Rätsel

## Technologien

- HTML5
- CSS3
- Vanilla JavaScript (ohne Frameworks/Bibliotheken)

## Architektur

Das gesamte Spiel läuft in einer einzigen HTML-Datei mit eingebettetem JavaScript. Der Ablauf ist funktional aufgeteilt:

- **`Fortfahren()`** – baut die Ansicht für die aktuelle Rätsel-Runde auf (Fragen, Eingabefelder, Button)
- **`Pruefen()`** – wertet die eingegebenen Antworten aus, markiert sie farblich und schaltet bei vollständig richtiger Antwort zur nächsten Runde
- **`RichtigeAntworten()`** – zentrale Stelle, die für jede Runde/Frage die korrekte Lösung liefert

## Ausführen

`EscapeTheWebsite.html` direkt im Browser öffnen (keine weiteren Abhängigkeiten oder Installation nötig).

## Was ich dabei gelernt habe

- Dynamisches Erzeugen und Austauschen von Seiteninhalten per JavaScript
- Validierung von Nutzereingaben und visuelles Feedback direkt im UI
- Vermeidung von `eval()` zugunsten sauberer Array-Zugriffe und direkter Funktionsaufrufe
- Strukturierung eines mehrstufigen, zustandsbasierten Ablaufs (Rätsel-Runden) in reinem JavaScript

## Mögliche Weiterentwicklung

Aktuell wird der Seiteninhalt zwischen den Rätsel-Runden über `document.write()` und `innerHTML`-Resets ausgetauscht. Eine modernere Umsetzung würde stattdessen den Inhalt direkt über Template-Strings und `innerHTML` setzen sowie Event-Listener statt inline `onclick`-Attribute verwenden.
