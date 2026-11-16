# Cahier des charges – Version 1
**Projet :** SI de gestion des patients du CSCOM « Espoir » (Bamako)
**Rédigé par :** Alassane Coulibaly, Djibril Diarra – Licence Génie logiciel
**Date :** 16/11/2026

---

## 1. Contexte et objectifs (repris du cadrage)

**Contexte.** Le CSCOM « Espoir » reçoit environ 80 patients par jour. La gestion des patients se fait sur papier. L'enregistrement prend environ 15 minutes, des fiches sont perdues ou en double, et le rapport mensuel au district demande environ 5 jours.
**MOA :** l'ASACO, représentée par le médecin-chef. **MOE :** l'équipe projet (Alassane Coulibaly, Djibril Diarra).

**Objectifs mesurables.**
- O1 : temps d'enregistrement d'un patient de 15 min à 7 min au maximum.
- O2 : retrouver le dossier d'un patient en moins d'1 min.
- O3 : aucun nouveau doublon de dossier.
- O4 : rapport mensuel produit en 1 jour au maximum.
- O5 : 100 % du personnel concerné formé avant la mise en service.

## 2. Tableau des exigences

Types : **F** = fonctionnelle, **NF** = non fonctionnelle.

| ID | Énoncé | Type | Priorité | Critère d'acceptation |
|---|---|---|---|---|
| US01 | L'agent d'accueil enregistre un nouveau patient. | F | Must | Un numéro de dossier unique est attribué. Les champs obligatoires sont contrôlés. Un doublon possible est signalé. |
| US02 | L'agent d'accueil recherche un patient par nom, téléphone ou numéro. | F | Must | Fonctionne avec une partie du nom. Résultat en moins de 2 s. |
| US03 | Le caissier encaisse une consultation avec calcul automatique de la part AMO. | F | Must | 5 000 F pour un patient non assuré, 1 500 F pour un assuré AMO. Paiement enregistré avec la date et le caissier. |
| US04 | Le caissier imprime un reçu. | F | Should | Le reçu indique le numéro, le patient, la date, le montant et la part AMO. |
| US05 | Le soignant saisit une consultation. | F | Must | La consultation est liée au dossier. Motif obligatoire. Saisie possible seulement si la consultation est payée. |
| US06 | Le médecin consulte l'historique du patient. | F | Must | Les consultations sont triées de la plus récente à la plus ancienne. |
| US07 | Le médecin-chef génère le rapport mensuel. | F | Should | Statistiques par sexe, âge et motif. Export en PDF ou Excel. |
| US08 | L'administrateur gère les comptes et les rôles. | F | Must | Créer, modifier, désactiver un compte. Chaque rôle n'a que ses droits. |
| US09 | Le caissier fait le point de caisse du jour. | F | Should | Total encaissé, nombre de paiements, répartition AMO et non-AMO. |
| US10 | Le patient reçoit un SMS de rappel de rendez-vous. | F | Could | SMS envoyé la veille du rendez-vous. |
| ENF01 | La recherche de patient est rapide. | NF – Performance | Should | Moins de 2 s avec 50 000 dossiers. |
| ENF02 | Le système fonctionne sans Internet et résiste aux coupures. | NF – Disponibilité | Must | Réseau local seul. Aucune donnée validée perdue après une coupure. |
| ENF03 | Les données sont protégées. | NF – Sécurité | Must | Connexion obligatoire, mot de passe de 8 caractères minimum, droits par rôle, connexions journalisées. |
| ENF04 | Les données sont sauvegardées. | NF – Sauvegarde | Must | Sauvegarde automatique quotidienne. Restauration en moins d'1 h. |
| ENF05 | Le système est facile à utiliser. | NF – Utilisabilité | Should | Après 2 h de formation, enregistrement d'un patient en moins de 3 min. Interface en français. |

## 3. Backlog produit ordonné

Estimation relative en **points d'effort** (suite de Fibonacci : 1, 2, 3, 5, 8, 13). Plus le nombre est grand, plus la tâche est complexe.

| Rang | ID | Élément | Priorité | Estimation |
|---|---|---|---|---|
| 1 | US08 + ENF03 | Comptes, rôles et connexion sécurisée | Must | 5 |
| 2 | US01 | Enregistrer un patient | Must | 5 |
| 3 | US02 + ENF01 | Rechercher un patient | Must | 3 |
| 4 | US03 | Encaisser avec calcul AMO | Must | 5 |
| 5 | US05 | Saisir une consultation | Must | 5 |
| 6 | US06 | Historique des consultations | Must | 3 |
| 7 | ENF02 + ENF04 | Fonctionnement en local et sauvegardes | Must | 5 |
| 8 | US04 | Imprimer un reçu | Should | 2 |
| 9 | US09 | Point de caisse journalier | Should | 3 |
| 10 | US07 | Rapport mensuel pour le district | Should | 8 |
| 11 | ENF05 | Tests d'utilisabilité et formation | Should | 3 |
| 12 | US10 | SMS de rappel | Could | 8 |

**Total :** 55 points, dont 31 points de « Must ».

## 4. Choix de la démarche : agile (Scrum)

Nous choisissons une démarche **agile de type Scrum**, avec des sprints de 2 semaines.
Le besoin n'est pas complètement stable : l'entretien a fait apparaître de nouvelles règles (AMO) et d'autres viendront.
Le client (le médecin-chef) est disponible et peut valider une version à la fin de chaque sprint.
Les « Must » sont livrés en premier, ce qui donne vite une version utilisable à l'accueil et à la caisse.
Une démarche en cascade serait trop risquée : une erreur de compréhension ne serait découverte qu'à la fin du projet.
