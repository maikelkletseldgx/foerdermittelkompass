# Fördermittelkompass — Online-Setup

Zwei Dateien, eine feste Adresse, kein Dateiversand mehr.

## Was ist was

| Datei | Zweck | Adresse nach dem Einrichten |
|---|---|---|
| `index.html` | **Live** — der stabile Stand fürs Tagesgeschäft | `https://<name>.github.io/<repo>/` |
| `test.html` | **Test** — neue Änderungen zum Ausprobieren | `https://<name>.github.io/<repo>/test.html` |

Beide Dateien sind identisch aufgebaut. Der Generator erkennt selbst, welcher Stand geöffnet ist, und zeigt oben links im Panel „Live" oder „TEST" mit Datum an — so weiß jeder sofort, womit er arbeitet.

## Einmalig einrichten (ca. 5 Minuten)

1. Auf github.com ein neues Repository anlegen, z. B. `foerdermittelkompass`. **Public** wählen — für GitHub Pages nötig.
2. Beide Dateien per Drag-and-drop ins Repository ziehen, „Commit changes".
3. Im Repository auf **Settings → Pages** gehen.
4. Unter „Source" **Deploy from a branch** wählen, Branch `main`, Ordner `/ (root)`, speichern.
5. Nach ein bis zwei Minuten ist die Adresse erreichbar. GitHub zeigt sie oben auf derselben Seite an.

## Änderungen einspielen

1. Neue Datei aus dem Chat herunterladen.
2. Im Repository die Datei anklicken → Stift-Symbol → alten Inhalt ersetzen. Oder einfacher: die neue Datei per Drag-and-drop hochladen, GitHub überschreibt sie bei gleichem Namen.
3. „Commit changes" — nach etwa einer Minute ist die Seite aktuell.

Erst `test.html` aktualisieren, ausprobieren, und wenn alles passt, denselben Stand als `index.html` hochladen.

## Wichtig für den Umstieg

**Bestehende Projekte vorher sichern.** Der Generator speichert Projekte im Browser, gebunden an den Ort, von dem er geöffnet wurde. Beim Wechsel von der lokalen Datei auf die Web-Adresse sind die alten Projekte nicht automatisch da.

Vorgehen: In der alten Datei jedes Projekt über **Export (Datei)** sichern, danach in der Online-Version über **Import (Datei)** wieder einlesen. Das ist einmalig nötig.

Ab dann bleiben Projekte stabil erhalten — auch wenn die Datei online aktualisiert wird. Das ist der eigentliche Gewinn gegenüber heruntergeladenen Dateien.

## Zum Zugriff

Die Seite ist über die Adresse öffentlich erreichbar, aber nicht auffindbar: Beide Dateien enthalten eine `noindex`-Anweisung, Suchmaschinen nehmen sie nicht auf. Wer die Adresse nicht kennt, findet sie im Normalfall nicht.

Zu bedenken: Das Repository ist öffentlich, der Quelltext also einsehbar — darin stecken eure Förderlogik und Fördersätze. **Kundendaten sind nicht betroffen**, die liegen ausschließlich im Browser des jeweiligen Rechners und werden nie hochgeladen.

Wenn ihr später echten Zugriffsschutz wollt, ist der günstigste Weg Cloudflare Pages mit Cloudflare Access: kostenlos bis 50 Nutzer, Login per E-Mail-Code, verbindet sich mit demselben Repository. Sag Bescheid, dann beschreibe ich das Setup.
