# bin
quelques exercices de scripting en Bash.

###creagif

Ce script permet de créer des captures d'ecran animées au format gif.
Il est écrit en bash et utilise imagemagic, ffmpeg et xrandr.
Il fonctionne en plusieurs étapes. Dans un premier temps, il fera une capture de l'écran et créera 15 images par seconde au format PNG via ffmpeg. 
Dès lors, il sera possible de modifier le contenu en supprimant des images. Par exemple les quelques secondes ou vous lancez le script.
Ensuite, imagemagick fusionnera le reste en un fichier GIF.
