# Schriften für die Website

Hier hinein gehören vier Dateien. Solange sie fehlen, funktioniert die Seite,
sie greift dann nur auf Systemschriften zurück und sieht etwas gewöhnlicher aus.

## Was gebraucht wird

| Datei (genau so benennen)        | Schrift          | Schnitt   |
|----------------------------------|------------------|-----------|
| `playfair-display-400.woff2`     | Playfair Display | Regular   |
| `playfair-display-500.woff2`     | Playfair Display | Medium    |
| `montserrat-400.woff2`           | Montserrat       | Regular   |
| `montserrat-600.woff2`           | Montserrat       | SemiBold  |

## Warum diese beiden

- **Playfair Display** für die großen Überschriften. Hoher Strichkontrast,
  derselbe Duktus wie der Titel auf dem Buchcover.
- **Montserrat** für Fließtext, Navigation und Buttons. Das ist bereits die
  Schrift im Buchsatz, damit sehen Print und Web endlich gleich aus.

Beide stehen unter der SIL Open Font License, kommerzielle Nutzung ausdrücklich
erlaubt, auch das Mitliefern im eigenen Repository.

## Woher

1. Auf **https://gwfh.mranftl.com** gehen.
2. Schrift suchen (erst „Playfair Display", dann „Montserrat").
3. Bei *Select charsets* **latin** und **latin-ext** anhaken.
   (latin-ext bringt osteuropäische Zeichen mit. Kostet ein paar Kilobyte,
   erspart aber Kästchen statt Buchstaben in Namen wie „Łukasz".)
4. Bei *Select styles* nur die oben genannten Schnitte anhaken.
5. Unten das ZIP herunterladen, entpacken, **nur die `.woff2`-Dateien** hierher
   kopieren und exakt so umbenennen wie in der Tabelle.

Die anderen Formate aus dem ZIP (ttf, woff, eot, svg) werden nicht gebraucht.
Kein moderner Browser braucht sie noch, und sie sind zwei- bis dreimal so groß.

## Warum nicht einfach Google Fonts einbinden

Weil dabei bei jedem Seitenaufruf die IP-Adresse der Besucherin an einen
Google-Server in den USA geht. Genau dafür sind in Deutschland Abmahnungen
verschickt worden (Landgericht München I, Urteil vom 20.01.2022, Az. 3 O 17493/20).
Selbst gehostet stellt sich die Frage gar nicht erst: die Schrift kommt vom
eigenen Server, es fließen keine Daten irgendwohin.

Dieselbe Regel gilt für alles andere auf der Seite. Keine Icon-Dienste, keine
Analyse-Skripte, keine eingebetteten Karten, nichts von fremden Servern.

## Danach

Nichts weiter zu tun. Die `@font-face`-Regeln stehen bereits oben in
`index.html` und `404.html` und zeigen genau auf diese Dateinamen.
Einmal die Seite im Browser neu laden, die Überschriften sollten sofort anders
aussehen.
