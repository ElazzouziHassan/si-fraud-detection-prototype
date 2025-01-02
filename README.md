# Système de Détection des Fraudes avec Python (Prototype).

Ce projet présente un prototype de **système intelligent de détection des fraudes bancaires**. Le système utilise un modèle de régression logistique pour prédire si une transaction est frauduleuse ou non, en se basant sur des transactions historiques de cartes de crédit. Le projet est développé en Python et utilise des bibliothèques courantes comme **Pandas**, **Scikit-Learn**, et **Seaborn** pour l'analyse des données et l'entraînement du modèle.

## Objectifs

- Détecter les fraudes bancaires dans un ensemble de données de transactions de cartes de crédit.
- Utiliser un modèle de machine learning pour classer les transactions comme frauduleuses ou non.
- Fournir une démonstration simple de la détection de fraude en utilisant des règles basées sur les montants des transactions.

## Prérequis

Pour exécuter ce projet, vous devez avoir les bibliothèques suivantes installées :

- **Python** 3.x
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**

## Résultats

Voici les résultats du modèle de détection des fraudes :

### Matrice de confusion

La matrice de confusion montre la performance du modèle sur les données de test. Elle permet de visualiser les **faux positifs**, **faux négatifs**, **vrais positifs** et **vrais négatifs**.

![Matrice de Confusion](./results/confusion%20metrix.png)

### Rapport de classification

Le rapport de classification fournit des métriques détaillées pour chaque classe : **Précision**, **Rappel**, et **F1-Score**.

![Rapport de Classification](./results/classification%20repport.png)

- **Précision** : 0.98
- **Rappel** : 0.95
- **F1-Score** : 0.96

### Détection Simple Basée sur un Seuil

Une règle simple a été utilisée pour marquer les transactions comme frauduleuses si le montant dépasse 1000 DHs. Voici un exemple de détection :

```python
def simple_fraud_detection(transaction):
    if transaction['Amount'] > 1000:
        return 1  # Fraude
    return 0  # Non fraude
```
### Conclusion
Le prototype de détection des fraudes bancaires présente un bon début avec un modèle de régression logistique. Toutefois, il peut être amélioré en explorant des techniques avancées, telles que l'utilisation de forêts aléatoires ou l'ajustement des données déséquilibrées.

