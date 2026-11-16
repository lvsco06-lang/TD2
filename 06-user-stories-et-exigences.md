# TD2 – 3. User stories et exigences non fonctionnelles

## 10 user stories avec critères d'acceptation

Forme : *En tant que [rôle], je veux [action] afin de [bénéfice].*

| ID | User story | Critères d'acceptation |
|---|---|---|
| US01 | En tant qu'**agent d'accueil**, je veux **enregistrer un nouveau patient** afin qu'il ait un dossier unique. | Le système attribue automatiquement un numéro de dossier unique. Nom, prénom, sexe, date de naissance et téléphone sont obligatoires. Un message prévient si un patient avec le même nom et la même date de naissance existe déjà. |
| US02 | En tant qu'**agent d'accueil**, je veux **rechercher un patient** par nom, téléphone ou numéro de dossier afin de retrouver son dossier sans le recréer. | La recherche fonctionne avec une partie du nom. Les résultats s'affichent en moins de 2 secondes. |
| US03 | En tant que **caissier**, je veux **encaisser une consultation avec calcul automatique de la part AMO** afin de ne pas faire d'erreur de montant. | Patient non assuré : le montant affiché est 5 000 F. Patient assuré AMO avec un numéro AMO renseigné : le montant affiché est 1 500 F. Le paiement est enregistré avec la date, l'heure et le nom du caissier. |
| US04 | En tant que **caissier**, je veux **imprimer un reçu** afin de le remettre au patient. | Le reçu indique le numéro du reçu, le nom du patient, la date, le montant payé et la part AMO s'il y en a une. |
| US05 | En tant qu'**infirmier ou médecin**, je veux **saisir une consultation** (motif, diagnostic, traitement) afin de garder une trace des soins. | La consultation est liée au dossier du patient. Le motif est obligatoire. La saisie n'est possible que si la consultation a été payée. |
| US06 | En tant que **médecin**, je veux **voir l'historique des consultations** d'un patient afin de mieux le soigner. | Les consultations s'affichent de la plus récente à la plus ancienne, avec la date, le motif, le diagnostic et le traitement. |
| US07 | En tant que **médecin-chef**, je veux **générer le rapport mensuel** afin de l'envoyer au district sanitaire. | Le rapport donne le nombre de consultations par sexe, tranche d'âge et motif pour le mois choisi. Il est exportable en PDF ou en Excel. |
| US08 | En tant qu'**administrateur**, je veux **gérer les comptes et les rôles** des utilisateurs afin que chacun n'accède qu'à ce qui le concerne. | On peut créer, modifier et désactiver un compte. Un caissier ne peut pas voir les diagnostics. Un agent d'accueil ne peut pas encaisser. |
| US09 | En tant que **caissier**, je veux **faire le point de caisse du jour** afin de contrôler les recettes. | Le système affiche le total encaissé, le nombre de paiements et la répartition entre patients AMO et non-AMO. |
| US10 | En tant que **patient**, je veux **recevoir un SMS de rappel** avant mon rendez-vous de suivi afin de ne pas l'oublier. | Un SMS est envoyé la veille du rendez-vous au numéro enregistré. |

## 5 exigences non fonctionnelles mesurables

| ID | Type | Exigence | Mesure (comment vérifier) |
|---|---|---|---|
| ENF01 | Performance | La recherche d'un patient est rapide, même avec beaucoup de dossiers. | Réponse en moins de 2 s avec 50 000 dossiers en base. |
| ENF02 | Disponibilité | Le système fonctionne sans Internet et résiste aux coupures. | Fonctionne sur le réseau local seul. Après une coupure de courant, aucune donnée déjà validée n'est perdue. |
| ENF03 | Sécurité | Les données médicales sont protégées. | Connexion obligatoire, mot de passe d'au moins 8 caractères, droits par rôle, 100 % des connexions enregistrées dans un journal. |
| ENF04 | Sauvegarde | Les données sont sauvegardées régulièrement. | Sauvegarde automatique chaque jour. Restauration complète en moins d'1 heure. |
| ENF05 | Utilisabilité | Le système est facile à prendre en main. | Après 2 h de formation, un agent enregistre un nouveau patient en moins de 3 min. Interface entièrement en français. |
