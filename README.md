# Robotique-et-IA
devoir de robotique de SAINT JUSTE Jn Rooths vinski 

## Objectif du Projet:

Réaliser un voltmètre numérique avec une carte Arduino Uno, simulé sur Wokwi. Le projet permet de:

- mesurer une tension (simulée par un potentiomètre) et l'afficher en volts sur un écran LCD ;
- signaler le niveau de tension avec trois LED (verte, jaune, rouge) et un buzzer d'alarme ;
- figer la mesure avec un bouton HOLD, comme sur un vrai multimètre ;
- comprendre le rôle de chaque composant dans une chaîne de mesure : capteur, conversion, traitement, affichage et alerte.

## Les composant qu'on a utiliser 

-Un Arduino Uno
-Un Potentiomètre (il simule la tension à mesurer, de 0 à 5 V)
-Un LCD 1602 en version I2C 
-3 LED (verte, jaune, rouge)
-3 résistances de 220 Ω
-Un Buzzer
-Un Bouton poussoir (HOLD)

## Le fonctionnement du projet

-On a un potentiomètre qui est alimenté entre 5 V et GND. Son curseur envoie une tension variable de 0 à 5 V sur la broche A0.
Et ensuit le convertisseur analogique-numérique de l'Arduino transforme cette tension en un nombre de 0 à 1023. Le programme fait la moyenne de 10 lectures pour stabiliser la valeur.
l'Arduino retrouve la tension et l'écran LCD (I2C) indique la tension, par exemple U = 2.50 V, et le mode, LIVE ou HOLD.
Puis il y a une signalisation pour indiquer l'etat de danger du tension qui traverse l'écran LCD(I2C) 
			U < 2 V : LED verte (normal) ;
			2 V ≤ U ≤ 4 V : LED jaune (à surveiller) ;
			U > 4 V : LED rouge et buzzer continu (danger).
lE bouton HOLD permet un appui qui fige la valeur affichée (mode HOLD) et un bip confirme l'action et un second appui reprend la mesure en direct.

## Résultat obtenu

-A chaque fois que le volume du potentiomètre augmente l'ecran du LCD affiche la tension a l'ecran et les couleur changes a chaque niveau atteint et quand la tension dépasse 
les 4v le buzzer commence a crier.
Avec HOLD activé, l'écran reste figé sur « Mode : HOLD » même si vous tournez le potentiomètre. Un nouvel appui relance la mesure en temps réel.

En conclusion le montage fonctionne comme un petit voltmètre avec alarme. Il montre comment un microcontrôleur mesure une grandeur analogique, la convertit en valeur numérique, l'affiche et déclenche des alertes selon des seuils.

###### le lien WOKWI ci-dessous
https://wokwi.com/projects/477616187456708609 
