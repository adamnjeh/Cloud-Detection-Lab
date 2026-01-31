# Périmètre du projet - Cloud Detection Lab (Blue Team) - AWS

## 1. Présentation du projet
Ce projet consiste à concevoir et implémenter un **laboratoire cloud défensif** sur **AWS**, visant à démontrer une démarche Blue Team complète :
- déploiement d’un **service cible bénin**,
- **centralisation des logs**,
- mise en place de **mécanismes de détection**,
- déclenchement de **réponses sûres et contrôlées**,
- analyse et restitution via des **walkthroughs d’incidents**.

Le projet est strictement orienté **défense et détection**.

## 2. Objectifs du projet
Le projet doit permettre de :
1. Déployer un environnement AWS fonctionnel comprenant :
   - un service cible (VM / application simple),
   - un système de collecte et de centralisation des logs.
2. Définir et documenter **au moins 5 scénarios de menace simples** (simulation uniquement).
3. Implémenter une couche de **détection basée sur les logs** :
   - règles par seuil,
   - règles par motifs (patterns).
4. Mettre en œuvre **au moins une réponse automatisée**, sûre et réversible.
5. Fournir une documentation claire assurant la **reproductibilité** du lab.

## 3. Hors périmètre (out of scope)
Ce projet n’inclut pas :
- l’exploitation de vulnérabilités,
- le développement ou l’utilisation de malware,
- l’élévation de privilèges ou la persistance,
- les attaques sur des systèmes réels ou tiers,
- la mise en place d’un SIEM industriel complet.

## 4. Environnement cible (AWS)
- **Cloud provider** : Amazon Web Services (AWS)
- **Région** : unique, figée dès le début du projet
- **Compte** : compte AWS dédié au projet

### Ressources minimales recommandées
- 1 instance EC2 Linux (service cible)
- IAM avec principe du **moindre privilège**
- VPC et Security Groups à exposition réseau minimale

## 5. Périmètre de collecte des logs
### Logs obligatoires
- Logs d’authentification (SSH)
- Logs système (syslog / journald)
- Traces réseau visibles via les logs système ou cloud

### Logs AWS (optionnels mais valorisants)
- AWS CloudTrail
- VPC Flow Logs
- CloudWatch Logs

## 6. Périmètre de détection
### Types de règles
- **Seuil** : nombre anormal d’événements sur une fenêtre temporelle
- **Pattern** : motifs suspects récurrents dans les logs

### Sorties attendues
Chaque alerte doit contenir :
- horodatage,
- règle déclenchée,
- extrait de log,
- niveau de sévérité,
- action recommandée.

## 7. Périmètre de réponse
Au moins une réponse automatisée, respectant :
- réversibilité,
- durée limitée,
- traçabilité complète.

Exemples :
- notification,
- restriction réseau temporaire,
- enrichissement des logs ou alertes.

## 8. Livrables attendus
- `docs/project-scope.md`
- `docs/ethics-and-limitations.md`
- `docs/architecture.md`
- `docs/environment-setup.md`
- `docs/log-analysis.md`
- `docs/threat-model.md`
- `docs/detection-logic.md`
- `docs/incident-response.md`
- `docs/incident-walkthroughs.md`
- `reports/final-report.pdf`

## 9. Critères de réussite
- Environnement reproductible et documenté
- Scénarios clairement traçables dans les logs
- Alertes pertinentes après ajustement des faux positifs
- Démonstration d’au moins une réponse automatique
- Dépôt propre, documenté et assaini

## 10. Maîtrise des coûts
- Budget mensuel plafonné
- Utilisation prioritaire du Free Tier
- Extinction des ressources inutilisées
- Une seule région AWS utilisée
