# bin
quelques exercices de scripting en Bash.

###creagif

Ce script permet de créer des captures d'ecran animées au format gif.
Il est écrit en bash et utilise imagemagic, ffmpeg et xrandr.
Il fonctionne en plusieurs étapes. Dans un premier temps, il fera une capture de l'écran et créera 15 images par seconde au format PNG via ffmpeg. 
Dès lors, il sera possible de découper certaines parties de la capture en supprimant les images correspondantes. Par exemple pour couper les quelques secondes lors du lancement du script.
Ensuite, imagemagic fusionnera le reste en un fichier GIF.

###creaicon

Ce script permet de créer des icones au format png conformes à ce que je cherche pour mes widgets awesome WM.
Ceux ci sont au format png, ont un fond transparent, sont blancs et ont une légère marge.
Donne des icones "out of the box" avec ceux du dossier joint, de sm4tik du projet dzen.
