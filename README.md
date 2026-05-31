# 🎵 Blind Test

Application web autonome de blind test (single-file HTML + dossier audio externe).

## Structure

```
blind-test/
├── index.html       — l'application complète (37 génériques embarqués en base64)
└── audio/           — 60 musiques additionnelles servies en URL relative
```

## Déploiement GitHub Pages

1. Crée un repo public sur https://github.com/new
2. Upload `index.html` à la racine et le dossier `audio/` complet
3. Settings → Pages → branch `main` / `(root)` → Save
4. URL : `https://<ton-pseudo>.github.io/<nom-repo>/`

## En ligne de commande

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<TON-PSEUDO>/<REPO>.git
git push -u origin main
```

Puis Settings → Pages comme ci-dessus.
