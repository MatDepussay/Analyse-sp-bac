# Analyse-sp-bac

# 📊 Influence de la filière du baccalauréat sur les choix de vie

## 👥 Auteurs
- JB  
- Mathias  

## 📅 Année
- 2023

---

## 🧠 Problématique

Ce projet se penche sur une question provocante et souvent discutée :  
> **"La filière choisie pour le bac a-t-elle une influence sur nos choix de vie ?"**

À travers une série d’analyses statistiques, nous avons tenté de vérifier si les stéréotypes associés aux différentes filières du lycée (S, ES, STMG, etc.) sont justifiés ou non, en étudiant des comportements tels que l’usage des réseaux sociaux, la consommation de tabac et d’alcool.

---

## 📂 Données

Le jeu de données provient d’un **questionnaire anonyme** administré à la rentrée 2023 via la plateforme Célène. Il a été rempli par des étudiants de Licence 1 en **Économie** et **Gestion** à l’Université de Tours.

### Format :
- Fichier CSV : `sondage_version_finale.csv`
- Encodage : UTF-8
- Séparateur : `;`

---

## 📦 Packages R utilisés

Le projet utilise les packages suivants :

```r
library(knitr)
library(kableExtra)
library(ggplot2)
library(ggridges)
library(forcats)
library(patchwork)
library(readr)
library(dplyr)
library(gridExtra)
library(modelsummary)

## 🛠 Traitement des données
Regroupement des bacs avec spécialités pour correspondre aux anciennes filières (S, ES, STMG).

Création d’une variable Filière2 regroupant les étudiants selon les filières ou spécialités équivalentes.

Nettoyage des données manquantes (ex. : NA pour les spécialités).

## 📈 Analyses réalisées
1. Répartition des répondants par filière
Visualisation du nombre de répondants par filière (S, ES, STMG, Autres).

2. Réseaux sociaux
Analyse du réseau social le plus utilisé par filière.

Test du Chi² pour évaluer la significativité des différences.

3. Tabagisme
Répartition des fumeurs selon leur filière.

Test du Chi² pour valider l’influence statistique de la filière sur la consommation de tabac.

4. Consommation d’alcool
Analyse du rythme de consommation par filière.

Test du Chi² pour mesurer la significativité.

## 🧪 Méthodologie statistique
Pour chaque comportement (tabac, alcool, réseaux sociaux), un test du Chi² d’indépendance est utilisé afin de déterminer si les différences observées entre les filières sont statistiquement significatives.

Hypothèse nulle (H0) : pas d’influence de la filière sur le comportement étudié.

Hypothèse alternative (H1) : la filière influence significativement le comportement.

## 🔍 Résultats principaux

| Thème           | Résultat du test du Chi² | Conclusion                               |
| --------------- | ------------------------ | ---------------------------------------- |
| Réseaux sociaux | p-value > 0.05           | Pas de lien significatif avec la filière |
| Tabac           | p-value < 0.05           | Lien significatif avec la filière        |
| Alcool          | p-value > 0.05           | Pas de lien significatif avec la filière |

## 📝 Remarques
Certaines catégories de spécialités ont été regroupées manuellement pour correspondre aux anciennes filières (ex. : Maths/Physique = filière S).

Les résultats sont basés sur un échantillon d’étudiants de L1 ; ils ne peuvent pas être généralisés à toute la population sans prudence.

