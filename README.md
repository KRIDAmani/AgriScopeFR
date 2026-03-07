# AgriScopeFR 🌾

**Observatoire interactif de l'agriculture française (1990-2020)**

Visualisation de données interactive explorant l'évolution de l'agriculture en France sur 30 ans à travers une carte choroplèthe, des graphiques analytiques et des bulletins d'analyse automatisés.

**Projet MOS 9.1 — Visualisation de données**  
Amani KRID & Shreeniketh ARASANIPALAI KRISHNAN

[![Live Demo](https://img.shields.io/badge/🌐_Démo-Accéder_au_site-success?style=for-the-badge)](https://kridamani.github.io/AgriScopeFR/)

> 👆 **Cliquez sur "Démo" ci-dessus pour accéder directement à l'application**

---

##  À propos

AgriScopeFR est une application web interactive qui permet d'explorer l'évolution de l'agriculture française à travers :

-  **Répartition géographique** des cultures par région (12 régions métropolitaines)
-  **Évolution temporelle** sur 30 ans (recensements 1990, 2000, 2010, 2020)
-  **Impact environnemental** : consommation d'eau et émissions de GES
-  **Tendances de spécialisation** des territoires agricoles

### Résultats principaux

- **Spécialisation territoriale** : Les grandes cultures progressent de +9 points en Île-de-France entre 1990 et 2020
- **Impact eau** : Augmentation moyenne de +300 m³/ha sur 30 ans, avec des pics dans le sud (PACA : +500 m³/ha)
- **Réduction GES** : Baisse globale de -2,7 Mt CO₂eq malgré des disparités régionales
- **Diversité régionale** : Chaque région développe son identité (viticulture en Grand Est/Nouvelle-Aquitaine, maraîchage en PACA)

---

## Fonctionnalités

### Carte interactive
- Visualisation choroplèthe par région avec zoom
- **3 modes d'affichage** :
  - Cultures dominantes (avec emojis animés)
  - Consommation d'eau (gradient bleu)
  - Émissions de GES (gradient rouge)
- Slider temporel décennal (1990-2020)
- **Tooltips contextuels** au survol des régions
- Bouton "France entière" pour revenir à la vue globale

###  Graphiques analytiques
- **Radar chart** : Profil agricole comparatif des 12 régions (ou région sélectionnée)
- **Graphique d'évolution** : Tendances 1990-2020 pour 4 cultures principales
- **Barres statistiques** : Répartition détaillée par type de culture

### Analyse automatisée
- **Bulletin d'analyse** généré automatiquement à chaque changement d'année
- Identification des évolutions majeures (cultures, eau, GES)
- Comparaison inter-décennale avec contexte

### Outils
- **Mode lecture automatique** : Parcours animé des décennies
- **Export PNG** : Carte haute résolution (2x)
- **Export PDF** : Rapport complet avec graphiques et statistiques
- **Sidebar redimensionnable** : Ajustez la largeur du panneau de droite

### UX améliorée
- **Modal d'introduction** : Présentation des résultats principaux au lancement
- **Page "Sources & Méthodologie"** : Documentation complète des données et limites
- **Légendes visibles** : Design amélioré avec contraste renforcé
- **Design responsive** : Optimisé pour desktop (min. 1024px)

---

## Technologies

| Technologie | Usage |
|------------|-------|
| **React 18** | Interface utilisateur réactive |
| **D3.js v7** | Visualisations cartographiques et graphiques |
| **GeoJSON** | Données géographiques (france-geojson) |
| **html2canvas** | Export PNG haute résolution |
| **jsPDF** | Génération de rapports PDF |
| **Google Fonts** | Source Serif 4, IBM Plex Sans/Mono |

---

## Installation & Déploiement

### Option 1 : Utilisation directe
Le projet fonctionne directement dans le navigateur, **aucune installation requise**.

```bash
# Télécharger le fichier HTML
# Ouvrir dans votre navigateur préféré (Chrome/Edge recommandés)
```

### Option 2 : Cloner le repository

```bash
git clone https://github.com/KRIDAmani/AgriScopeFR.git
cd AgriScopeFR
# Ouvrir index.html dans le navigateur
```

### Déploiement sur GitHub Pages

1. Renommer le fichier en `index.html`
2. Créer un repository GitHub
3. Uploader le fichier dans la branche `main`
4. Activer GitHub Pages : **Settings → Pages → Source: `main` branch**
5. Le site sera disponible à : `https://[username].github.io/AgriScopeFR/`

---

## Structure des données

### Régions
12 régions métropolitaines françaises (découpage 2016)

### Types de cultures (6 catégories)
- **Grandes cultures** : Céréales, oléagineux, protéagineux
- **Élevage** : Prairies permanentes et temporaires
- **Maraîchage** : Légumes frais, horticulture
- **Viticulture** : Vignes pour vin et raisin de table
- **Fruits** : Vergers, cultures fruitières
- **Autres** : Jachères, surfaces non agricoles

### Indicateurs environnementaux
- **Consommation d'eau** : Volume total prélevé / SAU irriguée (m³/ha)
- **Émissions de GES** : Fermentation entérique + fertilisation azotée + effluents (Mt CO₂eq)

---

## Sources de données

| Source | Description | Données |
|--------|-------------|---------|
| **[Agreste](https://agreste.agriculture.gouv.fr/)** | Service de la statistique agricole (Ministère de l'Agriculture) | Recensements agricoles 1990, 2000, 2010, 2020 — Surfaces agricoles par type de culture |
| **[Citepa](https://www.citepa.org/)** | Centre Interprofessionnel Technique d'Études de la Pollution Atmosphérique | Inventaire SECTEN — Émissions de GES par secteur et région |
| **[SDES](https://www.statistiques.developpement-durable.gouv.fr/)** | Service des Données et Études Statistiques (Ministère de la Transition écologique) | Comptes de l'environnement — Volumes d'eau pour irrigation |
| **[france-geojson](https://github.com/gregoiredavid/france-geojson)** | Grégoire David | Contours régionaux simplifiés (GeoJSON) |

**Licence** : Toutes les données sont diffusées sous [Licence Ouverte v2.0 (Etalab)](https://www.etalab.gouv.fr/licence-ouverte-open-licence/)

---

## Limites connues

- **Données simplifiées** : Pourcentages arrondis et ajustés pour atteindre 100% par région (objectif pédagogique)
- **Couverture géographique** : France métropolitaine uniquement (pas de DROM-COM)
- **Export PDF** : Peut échouer sur Firefox ancien ou Safari iOS (privilégier Chrome/Edge)
- **Performance** : Animations potentiellement saccadées sur navigateurs anciens ou écrans basse résolution
- **Responsivité mobile** : Interface optimisée pour desktop (min. 1024px), affichage mobile fonctionnel mais compressé

---

##  Modifications depuis la soutenance

Pour le rendu final du **9 mars 2026** :

**Modal d'introduction** avec résultats principaux et guide d'utilisation  
**Page "Sources & Méthodologie"** détaillant données, méthodologie, limites et crédits  
**Légendes améliorées** : plus visibles, avec titre et ombre portée  
**Tooltips enrichis** au survol des régions (culture dominante, eau, GES)  
**Lien "En savoir plus"** dans le footer vers la documentation complète  
**Accessibilité** : rel="noopener noreferrer" sur liens externes  

---

##  Équipe

**Développeurs**  
- [Amani KRID](https://github.com/KRIDAmani) — amani.krid@etu.ec-lyon.fr
- [Shreeniketh ARASANIPALAI KRISHNAN](https://github.com/Shreeniketh-AK) — shreeniketh.arasanipalai-krishnan@etu.ec-lyon.fr


**Encadrement**  
- MOS 9.1 — Visualisation de données  
- CentraleLyon, 2025-2026

---

## 📄 Licence

Le code source de cette visualisation est disponible sur ce repo.  
Les données sont diffusées sous Licence Ouverte v2.0 (Etalab).

---

**Développé dans le cadre du cours MOS 9.1 — Visualisation interactive de données**

⭐ Si vous trouvez ce projet utile, n'hésitez pas à lui donner une étoile sur GitHub !
