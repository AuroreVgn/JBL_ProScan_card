[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2026.3%2B-41BDF5.svg?style=flat-square&logo=homeassistant)](https://www.home-assistant.io/)
[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=flat-square)](https://hacs.xyz/)
[![Maintainer](https://img.shields.io/badge/Maintainer-AuroreVgn-blue.svg?style=flat-square)](https://github.com/AuroreVgn)

**Langue / Language :** [🇫🇷 Français](#-documentation-française) · [🇬🇧 English](#-english-documentation)

---

<a id="-documentation-française"></a>
# 🇫🇷 Documentation française

## 🏠 Mes projets Home Assistant

Retrouvez toutes mes intégrations et mes projets sur ma page dédiée : [**🏠 Découvrir mes projets Home Assistant**](https://gentle-suggestion-7c3.notion.site/Mes-projets-Home-Assistant-3eda02eefa8f81a48621c3caeef7fa8e)

## ☕ Soutenir le projet

Si cette carte vous est utile et que vous souhaitez soutenir son développement et sa maintenance :

<p>
  <a href="https://ko-fi.com/aurorevgn">
    <img src="https://storage.ko-fi.com/cdn/kofi4.png?v=3" alt="Soutenir sur Ko-fi" height="45">
  </a>
</p>

## ⚠️ Important

# Carte Lovelace JBL ProScan

Une carte Lovelace moderne pour l'intégration Home Assistant **JBL ProScan**.

➡️ **Intégration nécessaire :** https://github.com/AuroreVgn/JBL_ProScan

## ✨ Fonctionnalités

- 🎨 Design inspiré de Mushroom
- 📱 Interface responsive
- 🌍 Traductions disponibles (🇫🇷 🇬🇧 🇩🇪 🇪🇸 🇮🇹 🇳🇱 🇵🇹)
- 🧩 Éditeur visuel Home Assistant
- 🌞 Thèmes clair et sombre
- 🔄 Bouton d'actualisation manuelle
- 📊 Graphique historique interactif
- 📈 Statistiques longue durée Home Assistant
- 📅 Sélection de la période historique
- 🔍 Infobulles interactives
- 📉 Plages recommandées JBL
- 🔄 Comparaison avec l'analyse précédente
- 🎨 Sélecteur de couleurs natif Home Assistant
- 🎭 Sélecteur d'icônes natif Home Assistant
- ⚙️ Personnalisation avancée

## 📦 Installation

### HACS (recommandé)

#### Ajouter le dépôt à HACS

##### Automatiquement

[![Ouvrir ce dépôt dans HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=AuroreVgn&repository=JBL_ProScan_card&category=plugin)

##### Manuellement

```text
HACS
 └── Tableaux de bord
      └── ⋮
           └── Dépôts personnalisés

Dépôt
https://github.com/AuroreVgn/JBL_ProScan_card

Catégorie
Dashboard
```

#### Télécharger

```text
HACS
 └── JBL ProScan Card
      └── Télécharger
```

Redémarrez Home Assistant si nécessaire.

## ⚙️ Configuration

Configuration minimale :

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

Remplacez `sensor.bassin_historique` par l'identifiant de votre capteur historique si celui-ci est différent.

## 🎛️ Seuils de qualité de l'eau

Chaque mesure et chaque point du graphique historique reçoivent individuellement une couleur selon les seuils ci-dessous.

> Les valeurs exactement égales aux limites de la plage recommandée sont considérées comme conformes et affichées en 🟢 vert.

| Paramètre | 🟢 Bon | 🟠 À surveiller | 🔴 Mauvais |
|---|---|---|---|
| **pH** | 6,5 ≤ pH ≤ 8,5 | 6,0 ≤ pH < 6,5 ou 8,5 < pH ≤ 9,0 | pH < 6,0 ou pH > 9,0 |
| **KH** | 5 ≤ KH ≤ 15 °dKH | 3 ≤ KH < 5 ou 15 < KH ≤ 20 °dKH | KH < 3 ou KH > 20 °dKH |
| **GH** | 4 ≤ GH ≤ 21 °dGH | 2 ≤ GH < 4 ou 21 < GH ≤ 28 °dGH | GH < 2 ou GH > 28 °dGH |
| **NO₂** | 0 ≤ NO₂ ≤ 0,25 mg/L | — | NO₂ > 0,25 mg/L |
| **NO₃** | NO₃ ≤ 25 mg/L | 25 < NO₃ ≤ 50 mg/L | NO₃ > 50 mg/L |
| **CO₂** | Information uniquement | — | — |
| **Chlore** | 0 ≤ Chlore ≤ 0,8 mg/L | — | Chlore > 0,8 mg/L |

## 📸 Captures d'écran

### Mode clair

<img width="800" alt="JBL ProScan en mode clair" src="https://github.com/user-attachments/assets/d9880589-87c8-4aca-ae74-e8d79fd6799d" />

### Mode sombre

<img width="800" alt="JBL ProScan en mode sombre" src="https://github.com/user-attachments/assets/67da56b6-22fc-4fc3-b386-657fd10cfeaa" />

## 🎨 Éditeur visuel

La carte est compatible avec l'éditeur visuel Home Assistant.

Options disponibles :
- Titre
- Longueur de l'historique
- Nombre de mesures affichées
- Mode compact
- Affichage du CO₂
- Seuils de qualité de l'eau
- Bouton d'actualisation manuelle
- Sélecteur de période historique
- Couleurs personnalisées
- Icônes personnalisées
- Plages recommandées JBL

Pour la plupart des utilisateurs, aucune modification YAML n'est nécessaire.

## 📈 Tableau de bord interactif

La carte propose :
- 📊 Vue d'ensemble de la qualité de l'eau
- 📈 Graphiques historiques
- 📅 Périodes sélectionnables : 1 mois, 3 mois, 1 an ou tout l'historique
- 🔄 Actualisation manuelle
- 📉 Comparaison avec l'analyse précédente
- 📍 Plages recommandées JBL
- 🖱 Infobulles interactives détaillées
- 📊 Prise en charge des statistiques Home Assistant

## ⚙️ Personnalisation

L'apparence se personnalise directement dans l'éditeur visuel.

### Couleurs
- Couleur principale
- Bon
- À surveiller
- Critique

Ces couleurs utilisent le sélecteur natif Home Assistant.

### Icônes

Le sélecteur natif Home Assistant permet de personnaliser les icônes :
- En-tête
- Actualisation
- pH
- KH
- GH
- NO₂
- NO₃
- CO₂
- Chlore

## 🧩 Intégration associée

Cette carte nécessite l'intégration **JBL ProScan**.

➡️ https://github.com/AuroreVgn/JBL_ProScan

## 📄 Licence

Distribué sous licence MIT.

---

<a id="-english-documentation"></a>
# 🇬🇧 English documentation

## 🏠 My Home Assistant Projects

Discover all my Home Assistant integrations and projects on my dedicated page: [**🏠 Discover my Home Assistant Projects**](https://gentle-suggestion-7c3.notion.site/Mes-projets-Home-Assistant-3eda02eefa8f81a48621c3caeef7fa8e)

## ☕ Support the project

If you find this integration useful and would like to support its development and maintenance:

<p>
  <a href="https://ko-fi.com/aurorevgn">
    <img src="https://storage.ko-fi.com/cdn/kofi4.png?v=3"
         alt="Support me on Ko-fi"
         height="45">
  </a>
</p>

## ⚠️ Important

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

## 📦 Installation

### HACS (recommended)

#### Add to HACS

##### Automatically
[![Open your Home Assistant instance and open this repository in HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=AuroreVgn&repository=JBL_ProScan_card&category=plugin)

##### Manually
```
HACS
 └── Dashboards
      └── ⋮
           └── Custom repositories

Repository
https://github.com/AuroreVgn/JBL_ProScan_card

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


## ⚙️ Configuration
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


## 🎛️ Water quality thresholds

Each measurement and each point on the history chart is colored individually
according to the thresholds below.

> Values exactly equal to the lower or upper limit of the recommended range
> are considered within the recommended range and are therefore displayed in 🟢 green.

| Parameter | 🟢 Good | 🟠 Warning | 🔴 Poor |
|---|---|---|---|
| **pH** | 6.5 ≤ pH ≤ 8.5 | 6.0 ≤ pH < 6.5 or 8.5 < pH ≤ 9.0 | pH < 6.0 or pH > 9.0 |
| **KH** | 5 ≤ KH ≤ 15 °dKH | 3 ≤ KH < 5 or 15 < KH ≤ 20 °dKH | KH < 3 or KH > 20 °dKH |
| **GH** | 4 ≤ GH ≤ 21 °dGH | 2 ≤ GH < 4 or 21 < GH ≤ 28 °dGH | GH < 2 or GH > 28 °dGH |
| **NO₂** | 0 ≤ NO₂ ≤ 0.25 mg/L | — | NO₂ > 0.25 mg/L |
| **NO₃** | NO₃ ≤ 25 mg/L | 25 < NO₃ ≤ 50 mg/L | NO₃ > 50 mg/L |
| **CO₂** | Information only | — | — |
| **Chlorine** | 0 ≤ Chlorine ≤ 0.8 mg/L | — | Chlorine > 0.8 mg/L |

## 📸 Screenshots

### Light mode
<img width="800" alt="image" src="https://github.com/user-attachments/assets/d9880589-87c8-4aca-ae74-e8d79fd6799d" />

### Dark mode
<img width="800" alt="image" src="https://github.com/user-attachments/assets/67da56b6-22fc-4fc3-b386-657fd10cfeaa" />

## 🎨 Visual Editor
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


## 📈 Interactive Dashboard
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

## ⚙️ Customization
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

## 🧩 Companion Integration
This card requires the **JBL ProScan** integration.
➡️ https://github.com/AuroreVgn/JBL_ProScan


## 📄 License
Distributed under the MIT License.

[releases-shield]: https://img.shields.io/github/v/release/AuroreVgn/JBL_ProScan_card?style=flat-square
[releases]: https://github.com/AuroreVgn/JBL_ProScan_card/releases
[license-shield]: https://img.shields.io/github/license/AuroreVgn/JBL_ProScan_card?style=flat-square
