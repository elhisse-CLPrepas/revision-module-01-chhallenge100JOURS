# AGENT.md - Collecte et suivi des réponses candidats

## 1. Rôle de l'agent

L'agent accompagne la collecte des retours de révision du Module 01.

Il ne remplace pas la validation humaine de l'atelier.

Son rôle est de :

- lire le récapitulatif produit par la mini-application ;
- vérifier que le candidat a fourni un ID-mail au format valide ;
- aider à classer les réponses ;
- préparer une ligne de suivi ;
- guider l'enregistrement dans le dossier de suivi candidats ;
- éviter la publication de données privées dans GitHub.

## 2. Principe de sécurité

La page `index.html` est une page publique ou publiable.

Elle ne doit pas enregistrer automatiquement :

- liste réelle des candidats ;
- fichier Excel privé ;
- résultats individuels détaillés ;
- téléphone ;
- mot de passe ;
- token ;
- données personnelles sensibles.

La collecte doit rester contrôlée par le formateur ou l'encadrant.

## 3. Dossier cible de suivi

Le dossier de suivi attendu doit rester hors de la page publique.

Chemin officiel de suivi retenu :

```txt
C:\DEV\CHALLENGE-01-Juin-2026\06-SUIVI-CANDIDATS
```

Remarque : Windows ne distingue pas les majuscules et minuscules dans les chemins. Le nom peut donc apparaître comme `CHALLENGE-01-JUIN-2026` ou `CHALLENGE-01-Juin-2026` selon l'affichage, mais il s'agit du même dossier local.

Ne pas utiliser de dossier approximatif comme `CHALLENG-JUIN-2026` ou `CHALLENGE-01-JUIN-026` si ce dossier n'existe pas réellement sur la machine.

## 4. Ce que la mini-application peut collecter

La mini-application peut préparer localement :

- ID-mail candidat saisi ;
- nombre de points cochés dans la checklist ;
- réponses d'auto-évaluation ;
- statut du bouton "Je suis prêt pour le quiz" ;
- date et heure de génération du récapitulatif ;
- actions cochées ;
- actions restantes.

Ces informations sont affichées dans le champ "Récapitulatif local des actions".

## 5. Ce que la mini-application ne fait pas

La mini-application ne fait pas :

- écriture automatique dans un dossier local ;
- écriture automatique dans GitHub ;
- envoi automatique d'email ;
- connexion à une base de données ;
- validation officielle du candidat ;
- comparaison automatique avec la liste Excel privée.

Cette limite est normale pour une page HTML publique.

## 6. Workflow de collecte recommandé

### Étape 1 - Le candidat révise

Le candidat :

1. ouvre `index.html` ;
2. saisit son ID-mail ;
3. coche la checklist ;
4. répond à l'auto-évaluation ;
5. clique sur "Je suis prêt pour le quiz" ;
6. copie le récapitulatif ou télécharge le fichier CSV local.

### Étape 2 - Le candidat transmet le retour

Le candidat transmet le retour par :

- email ;
- formulaire privé de l'atelier ;
- fichier remis à l'encadrant ;
- canal interne validé.

### Étape 3 - L'encadrant contrôle

L'encadrant vérifie :

- format de l'ID-mail ;
- présence du candidat dans la liste privée ;
- cohérence du récapitulatif ;
- absence de donnée sensible ;
- statut de préparation avant quiz.

### Étape 4 - L'encadrant enregistre

L'encadrant ajoute ou importe la ligne CSV dans le fichier de suivi candidats.

Exemple de structure CSV :

```csv
date,module,email_id,checklist_total,checklist_ok,auto_oui,auto_pas_encore,pret_quiz,statut_validation,commentaire
2026-06-16,module-01,candidat@example.com,7,6,4,1,oui,a_verifier,Retour reçu avant quiz
```

## 7. Format de ligne de suivi conseillé

Champs recommandés :

```txt
date
module
email_id
checklist_total
checklist_ok
auto_oui
auto_pas_encore
pret_quiz
statut_validation
commentaire
```

Valeurs possibles pour `statut_validation` :

```txt
a_verifier
valide
a_corriger
absent_liste
doublon
```

## 8. Règles de nommage des fichiers de suivi

Nom recommandé :

```txt
suivi-reponses-module-01.csv
```

Emplacement recommandé :

```txt
06-SUIVI-CANDIDATS\suivi-reponses-module-01.csv
```

Ne pas placer ce fichier dans le dépôt public de la page de révision si les emails réels y sont présents.

## 9. Données publiques et données privées

### Peut rester public

- structure de la page ;
- README ;
- AGENT.md ;
- explication du workflow ;
- exemples fictifs ;
- modèles de champs.

### Doit rester privé

- emails réels ;
- fichier de suivi réel ;
- liste d'inscription ;
- décisions individuelles ;
- notes personnelles ;
- exports Excel ou CSV réels.

## 10. Export CSV local

La page contient un bouton :

```txt
Télécharger le suivi CSV
```

Ce bouton génère un fichier local :

```txt
suivi-reponses-module-01.csv
```

L'encadrant peut ensuite copier ou importer ce fichier dans le dossier privé de suivi candidats.

Cette approche reste plus sûre qu'une écriture automatique directe dans un dossier local, car le navigateur ne peut pas écrire dans un dossier privé sans action humaine.

## 11. Règle finale

L'agent aide à organiser la collecte.

L'humain valide.

Le dossier de suivi reste privé.

GitHub ne doit recevoir que le code, la documentation et les modèles sans données personnelles réelles.
