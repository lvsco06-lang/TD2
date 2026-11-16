# TD2 – 4. Priorisation MoSCoW

| Priorité | Signification | Éléments |
|---|---|---|
| **Must** (doit avoir) | Indispensable : sans cela, le système ne sert à rien | US01, US02, US03, US05, US06, US08 ; ENF02, ENF03, ENF04 |
| **Should** (devrait avoir) | Important, mais on peut livrer une première version sans | US04, US07, US09 ; ENF01, ENF05 |
| **Could** (pourrait avoir) | Un plus pour le projet, si on a le temps | US10 (SMS de rappel) |
| **Won't** (n'aura pas cette fois) | Exclu de cette version, à éliminer en premier si besoin | Prise de rendez-vous en ligne, gestion du stock de la pharmacie, application mobile |

## Justification des « Must »

- **US01 – Enregistrer un patient** et **US02 – Rechercher un patient** : c'est le cœur du problème identifié au cadrage. L'enregistrement prend 15 min et les fiches se perdent. Sans ces deux fonctions, l'objectif O1 (réduire de moitié le temps d'enregistrement) est impossible.
- **US03 – Encaisser avec calcul AMO** : aucun patient n'est consulté sans payer. Le client a insisté sur la règle des 5 000 F et des 1 500 F avec l'AMO. Une erreur de montant fait perdre de l'argent au CSCOM.
- **US05 – Saisir une consultation** et **US06 – Voir l'historique** : sans eux, le dossier patient reste vide et le médecin ne connaît pas les antécédents (risque médical cité dans le cadrage).
- **US08 – Gérer les comptes et les rôles**, **ENF03 – Sécurité** : les données médicales sont confidentielles. On ne peut pas mettre le système en service sans contrôle d'accès.
- **ENF02 – Fonctionner sans Internet et résister aux coupures**, **ENF04 – Sauvegarde** : à Bamako, les coupures sont fréquentes et Internet est peu fiable. Si le système tombe ou perd des données, le personnel reviendra au papier.
