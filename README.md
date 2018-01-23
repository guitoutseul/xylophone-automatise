![Polytech](https://camo.githubusercontent.com/2fe98f1f93a495607acfac1a6b62cb1d4affdbca/687474703a2f2f7777772e706f6c79746563686e6963652e66722f6a616869612f6a73702f6a616869612f74656d706c617465732f696e632f696d672f706f6c79746563685f6e6963652d736f706869612e706e67)

Ce projet est réalisé dans le cadre de la formation de prépa intégrée de Polytech'Nice Sophia



# xylophone-automatisé
Le xylophone est frappé automatiquement par des maillets en lisant un fichier MIDI, fichier qui contient toutes les informations sur la composition d'une musique.

Le traitement de l'information MIDI va se faire à partir d'un sequenceur MIDI, qui va comprendre cette information et me revoyer une suite binaire. Il faudra que je lie la sortie de ce sequenceur à l'entrée de l'arduino à l'aide d'un logiciel tierce. Ainsi, quand je lirais le fichier en direct a partir du sequenceur, j'obtiendrais les informations (en binaire) sur l'arduino de ce qui est joué en temps réel.
Il faudra ensuite ecrire un programme pour transformer cette suite binaire en un message compréhensible.
A partir de ce moment, je m'interesserais à l'aspect mecanique du projet, c'est à dire la mécanisation du xylophone.
