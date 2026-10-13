# Site web snAIl

Site bilingue (français par défaut, anglais) construit avec [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) et le plugin [mkdocs-static-i18n](https://github.com/ultrabug/mkdocs-static-i18n).

## Prévisualiser en local

```bash
cd website
python3 -m venv .venv            # une seule fois
.venv/bin/pip install -r requirements.txt
.venv/bin/mkdocs serve           # puis ouvrir http://127.0.0.1:8000
```

## Ajouter une leçon

1. Copier `docs/lecons/modele.md` vers `docs/lecons/<nom-de-la-lecon>.md` (version française).
2. Créer la version anglaise au même endroit avec le suffixe `.en.md` : `<nom-de-la-lecon>.en.md`.
3. Ajouter la page dans la section `nav:` de `mkdocs.yml` (et sa traduction de titre dans `nav_translations` si besoin).

Règle générale du bilinguisme : `page.md` = français (langue par défaut), `page.en.md` = anglais. Si la version anglaise manque, le site affiche la française.

## Mettre en ligne (GitHub Pages, gratuit)

1. Créer un dépôt GitHub (par exemple `snail-site`) et pousser le contenu de ce dossier `website/` à la racine du dépôt.
2. Le workflow `.github/workflows/deploy.yml` construit et publie le site automatiquement à chaque push sur `main` (branche `gh-pages`).
3. Dans les réglages GitHub du dépôt : **Settings → Pages → Branch : `gh-pages`**.
4. Mettre à jour `site_url:` dans `mkdocs.yml` avec l'adresse réelle.

## Nom de domaine (optionnel, ~12 €/an)

Acheter un domaine (OVH, Gandi…), puis dans **Settings → Pages → Custom domain** indiquer le domaine et créer l'enregistrement DNS `CNAME` vers `<votre-compte>.github.io`. HTTPS est fourni automatiquement.
