# Joartoxx news

Le journal (très sérieux) de notre village Minecraft.

Site statique : uniquement du HTML et du CSS, aucune dépendance, aucun build.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Page d'accueil, liste les articles sous forme de cartes |
| `about.html` | Page « À propos » |
| `article-1.html` … `article-3.html` | Un fichier par article |
| `style.css` | Feuille de style unique pour tout le site |
| `favicon.svg` | Icône (bloc d'herbe) |

## Ajouter un article

1. Duplique un `article-N.html` existant et renomme-le.
2. Change le `<title>`, la balise `<meta name="description">` et le `<h1>`.
3. Mets à jour la ligne `.meta` (date · auteur · catégorie) et le texte.
4. Ajoute la carte correspondante dans `index.html`, entre les deux marqueurs, et
   garde l'ordre décroissant par date.

## Marqueurs du générateur

`index.html` contient deux commentaires que le générateur C++ utilise comme
bornes d'insertion. **Ne les supprime pas, ne les déplace pas :**

```html
<!-- DEBUT-ARTICLES (ne pas supprimer cette ligne : le générateur C++ ajoute les cartes ici) -->
...
<!-- FIN-ARTICLES -->
```

## Conventions

- Dates en minuscules : `8 octobre 2026` (usage français).
- Guillemets français : `« … »`.
- Encodage UTF-8, fins de ligne LF.
- Couleurs via les variables CSS de `:root` dans `style.css`.

## Publier

Hébergeable tel quel sur GitHub Pages (branche `main`, racine du dépôt).