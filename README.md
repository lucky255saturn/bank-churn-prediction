# 🏦 Bank Customer Churn Prediction

## Description
Projet de Machine Learning visant à prédire le churn (départ) des clients d'une banque.
À partir des caractéristiques d'un client, le modèle prédit s'il va quitter la banque ou non.

## Contexte
En banque, retenir un client existant coûte 5x moins cher qu'en acquérir un nouveau.
Ce modèle permet d'identifier les clients à risque **avant** qu'ils partent, pour que la banque puisse agir proactivement.

## Dataset
- **Source** : Kaggle - Bank Customer Churn Dataset
- **Taille** : 10 000 clients
- **Variables** : age, balance, credit score, pays, genre, ancienneté, produits, activité, salaire
- **Cible** : churn (0 = reste, 1 = part)

## Résultats

| Modèle | Accuracy | Rappel (churneurs) | F1-score |
|--------|----------|-------------------|----------|
| Régression Logistique | 81% | 20% | 0.29 |
| **Random Forest** | **87%** | **47%** | **0.58** |

Le Random Forest est significativement meilleur pour détecter les vrais churneurs.

## Variables les plus prédictives
1. **Age** (24%) → les clients plus âgés churnnent plus
2. **Salaire estimé** (15%) → les clients aisés reçoivent de meilleures offres ailleurs
3. **Credit Score** (14%)
4. **Balance** (14%) → un solde élevé corrèle avec le churn

## Conclusions
- Le profil type du churner : **client âgé, avec un solde élevé, peu actif**
- Hypothèse : ces clients reçoivent des offres concurrentes plus attractives
- Le credit score seul n'est **pas** prédictif du churn contrairement à l'intuition initiale

## Technologies
- Python 3
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (LogisticRegression, RandomForestClassifier)
- Jupyter Notebook

## Structure du projet
```
bank-churn-prediction/
│
├── churn_prediction.ipynb  # Notebook principal
├── churn.csv               # Dataset
└── README.md               # Documentation
```

## Étapes du projet
1. **Exploration** — statistiques descriptives, visualisations
2. **Préparation** — encodage des variables catégorielles, normalisation
3. **Modélisation** — régression logistique et Random Forest
4. **Évaluation** — accuracy, précision, rappel, F1-score
5. **Interprétation** — feature importance, conclusions métier

## Auteur
**Saad Ouaziz** — Ingénieur en Systèmes d'Information
