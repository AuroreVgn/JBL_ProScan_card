[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2026.3%2B-41BDF5.svg?style=flat-square&logo=homeassistant)](https://www.home-assistant.io/)
[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=flat-square)](https://hacs.xyz/)
[![Maintainer](https://img.shields.io/badge/Maintainer-AuroreVgn-blue.svg?style=flat-square)](https://github.com/AuroreVgn)

# JBL ProScan Lovelace Card
A modern Lovelace card for the **JBL ProScan** Home Assistant integration.

➡️ **Integration available here:** https://github.com/AuroreVgn/JBL_ProScan

## ✨ Features
- 🎨 Mushroom-inspired design
- 📱 Fully responsive
- 🌍 Multi-language support (🇫🇷 🇬🇧 🇩🇪 🇪🇸 🇮🇹 🇳🇱 🇵🇹)
- 🧩 Native Home Assistant visual editor
- 🌞 Light & Dark theme support
- 🔄 Manual refresh button
- 📊 Interactive history graph
- 📈 Home Assistant Long-Term Statistics support
- 📅 History period selector
- 🔍 Interactive tooltips
- 📉 JBL recommended ranges
- 🔄 Previous analysis comparison
- 🎨 Native Home Assistant color picker
- 🎭 Native Home Assistant icon picker
- ⚙️ Highly customizable

## Screenshots

### Light mode
<img width="762" height="1031" alt="image" src="https://github.com/user-attachments/assets/1985667d-bb58-4636-9398-c0945741cf09" />

### Dark mode
<img width="762" height="1031" alt="image" src="https://github.com/user-attachments/assets/c7c45b70-2812-4550-bea3-b244e478ceaa" />

### Visual editor
<img width="513" height="1173" alt="image" src="https://github.com/user-attachments/assets/d64ccabd-641c-4fbe-b437-85c71a8a93e4" />
<img width="513" height="551" alt="image" src="https://github.com/user-attachments/assets/bcd6cd50-0965-4f3e-8444-c42f3b3a81cd" />


## Installation

### HACS (recommended)

#### Add to HACS

##### Automatically
[![Open your Home Assistant instance and open this repository in HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=AuroreVgn&repository=JBL_ProScan_Card&category=plugin)

##### Manually
```
HACS
 └── Dashboards
      └── ⋮
           └── Custom repositories

Repository
https://github.com/AuroreVgn/JBL_ProScan_Card

Category
Dashboard
```

#### Download
```
HACS
 └── JBL ProScan Card
      └── Download
```

Restart Home Assistant if requested.


## Configuration
Minimal configuration:

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

If your history sensor has a different entity ID, simply replace:

```yaml
sensor.bassin_historique
```
with your own sensor.


## Visual Editor
The card fully supports the Home Assistant visual editor.

Available options include:
- Title
- History length
- Number of displayed measurements
- Compact mode
- Show / hide CO₂
- Water quality thresholds
- Manual refresh button
- History period selector
- Custom colors
- Custom icons
- Recommended JBL ranges

No YAML editing required for most users.


## Interactive Dashboard
The card provides:
- 📊 Water quality overview
- 📈 Historical charts
- 📅 Selectable periods
  - 1 month
  - 3 months
  - 1 year
  - All history
- 🔄 Manual refresh
- 📉 Comparison with the previous analysis
- 📍 JBL recommended ranges
- 🖱 Rich interactive tooltips
- 📊 Home Assistant statistics support

## Customization
The appearance can be customized directly from the visual editor.

### Colors
- Accent color
- Good
- Warning
- Critical
(using the native Home Assistant color picker)

| Parameter | Good | Warning | Critical |
|---|---:|---:|---:|
| **pH** | 6.5 ≤ pH ≤ 8.5 | 6.0 ≤ pH < 6.5 ou 8.5 < pH ≤ 9.0 | pH < 6.0 ou pH > 9.0 |
| **KH** | 5 ≤ KH ≤ 15 °dKH | 3 ≤ KH < 5 ou 15 < KH ≤ 20 °dKH | KH < 3 ou KH > 20 °dKH |
| **GH** | 4 ≤ GH ≤ 21 °dGH | 2 ≤ GH < 4 ou 21 < GH ≤ 28 °dGH | GH < 2 ou GH > 28 °dGH |
| **NO₂** | NO₂ = 0 mg/L | 0 < NO₂ ≤ 0.25 mg/L | NO₂ > 0.25 mg/L |
| **NO₃** | NO₃ ≤ 25 mg/L | 25 < NO₃ ≤ 50 mg/L | NO₃ > 50 mg/L |
| **CO₂** | Info | — | — |
| **Chlore** | Chlore = 0 mg/L | 0 < Chlore ≤ 0.8 mg/L | Chlore > 0.8 mg/L |

### Icons
Customize every icon using the native Home Assistant icon picker:
- Header
- Refresh
- pH
- KH
- GH
- NO₂
- NO₃
- CO₂
- Chlorine

## Companion Integration
This card requires the **JBL ProScan** integration.
➡️ https://github.com/AuroreVgn/JBL_ProScan


## License
Distributed under the MIT License.

[releases-shield]: https://img.shields.io/github/v/release/AuroreVgn/JBL_ProScan_Card?style=flat-square
[releases]: https://github.com/AuroreVgn/JBL_ProScan_Card/releases
[license-shield]: https://img.shields.io/github/license/AuroreVgn/JBL_ProScan_Card?style=flat-square
