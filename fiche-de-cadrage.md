# Fiche de cadrage
**Projet :** SI de gestion des patients du CSCOM « Espoir » (Bamako)
**Rédigé par :** Alassane Coulibaly, Djibril Diarra – Licence Génie logiciel
**Phase :** Cadrage

---

## 1. Contexte et problème à résoudre

**Contexte.** Le CSCOM « Espoir » est un centre de santé communautaire de Bamako qui reçoit environ 80 patients par jour. Il est géré par une ASACO (association de santé communautaire). Toute la gestion des patients se fait sur papier : registres, fiches rangées dans des armoires, reçus manuscrits.

**MOA (maîtrise d'ouvrage) :** l'ASACO, représentée par le médecin-chef du CSCOM. Elle exprime le besoin, finance et valide le projet.
**MOE (maîtrise d'œuvre) :** l'équipe projet (Alassane Coulibaly et Djibril Diarra, étudiants en Génie logiciel), qui conçoit et réalise la solution.

**Problème.** L'enregistrement d'un patient prend environ 15 minutes, les fiches se perdent ou sont en double, l'historique médical est incomplet et les statistiques mensuelles envoyées au district sont longues à produire (environ 5 jours) et peu fiables.

## 2. Périmètre

| Inclus dans le projet | Exclu du projet |
|---|---|
| Enregistrement des patients avec un identifiant unique | Gestion du stock de la pharmacie (projet suivant) |
| Recherche du dossier et de l'historique des consultations | Dossier médical complet (imagerie, laboratoire) |
| Saisie des consultations par le personnel soignant | Prise de rendez-vous en ligne par les patients |
| Enregistrement des paiements à la caisse | Paie et gestion du personnel |
| Statistiques mensuelles pour le district sanitaire | Connexion avec les systèmes nationaux (DHIS2) |
| Réseau local et sauvegarde des données | Application mobile |
| Formation des utilisateurs | Achat de matériel au-delà de 3 postes |

## 3. Acteurs et parties prenantes

| Partie prenante | Rôle | Influence | Intérêt |
|---|---|---|---|
| ASACO | MOA, financeur | Forte | Fort |
| Médecin-chef | Représentant MOA, utilisateur | Forte | Fort |
| Équipe projet | MOE | Moyenne | Fort |
| Agents d'accueil, caissier | Utilisateurs quotidiens | Faible | Fort |
| Infirmiers, sages-femmes | Utilisateurs | Moyenne | Fort |
| Patients | Bénéficiaires | Faible | Moyen |
| District sanitaire | Destinataire des rapports | Forte | Moyen |
| Gestionnaire pharmacie | Futur utilisateur | Faible | Moyen |

(Détail et matrice influence/intérêt : voir `02-parties-prenantes.md`.)

## 4. Objectifs mesurables

| # | Objectif | Situation actuelle | Cible | Délai |
|---|---|---|---|---|
| O1 | Réduire de moitié le temps d'enregistrement d'un patient | ≈ 15 min | ≤ 7 min | 3 mois après mise en service |
| O2 | Retrouver le dossier d'un patient déjà venu | ≈ 10 min | < 1 min | Dès la mise en service |
| O3 | Supprimer les doublons de dossiers | Nombreux | 0 nouveau doublon | Dès la mise en service |
| O4 | Produire le rapport mensuel du district | ≈ 5 jours | ≤ 1 jour | 2 mois après mise en service |
| O5 | Former le personnel concerné | 0 % | 100 % des agents d'accueil, caissier et soignants | Avant la mise en service |

## 5. Risques et hypothèses

### Risques

| Risque | Probabilité | Impact | Mesure prévue |
|---|---|---|---|
| Coupures d'électricité fréquentes | Forte | Fort | Onduleurs, sauvegarde automatique quotidienne |
| Résistance au changement du personnel | Moyenne | Fort | Impliquer les utilisateurs dès le début, formation pratique |
| Faible maîtrise de l'informatique par certains agents | Moyenne | Moyen | Interface simple, en français, avec peu d'écrans |
| Budget insuffisant pour le matériel | Moyenne | Fort | Réutiliser l'ordinateur existant, solution open source |
| Perte ou fuite de données médicales | Faible | Fort | Comptes avec mot de passe, droits par rôle, sauvegardes |
| Retard de l'équipe projet | Moyenne | Moyen | Planning par phases, livraisons intermédiaires |

### Hypothèses
- L'ASACO accepte de financer au moins 2 ordinateurs supplémentaires et un onduleur.
- Le médecin-chef est disponible 1 heure par semaine pour valider les étapes.
- Le personnel accepte d'être formé (2 demi-journées).
- Les anciennes fiches papier ne seront pas toutes ressaisies : seuls les patients qui reviennent seront enregistrés dans le nouveau système.
- Le format du rapport mensuel exigé par le district reste le même pendant le projet.
