# Home Assistant iOS Liquid Glass

Ein iOS-inspiriertes **Liquid Glass** Dark-Mode-Design für Home Assistant: tiefes Schwarz, transluzente Karten, Backdrop-Blur, weiche Glasränder und ein blauer Akzent.

## Voraussetzung

Für den vollständigen Liquid-Glass-Effekt wird **[card-mod](https://github.com/thomasloven/lovelace-card-mod)** benötigt. Installiere es über HACS unter **Frontend**.

Ohne card-mod funktioniert das Theme weiterhin, aber die Karten erhalten keinen Backdrop-Blur bzw. keinen Glass-Reflex.

## Installation

### Variante 1: HACS

1. Öffne **HACS > drei Punkte > Custom repositories**.
2. Füge diese Repository-URL hinzu:

   ```text
   https://github.com/Hoffi96/home-assistant-ios-dark
   ```

3. Wähle als Kategorie **Theme**.
4. Installiere **iOS Dark**.
5. Wähle unter **Benutzerprofil > Theme** das Theme **iOS Dark**.

### Variante 2: Manuell

1. Kopiere `ios_dark.yaml` oder `themes/ios_dark.yaml` nach:

   ```text
   /config/themes/ios_dark.yaml
   ```

2. Ergänze in `configuration.yaml`:

   ```yaml
   frontend:
     themes: !include_dir_named themes
   ```

3. Lade die Frontend-Konfiguration über **Entwicklerwerkzeuge > YAML** neu.
4. Wähle **iOS Dark** unter **Benutzerprofil > Theme**.

## Dashboard

Kopiere den Inhalt aus `lovelace/ios_dark_dashboard.yaml` in den YAML-Editor eines neuen Dashboards.

Passe anschließend die Beispiel-Entitäten an, insbesondere:

- `sensor.temperature_indoor`
- `sensor.humidity_indoor`
- `sensor.outdoor_temperature`
- `light.living_room`
- `light.kitchen`
- `light.bedroom`
- `light.office`
- `scene.good_morning`
- `scene.movie_night`
- `scene.goodnight`
- `scene.leave_home`
- `sensor.home_assistant_cpu`
- `sensor.home_assistant_memory`
- `binary_sensor.home_assistant_connected`

## Liquid-Glass-Stil

- Hintergrund: `#000000`
- Karten: `rgba(255, 255, 255, 0.08)`
- Blur: `blur(24px) saturate(180%)`
- Glasrand: `1px solid rgba(255, 255, 255, 0.14)`
- Radius: `24px`
- Akzent: `#0A84FF`
- Erfolgsgrün: `#30D158`
- Warnorange: `#FF9F0A`
- Fehlerrot: `#FF453A`

Der Glass-Effekt wird über eine zentrale `card-mod-card`-Regel auf alle Standard-`ha-card`-Elemente angewendet.
