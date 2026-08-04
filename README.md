[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2026.3%2B-41BDF5.svg?style=flat-square&logo=homeassistant)](https://www.home-assistant.io/)
[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=flat-square)](https://hacs.xyz/)
[![Maintainers](https://img.shields.io/badge/maintainers-@AuroreVgn%20-blue.svg?style=flat-square)](https://github.com/AuroreVgn)

# JBL ProScan Lovelace Card

Integration available **[here](https://github.com/AuroreVgn/JBL_ProScan/)**.

## Features
- Responsive
- Visual editor
- Multi-language support : 🇫🇷 🇬🇧 🇩🇪 🇪🇸 🇮🇹 🇳🇱 🇵🇹
- Water quality indicators
- History graph
- Mushroom-inspired design
- Light / Dark theme

## Installation

### HACS (recommended)

#### Add to HACS

- **Automatically**
  [![Open your Home Assistant instance and open this repository in HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=AuroreVgn&repository=JBL_ProScan_Card&category=plugin)

- **Manually**
  ```
  HACS
      ➜ Dashboard
          ➜ Menu "⋮"
              ➜ Custom repositories
  ```
  **Repository**
  ```
  https://github.com/AuroreVgn/JBL_ProScan_Card
  ```
  **Category**
  ```
  Dashboard
  ```

#### Download
```
HACS
    ➜ Dashboard
        ➜ JBL ProScan Card
            ➜ Download
```

Restart Home Assistant if requested.

## Configuration
Add a new Lovelace card:

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

If your history sensor has a different name, replace:

```yaml
sensor.bassin_historique
```

with your own entity.

## Visual Editor

The card supports the Home Assistant visual editor.

Available options include:

- Title
- History length
- Number of displayed measurements
- Compact mode
- CO₂ display
- Water quality thresholds

<img width="333" height="315" alt="image" src="https://github.com/user-attachments/assets/f5c514ca-761b-47e0-b696-06aec20d3ef3" />

## Screenshots
<img width="368" height="863" alt="image" src="https://github.com/user-attachments/assets/a22c70c7-bd5f-44b8-8af3-fa19182adf93" />

<img width="371" height="870" alt="image" src="https://github.com/user-attachments/assets/02aacc23-b05b-46be-91fd-c9a621a89771" />

## License
This project is distributed under the MIT License.
``LICENSE``

[releases-shield]: https://img.shields.io/github/v/release/AuroreVgn/JBL_ProScan?style=flat-square
[releases]: https://github.com/AuroreVgn/JBL_ProScan/releases
[license-shield]: https://img.shields.io/github/license/AuroreVgn/JBL_ProScan?style=flat-square
