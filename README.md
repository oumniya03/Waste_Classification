# ♻️ IoT Waste Classification with ESP32-CAM & Edge Impulse

[![Edge Impulse](https://img.shields.io/badge/Edge_Impulse-Machine_Learning-blue.svg)](https://edgeimpulse.com/)
[![ESP32-CAM](https://img.shields.io/badge/Hardware-ESP32--CAM-orange.svg)]()
[![Arduino](https://img.shields.io/badge/IDE-Arduino-00979D.svg)](https://www.arduino.cc/)

## 📝 Description du Projet
Ce projet propose une solution innovante et embarquée pour automatiser le tri sélectif des déchets grâce à l'Internet des Objets (IoT) et au Machine Learning. 
L'objectif est d'utiliser une **ESP32-CAM** pour capturer des images en temps réel et utiliser un modèle de Computer Vision entraîné via **Edge Impulse** pour classifier les déchets en trois catégories : **Carton, Verre et Papier**.

Selon le type de déchet détecté, une LED spécifique s'allume pour simuler le déclenchement d'un mécanisme de tri physique.

## 🎯 Objectifs
- **Réduire les erreurs** de tri manuel.
- **Accélérer le processus** de tri sélectif.
- Déployer un modèle d'IA directement sur un microcontrôleur à faible coût (Edge AI).

## 🛠️ Matériel Utilisé (Hardware)
- **ESP32-CAM** (Module caméra OV2640)
- Module **FTDI** (Convertisseur USB-Série pour la programmation)
- Breadboard et câbles de connexion (Jumpers)
- 3 LEDs (Rouge, Jaune, Verte)
- Résistances de protection
  
<img width="100" height="100" alt="Image1" src="https://github.com/user-attachments/assets/306d2627-f560-44d3-923c-34fc4169a4dd" />
<img width="100" height="100" alt="Image2" src="https://github.com/user-attachments/assets/56431547-ecb8-4fd9-8eed-e42e42bef024" />
<img width="100" height="100" alt="Image3" src="https://github.com/user-attachments/assets/0bb5718f-603e-48a9-aeb4-458d516592ff" />
<img width="100" height="100" alt="Image4" src="https://github.com/user-attachments/assets/3d694099-3c6d-42ec-8db3-30871d28036a" />
<img width="100" height="100" alt="Image5" src="https://github.com/user-attachments/assets/1b3aeec0-c186-4c35-ae84-32e38ad2e658" />
<img width="100" height="100" alt="Image6" src="https://github.com/user-attachments/assets/50f59034-4db3-4e5f-b100-2c0640d34417" />


## 💻 Logiciels & Technologies (Software)
- **Edge Impulse** (Pour l'acquisition des données, l'entraînement et le déploiement du modèle d'apprentissage par transfert)
- **Arduino IDE** (Pour la programmation de l'ESP32 et le contrôle logique des LEDs)

## 🏗️ Architecture du Système
1. **Acquisition (Data Collection) :** Collecte d'images (96x96 pixels) des 3 classes de déchets via la plateforme Edge Impulse.
2. **Traitement d'image (DSP) :** Conversion des images en niveaux de gris (Grayscale) pour alléger le traitement.
3. **Apprentissage (Transfer Learning) :** Entraînement d'un modèle de classification visuelle.
4. **Déploiement (Edge AI) :** Exportation du modèle sous forme de librairie C++ Arduino.
5. **Exécution (Inférence) :** L'ESP32-CAM capture l'image, exécute le modèle localement et allume la LED correspondante au déchet :
   - 🔴 **LED Rouge :** Papier
   - 🟡 **LED Jaune :** Carton
   - 🟢 **LED Verte :** Verre
     
<img width="300" height="300" alt="Image7" src="https://github.com/user-attachments/assets/584f90b6-6ad5-427a-8c8e-9c362739a1cd" />

## 📸 Démonstration
*(Ajoute ici une image de ton câblage et un lien vers la vidéo de démo)*

> **[Lien vers la vidéo de démonstration du tri automatique]** (Remplacer par le lien YouTube de ta vidéo)

## 🚀 Installation & Utilisation

1. Clonez ce dépôt :
   ```bash
   git clone [https://github.com/votre-pseudo/IoT-Waste-Classification.git](https://github.com/votre-pseudo/IoT-Waste-Classification.git)
    ```
2. Ouvrez le fichier .ino avec Arduino IDE.
3. Assurez-vous d'avoir installé le support des cartes ESP32 dans Arduino IDE.
4. Installez la librairie générée par Edge Impulse (fournie sous forme de fichier .zip).
5. Sélectionnez le bon modèle de caméra (ex: CAMERA_MODEL_AI_THINKER) dans le code.
6. Branchez l'ESP32-CAM via le module FTDI, compilez et téléversez le code.
7. Ouvrez le moniteur série (baud rate : 115200) pour voir les prédictions en temps réel.

##🔮 Perspectives d'évolution

1. Amélioration du Dataset : Ajouter de nouvelles classes (Plastique, Métal, Déchets organiques).
2. Actionneurs physiques : Remplacer les LEDs par des servomoteurs ou un bras robotique pour trier réellement les déchets.
3. Connectivité Cloud : Remonter les statistiques de tri vers un Dashboard (via MQTT ou HTTP).

## 👥 Auteurs
Oumniya Moutaouakil

Encadré par : Pr. ANAS BOUAYAD
