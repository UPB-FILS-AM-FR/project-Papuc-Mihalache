<h1 align="center">🔥 IgnisBot – Robot autonome de détection et d’extinction de feu 🌊</h1>

<p align="center">
  <img src="images/IgnisBOT_logo.png" width="180" alt="Logo d’IgnisBot" />
</p>

<p align="center">
  <b>IgnisBot est un robot autonome et intelligent, conçu à partir d'une carte Arduino Uno, capable de détecter la présence de flammes grâce à des capteurs infrarouges, et de réagir instantanément en déployant un système de pulvérisation d’eau pour les éteindre. Il combine des capteurs de feu, un servo-moteur dirigeant le bras de pulvérisation et une logique embarquée pour assurer une intervention rapide, précise et sécurisée face à un départ de feu. Ce robot a été pensé comme une solution pédagogique, innovante et pratique pour sensibiliser à la sécurité incendie tout en explorant les possibilités de la robotique embarquée. 🤖</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/état-build_passing-brightgreen" />
  <img src="https://img.shields.io/badge/licence-MIT-blue" />
  <img src="https://img.shields.io/badge/Arduino-compatible-orange" />
</p>

---

## 📋 Table des matières

- [Fonctionnalités](#fonctionnalites)
- [Demonstration](#demonstration)
- [Materiel requis](#materiel-requis)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Structure du projet](#structure-du-projet)
- [Contribuer](#contribuer)
- [Licence](#licence)

---

## ✅ Fonctionnalités

- 🔍 **Détection en temps réel des flammes** via capteurs infrarouges  
- 💧 **Pulvérisation automatique d’eau** en cas d’incendie  
- 🔔 **Alertes sonores** grâce à un buzzer  
- 🌡️ **Surveillance de la température et de l’humidité**  
- 🛡️ Design sécurisé, piloté par une carte Arduino Uno  

---

## 🧰 Matériel requis

## 🧾 Composants électroniques

| Produit                                              | Quantité | Prix unitaire (lei) | Prix total (lei) | Utilisation |
|------------------------------------------------------|----------|----------------------|------------------|-------------|
| Résistance 0,25W 1kΩ                                 | 5        | 0,10                 | 0,50             | Protection et limitation de courant pour signaux ou LED |
| Module pilote de moteur double L298N (rouge)         | 1        | 10,99                | 10,99            | Contrôle de deux moteurs DC via Arduino Uno |
| Breadboard (400 points)                              | 1        | 4,56                 | 4,56             | Prototypage rapide des circuits sans soudure |
| Kit de fils pour breadboard                          | 1        | 7,99                 | 7,99             | Connexions entre composants sur la breadboard |
| Fils dupont femelle-mâle (40 pièces, 20 cm)          | 1        | 7,99                 | 7,99             | Connexions entre capteurs, modules et microcontrôleur |
| Support pour 2 piles 18650                           | 1        | 3,99                 | 3,99             | Alimentation portable du robot |
| Servomoteur MG90S                                    | 1        | 19,33                | 19,33            | Orientation de la buse/pulvérisateur pour extinction |
| Diode 1N4148-NXP                                     | 2        | 0,49                 | 0,98             | Protection contre les surtensions (roues libres) |
| Moteur avec réducteur et roue                        | 4        | 14,99                | 59,96            | Déplacement du robot |
| Interrupteur marche/arrêt avec LED                   | 1        | 1,99                 | 1,99             | Allumage/arrêt général du robot avec indicateur |
| Câble USB AM-BM 50 cm pour Arduino MEGA/UNO          | 1        | 4,38                 | 4,38             | Programmation et alimentation via PC |
| Capteur de flamme (analogique/numérique, 4 broches)  | 3        | 5,00                 | 15,00            | Détection des flammes (feu) dans l’environnement |
| Tuyau pour pompe à eau 6x8 mm (1 mètre)              | 1        | 5,26                 | 5,26             | Acheminement de l’eau vers la sortie du système |
| Pompe à eau/air R385 (6–12V, à diaphragme)           | 1        | 23,47                | 23,47            | Extinction de feu via jet d’eau ou air |
| Fils dupont femelle-femelle 20 cm                    | 1        | 7,41                 | 7,41             | Connexion entre modules femelle (ex. capteur-capteur) |
| Fils dupont mâle-mâle 30 cm                          | 1        | 6,67                 | 6,67             | Connexions longues pour signaux ou alimentation |
| Kit de condensateurs céramiques (300 pièces)         | 1        | 10,08                | 10,08            | Filtrage des parasites et stabilisation des signaux |
| Pile 18650 (individuelle)                            | 2        | 18,00                | 36,00            | Source principale d’énergie (batteries rechargeables) |
| Transisteur                                          | 1        | 12,00                | 12,00            | Interrupteur contrôlé électroniquement|

---

