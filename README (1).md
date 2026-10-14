# colinse21

Meine Bio-Seite: **[corleonecity.github.io/colinse21](https://corleonecity.github.io/colinse21/)**

Alle Dateien liegen im selben Ordner wie `index.html`. Der Name muss genau so heißen, sonst findet die Seite die Datei nicht. Klick auf einen Dateinamen, um ihn direkt zu öffnen.

## Dateien zum Bearbeiten

| Datei | Was sie macht |
| --- | --- |
| [`profile.json`](profile.json) | Name, Ort und die getippten Bio-Zeilen. |
| [`buttons.json`](buttons.json) | Die Buttons links. Hier fügst du neue Buttons ein. |
| [`songs.json`](songs.json) | Die Musik. Hier fügst du neue Songs ein. |
| [`commands.json`](commands.json) | Die eigenen Befehle im Terminal unten rechts. |
| [`quotes.json`](quotes.json) | Die Zitate auf dem Startbildschirm. Jeder Besucher bekommt jeden Tag sein eigenes „Zitat des Tages“. |

## Alle anderen Dateien

| Datei | Was sie macht |
| --- | --- |
| [`index.html`](index.html) | Die ganze Seite. Normalerweise musst du die nicht anfassen. |
| `buttom1.jpeg` bis `buttom6.jpeg` | Die Bilder in den Buttons. Neue Bilder genauso benennen, zum Beispiel `buttom7.jpeg`. |
| `song-1.mp3`, `song-2.mp3` | Die Musikdateien. Neue Songs zum Beispiel `song-3.mp3`. |
| `cover-1.jpeg`, `cover-2.jpeg` | Das Bild neben dem Song. Neue Cover zum Beispiel `cover-3.jpeg`. |
| `avatar.webp` | Dein Bild oben links auf der Karte. |
| `sparkle.gif` | Das Glitzern über dem Namen. |
| `cursor.png` | Die Maus. |
| `bg.mp4` | Das Hintergrundvideo auf dem Handy. |
| [`preview.png`](preview.png) | Das Vorschaubild, wenn man den Link auf Discord, WhatsApp und Co. teilt (1200×630). |
| [`icon.png`](icon.png) | Das kleine Bild oben links im Browser-Tab und auf dem Handy-Homescreen. |
| [`README.md`](README.md) | Diese Erklärung. |

## Was live von außen kommt

Diese Sachen kommen nicht aus einer Datei, sondern werden live geladen:

| Funktion | Woher |
| --- | --- |
| Discord-Status, Spiel, Spielzeit, Spotify | [Lanyard](https://github.com/Phineas/lanyard) (live, ohne Neuladen) |
| Aufrufe (1 pro IP alle 12 Std.) | Cloudflare Worker |
| Likes (1 pro IP) | Cloudflare Worker |
| Feedback im Terminal (1x pro Tag an Discord) | Cloudflare Worker |
| „Last played“ | Cloudflare Worker |
| Spielzeit (Controller-Button unten rechts) | Cloudflare Worker |
| Zitat des Tages (welches Zitat du heute bekommst) | Cloudflare Worker |
| Wetter-Effekt im Hintergrund | Cloudflare Worker |
| LIVE-Buttons (Twitch/TikTok) | Cloudflare Worker + altes Backend |

Der Worker läuft unter `https://page.keulecolin2005.workers.dev`. Den Code bearbeitest du im Cloudflare-Dashboard unter **Edit code**. Der Discord-Webhook und `IP_SALT` sind dort als **Secrets** gespeichert. **Niemals** in eine Datei hier auf GitHub schreiben!

## Profil

In [`profile.json`](profile.json):

```json
{
  "name": "colinse21",
  "location": ["Deutschland", "Thüringen"],
  "bio": [
    "Carry Freedom in Your Heart",
    "Thüringen, Deutschland",
    "Komm auf meinen Discord"
  ]
}
```

- `name` ist der große Name auf der Karte.
- `location` ist der Ort oben rechts. Mehrere Einträge werden mit Komma verbunden.
- `bio` sind die Zeilen, die nacheinander getippt werden. So viele, wie du willst.

## Buttons

In [`buttons.json`](buttons.json) ist jeder Button ein Block. Es sind immer 5 auf einmal zu sehen. Ab dem sechsten kannst du in der Liste hoch und runter scrollen.

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

## Songs

In [`songs.json`](songs.json) ist jeder Song ein Block. Beim Öffnen startet ein zufälliger Song. Vor, Zurück und das Ende vom Lied wählen wieder zufällig einen anderen.

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

## Terminal-Befehle

In [`commands.json`](commands.json) ist jeder Befehl ein Block:

```json
{
  "name": "setup",
  "description": "mein PC",
  "output": ["RTX 4070", "Ryzen 7"]
}
```

- `name` ist das, was man eintippt.
- `description` steht neben dem Befehl, wenn man `help` eingibt.
- `output` sind die Zeilen, die erscheinen. Für einen Link schreibst du `{ "text": "YouTube", "url": "https://..." }`.
- Diese Platzhalter werden automatisch ausgefüllt: `{status}`, `{activity}`, `{song}`, `{time}`.

`help`, `feedback`, `playtime`, `clear` und `exit` sind fest eingebaut und müssen nicht in die Datei.

- `feedback deine Nachricht` schickt eine Nachricht in Colins Discord (1x pro Tag pro IP).

## Zitate

In [`quotes.json`](quotes.json) steht jedes Zitat in einer eigenen Zeile:

```json
[
  "Respawn ist kein Rückschritt, sondern ein neuer Versuch.",
  "Heute grinden, morgen glänzen.",
  "Dein neues Zitat hier"
]
```

Neues Zitat: einfach eine neue Zeile in `"Anführungszeichen"` dazuschreiben, mit Komma dahinter (außer beim letzten). Löschen geht genauso. Die Seite merkt automatisch, wie viele Zitate es gibt.

## Kleine Geheimnisse

Auf der Seite sind ein paar versteckte Sachen eingebaut. Manche hängen vom Wetter ab, manche von dir, und manche muss man einfach finden. Mehr wird hier nicht verraten. 👀

## Wichtig bei allen .json-Dateien

- Hinter jedem Block oder jeder Zeile außer der letzten muss ein **Komma** stehen.
- Text immer in **"Anführungszeichen"**.
- Listen fangen mit `[` an und hören mit `]` auf.
- Wenn die Seite danach etwas nicht mehr anzeigt, fehlt meistens ein Komma oder Anführungszeichen.

## Link-Vorschau und Icon

Das Vorschaubild ist `preview.png`, das Tab-Icon ist `icon.png`. Zum Ändern lädst du einfach ein neues Bild mit genau demselben Namen hoch. Für die Vorschau am besten im Format 1200×630, für das Icon ein quadratisches Bild.

Discord merkt sich alte Vorschauen eine Weile. Zum Testen hängst du `?1`, `?2` usw. an den Link.

## Hochladen

Neue Bild- oder Musikdatei und die geänderte `.json`-Datei auf GitHub in denselben Ordner laden. Danach die Seite hart neu laden: am PC `Strg + F5`, am Handy den Tab schließen und neu öffnen.
