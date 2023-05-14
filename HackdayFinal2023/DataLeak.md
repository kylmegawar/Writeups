En lisant l'énoncé on nous parle d'écouter etc on comprend donc qu'il faut surement écouter le réseau sachant qu'aucun fichier n'était donné au début, et vu que l'on sait qu'on est sur un subnet par équipe il y a peu de bruit.

On remarque assez facilement les gros blocs de Requêtes UDP, [img]

On vois notament une liste de pokémon, des url en bit.ly de rikroll et le nom des équipes.

Au début, j'ai testé les url en me disant qu'une url parmis les... beaucoup trop menaient vers le flag mais en recherchant un peu on tombe sur un tool magique

https://letmegooglethat.com/lucky.html?q=tool+exfiltration+pokemon

Du coup, on arrive sur le git de ce tool, on commence à déchiffrer les deux requêtes avec des noms de pokemon et les bit.ly de rickroll

Mais nous obtenons un résultat bizarre la requête avec les noms de pokemon renvoie le nom des équipes [img]

Et là, éclair de génie sachant que le troisième gros batch de data était des noms d'équipes on comprend que le chall maker a créé un nouveau cipher et que ce qu'on vient d'obtenir est le "dictionnaire", on se renseigne sur le git sur comment créer un nouveau cipher et il faut juste des mots/phrases et un ordre (autrement dit on crée une nouvelle "base" enfin je le vois comme ça) et la magie on a le cipher qui permet de chiffrer /  déchiffrer et le msg chiffrer et là bien content de moi j'exécute la commande decloakify avec "mon cipher" et ce que j'ai extrait des requêtes udp mais là
[img meme]


Je ne comprend pas, il semblerait que des nom soient mal ortographiés ? et là j'ai une envie de tuer le dev du chall et je commence a "corrigé" le fichier mais au bout d'un moment je me dis que c'est impossible je vérifie avec lui et effectivement ce n'est pas normal, d'ou le fait qu'il y avais a la fin de l'event un pcap de donné, en gros pour l'explication du pouruqoi du comment l'UDP c'est pas bien et ducoup les requêtes se marchaient dessus et créent des artéfacts.

Une fois le pcap donné on test avec ce qu'on extrait et ça marche nickel on optient un fichier qu'on devine être une image et qu'on on l'ouvre on obtient le flag
