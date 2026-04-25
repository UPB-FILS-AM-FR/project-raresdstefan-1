# Détecteur de Monoxyde de Carbone Bluetooth avec Arduino

| | |
|-|-|
|`Auteur` | [Delamarian Rares Stefan] |

## Description

Ce projet consiste à réaliser un dispositif capable de détecter le niveau de monoxyde de carbone (CO) dans l'environnement et de transmettre ces données en temps réel à un smartphone via une connexion Bluetooth. Le capteur MQ-7 surveille en permanence la qualité de l'air, et la carte Arduino traite les signaux analogiques reçus. Les informations sont ensuite envoyées sans fil par le module Bluetooth vers une application mobile (Terminal Bluetooth). C'est un projet pratique pour surveiller la sécurité de l'air ambiant sans nécessiter d'écran physique sur le dispositif.

## Motivation

Le monoxyde de carbone est un gaz incolore, inodore et très toxique, souvent appelé le "tueur silencieux". La principale motivation de ce projet est de créer un système de prévention accessible et à faible coût. De plus, d'un point de vue éducatif, ce projet permet d'explorer les bases de l'Internet des Objets (IoT) en apprenant à interfacer un capteur environnemental avec un microcontrôleur et à établir une communication sans fil avec un appareil mobile.

## Architecture

### Schéma fonctionnel (Block diagram)

![Block Diagram](schematics/block_diagram.png)

### Schéma électrique (Schematic)

![Schematic](schematics/kicad_schematic.png)

### Composants

| Composant | Utilisation | Prix estimé |
|--------|--------|-------|
| [Carte Arduino Uno](https://www.optimusdigital.ro/ro/placi-compatibile-arduino/12-placa-de-dezvoltare-uno-r3-compatibila-arduino-cu-cablu-usb.html) | Microcontrôleur (Cerveau du projet) | 45 RON |
| [Capteur MQ-7](https://www.optimusdigital.ro/ro/senzori-senzori-de-gaze/84-senzor-de-monoxid-de-carbon-mq-7.html) | Détection de gaz CO | 20 RON |
| [Module Bluetooth HC-05](https://www.optimusdigital.ro/ro/wireless-bluetooth/13-modul-bluetooth-hc-05.html) | Communication sans fil | 35 RON |
| [Breadboard](https://www.optimusdigital.ro/ro/prototipare-breadboard-uri/8-breadboard-830-points.html) | Platine de prototypage | 10 RON |
| [Fils de connexion](https://www.optimusdigital.ro/ro/fire-fire-mufate/884-set-fire-tata-tata-40p-10-cm.html) | Câblage des composants | 7 RON |
| [Résistances (1kΩ et 2kΩ)](https://www.optimusdigital.ro/ro/componente-electronice-rezistene/124-set-rezistente-cu-pelicula-metalica-14w-1-600-de-bucati.html) | Diviseur de tension pour le port RX du HC-05 | 15 RON (Set) |
| Connecteur Pile 9V | Alimentation portable | 5 RON |

### Bibliothèques

| Bibliothèque | Description | Utilisation |
|---------|-------------|-------|
| [SoftwareSerial.h](https://docs.arduino.cc/learn/built-in-libraries/software-serial) | Bibliothèque standard Arduino | Utilisée pour créer des ports série virtuels sur d'autres broches numériques afin de communiquer avec le module Bluetooth HC-05 sans bloquer le port série matériel (USB). |

## Journal de bord (Log)



## Liens de référence

[Tutoriel : Utiliser un module Bluetooth HC-05 avec Arduino](https://howtomechatronics.com/tutorials/arduino/arduino-and-hc-05-bluetooth-module-tutorial/)

[Guide : Interfacer le capteur de gaz MQ-7 avec Arduino](https://randomnerdtutorials.com/arduino-mq-3-gas-sensor/) *(Note : le principe est le même pour le MQ-7)*

[Application Serial Bluetooth Terminal (Google Play)](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal)
