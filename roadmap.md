# Plan de Projet — Blue Team / Cloud Detection Lab

## 🟦 Phase 0 — Cadrage (Semaine 0)

**Objectif :** verrouiller le périmètre pour éviter toute dérive.

### À faire
- Valider le sujet officiel du projet  
- Définir le périmètre éthique (**défensif uniquement**)  
- Choisir :
  - cloud provider (ex : AWS)
  - outils (cloud-native + scripts Python)
- Créer le repository Git (privé)

### Livrables
- `docs/project-scope.md`
- `docs/ethics-and-limitations.md`

---

## 🟦 Phase 1 — Architecture & Design (Semaine 1)

**Objectif :** montrer la capacité à concevoir un système complet.

### À faire
- Concevoir l’architecture du lab :
  - service protégé
  - collecte de logs
  - détection
  - réponse
- Définir **5 scénarios de menace simples**

### Livrables
- `docs/architecture.md`
- Schéma réseau
- `docs/threat-model.md`

---

## 🟦 Phase 2 — Mise en place de l’environnement cloud (Semaines 2–3)

**Objectif :** environnement fonctionnel et maîtrisé.

### À faire
- Déployer :
  - une instance / service cible
  - un système de logs centralisés
- Sécuriser :
  - accès réseau
  - authentification
- Tester la remontée correcte des logs

### Livrables
- `infrastructure/`
- `docs/environment-setup.md`
- Captures d’écran (preuves)

---

## 🟦 Phase 3 — Collecte et compréhension des logs (Semaine 4)

**Objectif :** cœur Blue Team — comprendre le signal.

### À faire
- Identifier les logs utiles :
  - authentification
  - système
  - réseau
- Analyser leur structure
- Documenter :
  - informations pertinentes
  - bruit

### Livrables
- `docs/log-analysis.md`
- Échantillons de logs sanitisés
- Notes d’interprétation

---

## 🟦 Phase 4 — Simulation de comportements malveillants (Semaine 5)

**Objectif :** générer des signaux observables, sans exploitation.

### À faire
- Simuler :
  - échecs d’authentification répétés
  - comportements anormaux simples
- Vérifier l’impact sur les logs

⚠️ **Pas d’exploit, pas de payload.**

### Livrables
- `docs/threat-simulation.md`
- Logs avant / après
- Timeline des événements

---

## 🟦 Phase 5 — Détection (Semaines 6–7)

**Objectif :** transformer les logs en alertes.

### À faire
- Implémenter :
  - règles par seuil
  - règles par pattern
- Tester chaque règle
- Ajuster les faux positifs

### Livrables
- `detection/rules/`
- `docs/detection-logic.md`
- Tableau règles → alertes

---

## 🟦 Phase 6 — Réponse et automatisation (Semaine 8)

**Objectif :** démontrer une maturité SOC.

### À faire
- Implémenter au moins une réponse automatique :
  - alerte
  - blocage temporaire
  - enrichissement de logs
- Justifier les choix

### Livrables
- `automation/response-scripts/`
- `docs/incident-response.md`

---

## 🟦 Phase 7 — Walkthroughs d’incidents (Semaine 9)

**Objectif :** capacité d’analyse et de restitution.

### À faire
Pour **2 à 3 scénarios** :
- décrire l’attaque simulée
- présenter les logs
- expliquer la détection
- expliquer la réponse

### Livrables
- `docs/incident-walkthroughs.md`
- Diagrammes temporels

---

## 🟦 Phase 8 — Nettoyage & sécurisation (Semaine 10)

**Objectif :** rigueur professionnelle.

### À faire
- Supprimer toute donnée sensible
- Vérifier le repo public
- Ajouter disclaimers et limites
- Vérifier les coûts cloud (shutdown)

### Livrables
- Repository prêt à publication
- Section **Limitations & Future Work**

---

## 🟦 Phase 9 — Rapport final (Semaines 11–12)

**Objectif :** valorisation académique et professionnelle.

### À faire
- Rédiger le rapport :
  - contexte
  - architecture
  - méthodologie
  - résultats
  - limites
- Exporter le PDF
- Préparer la soutenance

### Livrables
- `reports/final-report.pdf`
- Slides (optionnel)

---

## 🧠 Ce que ce plan démontre
- pensée défensive
- compréhension cyber réaliste
- capacité de structuration
- usage responsable du cloud
- maturité Blue Team