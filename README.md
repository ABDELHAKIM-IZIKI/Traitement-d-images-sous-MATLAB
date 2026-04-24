# matlab-outil-amelioration-image

Application MATLAB créée avec App Designer. Elle permet de charger une image et d'appliquer différents filtres : gamma correction, logarithmique, exponentielle, Sobel et OTSU. L'application affiche l'histogramme et les statistiques de l'image transformée. Elle est déployée comme programme indépendant avec MATLAB Compiler.

---

## Filtres disponibles

| Filtre | Description |
|--------|-------------|
| Gamma correction | Éclaircit l'image avec γ = 0.5 |
| Transformation exponentielle | Amplifie les intensités faibles |
| Transformation logarithmique | Compresse les hautes intensités |
| Étirement linéaire | Améliore le contraste global |
| Égalisation d'histogramme | Distribue uniformément les pixels |
| Filtre Sobel | Détecte les contours |
| Méthode OTSU | Binarise l'image (noir et blanc) |

---

## Prérequis pour l'installation

Avant de lancer l'application, vous devez installer **MATLAB Runtime R2024a**.

### Option 1 — Téléchargement automatique
Utilisez l'installateur dans le dossier `for_redistribution` :
```
MyAppInstaller_web.exe
```
Il télécharge et installe le Runtime automatiquement.

### Option 2 — Téléchargement manuel
Téléchargez MATLAB Runtime R2024a depuis le site MathWorks :

👉 https://www.mathworks.com/products/compiler/mcr/index.html

> **Note :** Vous avez besoin des droits administrateur pour installer MATLAB Runtime.

---

## Installation et lancement

1. Clonez ce repository :
```bash
git clone https://github.com/votre-username/matlab-outil-amelioration-image.git
```

2. Allez dans le dossier `for_redistribution_files_only` :
```
MyFilter.exe
```

3. Lancez `MyFilter.exe`.

---

## Structure du repository

```
matlab-outil-amelioration-image/
│
├── for_redistribution/
│   └── MyAppInstaller_web.exe    # Installateur avec Runtime intégré
│
└── for_redistribution_files_only/
    ├── MyFilter.exe              # Application standalone
    ├── splash.png                # Écran de démarrage
    └── readme.txt                # Instructions en anglais
```

---

## Démonstration

![Demo - Filtre Sobel](demo.png)
*Exemple : application du Filtre Sobel sur une image d'éléphant — détection des contours avec histogramme et statistiques.*

---

## Utilisation

1. Lancez l'application `MyFilter.exe`
2. Cliquez sur **l'image originale** pour charger une image (`.jpg`, `.png`, `.jpeg`)
3. Sélectionnez un filtre dans le menu déroulant
4. Entrez une valeur de seuil si nécessaire (pour OTSU)
5. Cliquez sur **Appliquer**
6. Consultez l'histogramme et les statistiques

---

## Technologies utilisées

- **MATLAB R2024a**
- **MATLAB App Designer**
- **MATLAB Compiler** (déploiement standalone)

---

## Auteur

Développé dans le cadre d'un projet universitaire de traitement d'image.
