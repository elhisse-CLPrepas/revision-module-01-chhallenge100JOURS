# Révision Module 01 - Challenge 100 jours LN-IA

Mini-application HTML de révision avant le quiz du Module 01.

Elle aide les candidats à revoir les points essentiels du cadrage, des preuves, du rôle de l'IA et de l'engagement candidat avant de passer au quiz officiel.

## Objectif

Cette page sert à :

- revoir les notions importantes du Module 01 ;
- vérifier sa préparation avant le quiz ;
- confirmer son ID-mail candidat localement ;
- générer un récapitulatif de révision ;
- préparer un mail de retour vers l'atelier ;
- rappeler les règles de prudence avant publication.

## Fichiers principaux

```txt
revision-module-01-avant-quiz/
  index.html
  README.md
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
- Récapitulatif prêt à copier.
- Lien `mailto:` pour préparer le message de retour.
- Rappel de confidentialité avant publication.

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

## Sauvegardes locales

Les fichiers de sauvegarde nommés `*.backup-*.html` sont ignorés par Git grâce au fichier `.gitignore`.

Ils peuvent rester localement sans être publiés sur GitHub.

## Statut

Version initiale publiée pour accompagner la révision du Module 01 avant quiz.
