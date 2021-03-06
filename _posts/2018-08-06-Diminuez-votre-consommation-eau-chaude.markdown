---
layout: post
title:  "Diminuez votre facture d'eau chaude"
date:   2018-08-06 22:30:21
categories: jekyll update
image : Test2.png
resume : "Cet article vous propose un module électronique capable de commander à distance la commande de chauffe de votre cumulus au plus juste besoin"
tags: Economie Ecologie
author: Arnaud
---

Un jour, je me suis posé la question de savoir si j'arrivais à consommer quotidiennement toute la quantité d'eau chaude stockée dans mon cumulus ?
<blockquote>
Vous êtes-vous posé la question? Non? Alors lisez cet article pour limiter votre empreinte écologique!
</blockquote>
En effet, l'eau chaude sanitaire représente le second poste consommation d'électricité, après le chauffage.

<h2> Premier axe d'amélioration : bien connaître ses besoins </h2>
Tout d'abord, avez-vous suffisament bien dimensionné la taille de votre cumulus? Car toute eau chauffée non utilisée subira des pertes thermiques inutiles. 

Il faut l'admettre, c'est un paramètre très difficile à anticiper, car il faut prendre en compte pas mal de paramètres (je fais la vaisselle, famille qui risque de s'aggrandir, est-ce que je me douche toujours à la même heure?, etc...)

<strong>Une règle d'or</strong>, c'est de <a href="https://www.mychauffage.com/blog/comment-choisir-capacite-chauffe-eau">sélectionner un chauffe-eau</a> avec une capacité au plus juste besoin. 
En effet, non seulement vous aurez besoin de moins chauffer d'eau et en plus vous diminuerez les pertes (en effet, un ballon plus gros dissipe plus d'énergie)

Pour avoir une idée des pertes de votre cumulus, il existe un chiffre intitulé "Consommation d'entretien" dans la notice de votre chauffe-eau. Elle est exprimée en kWh pour maintenir pendant 24h l'eau à 60°C dans une pièce de 20°C.
Au premier ordre, on peut compter 1kWh tous les 100L pour une journée, soit 365kWh par an. <strong>On arrive déjà à une cinquantaine d'euros de perdu par an! <i class="fas fa-surprise"></i></strong>  Pour 200L, cette valeur sera doublée.

<h2> Deuxième axe d'amélioration : Le type d'alimentation électrique </h2>
Côté alimentation électrique, il existe deux cas de figure possibles : 
<ol>
<li>Cumulus constamment allumé avec la tarification de base</li>
<li>Cumulus uniquement allumé aux heures creuses, avec l'abonnement heures pleines / heures creuses (HP / HC)</li>

<strong>Dans ce post, je vous en propose un troisième <i class="fas fa-kiss-beam"></i> : </strong>
<li>Pose d'un <a href="{{ site.baseurl }}/jekyll/update/2018/08/21/fabriquer-votre-module-cumulus.html">module électronique</a> pour réguler la chauffe de votre chauffe-eau à votre guise. Il peut convenir pour les deux types de tarification.</li>
</ol>
<h3> Les avantages et inconvénients de ces solutions </h3>


<table>
<tr><td>Solution N°</td><td>Avantages</td><td>Inconvénients</td>
</tr>
<tr><td>1</td><td>Eau chaude à disposition en permanence</td><td>Solution coûteuse et peu écologique</td></tr>
<tr><td>2</td><td>Permet de profiter d'une tarification heure creuse et allume le chauffe eau pendant vos 8h de créneau HC</td><td>Nécessite l'installation d'un boitier dans votre tableau électrique</td></tr>
<tr><td>3</td><td>Permet de chauffer de l'eau au juste besoin</td><td>Nécessite d'installer un module</td></tr>
</table>

Dans le premier cas, votre cumulus est constamment connecté au secteur. Il va donc constamment maintenir votre température à la consigne. Cette solution est source de perte d'énergie.

Dans le second cas, vous activerez uniquement votre cumulus pendant les heures creuses, via un boitier avec trois positions : arrêt, auto et marche, qu'il faut installer dans votre tableau électrique et régler sur la position auto.Ces boitiers sont disponibles dans la plupart des magasins de bricolage.

Dans la <a href="{{ site.baseurl }}/jekyll/update/2018/08/21/fabriquer-votre-module-cumulus.html">solution proposée</a>, vous allez pouvoir alimenter votre chauffe eau au plus juste besoin. En effet, vous avez la possibilité de déclencher à n'importe quelle heure votre chauffe eau, en fonction de vos habitudes. 
<blockquote>
Vous vous douchez le soir? allumez-le 5h en avance pour laisser le temps à votre cumulus de chauffer l'eau.
Vous êtes plutôt du matin? Allumez-le à 2h du matin, en pleine heure creuse, pour avoir une eau chaude à 7h.
Encore une fois attention, si votre ballon est plus gros, les temps de chauffe s'allongeront...  
</blockquote>

