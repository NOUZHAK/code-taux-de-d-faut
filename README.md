#  Modélisation du Risque de Crédit (PD) et du Taux de Remboursement Anticipé (CPR)
Open in colabe:
le script de taux de defaut: https://colab.research.google.com/drive/1CDLk-Moc8NuY2hpJvyTZTbLW8bWni4WL
le script de taux de RPA : https://colab.research.google.com/drive/1dB4ZVuIGHZaPNoKQltYN7B7CJ33mETp6

## 📌 Présentation du Projet
Ce dépôt rassemble les travaux de recherche, de traitement de données et de modélisation financière réalisés dans le cadre de mon **Projet de Fin d'Études (PFE)**. L'objectif principal est l'optimisation des modèles prédictifs appliqués à la gestion d'un fonds de titrisation, et plus particulièrement sur le compartiment **Invest Al Mouaddaf III**.

Le projet se divise en deux problématiques majeures de la gestion actif-passif (ALM) et du risque de crédit :
1. **Modélisation de la Probabilité de Défaut (PD)** pour évaluer la qualité de crédit des contreparties.
2. **Modélisation du Taux de Remboursement Anticipé (CPR / SMM)** pour anticiper les comportements de remboursement et sécuriser les flux financiers du portefeuille (Waterfall mechanism).

---

## 🛠️ Travail Réalisé & Démarche Scientifique

### 1. Analyse Risque de Crédit (Modélisation de la PD)
* **Algorithmes entraînés :** Régression Logistique, Random Forest, et sélection du **modèle champion XGBoost**.
* **Interprétabilité Globale et Locale :** Implémentation des frameworks **SHAP (TreeExplainer)** et **LIME (LimeTabularExplainer)** pour auditer les décisions du modèle champion et lever l'effet "boîte noire".
* **Variables Clés Identifiées :** Ancienneté du crédit (courbe en J), Capital Restant Dû, Engagement Total et indicateurs démographiques.

### 2. Analyse du Comportement de Remboursement (Modélisation du CPR)
* **Approches comparées :** Méthode traditionnelle par Courbes de Vintage face aux algorithmes de Machine Learning (Random Forest, XGBoost) et réseaux de neurones (LSTM).
* **Variables Clés Identifiées :** Forte saisonnalité mensuelle, âge/ancienneté de la ligne de crédit, et écart (spread) entre le taux contractuel et le taux de marché.

---

## 📁 Structure du Dépôt
* 📂 **`PDtests.ipynb`** : Notebook contenant la préparation des données, l'entraînement des modèles de classification (PD) et l'analyse de l'interprétabilité avec SHAP & LIME.
* 📂 **`RPAtests.ipynb`** : Notebook dédié à la prédiction du taux de remboursement anticipé (RPA/CPR) et à l'analyse de sa saisonnalité.
* 📂 **`Fichier_Encadrants.xlsx`** : Base de recherche quantitative, statistiques descriptives, cadrage théorique et données de suivi du projet.

---

## 💻 Technologies et Librairies Utilisées
* **Langage :** Python (Google Colab)
* **Machine Learning :** Scikit-Learn, XGBoost, TensorFlow/Keras (LSTM)
* **Explicabilité (XAI) :** SHAP, LIME
* **Analyse de données :** Pandas, NumPy, Matplotlib, Seaborn
* **Cadrage :** Microsoft Excel / Power Query
