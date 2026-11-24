# Essen fassen

WebApp, die vorschlägt, was es zu essen geben kann. Läuft komplett im Browser, keine Abhängigkeiten, kein Build-Schritt.

## Funktionen

- Zufallsvorschlag aus 78 Gerichten mit Würfel-Animation
- Filter: vegetarisch, vegan, Fleisch, Fisch, Küche, Schnell (unter 30 Min), nur ohne Ofen
- Gerichte merken oder dauerhaft ausschließen (wird pro Browser über localStorage gespeichert)

## GitHub Pages aktivieren (einmalig)

1. Repo öffnen, dann Settings -> Pages
2. Unter "Build and deployment" als Source "GitHub Actions" auswählen
3. Danach läuft der Workflow "Deploy to GitHub Pages" bei jedem Push auf main

Die App ist anschließend unter `https://frank-a-i.github.io/essen-fassen/` erreichbar.

## Lokal testen

`index.html` einfach im Browser öffnen.

## Gericht hinzufügen

In `index.html` im Array `MEALS` eine Zeile ergänzen:

```js
{n:"Name", e:"Emoji", d:"Kurze Zutatenbeschreibung", f:"vegi", c:"deutsch", t:25, oven:false}
```

Felder: `f` = vegi/vegan/meat/fish, `c` = deutsch/italienisch/asiatisch/orientalisch/mexikanisch/amerikanisch/sonstige, `t` = Dauer in Minuten, `oven` = true, wenn der Ofen nötig ist.
