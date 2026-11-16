# 1. Analyse d'un SI existant

**Organisation étudiée :** CSCOM « Espoir », centre de santé communautaire à Bamako (environ 80 patients par jour).
**SI étudié :** le système actuel d'accueil, d'enregistrement et de suivi des patients, géré presque entièrement sur papier.

## Tableau des cinq composantes

| Composante | Description de l'existant au CSCOM |
|---|---|
| **1. Acteurs** (ressources humaines) | 2 agents d'accueil, 1 caissier, 3 infirmiers, 2 sages-femmes, 1 médecin-chef, 1 gestionnaire de pharmacie, les patients. |
| **2. Processus** (procédures) | Accueil → recherche ou création de la fiche patient → paiement du ticket → attente → consultation → ordonnance → pharmacie → rapport mensuel au district sanitaire. |
| **3. Données** (informations) | Identité du patient, fiches de consultation, carnets de santé, registres de consultation, reçus de caisse, stock de médicaments, statistiques mensuelles. |
| **4. Matériel** (ressources matérielles) | Registres papier, armoires de rangement des fiches, 1 ordinateur au bureau du médecin-chef, 1 imprimante, téléphones portables du personnel. |
| **5. Logiciels et réseaux** | Excel pour les statistiques mensuelles, WhatsApp pour communiquer entre le personnel et avec le district. Pas de réseau local ni de logiciel de gestion des patients. |

## Deux dysfonctionnements identifiés

### Dysfonctionnement 1 : enregistrement des patients trop long
- **Constat :** il faut environ 15 minutes pour enregistrer un patient (recherche de son ancienne fiche dans les armoires, ou recopie complète de ses informations).
- **Cause :** les fiches sont sur papier et classées à la main, sans identifiant unique pour chaque patient.
- **Conséquences :** longues files d'attente le matin, patients mécontents, consultations qui commencent en retard.

### Dysfonctionnement 2 : perte d'informations et doublons
- **Constat :** des fiches sont perdues ou abîmées, et un même patient peut avoir plusieurs fiches.
- **Cause :** aucune sauvegarde ni base de données centralisée.
- **Conséquences :** le médecin ne connaît pas l'historique du patient (risque médical), les statistiques envoyées au district sont fausses, et les recettes de caisse sont difficiles à contrôler.
