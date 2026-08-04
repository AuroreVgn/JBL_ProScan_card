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

### Dashboard
<img width="368" alt="Dashboard" src="https://github.com/user-attachments/assets/a22c70c7-bd5f-44b8-8af3-fa19182adf93" />

### Dark mode
<img width="371" alt="Dark mode" src="https://github.com/user-attachments/assets/02aacc23-b05b-46be-91fd-c9a621a89771" />

### Visual editor
<img width="333" alt="Visual editor" src="https://github.com/user-attachments/assets/f5c514ca-761b-47e0-b696-06aec20d3ef3" />


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
