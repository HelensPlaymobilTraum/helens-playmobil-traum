# Homepage-Pruefung

Datum: 2026-03-30

## Feststellungen

1. Hoch: Die Seite ist noch nicht veroeffentlichungsreif, weil Kontakt und Social-Media-Aktionen Platzhalter sind. Der CTA fuehrt zum Kontaktbereich, aber dort steht nur `deine-email@beispiel.de`, und beide Social-Links zeigen auf `#`. Nutzer landen also bei Sackgassen statt bei echten Kontaktmoeglichkeiten. Siehe `index.html:106`, `index.html:147`, `index.html:148`, `index.html:158`.

2. Hoch: Fuer eine Vereinswebseite muessen die rechtlichen Pflichtangaben vor einer Veroeffentlichung fuer die Schweiz geprueft werden. Das ist kein Rechtsrat, aber vor einem Livegang sollte das verbindlich nach Schweizer Vorgaben geklaert sein.

3. ~~Mittel: Die Galerie hat zuvor Bilder ueber GitHub-Raw-URLs geladen statt ueber lokale relative Pfade. Das erzeugt eine unnoetige externe Abhaengigkeit fuer eigene Dateien, macht lokale und Offline-Vorschauen unzuverlaessiger und ist fehleranfaellig, wenn sich Branch oder Repo-Pfad aendern. Diese Dateien sollten lokal eingebunden sein. Siehe `index.html:138`, `index.html:139`, `index.html:140`.~~

4. Mittel: Die Seite wirkt derzeit eher wie eine allgemeine Vorlage als wie eine echte Vereinswebseite. Die Texte sind noch weitgehend Platzhalter, es fehlen konkrete Angaben zu Ort, Termin, Kontakt oder verantwortlichen Personen, und die vorhandene visuelle Identitaet aus Sticker oder Logo wird noch nicht sichtbar eingesetzt. Dadurch entsteht noch nicht genug Vertrauen oder Wiedererkennung.

5. Niedrig: Die konvertierten PNGs sehen visuell in Ordnung aus und behalten die Transparenz, sind aber deutlich groesser als das originale WebP-Stickerbild, ohne erkennbaren Mehrwert: etwa `74 KB` fuer das WebP gegen etwa `407 KB` pro PNG. Falls das spaeter als Logo verwendet wird, sind die PNGs in dieser Form unnoetig schwer, sofern PNG nicht ausdruecklich benoetigt wird.

6. Niedrig: Im Repo gibt es etwas Dateichaos und Duplikate. `IMG-20260330-WA0000(1).jpg` und `WhatsApp Image 2026-03-30 at 15.29.57.jpeg` wirken wie dieselbe Bildquelle, und der Ordner `temp` enthaelt Zwischenstaende aus der Konvertierung statt produktiver Dateien. Das wird schnell unuebersichtlich, sobald weitere Entwuerfe dazukommen.

## Offene Fragen und Annahmen

- Diese Pruefung geht davon aus, dass der Entwurf spaeter eine echte oeffentliche Vereinswebseite werden soll und nicht nur ein visuelles Mockup ist.
- Diese Pruefung geht ausserdem davon aus, dass der WhatsApp-Sticker spaeter als Logo oder als Grundlage dafuer gedacht ist.

## Zusammenfassung

Die PNG-Konvertierung selbst wirkt brauchbar. Die Ausgaben von Windows und Linux sehen in sichtbarer Qualitaet und beim Transparenzverhalten praktisch gleich aus.

Die groesseren Probleme liegen auf Seiten der Homepage: Sie ist noch ein Vorlagenentwurf, es fehlen zentrale Informationen fuer einen echten Start, und das vorhandene Branding wird noch nicht stimmig eingesetzt.

## Gepruefte Dateien

- `index.html`
- `bilder/galerie/vereinsfoto.jpg`
- `bilder/galerie/gartenszene.jpg`
- `bilder/galerie/marktszene.jpg`
- `bilder/logo/logo-vorschau.jpg`
- `WhatsApp Image 2026-03-30 at 15.29.57.jpeg`
- `temp/WhatsApp Sticker 2026-03-30 at 15.16.49.webp`
- `temp/output.png`
- `temp/output.linux.png`
