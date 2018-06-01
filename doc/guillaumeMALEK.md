

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

M.Masson m'a mis en contact avec une étudiante en élec4 (Lucie GRANDBOUCHE) qui partage presque le même projet que moi. Nous avons choisi de collaborer ensemble pour réaliser le même projet. Désormais, mes séances de projet auront lieu tous les vendredi de 13h à 16h. Au lieu de partir d'un fichier MIDI, elle part d'une partition XML. Elle s'occupera de transformer ce fichier XML en fichier texte à l'aide d'un programme C. Ce fichier texte comprendra toutes les notes de la musique les unes apres les autres. Mon role sera désormait de faire la partie branchement électrique du projet ainsi que la partie programmation arduino. Je m'attaque d'abord aux branchements. Mon but est d'étendre le nombre de sorties de l'arduino en utilisant un registre à décallage (74hc595). Je passe donc ma séance à m'imprénier du nouveau projet, comprendre les tenant et aboutissants, et je me renseigne sur le fonctionnement des registres à décallage. Le branchement du registre à décallage est terminé

compte rendu du 16/02/2018

Je code le fonctionnement du registre à décallage (je ne savais pas qu'il y avait des fonctions toutes faites pour faire fonctionner le registre à décallage) . Le programme fini, je le teste en essayant d'allumer des leds connectés à ce registre. Elles s'allument correctement. Je fais ensuite le branchement du deuxieme registre à décallage (pour pouvoir avoir 16 sorties, 8 sortie par registre). les deux registres fonctionnent ensemble, donc les 16 sorties aussi. Comme les registres envoient en sortie un courant trop faible, je dois connecter chaque sortie du registre à décallage à un transistor darlington pour amplifier le courant. Avant de réaliser le montage, je souhaite commencer la programmation du projet. Le but pour moi est tout d'abord de lire un fichier texte depuis l'ordinateur et de le transmettre sur l'arduino (cela s'apparente un peu à la semaine 04, ou je devais lier la sortie de JACK 2 à l'arduino, sauf que la je dois lier un fichier texte à l'arduino). Apres beaucoup de recherches sur internet, je vois beaucoup parler de "processing" pour lire un fichier texte sur l'arduino. Il faudrait donc que je lise le fichier texte à partir de processing, et que je l'envoie en temps direct à l'arduino pour que ce dernier recoive les données du fichier texte.

compte rendu du 23/02/2018

Je commence à faire la programmation sur processing. J'arrive à lire le fichier texte sur processing. Je stocke chaque ligne du fichier texte dans un tableau. J'essaye donc d'envoyer les informations du tableau vers arduino, mais je passe la séance à essayer de comprendre pourquoi cela ne fonctionne pas. Si je créé une chaine de caractere à partir de processing et que je l'envoie à Arduino, cela fonctionne, mais quand j'importe le contenu du fichier texte dans un tableau, et que j'essaye d'envoyer le tableau a Arduino, plus rien ne marche.

compte rendu du 02/03/2018

Absent à cause d'un vol d'avion pour rentrer chez moi en Lorraine.

compte rendu du 16/03/2018

J'ai continué à me prendre la tête avec processing qui refuse catégoriquement d'envoyer les informations du fichier texte vers arduino. Je me demande si ce n'est pas un probleme d'encodage du fichier texte qui fait que processing n'arrive pas à bien comprendre que les lignes du fichier texte sont bien des Strings. Je m'occupe donc du reste du programme et laisse cette partie de coté. Je décide de coder la partie arduino. 

compte rendu du 23/04/2018

J'apprends que l'on utilise une carte sd pour lire les informations du fichier texte. J'aurais donc perdu énormément de temps à essayer de faire fonctionner mon programme avec processing. Je sais maintenant que j'aurais du plus communiquer avec mes deux partenaires qui font la meme partie que moi. Je me renseigne donc sur le fonctionnement de la carte sd et sur comment lire un fichier depuis une carte sd. J'ai de nouveau des problemes avec la lecture des Strings, et je commence à vraiment m'inquiéter quant à l'issue du projet car je n'arrive pas à régler ce probleme. je décide donc de continuer le branchement électrique en rajoutant deux transistors Darlington pour amplifier le signal de sortie des registres à décallage.

compte rendu du 30/04/2018

Absent à cause d'un vol d'avion.

compte rendu du 06/04/2018

Ma présentation de mi-parcours s'est fait le 06/04/2018 et non le 05/04/2018. J'ai en effet eu la possibilité de faire ma présentation devant les élec4 en anglais.

compte rendu du 13/04/2018

Le 12/04/2018, M.Masson nous a aidé dans notre projet en nous fournissant une version fonctionnelle du programme et du branchement électrique (je le remercie grandement !). En clair, il s'est occupé de faire ma partie. Je ne cache pas que j'ai un peu honte de ne pas avoir réussi à avancer comme je le voulais, et que M.Masson a du prendre de grandes initiatives pour nous aider. Nous nous attaquons donc à la partie mécanique du projet. la structure est faite en bois avec tes trous carrés de la largeur des solénoides. Une deuxieme structure en bois vient se caler contre la première pour bloquer les solénoides et les faire tenir. Les trous, et donc les solénoides sont alignés avec les lames métalliques du Glockenspiel. Le but est de connecter chacune des 13 solénoides au transistor Darlington.

compte rendu du 20/04/2018

Absent à cause d'un vol d'avion

compte rendu du 04/05/2018






