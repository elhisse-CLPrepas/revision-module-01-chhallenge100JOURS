# Révision Module 01 - Challenge 100 jours LN-IA

Mini-application HTML de révision avant le quiz du Module 01.

Elle aide les candidats à revoir les points essentiels du cadrage, des preuves, du rôle de l'IA et de l'engagement candidat avant de passer au quiz officiel.

Cette version privilégie une interface plus large, plus respirante et plus robuste pour accompagner un usage en atelier, en autonomie ou en projection collective.

## Objectif

Cette page sert à :

- revoir les notions importantes du Module 01 ;
- vérifier sa préparation avant le quiz ;
- confirmer son ID-mail candidat localement ;
- générer un récapitulatif de révision ;
- suivre une progression visuelle ;
- préparer un mail de retour vers l'atelier ;
- rappeler les règles de prudence avant publication.

## Fichiers principaux

```txt
revision-module-01-avant-quiz/
  index.html
  README.md
  AGENT.md
  .gitignore
  assets/
    img/
      logo-LN-IA.png
```

## Utilisation locale

Ouvrir directement le fichier :

```txt
index.html
```

La page fonctionne sans serveur et sans base de données.

## Fonctionnalités

- Identification locale par ID-mail.
- Révision par séance.
- Synthèse essentielle du Module 01.
- Mini-checklist avant quiz.
- Auto-évaluation rapide.
- Tableau de progression avec indicateurs visuels.
- Récapitulatif prêt à copier.
- Bouton de copie du récapitulatif.
- Export CSV local pour préparer une ligne de suivi candidat.
- Lien `mailto:` pour préparer le message de retour.
- Rappel de confidentialité avant publication.

## Robustesse de l'application

L'application reste volontairement simple : un seul fichier HTML, sans serveur, sans base de données et sans dépendance externe.

Les renforcements ajoutés sont :

- largeur d'affichage augmentée pour améliorer la lecture ;
- sections plus espacées pour réduire la fatigue visuelle ;
- indicateurs de progression pour la checklist, l'auto-évaluation et l'ID-mail ;
- mise à jour automatique du récapitulatif ;
- bouton de copie avec solution de secours si l'API presse-papiers du navigateur est limitée ;
- bouton de téléchargement CSV pour transmettre une ligne de suivi au dossier privé ;
- rappel clair que la page ne valide pas officiellement un candidat.

Cette robustesse est pédagogique : elle aide l'utilisateur à mieux comprendre son état de préparation, sans collecter automatiquement ses données.

## Agent de suivi

Le fichier `AGENT.md` décrit le protocole de collecte et de suivi des réponses candidats.

Il précise :

- ce que l'agent peut aider à collecter ;
- ce qui doit rester privé ;
- comment préparer une ligne de suivi ;
- comment utiliser l'export CSV local ;
- pourquoi la page publique ne doit pas écrire directement dans un dossier local ;
- comment enregistrer les retours dans un dossier privé de suivi candidats.

## Confidentialité

Cette page ne vérifie pas automatiquement la liste privée des candidats.

Elle ne doit pas contenir :

- fichier Excel privé ;
- liste réelle des candidats ;
- téléphone ;
- mot de passe ;
- token ;
- données personnelles sensibles ;
- résultats individuels non publics.

La vérification officielle de l'ID-mail reste faite par l'atelier avec ses fichiers privés.

## Publication GitHub Pages

Si le dépôt est publié avec GitHub Pages, utiliser :

```txt
Settings > Pages > Deploy from a branch > main > /root
```

La page publique attendue sera basée sur :

```txt
index.html
```

## Workflow Git recommandé

```bash
git status
git add index.html README.md
git commit -m "Ajouter page de revision Module 01 LN-IA"
git push
```

Pour une amélioration de version :

```bash
git status
git add index.html README.md
git commit -m "Renforcer interface et documentation de revision"
git push
```

## Sauvegardes locales

Les fichiers de sauvegarde nommés `*.backup-*.html` sont ignorés par Git grâce au fichier `.gitignore`.

Ils peuvent rester localement sans être publiés sur GitHub.

## Statut

Version enrichie pour accompagner la révision du Module 01 avant quiz avec une interface plus lisible, un suivi de progression et un récapitulatif plus facile à réutiliser.
