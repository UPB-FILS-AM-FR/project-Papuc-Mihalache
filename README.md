<h1 align="center"> IgnisBot <br>
  Robot autonome de détection et d’extinction de feu</h1>

<p align="center">
  <b>Auteur : PAPUC Mihalache</b><br>
  Étudiant en 2<sup>e</sup> année – Faculté d’Ingénierie en Langues Étrangères<br>
  Université Nationale de Science et Technologie POLITEHNICA de Bucarest<br><br>
</p>

<h1>
  DESCRIPTION
</h1>

<p>
  <b>IgnisBot est un robot mobile autonome conçu autour d’une carte microcontrôleur Arduino Uno. Il est spécifiquement développé pour la détection et l’extinction de foyers d’incendie localisés dans son champ d’action frontal.Le système repose sur trois capteurs de flamme disposés à l’avant du châssis, permettant une surveillance angulaire étendue. Lorsqu’un départ de feu est détecté, l’Arduino active automatiquement une pompe électrique, montée sur un bras motorisé (servo), capable de réaliser un balayage de 180° pour pulvériser de l’eau avec précision dans la zone ciblée. L’ensemble des composants (capteurs, actionneurs, pompe, relais) est intégré sur un châssis robotisé à 4 roues motrices, piloté via un module L298N. Cette configuration permet au robot de se déplacer de manière autonome vers la source de l’incendie, assurant une intervention mobile, rapide et localisée.</b>
</p>

<h1>
  MOTIVATION
</h1>

<p>
  La motivation derrière IgnisBot repose sur la montée des incendies liés au changement climatique, notamment dans les zones boisées, où les ressources d’intervention sont souvent insuffisantes. Ce robot symbolise une solution autonome de détection et de réaction face à un départ de feu, en illustrant le potentiel de la technologie embarquée dans des contextes critiques. Il constitue un outil d'apprentissage pour initier les étudiants à l’électronique, à la robotique mobile et à la programmation appliquée. En combinant utilité, apprentissage et conscience environnementale, IgnisBot représente une approche moderne de la formation par projet.
</p>

<h1>ARCHITECTURE</h1>
<p>L'architecture d'IgnisBot repose sur une structure modulaire combinant détection, décision et action, organisée autour de la carte microcontrôleur Arduino Uno.</p>

<h2>DIAGRAMME FONCTIONNEL</h2>
<p>Ce diagramme montre les interactions principales entre les composants du robot.</p>

<p align="center">
  <img src="images/block_diagram_ignisbot.png" alt="Diagramme fonctionnel d’IgnisBot" width="80%">
</p>
 <p>
   Le diagramme fonctionnel présente de façon simplifiée l’architecture logique du système. Il permet de visualiser les fonctions principales du robot ainsi que les échanges d’informations entre les différents modules. Ce schéma joue un rôle clé pour comprendre comment chaque composant contribue à la mission du robot et comment l’ensemble coopère pour assurer un fonctionnement autonome et coordonné.
 </p>

<h2>SCHÉMA ÉLECTRONIQUE</h2>
<p>Le schéma suivant illustre les connexions électriques du projet</p>

<p align="center">
  <img src="images/schematic_ignisbot.png" alt="Schéma électronique IgnisBot" width="80%">
</p>

<p>Le schéma électrique illustre le câblage réel de tous les composants du robot, en montrant les connexions entre la carte Arduino Uno, les capteurs de flamme, le servomoteur, les moteurs, le module L298N, la pompe, le relais et les sources d’alimentation. Il permet de visualiser précisément la circulation des signaux et de l’énergie dans le système. Ce schéma est essentiel pour assembler le robot correctement, et il constitue une base précieuse pour le prototypage, la maintenance ou la reproduction du projet.</p>


<h1>COMPOSANTES ÉLECTRONIQUES</h1>

