# Classification ML pour la détection du risque d'hypertension

## 📋 Aperçu du Projet

Ce projet implémente un modèle de classification supervisée pour prédire le risque d'hypertension chez les patients en utilisant des données médicales et démographiques.

## 🎯 Objectifs

- **Objectif principal** : Établir un modèle de classification performant pour la prédiction du risque d'hypertension
- **Objectif secondaire** : Identifier les caractéristiques critiques corrélées au risque d'hypertension

## 📊 Dataset

- **Source** : [Hypertension Risk Model Dataset](https://www.kaggle.com/datasets/khan1803115/hypertension-risk-model-main/) (Kaggle)
- **Taille initiale** : 4 240 entrées
- **Taille après nettoyage** : 3 282 entrées (suppression des valeurs manquantes et des outliers)
- **Indicateur d'utilisabilité** : 7.65/10

### Variables analysées
- **Démographiques** : âge, sexe (male)
- **Comportementales** : tabagisme actuel (currentSmoker), cigarettes par jour (cigsPerDay)
- **Médicales** : médication BP (BPMeds), diabète, cholestérol total (totChol)
- **Physiologiques** : tension systolique/diastolique (sysBP/diaBP), IMC (BMI), rythme cardiaque (heartRate), glucose
- **Cible** : Risque d'hypertension (Risk) - binaire (0/1)

## 🔧 Préparation des Données

### Nettoyage effectué :
1. **Valeurs manquantes** : Suppression de 489 entrées (11.5%) avec approche brute-force
2. **Détection d'outliers** : 
   - Méthode IQR retenue (469 outliers supprimés)
   - Comparaison avec méthode Z-score (205 outliers détectés)
3. **Vérifications** : Aucun doublon détecté, cohérence des valeurs BP

### Caractéristiques du dataset final :
- **Distribution de classe** : Déséquilibre vers les sujets sains (~2:1)
- **Biais identifiés** : Forte sous-représentation des patients sous médication BP et diabétiques

## 📈 Analyse Exploratoire

- Analyse univariée des variables numériques et catégorielles
- Détection et traitement des outliers (méthode IQR privilégiée)
- Analyse de l'asymétrie (skewness) et de l'aplatissement (kurtosis)
- Visualisations avec boxplots et histogrammes

## 📋 Prérequis

```python
pandas
numpy
matplotlib
seaborn
scipy
```
---

*Projet réalisé dans le cadre d'un projet en autonomie à Loughborough University*
