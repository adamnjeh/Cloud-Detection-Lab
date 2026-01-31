# Éthique et limitations — Cloud Detection Lab (Blue Team)

## 1. Positionnement défensif
Ce projet est **exclusivement défensif**. Il vise l’observation, l’analyse et la détection d’événements de sécurité à partir de logs, ainsi que la mise en place de réponses contrôlées.

## 2. Interdictions explicites
Sont strictement interdits :
- l’exploitation de vulnérabilités,
- l’utilisation ou le développement de payloads malveillants,
- toute forme d’attaque réelle ou intrusive,
- la compromission de systèmes tiers,
- l’usage de données réelles ou sensibles.

## 3. Simulations autorisées
Uniquement des comportements générant des **signaux observables**, par exemple :
- échecs d’authentification répétés,
- comportements anormaux simples (fréquence, volume),
- événements de configuration simulés,
- anomalies bénignes et contrôlées.

## 4. Données et confidentialité
- Données synthétiques ou logs sanitisés uniquement
- Suppression ou masquage des identifiants sensibles
- Aucune clé, secret ou token dans le dépôt Git

## 5. Sécurité et responsabilité
- Principe du moindre privilège (IAM)
- Surface d’attaque minimale
- Réponses automatiques :
  - réversibles,
  - temporaires,
  - journalisées.

## 6. Cadre légal
Le laboratoire est destiné à un usage pédagogique dans un environnement autorisé. Le respect des règles institutionnelles et des conditions AWS est obligatoire.

## 7. Limitations connues
- Environnement de petite taille
- Couverture limitée comparée à un SOC industriel
- Détection majoritairement basée sur des règles
- Contraintes budgétaires

## 8. Découverte fortuite de vulnérabilité
Toute vulnérabilité réelle découverte accidentellement ne doit pas être exploitée. Elle doit être documentée de manière responsable.
