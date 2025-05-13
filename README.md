<h1 align="center">🔥 IgnisBot – Robot autonome de détection et d’extinction de feu 🌊</h1>

### Auteur
PAPUC Mihalache


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

<p align="center">
  <b>Motivation

L’idée d’IgnisBot est née d’une double volonté: sensibiliser à la prévention des incendies et promouvoir l’apprentissage de la robotique embarquée chez les jeunes et les passionnés de technologie. Chaque année, des milliers d’incendies domestiques se déclenchent et pourraient être évités ou circonscrits plus rapidement avec une détection précoce et une intervention automatisée. En ce sens, IgnisBot agit comme une maquette intelligente illustrant comment la technologie peut répondre à des enjeux très concrets.

Sur le plan éducatif, le projet offre un excellent cadre pour combiner plusieurs disciplines: programmation Arduino, électronique, contrôle moteur, capteurs, automatisation, conception 3D, et même durabilité énergétique. Ce robot est aussi un tremplin pour encourager la créativité dans des projets STEM (Science, Technology, Engineering, Mathematics) et faire naître des vocations techniques.

Enfin, la motivation profonde est de rendre visible et accessible la puissance de l’intelligence embarquée appliquée à un problème concret et universel : la lutte contre les incendies.</b>
</p>

<h3>Architecture</h3>
<p>L'architecture d'IgnisBot repose sur une structure modulaire combinant détection, décision et action, organisée autour de la carte microcontrôleur Arduino Uno. Voici une vue d'ensemble détaillée :</p>

<ul>
  <li><strong>Unité centrale de contrôle (Arduino Uno)</strong>
    <ul>
      <li>Reçoit les données des capteurs (flammes, température, humidité)</li>
      <li>Traite les informations via un algorithme de détection</li>
      <li>Déclenche les actions appropriées (alerte sonore, activation du servo et de la pompe)</li>
    </ul>
  </li>

  <li><strong>Système de détection</strong>
    <ul>
      <li>3 capteurs de flamme répartis sur la face avant du robot pour une couverture directionnelle</li>
      <li>Capteur de température et humidité (DHT11 ou DHT22 selon la version)</li>
    </ul>
  </li>

  <li><strong>Système d'action</strong>
    <ul>
      <li>Servomoteur MG90S pour orienter la buse de pulvérisation</li>
      <li>Pomme à eau R385, activée via un transistor NPN, pour envoyer un jet d'eau ciblé</li>
      <li>Buzzer pour alerter lors de la détection d'un incendie</li>
    </ul>
  </li>

  <li><strong>Système de déplacement</strong>
    <ul>
      <li>4 moteurs à courant continu avec réduction, contrôlés par un pont en H (L298N)</li>
      <li>Contrôle différentiel gauche/droite pour le guidage autonome</li>
    </ul>
  </li>

  <li><strong>Alimentation</strong>
    <ul>
      <li>Deux piles 18650 fournissant l'énergie principale</li>
      <li>Régulation de tension possible via des condensateurs et diodes de protection</li>
    </ul>
  </li>

  <li><strong>Système de prototypage et câblage</strong>
    <ul>
      <li>Utilisation d'une breadboard pour faciliter les essais et les ajustements</li>
      <li>Fils Dupont (mâle-mâle, femelle-femelle, femelle-mâle) pour les connexions internes</li>
    </ul>
  </li>
</ul>

<p>Cette architecture permet une détection en temps réel, une réaction localisée, et une mobilité autonome, tout en gardant une structure pédagogique facilement compréhensible pour les débutants en électronique ou en robotique.</p>

<h3>Diagramme fonctionnel (Block Diagram)</h3>
<p>Ce diagramme montre les interactions principales entre les composants du robot :</p>

<p align="center">
  <img src="images/block_diagram_ignisbot.png" alt="Diagramme fonctionnel d’IgnisBot" width="80%">
</p>

<ul>
  <li><strong>Arduino Uno</strong> – centre de traitement et de commande</li>
  <li><strong>Capteurs de flamme</strong> – entrées de détection</li>
  <li><strong>Servo MG90S</strong> – oriente la buse d’eau</li>
  <li><strong>Pont en H L298N</strong> – contrôle des 4 moteurs DC</li>
  <li><strong>Pump R385</strong> – déclenchée via transistor NPN</li>
</ul>

<h3>📘 Schéma électronique (Schematic)</h3>
<p>Le schéma suivant illustre les connexions électriques du projet :</p>

<p align="center">
  <img src="images/schematic_ignisbot.png" alt="Schéma électronique IgnisBot" width="80%">
</p>

<p>Les connexions incluent :</p>
<ul>
  <li>Capteurs de flamme</li>
  <li>Servo MG90S</li>
  <li>Pompe 6-12V</li>
  <li>L298N relié aux moteurs et à Arduino </li>
</ul>

<p>Assurez-vous d’utiliser une alimentation séparée pour les moteurs/pompe pour éviter des redémarrages de la carte Arduino causés par une chute de tension.</p>



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
<h3>🗓️ Journal de bord (Logs)</h3>

<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>Semaine</th>
      <th>Période</th>
      <th>Activités réalisées</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Semaine 1</td>
      <td>29 avril – 5 mai</td>
      <td>
        <ul>
          <li>Commande des premiers composants</li>
          <li>Étude des composants électroniques choisis</li>
          <li>Analyse des connexions entre capteurs, moteurs, servomoteurs et alimentation</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Semaine 2</td>
      <td>6 – 12 mai</td>
      <td>
        <ul>
          <li>Montage matériel (hardware) de la première partie :</li>
          <ul>
            <li>Connexion des capteurs de flammes</li>
            <li>Installation des moteurs DC avec L298N</li>
            <li>Branchement et test du servomoteur MG90S</li>
          </ul>
          <li>Commande des composants restants pour la pompe à eau</li>
          <li>Début du codage pour les capteurs, moteurs et servo</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Semaine 3</td>
      <td>13 – 19 mai</td>
      <td>—</td>
    </tr>
    <tr>
      <td>Semaine 4</td>
      <td>20 – 26 mai</td>
      <td>—</td>
    </tr>
  </tbody>
</table>


<h3>🔗 Liens de référence</h3>

<ul>
  <li>
    <a href="https://lastminuteengineers.com/l298n-dc-stepper-driver-arduino-tutorial/" target="_blank">
      Tutoriel complet sur le module L298N (contrôle moteurs)
    </a>
  </li>
  <li>
    <a href="https://components101.com/sensors/flame-sensor-module" target="_blank">
      Informations techniques sur le capteur de flamme KY-026
    </a>
  </li>
  <li>
    <a href="https://docs.arduino.cc/tutorials/components/servo-motors" target="_blank">
      Guide Arduino officiel sur les servomoteurs
    </a>
  </li>
  <li>
    <a href="https://randomnerdtutorials.com/esp32-dht11-dht22-temperature-humidity-sensor/" target="_blank">
      Tutoriel DHT11/DHT22 avec microcontrôleur
    </a>
  </li>
  <li>
    <a href="https://www.hackster.io/search?i=projects&q=fire%20fighting%20robot" target="_blank">
      Projets similaires de robots pompiers sur Hackster.io
    </a>
  </li>
  <li>
    <a href="https://wokwi.com/" target="_blank">
      Wokwi – simulateur en ligne pour projets Arduino
    </a>
  </li>
</ul>


---

