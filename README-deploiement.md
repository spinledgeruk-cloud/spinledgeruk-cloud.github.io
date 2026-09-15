# Mettre le site en ligne gratuitement (30 minutes, sans terminal)

Le site utilise Jekyll, que GitHub Pages construit tout seul. Tu n'installes rien : tout se fait dans le navigateur.

## 1. Compte GitHub (5 min)
1. Crée un compte sur github.com avec ton adresse e-mail.
2. Vérifie l'e-mail.

## 2. Créer le dépôt (2 min)
1. Bouton « New repository ».
2. Nom : exactement `TONPSEUDO.github.io` (remplace TONPSEUDO par ton nom d'utilisateur GitHub). Ce nom précis donne l'adresse `https://TONPSEUDO.github.io`.
3. Public. Ne coche rien d'autre. « Create repository ».

## 3. Envoyer les fichiers (5 min)
1. Dézippe `site.zip` sur ton ordinateur.
2. Dans le dépôt vide, lien « uploading an existing file ».
3. Glisse **tout le contenu** du dossier `site` (les dossiers `_layouts`, `_reviews`, `_guides`, `assets` et les fichiers `.md`, `_config.yml`, `robots.txt`). Pas le dossier `site` lui-même.
4. En bas : « Commit changes ».

Si le glisser-déposer refuse les dossiers, fais-le dossier par dossier via « Add file → Upload files » en tapant le chemin (`_layouts/default.html`) dans le nom du fichier.

## 4. Activer Pages (1 min)
Settings → Pages → Source : « Deploy from a branch » → Branch : `main`, dossier `/ (root)` → Save.
Deux minutes plus tard, `https://TONPSEUDO.github.io` répond.

## 5. Personnaliser (5 min)
Ouvre `_config.yml` dans GitHub (icône crayon), modifie les 6 premières lignes :
- `title` : le nom du site
- `url` : `https://TONPSEUDO.github.io`
- `author_name`, `contact_email` : une adresse dédiée au site (Gmail gratuit suffit)
Commit. Le site se reconstruit seul.

## 6. Vérifier (5 min)
- La page d'accueil affiche le bandeau 18+ en haut et le bloc « Play responsibly » en bas.
- `/about/`, `/contact/`, `/privacy/`, `/affiliate-disclosure/`, `/responsible-gambling/` s'ouvrent.
- `/sitemap.xml` et `/robots.txt` existent.
- Test mobile : pagespeed.web.dev, score > 90 attendu (site statique sans JavaScript).

## 7. Google Search Console (5 min)
1. search.google.com/search-console → « Ajouter une propriété » → type « Préfixe d'URL » → `https://TONPSEUDO.github.io`.
2. Méthode de vérification « Balise HTML » : copie le code `content="..."` et ajoute dans `_config.yml` la ligne `google_site_verification: "LE_CODE"` (jekyll-seo-tag l'insère automatiquement).
3. Une fois vérifié, « Sitemaps » → envoie `sitemap.xml`.

## Écrire un avis
1. Dossier `_reviews` → « Add file → Create new file » → nom `leovegas.md` (le nom devient l'adresse `/reviews/leovegas/`).
2. Copie le contenu de `example-casino.md`, remplis l'en-tête (entre les `---`) et les sections.
3. Laisse `published: false` tant que la relecture n'est pas faite ; passe à `true` pour publier.

Même chose pour les guides dans `_guides`.

## Quand acheter un domaine
Quand tu passes en phase 3 (candidatures), un domaine à ≈ 10 €/an remplace `TONPSEUDO.github.io` : Settings → Pages → « Custom domain ». Les anciennes adresses redirigent automatiquement, rien à réécrire.
