# Sources de Méandres

Ce dossier contient tout ce qu'il faut pour retravailler la police plus tard.

| Fichier | Contenu |
|---|---|
| `Meandres_glyphes.svg` | Feuille de glyphes dessinés, telle que fournie par l'autrice (retravaillée dans un outil de dessin). |
| `Meandres_glyphes_avec_noms.svg` | Version générée depuis la police : un groupe par glyphe, nommé comme dans la police, avec repères de ligne de base et de hauteur des lettres. Utile pour reconstruire la police. |
| `glyphes.csv` | Liste des glyphes : nom, code Unicode, caractère, chasse (advance) et marges gauche/droite. |
| `scripts.zip` | Scripts Python utilisés pour construire la version actuelle (voir ci-dessous). À dézipper pour les utiliser. |

## Version de référence

Le fichier `fonts/Meandres-Regular.ttf` est la version de référence. Pour de futures modifications, repartez de ce fichier : il contient déjà les chiffres, les accents, les symboles, l'espacement et le crénage.

## Scripts (dans `scripts.zip`)

Ils sont fournis à titre de documentation et de point de départ. Ils ont été écrits pour un environnement précis : les chemins de fichiers y sont à adapter. Il faut Python 3 avec `fonttools`, `scipy`, `potracer`, `skia-pathops`, `numpy`, `Pillow`.

1. `01_chiffres_et_lettres_composees.py` : ajoute les chiffres (depuis le SVG) et construit les lettres et symboles assemblés à partir de tes lettres (`œ ï û ü Ç …`).
2. `02_espacement_et_crenage.py` (+ `lib.py`) : recalcule les marges de chaque lettre selon sa forme et crée le crénage par paires.
3. `03_symboles_depuis_image.py` : vectorise les symboles dessinés sur la feuille image et les ajoute à la police.

## Licence

SIL Open Font License 1.1 (voir `OFL.txt` à la racine du dépôt).