<h3> Et l'empreinte éco ? </h3>

J'ai fait pour vous une estimation de vos pertes d'énergie en fonction de ces 3 configurations.

Mes hypothèses : 
- 1 ballon de 150L de quelques années (je prends un facteur de vieillesse dans les pertes)
- Un flux thermique qui décroît linéairement en fonction de la différence de température entre l'eau dans la cuve et l'extérieur
- Un thermostat réglé à 65°C (pour vous éviter tout risque de légionellose)
- Une utilisation de 2 douches quotidiennes (soit 40L d'eau chaude) + lavage de mains, vaisselle (environ 5L d'eau chaude consommée)
- Un fonctionnement 365j/an (hypothèse pire-cas)
- Je fais mon raisonnement sur le mois de Mai, afin que la saison hivernale compense la saison estivale en terme de besoin d'eau chaude!
- Mon cumulus se situe dans une zone habitable régulée à 20°C

Pour vous donner quelques repères, voici quelques chiffres : 
- J'estime que sans alimenter mon chauffe eau, l'eau perd 0.9°C par heure lorsque l'eau est à 60°C.
- Avec l'alimentation, mon eau chauffe de 8°C par heure environ.
- Mon ballon chauffe en 5h.


Voici une représentation graphique de la température de l'eau, c'est beaucoup plus visuel! 
Chez moi, par exemple, nous prenons la douche le matin aux alentours de 7h.
<hr>
<center>
<img src="{{ "/assets/img/" | absolute_url }}graphe1.png">
</center>

<center>
<i>Profil de température de l'eau dans le cumulus sur une journée</i>
</center>
<hr>
<blockquote>
<strong>Vous visualisez mieux maintenant? <i class="fas fa-smile-wink"></i></strong>
</blockquote>
Voici les résultats : 

<table>
<tr><td>Solution N°</td><td>kWh annuels perdus</td><td>Coût annuel</td><td>Gain vis-à-vis de la première solution</td>
</tr>
<tr><td>1</td><td>1312kWh</td><td>175€</td><td>/</td></tr>
<tr><td>2</td><td>774kWh</td><td>95€</td><td>45%</td></tr>
<tr><td>3</td><td>676kWh</td><td>83€</td><td>52%</td></tr>
</table>

<strong>Attention, je le rappelle, ce n'est ici que des énergies perdus, ce n'est qu'une partie du montant de votre facture! 
 </strong>
<strong>Pour le reste de votre facture, c'est de l'énergie nécessaire à chauffer votre eau que vous allez consommer.
</strong>
<strong>Grosso modo, les pertes représentent la moitié de la facture. (A 45L d'eau consommée par jour, je suis à 1000kWh/an)
</strong>



<h3>Retenez</h3>
Pour diminuer notre empreinte énergétique, voici les principaux conseils : 
<ol>
<li>
Dimensionnez correctement votre ballon d'eau chaude. Il vaut mieux un peu plus petit que trop grand 
<blockquote>
Au pire, vous pourrez monter temporairement le thermostat, s'il y a plus de monde pour avoir plus d'eau chaude!
</blockquote>
</li>
<li>
Optez pour une option heure pleine - heure creuse. Et ne pas oublier d'acheter le module qui permet d'activer automatiquement votre chauffe eau en heures creuses chez votre magasin de bricolage préféré!
</li>
<li>
Attention, baissez la température de consigne sous  les 60°C n'est pas une solution viable. Vous risqueriez un développement microbien.
</li>
<li>
<a href="{{ site.baseurl }}/jekyll/update/2018/08/21/fabriquer-votre-module-cumulus.html">Fabriquez votre module</a> pour programmer les démarrages de votre chauffe-eau. Vous pouvez rester sur un forfait base si vous voulez et activer le chauffe eau au juste besoin en réglant la tranche horaire de fonctionnement.
</li>
</ol>


<h3>Pour aller plus loin</h3>
Si vous souhaitez aller encore plus loin, vous pouvez décider d'investir dans un chauffe-eau thermodynamique. Vous pourrez diminuer significativement votre facture d'énergie, mais vous pourrez toujours optimiser l'énergie perdue en faisant marcher votre chauffe-eau juste avant de prendre votre douche. 
