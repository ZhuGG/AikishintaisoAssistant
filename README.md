# Nação Capoeira — Oullins / Pierre-Bénite

Maquette statique premium pour présentation commanditaire (section rattachée au PLO).

## Lancer le site

```bash
python3 -m http.server 4173
```

Puis ouvrir : `http://localhost:4173`.

## Structure

- `index.html` : accueil prioritaire
- `cours-tarifs.html`, `ecole.html`, `galerie.html`, `contact.html`
- `site.config.json` : source éditable (coordonnées, horaires, textes)
- `public/assets/styles.css` : direction artistique + animations
- `public/assets/app.js` : shell global (nav, footer, mobile, SEO)

## Assets (sans fichiers binaires dans la PR)

Arborescence conservée :

- `public/assets/brand/`
- `public/assets/images/`
- `public/assets/textures/`

Le rendu actuel repose sur des placeholders CSS (gradients + patterns), pour rester propre même sans médias réels.

## Fichiers réels à remplacer en production

Conserver exactement ces noms lors du remplacement :

1. `public/assets/brand/logo-main.png`
2. `public/assets/images/hero-roda.jpg`
3. `public/assets/images/gallery-01.jpg`
4. `public/assets/textures/texture-grain.png`
5. `public/assets/images/og-image.jpg`

## Notes

- Pas de dépendance principale à des images hotlinkées.
- Compatibilité `file://` conservée via fallback de config embarquée dans `app.js`.
