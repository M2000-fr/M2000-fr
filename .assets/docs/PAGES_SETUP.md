# 🌸 Mise en ligne du portail GitHub Pages

Le portail est conçu pour le dépôt public **`M2000-fr/M2000-fr`**. Son README est affiché sur le profil GitHub, tandis que `index.html` fournit les **quatre zones réellement cliquables dans une seule image**.

## Installer

1. Décompresser le ZIP à la **racine** du dépôt `M2000-fr/M2000-fr`, branche `main`.
2. Les fichiers `README.fr.md`, `README.en.md`, `README.jp.md` et `mechard_42.png` déjà présents **ne sont pas modifiés**.
3. Commiter `README.md`, `index.html`, `.nojekyll`, `.assets/images/profile_portal_japan_geek.png` et ce guide.
4. Dans **Settings → Pages → Build and deployment**, choisir **Deploy from a branch**, `main`, `/(root)` puis **Save**.
5. Après activation, l'adresse attendue est **https://m2000-fr.github.io/M2000-fr/**. Vérifier l'URL affichée dans les réglages GitHub, celle-ci n'a pas été testée en production.

```bash
git add README.md index.html .nojekyll .assets/images/profile_portal_japan_geek.png .assets/docs/PAGES_SETUP.md
git diff --cached --check
git commit -m "docs: add interactive Japan-geek profile portal"
git push origin main
```

## Liens

- 🇫🇷 Français : [README.fr.md](../../README.fr.md)
- 🇬🇧 English : [README.en.md](../../README.en.md)
- 🇯🇵 日本語 : [README.jp.md](../../README.jp.md)
- 🎓 42 Paris : https://github.com/Mechard-Organization/42_Paris

Le site Pages utilise des **URL GitHub absolues** pour ouvrir les README avec le rendu Markdown GitHub ; les liens relatifs `./README.*.md` depuis Pages pointeraient vers des fichiers Markdown servis par Pages et non vers leur rendu GitHub.

## Pourquoi ne pas mettre les zones cliquables directement dans le README ?

GitHub filtre les éléments HTML/CSS nécessaires aux *hotspots* arbitraires. Un `<a>` autour d'un `<img>` rend l'image entière cliquable, mais ne peut pas associer plusieurs liens à différentes zones.

Cette livraison garde une image unique dans le README, associée au portail, et fournit des liens directs sous l'image pour la navigation sans passer par Pages.

## Modification future

- `.assets/images/profile_portal_japan_geek.png` : visuel statique complet (1916 × 821), **ne pas découper**.
- `index.html` : positions des quatre hotspots (règles `.hotspot--fr`, `--en`, `--ja`, `--school`) et leurs URLs.
- `README.md` : accueil GitHub du profil et liens directs.

L'image d'origine utilisée comme inspiration / fond provient des bannières de la DA Others validée précédemment.
