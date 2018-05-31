

compte rendu du 12/01/18

J'ai pris la décision de quitter mon groupe car on était trop nombreux (4), et donc de faire un projet seul. Celui-ci porte sur la lecture de fichier MIDI, récuperer une piste en particulier du fichier et la transferer vers l'arduino. Ensuite, a l'aide d'un programme arduino, faire bouger mecaniquement et indépendamment des 'maillets de xylophones' en fonction d'une note jouée. J'ai donc cherché comment lire un fichier MIDI et trouvé ce logiciel : http://www.canato.se/midiyodi/my_download.html

Il y a également un site qui permet de transformer une piste d'un fichier MIDI en un code lisible en arduino (pas encore testé) : https://extramaster.net/tools/midiToArduino/

compte rendu du 18/01/2018

Je vais plutot me tourner vers un séquenceur MIDI (reaper): https://www.reaper.fm/index.php pour traiter le fichier MIDI. Pour pouvoir rediriger l'output du logiciel vers un autre (pour rediriger l'output du sequenceur MIDI vers l'arduino) j'ai trouvé le logiciel JACK 2 :http://jackaudio.org/ Il faut encore configurer les logiciels entre eux pour pouvoir obtenir les informations sur l'arduino. La musique sera jouée en temps réelle a partir du sequenseur et les informations seront traités en temps réel.

compte rendu du 23/01/2018

Je commence à apprendre à utiliser REAPER pour l'utilisation que je souhaite en faire. Je passe la séance à essayer de connecter la sortie de REAPER à JACK 2, sans succes. 

compte rendu semaine 04 (25/01/2018 - 28/01/2018)

J'ai demandé de l'aide à Jean-Baptiste NIRASCOU, qui a participé aux projets arduino 2016-2017 et qui a également utilisé REAPER dans son projet. Il m'a répondu et m'a expliqué comment procéder. la liaison entre REAPER et JACK 2 fonctionne, mais je n'arrive pas a faire la liaison entre JACK 2 et arduino.

compte rendu du 09/02/2018

M.Masson m'a mis en contact avec une étudiante en élec4 (Lucie GRANDBOUCHE) qui partage presque le même projet que moi. Nous avons choisi de collaborer ensemble pour réaliser le même projet. Désormais, mes séances de projet auront lieu tous les vendredi de 13h à 16h. Au lieu de partir d'un fichier MIDI, elle part d'une partition XML. Elle s'occupera de transformer ce fichier XML en fichier texte à l'aide d'un programme C. Ce fichier texte comprendra toutes les notes de la musique les unes apres les autres. Mon role sera désormait de faire la partie branchement électrique du projet ainsi que la partie programmation arduino. Je m'attaque d'abord aux branchements. Mon but est d'étendre le nombre de sorties de l'arduino en utilisant un registre à décallage (74hc595). Je passe donc ma séance à m'imprénier du nouveau projet, comprendre les tenant et aboutissants, et je me renseigne sur le fonctionnement des registres à décallage.
