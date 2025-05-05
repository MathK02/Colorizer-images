
# 🖌️ Colorisation d’Images par Deep Learning

Ce projet repose sur un réseau de neurones convolutifs (CNN) pour coloriser automatiquement des images en niveaux de gris. Il est développé avec PyTorch et entraîné sur un dataset personnalisé d’images RGB, converties dans l’espace de couleur LAB.

## 📁 Dataset

Le dataset utilisé est un ensemble d’images RGB compressé dans un fichier `.zip`.

📥 **Lien de téléchargement du dataset** : [Télécharger le dataset](https://example.com/dataset.zip)  
*(Remplace ce lien par celui vers ton propre hébergement, comme Google Drive ou HuggingFace)*

Une fois uploadé dans l'environnement (Google Colab ou local), il est automatiquement extrait dans un dossier `dataset/`.

## 🏗️ Architecture du modèle

Le modèle utilise un backbone pré-entraîné de type `ResNet` provenant de `torchvision.models`, adapté pour une tâche de type image-à-image. L’objectif est de prédire les canaux chromatiques a et b à partir du canal de luminance L dans l’espace LAB.

## 📈 Performance de l'entraînement

Deux métriques principales sont suivies au cours de l’apprentissage :

- La **fonction de perte (loss)**, permettant d’évaluer la cohérence de la prédiction par rapport à l’image originale.
- Le **gain**, correspondant à une mesure qualitative de l’amélioration de la colorisation.

<p align="center">
  <img src="images_courbe/loss_curve.png" alt="Courbe de perte" width="400"/>
  <img src="images_courbe/gain_curve.png" alt="Courbe de gain" width="400"/>
</p>

## 🎨 Résultats visuels

Chaque image ci-dessous contient, de gauche à droite :  
**image en niveaux de gris**, **image colorisée (prédite)**, **vérité terrain (RGB)**.

| Exemples de colorisation |
|---------------------------|
| ![](images_exemples/exemple1.png) |
| ![](images_exemples/exemple2.png) |
| ![](images_exemples/exemple3.png) |

## 🚀 Exécution du projet

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/ton-pseudo/image-colorization.git
   cd image-colorization
