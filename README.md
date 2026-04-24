

Application MATLAB créée avec App Designer. Elle permet de charger une image et d'appliquer différents filtres :



## Filtres disponibles
 

 
| # | Filtre | Effet | Formule |
|---|--------|-------|---------|
| 1 | Correction gamma | Rend l'image plus claire. Les zones sombres deviennent visibles. | \(I_{out} = I_{in}^{\gamma}\) |
| 2 | Transformation exponentielle | Augmente les petites valeurs. Les zones sombres deviennent claires. | \(I_{out} = \frac{e^{I_{in}} - 1}{\max(e^{I_{in}} - 1)}\) |
| 3 | Transformation logarithmique | Réduit les grandes valeurs. Améliore le contraste dans le noir. | \(I_{out} = \frac{\log(1 + I_{in})}{\max(\log(1 + I_{in}))}\) |
| 4 | Étirement linéaire | Étale toutes les valeurs entre 0 et 255. Améliore le contraste. | \(I_{out} = 255 \times \frac{I_{in} - I_{min}}{I_{max} - I_{min}}\) |
| 5 | Égalisation d'histogramme | Distribue les pixels sur toutes les couleurs. Contraste maximum. | \(I_{out} = \text{CDF}(I_{in}) \times 255\) |
| 6 | Filtre Sobel | Trouve les contours de l'image. | \(\text{magnitude} = \sqrt{G_x^2 + G_y^2}\) |
| 7 | Méthode OTSU | Transforme l'image en noir et blanc. | \(I_{out} = \begin{cases} 255 & \text{si } I_{in} \geq \text{seuil} \\ 0 & \text{sinon} \end{cases}\) |
 
---

## Prérequis pour l'installation

Avant de lancer l'application, vous devez installer **MATLAB Runtime R2024a**.

### Option 1 — Téléchargement automatique
Utilisez l'installateur dans le dossier `The App/for_redistribution` :
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
git clone https://github.com/ABDELHAKIM-IZIKI/Traitement-d-images-sous-MATLAB.git
```

2. Allez dans le dossier `The App/for_redistribution_files_only` :
```
MyFilter.exe
```

3. Lancez `MyFilter.exe`.

---

## Structure du The App 

```
The App/
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
