# 🎵 Blind Test — Ajout via GitHub Pages

## Structure des fichiers à pousser sur GitHub

```
ton-repo/
├── index.html              ← l'application
└── audio/                  ← dossier des nouveaux génériques
    ├── Adele_-_Skyfall_Official_Lyric_Video.mp3
    ├── American_Beauty_-_Thomas_Newman_from_the_plastic_bag_scene.mp3
    ├── BO_Film_Intouchables_Ludovico_Einaudi_Una_Mattina.mp3
    ├── Belle_Sebastien_-_Loiseau.mp3
    ├── Comptine_dUn_Autre_Ete-_Die_fabelhafte_Welt_der_Amelie_Piano_Large_Version_2010_mp4.mp3
    ├── Film_Musique_-_Halloween.mp3
    ├── Irene_Cara_-_Flashdance_What_A_Feeling_Official_Music_Video.mp3
    ├── Jean_De_Florette_-_Jean_Claude_Petit.mp3
    ├── Jurassic_Park_theme_song.mp3
    ├── Pirates_des_Caraibes_-_Musique_complete.mp3
    ├── SCHINDLERS_LIST_IN_THE_LARGEST_EUROPEAN_SYNAGOGUE_XAVER_VARNUS_CSONGOR_KOROSSY-KHAYLL.mp3
    ├── Saw_SoundTrack.mp3
    ├── Titanic-_Roses_theme.mp3
    └── Vladimir_Cosma_-_bande_originale_du_film_la_chevre.mp3
```

## Procédure (interface web GitHub)

1. **Crée un repo** : github.com/new → nom au choix (ex. `blind-test`) → Public → Create
2. **Upload index.html** : sur la page du repo → "Add file" → "Upload files" → glisse `index.html`
3. **Crée le dossier audio/** : encore "Add file" → "Create new file" → tape `audio/.gitkeep` → Commit
4. **Upload les 14 MP3** : ouvre le dossier `audio/` → "Add file" → "Upload files" → glisse les 14 fichiers d'un coup → Commit
5. **Active GitHub Pages** : Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `/ (root)` → Save
6. **URL d'accès** : `https://<ton-pseudo>.github.io/<nom-du-repo>/` (visible après ~1 min)

## Procédure (en ligne de commande, alternative)

```bash
git clone https://github.com/<ton-pseudo>/<repo>.git
cd <repo>
cp ~/Downloads/index.html .
mkdir -p audio
cp ~/Downloads/audio/*.mp3 audio/
git add .
git commit -m "Ajout 14 musiques de films"
git push
```

## Comportement de l'app

- Les **37 génériques précédents** (Code Quantum, Friends, Le Parrain…) sont toujours embarqués en base64 dans `index.html` → fonctionnent même offline
- Les **14 nouveaux** sont en URL relative `audio/...mp3` → chargés depuis le dossier `audio/` du repo
- Le mécanisme `getAudioSrc()` gère les deux cas automatiquement
- Pour ajouter de futurs lots : continue sur le même schéma → dépose les MP3 dans `audio/` et envoie-moi la liste, je mets à jour `index.html`
