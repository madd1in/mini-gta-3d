# MINI GTA 3D

Browser-basiertes 3D-Open-World-Spiel mit Three.js — klau Autos, erledige Aufträge, entkomme der Polizei, fahr Rennen. Läuft komplett client-seitig, kein Build-Schritt nötig.

## Spielen

Einfach `index.html` öffnen, oder über GitHub Pages: siehe Link oben im Repo.

## Steuerung

**Desktop:** W/S Gas · A/D Lenken · Space Drift · Shift Nitro · R Rennen · Y Handy · X Bestechen · L Licht · B Bullet Time · E/G Tanken · F Kino-Modus · P Wetter · Tab Radio · J Ein-/Aussteigen/Klauen

**Mobile:** Touch-Buttons erscheinen automatisch (Gas/Bremse/Lenken/Handbremse/Nitro), Performance-Stufe wird automatisch anhand des Geräts reduziert. Ein Menü-Button (⋮) oben rechts öffnet Hupe, Radio, Karte, Rennen, Bullet Time, Licht, Bestechen, Lackierung, Glow, Wetter, Stumm und Tanken.

## Mobile-Optimierungen

- Automatische Touch-Erkennung schaltet Touch-Controls und eine leichtere Grafikqualität frei (weniger Verkehr/NPCs, kein Schatten, kleinere Bloom-Auflösung, niedrigere Pixel-Ratio)
- Sichere Bereiche (Notch/Home-Indicator) über `env(safe-area-inset-*)` für HUD, Minimap, Tacho und alle Touch-Buttons
- `viewport-fit=cover` sowie `theme-color`/Apple-Web-App-Meta-Tags fürs Vollbild-Erlebnis beim Hinzufügen zum Homescreen
- Skalierte HUD-Elemente (Minimap, Tacho) auf kleinen Bildschirmen
- Resize-Handling für Kamera/Renderer bei Drehung oder Browser-UI-Änderungen

## Tech

- [Three.js](https://threejs.org/) r128 (CDN, kein Bundler) mit Postprocessing (Bloom)
- Web Audio API für prozedural generierten Soundtrack, Motorensound und SFX
- `localStorage` für Speicherstand (Geld, Autos, Upgrades, Erfolge, Bestzeiten)
