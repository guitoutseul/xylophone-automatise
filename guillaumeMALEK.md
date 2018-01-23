compte rendu du 12/01/18

J'ai pris la décision de quitter mon groupe car on était trop nombreux (4), et donc de faire un projet seul.
Celui-ci porte sur la lecture de fichier MIDI, récuperer une piste en particulier du fichier et la transferer vers l'arduino.
Ensuite, a l'aide d'un programme arduino, faire bouger mecaniquement et indépendamment des 'maillets de xylophones' en fonction
d'une note jouée.
J'ai donc cherché comment lire un fichier MIDI et trouvé ce logiciel : http://www.canato.se/midiyodi/my_download.html

Il y a également un site qui permet de transformer une piste d'un fichier MIDI en un code lisible en arduino (pas encore testé) :
https://extramaster.net/tools/midiToArduino/



compte rendu du 18/01/2018

Je vais plutot me tourner vers un séquenceur MIDI (reaper): https://www.reaper.fm/index.php pour traiter le fichier MIDI. Pour pouvoir rediriger l'output du logiciel vers un autre (pour rediriger l'output du sequenceur MIDI vers l'arduino) j'ai trouvé le logiciel JACK 2 :http://jackaudio.org/
Il faut encore configurer les logiciels entre eux pour pouvoir obtenir les informations sur l'arduino. La musique sera jouée en temps réelle a partir du sequenseur et les informations seront traités en temps réel.
