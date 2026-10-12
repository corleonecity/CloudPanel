# colinse21

Alle Dateien liegen im selben Ordner wie `index.html`. Der Name muss genau so heißen, sonst findet die Seite die Datei nicht.

## Dateien

| Datei | Was sie macht |
| --- | --- |
| `index.html` | Die ganze Seite. Normalerweise musst du die nicht anfassen. |
| `buttons.json` | Die Buttons links. Hier fügst du neue Buttons ein. |
| `songs.json` | Die Musik. Hier fügst du neue Songs ein. |
| `buttom1.jpeg` bis `buttom6.jpeg` | Die Bilder in den Buttons. Neue Bilder genauso benennen, zum Beispiel `buttom7.jpeg`. |
| `song-1.mp3`, `song-2.mp3` | Die Musikdateien. Neue Songs zum Beispiel `song-3.mp3`. |
| `cover-1.jpeg`, `cover-2.jpeg` | Das Bild neben dem Song. Neue Cover zum Beispiel `cover-3.jpeg`. |
| `avatar.webp` | Dein Bild oben links auf der Karte. |
| `sparkle.gif` | Das Glitzern über dem Namen. |
| `cursor.png` | Die Maus. |
| `bg.mp4` | Das Hintergrundvideo auf dem Handy. |
| `README.md` | Diese Erklärung. |

Discord, Aufrufe und die LIVE-Buttons kommen nicht aus einer Datei. Die holt die Seite von der veröffentlichten Adresse.

## Buttons

In `buttons.json` ist jeder Button ein Block. Es sind immer 5 auf einmal zu sehen. Ab dem sechsten kannst du in der Liste hoch und runter scrollen.

```json
{
  "bild": "buttom7.jpeg",
  "titel": "Mein Link",
  "link": "https://example.com",
  "text": "example.com"
}
```

- `bild` ist das runde Bild. Die Datei muss im gleichen Ordner liegen.
- `titel` ist die dicke Zeile. Leer lassen, wenn der Button nur ein Bild sein soll.
- `link` ist die Adresse. Leer lassen, wenn man nicht klicken soll.
- `text` ist die kleine Zeile unter dem Titel.

Hinter jedem Block außer dem letzten muss ein Komma stehen. Die Datei fängt mit `[` an und hört mit `]` auf.

## Songs

In `songs.json` ist jeder Song ein Block. Beim Öffnen startet ein zufälliger Song. Vor, Zurück und das Ende vom Lied wählen wieder zufällig einen anderen.

```json
{
  "titel": "Mein Song",
  "datei": "song-3.mp3",
  "cover": "cover-3.jpeg"
}
```

- `titel` ist der Name, der im Player steht.
- `datei` ist die mp3-Datei.
- `cover` ist das Bild links neben dem Titel.

Auch hier: Komma hinter jedem Block außer dem letzten. `[` am Anfang, `]` am Ende.

## Hochladen

Neue Bild- oder Musikdatei und die geänderte `buttons.json` oder `songs.json` auf GitHub in denselben Ordner laden. Danach die Seite hart neu laden: am PC `Strg + F5`, am Handy den Tab schließen und neu öffnen.
