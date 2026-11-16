# 2. Parties prenantes

**Projet :** informatisation de la gestion des patients du CSCOM « Espoir ».

## Tableau des parties prenantes

| # | Partie prenante | Rôle dans le projet | Influence | Intérêt | Stratégie |
|---|---|---|---|---|---|
| 1 | **ASACO** (association de santé communautaire, gestionnaire du CSCOM) | **MOA** : commanditaire, finance le projet et valide | Forte | Fort | Gérer de près : réunions de validation à chaque phase |
| 2 | **Médecin-chef** | Représentant de la MOA, utilisateur principal | Forte | Fort | Gérer de près : impliquer dans la définition des besoins |
| 3 | **Équipe projet (étudiants développeurs)** | **MOE** : conçoit et réalise le système | Moyenne | Fort | Gérer de près : suivi hebdomadaire |
| 4 | **Agents d'accueil et caissier** | Utilisateurs quotidiens de l'enregistrement et de la caisse | Faible | Fort | Tenir informés, former, recueillir leurs remarques |
| 5 | **Infirmiers et sages-femmes** | Utilisateurs : saisie des consultations et des soins | Moyenne | Fort | Tenir informés, faire tester les écrans |
| 6 | **Patients** | Bénéficiaires finaux (moins d'attente, meilleur suivi) | Faible | Moyen | Informer (affichage, explication à l'accueil) |
| 7 | **District sanitaire / Direction régionale de la santé** | Reçoit les rapports, impose des formats de données | Forte | Moyen | Satisfaire : respecter les formats de rapport demandés |
| 8 | **Gestionnaire de la pharmacie** | Utilisateur du module stock (phase suivante) | Faible | Moyen | Surveiller et informer |

## Matrice influence / intérêt

```
                 INTÉRÊT faible            INTÉRÊT fort
              +------------------------+-------------------------------+
 INFLUENCE    |  SATISFAIRE            |  GÉRER DE PRÈS                |
 forte        |  - District sanitaire  |  - ASACO (MOA)                |
              |                        |  - Médecin-chef               |
              |                        |  - Équipe projet (MOE)        |
              +------------------------+-------------------------------+
 INFLUENCE    |  SURVEILLER            |  TENIR INFORMÉS               |
 faible       |  - Gestionnaire        |  - Agents d'accueil, caissier |
              |    pharmacie           |  - Infirmiers, sages-femmes   |
              |  - Patients            |                               |
              +------------------------+-------------------------------+
```

**MOA** (maîtrise d'ouvrage) : celui qui exprime le besoin et paie, ici l'ASACO représentée par le médecin-chef.
**MOE** (maîtrise d'œuvre) : celui qui réalise la solution, ici l'équipe projet.
