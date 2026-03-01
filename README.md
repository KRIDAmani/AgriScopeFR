# AgriScopeFR

**Observatoire interactif de l'agriculture française (1990-2020)**

Visualisation de données interactive explorant l'évolution de l'agriculture en France sur 30 ans.  
Projet MOS 9.1 — Amani KRID & Shreeniketh ARASANIPALAI KRISHNAN

[![Live Demo](https://img.shields.io/badge/demo-live-success)]((https://kridamani.github.io/AgriScopeFR/))

---

## À propos

AgriScopeFR permet d'explorer l'évolution de l'agriculture française à travers :

- La répartition géographique des cultures par région
- L'évolution temporelle sur 30 ans (1990-2020)
- Les impacts environnementaux : eau et émissions de GES
- Les tendances de spécialisation des territoires agricoles

## Fonctionnalités

**Carte interactive**
- Visualisation par région avec zoom
- 3 indicateurs : cultures dominantes, consommation d'eau, émissions de GES
- Slider temporel (1990-2020)
- Animations visuelles sur la carte

**Graphiques analytiques**
- Radar chart : profil agricole comparatif
- Graphique d'évolution temporelle
- Statistiques détaillées par région

**Outils**
- Mode lecture automatique
- Export PNG haute résolution
- Export PDF avec rapport complet

## Technologies

- **React 18** - Interface utilisateur
- **D3.js v7** - Visualisations de données
- **Tailwind CSS** - Styling
- **html2canvas** - Export PNG
- **jsPDF** - Génération PDF
- **GeoJSON** - Données géographiques

## Installation

Le projet fonctionne directement dans le navigateur, aucune installation requise.

```bash
# Option 1 : Télécharger et ouvrir index.html

# Option 2 : Cloner le repository
git clone https://github.com/votre-username/agriscopefr.git
cd agriscopefr
# Ouvrir index.html dans le navigateur
```

## Déploiement sur GitHub Pages

1. Renommer le fichier en `index.html`
2. Créer un repository GitHub
3. Uploader le fichier
4. Activer GitHub Pages : Settings → Pages → Source: `main` branch

Le site sera disponible à : `(https://kridamani.github.io/AgriScopeFR/)`

## Structure des données

**Régions** : 12 régions métropolitaines françaises

**Types de cultures** :
- Grandes cultures (céréales, oléagineux)
- Élevage (bovins)
- Maraîchage & horticulture
- Viticulture
- Cultures fruitières
- Polyculture-polyélevage

**Indicateurs environnementaux** :
- Consommation d'eau (m³/ha)
- Émissions de GES (Mt CO₂eq)

## Sources de données

- **Agreste** - Recensements Agricoles (Ministère de l'Agriculture)
- **Citepa** - Inventaire des émissions de GES
- **SDES** - Données sur l'irrigation
- **INSEE** - Statistiques régionales
- **france-geojson** - Données géographiques


## Contact

- Email : amani.krid@etu.ec-lyon.fr
- GitHub : [@Amani-KRID]((https://github.com/KRIDAmani))

---

Développé dans le cadre du projet MOS 9.1 - Visualisation interactive de données
