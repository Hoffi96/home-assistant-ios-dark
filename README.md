# Home Assistant iOS Dark

Ein iOS-inspiriertes Dark-Mode-Design für Home Assistant: dunkles Theme, klare Karten, abgerundete Ecken und ein blauer Akzent.

## Installation

1. Kopiere `themes/ios_dark.yaml` in deinen Home-Assistant-Ordner:

   ```text
   /config/themes/ios_dark.yaml
   ```

2. Aktiviere Themes in der `configuration.yaml`:

   ```yaml
   frontend:
     themes: !include_dir_named themes
   ```

3. Starte Home Assistant neu oder lade die Frontend-Konfiguration über **Entwicklerwerkzeuge > YAML > Frontend-Konfiguration neu laden**.

4. Wähle in Home Assistant unter **Benutzerprofil > Theme** das Theme `iOS Dark`.

## Dashboard importieren

1. Öffne in Home Assistant **Einstellungen > Dashboards**.
2. Erstelle ein neues Dashboard und öffne den YAML-Editor.
3. Kopiere den Inhalt aus `lovelace/ios_dark_dashboard.yaml` hinein.
4. Passe die Entitäts-IDs an deine Installation an, insbesondere Lichter, Sensoren, Szenen und Medienplayer.

## Enthaltene Dateien

- `themes/ios_dark.yaml` — iOS-inspiriertes Dark Theme
- `lovelace/ios_dark_dashboard.yaml` — Beispiel-Dashboard
- `.gitignore` — typische Ausschlüsse für Home-Assistant-Projekte

## Hinweis

Das Dashboard verwendet ausschließlich Standard-Home-Assistant-Karten. Damit funktioniert es ohne zusätzliche HACS-Integrationen.
