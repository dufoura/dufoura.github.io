---
layout: post
title:  "Régulez votre chauffe-eau"
date:   2018-08-21
categories: jekyll update
image : cumulus.png
resume : "Cet article vous propose un module électronique capable de commander à distance la commande de chauffe de votre cumulus au plus juste besoin"
---
Cet article va vous proposer une solution suite à l'article précédent sur le sujet  <a href="{{ site.baseurl }}/jekyll/update/2018/08/06/Diminuez-votre-consommation-eau-chaude.html">
de la réalisation d'économies d'énergie au niveau de votre cumulus</a>. 
Il s'agit d'un module implémentable au niveau de votre tableau électrique. 
Ce module est pilotable via le wifi, soit en se connectant en point à point, soit en l'appairant à votre réseau wifi.

<h2> Côté Hardware </h2>
Côté composants électroniques, j'adore travailler avec les modules ESP8266, car ils intègrent le module Wifi et ils disposent d'une flash embarquée assez importante, 
permettant ainsi de stocker facilement un petit site internet en guise d'interface! 
Pour le pilotage de la puissance, le plus simple est d'utiliser un relais qui va venir commuter le réseau EDF.
<blockquote>
<i class="fas fa-plug"></i>  Attention, ce module est en contact avec du 230V, autant dire que toute manipulation nécessite de couper l'électricité le temps de l'intervention!
Je ne suis pas responsable de vos mauvaises manipulations!
</blockquote>
Le plus souvent, les relais doivent être pilotés en 5V. L'ESP8266 ne fonctionnant qu'à 3.3V, il faut un circuit d'adaptation (un simple transistor MOSFET dans notre cas)
Afin de pouvoir déclencher le module à des heures fixes de la journée, il faut un module RTC capable de mémoriser l'heure. 
On rajoute également un régulateur de tension et quelques capacités de filtrage, voici la schématique : 
<img src="{{ "/assets/img/" | absolute_url }}esp_cumulus_schema.png">

<h2> Côté Software </h2>
Pour le côté logiciel, le plus intuitif de mon point de vue est une interface Web avec le module. 
Pour télécharger le code sous ESP8266, j'utilise l'outils Arduino IDE, qui est je trouve hyper pratique! 
<blockquote>
Quoi?!? Vous n'avez pas encore téléchargé Arduino et la librairie ESP8266 ??? Suivez <a href="https://github.com/esp8266/Arduino#installing-with-boards-manager">ce guide</a>
</blockquote>
Au niveau du board manager, il faut sélectionner le module utilisé (dans mon cas : NodeMCU 1.0 - ESP12E)
Pour uploader le code, il y a quelques manipulations nécessaires si vous souhaitez utiliser le module ESP8266 seul. 
En effet, avant le téléchargement du code, il faut faire entrer le module en mode 'boot'. 
Pour cela, il faut mettre au 0V les pins 0 et 2. Sur mon module, il suffit juste de relier le GPIO 0 et 2 au GND, avant de brancher la carte.
Il faut également un module usb to serial pour permettre de télécharger le code dans l'ESP.

Le code est disponible à cette adresse : <a href="https://github.com/dufoura/ESP_Cumulus.git"> Ici </a> 

<h2> Premiers pas avec le module </h2>
Vous avez réussi à transférer le programme dans l'ESP8266? Bravo!
Quelques petites étapes de vérification : 
<ol>
<li>Branchez le module avec une alimentation USB capable de délivrer au moins 5V/300mA. </li>
<li> A l'aide de votre PC ou smartphone, connecter vous au wifi ESPap. (Le mot de passe est écrit en dur dans votre code, vous pouvez mettre ce que vous voulez)</li>
<li> Une fois connecté, ouvrez une page Web et tapez dans la barre de recherche "192.168.4.1/edit". Vous devriez alors tomber sur une page Web.</li>
<li> Vous pourrez modifier les heures de démarrage et d'extinction de votre cumulus, connecter votre module à votre wifi domestique, etc...</li>
</ol>
<blockquote>
Attention au wifi en général. Vous pouvez potentiellement avoir pendant les étapes de configuration un petit hacker qui pourrait tenter de soutirer 
des informations sur vos log de wifi. Il faut être très vigilant et vérifier lorsque l'on réalise les premières connexions qu'il n'existe pas deux wifi avec un nom identique!
De même, faites l'effort de mettre un mot de passe dans le code pas trop facile à deviner. 
Normalement, vous n'avez rien à craindre. Mais il vaut mieux être prévenu!
</blockquote>

<h2> Quelques retours </h2>
J'utilise ce module depuis près de 3 ans maintenant. Je dois dire qu'il fonctionne très bien, Je n'ai jamais eu de problèmes, même avec les relais achetés en Chine. 
Pour être en conformité avec votre installation électrique, vous devez conserver votre disjoncteur de 2A sur le circuit de pilotage de votre cumulus. 