<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>Produit</th>
      <th>Quantité</th>
      <th>Prix unitaire (lei)</th>
      <th>Prix total (lei)</th>
      <th>Utilisation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Résistance 0,25W 1kΩ</td>
      <td>5</td>
      <td>0,10</td>
      <td>0,50</td>
      <td>Protection et limitation de courant pour signaux ou LED</td>
    </tr>
    <tr>
      <td>Module pilote de moteur double L298N (rouge)</td>
      <td>1</td>
      <td>10,99</td>
      <td>10,99</td>
      <td>Contrôle de deux moteurs DC via Arduino Uno</td>
    </tr>
    <tr>
      <td>Breadboard (400 points)</td>
      <td>1</td>
      <td>4,56</td>
      <td>4,56</td>
      <td>Prototypage rapide des circuits sans soudure</td>
    </tr>
    <tr>
      <td>Kit de fils pour breadboard</td>
      <td>1</td>
      <td>7,99</td>
      <td>7,99</td>
      <td>Connexions entre composants sur la breadboard</td>
    </tr>
    <tr>
      <td>Fils dupont femelle-mâle (40 pièces, 20 cm)</td>
      <td>1</td>
      <td>7,99</td>
      <td>7,99</td>
      <td>Connexions entre capteurs, modules et microcontrôleur</td>
    </tr>
    <tr>
      <td>Support pour 2 piles 18650</td>
      <td>1</td>
      <td>3,99</td>
      <td>3,99</td>
      <td>Alimentation portable du robot</td>
    </tr>
    <tr>
      <td>Servomoteur MG90S</td>
      <td>1</td>
      <td>19,33</td>
      <td>19,33</td>
      <td>Orientation de la buse/pulvérisateur pour extinction</td>
    </tr>
    <tr>
      <td>Diode 1N4148-NXP</td>
      <td>2</td>
      <td>0,49</td>
      <td>0,98</td>
      <td>Protection contre les surtensions (roues libres)</td>
    </tr>
    <tr>
      <td>Moteur avec réducteur et roue</td>
      <td>4</td>
      <td>14,99</td>
      <td>59,96</td>
      <td>Déplacement du robot</td>
    </tr>
    <tr>
      <td>Interrupteur marche/arrêt avec LED</td>
      <td>1</td>
      <td>1,99</td>
      <td>1,99</td>
      <td>Allumage/arrêt général du robot avec indicateur</td>
    </tr>
    <tr>
      <td>Câble USB AM-BM 50 cm pour Arduino MEGA/UNO</td>
      <td>1</td>
      <td>4,38</td>
      <td>4,38</td>
      <td>Programmation et alimentation via PC</td>
    </tr>
    <tr>
      <td>Capteur de flamme (analogique/numérique, 4 broches)</td>
      <td>3</td>
      <td>5,00</td>
      <td>15,00</td>
      <td>Détection des flammes dans l’environnement</td>
    </tr>
    <tr>
      <td>Tuyau pour pompe à eau 6x8 mm (1 mètre)</td>
      <td>1</td>
      <td>5,26</td>
      <td>5,26</td>
      <td>Acheminement de l’eau vers la sortie du système</td>
    </tr>
    <tr>
      <td>Pompe à eau/air R385 (6–12V, à diaphragme)</td>
      <td>1</td>
      <td>23,47</td>
      <td>23,47</td>
      <td>Extinction de feu via jet d’eau ou air</td>
    </tr>
    <tr>
      <td>Fils dupont femelle-femelle 20 cm</td>
      <td>1</td>
      <td>7,41</td>
      <td>7,41</td>
      <td>Connexion entre modules femelle (ex. capteur-capteur)</td>
    </tr>
    <tr>
      <td>Fils dupont mâle-mâle 30 cm</td>
      <td>1</td>
      <td>6,67</td>
      <td>6,67</td>
      <td>Connexions longues pour signaux ou alimentation</td>
    </tr>
    <tr>
      <td>Kit de condensateurs céramiques (300 pièces)</td>
      <td>1</td>
      <td>10,08</td>
      <td>10,08</td>
      <td>Filtrage des parasites et stabilisation des signaux</td>
    </tr>
    <tr>
      <td>Pile 18650 (individuelle)</td>
      <td>2</td>
      <td>18,00</td>
      <td>36,00</td>
      <td>Source principale d’énergie (batteries rechargeables)</td>
    </tr>
    <tr>
      <td>Transisteur</td>
      <td>1</td>
      <td>12,00</td>
      <td>12,00</td>
      <td>Interrupteur contrôlé électroniquement</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th colspan="3" style="text-align:right">Total général :</th>
      <th><strong>309,76 lei</strong></th>
      <th></th>
    </tr>
  </tfoot>
</table>



<h1>JOURNAL DE BORD</h1>

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

<h1>Galerie photo</h1>
 <img src="images/p1.png"  width="80%">
  <img src="images/p2.png"  width="80%">
   <img src="images/p3.png"  width="80%">
    <img src="images/p4.png"  width="80%">
     <img src="images/p5.png"  width="80%">
      <img src="images/p6.png"  width="80%">
       <img src="images/p7.png"  width="80%">
        <img src="images/p8.png"  width="80%">
         <img src="images/p9.png"  width="80%">
          <img src="images/p10.png"  width="80%">



<h1>LIENS DE RÉFÉRENCE</h1>

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


