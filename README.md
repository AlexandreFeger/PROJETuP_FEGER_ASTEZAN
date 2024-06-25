# PROJETuP_FEGER_ASTEZAN
Alexandre FEGER / Matthieu ASTEZAN – P21 ITII                            24 Juin 2024

                            Read Me & Rapport
 
Surveillance et Sécurité d'un Coffre-Fort avec STM32

Description du Projet

Ce projet vise à développer un système de sécurité avancé pour un coffre-fort en utilisant un microcontrôleur STM32. Le système offre une interaction utilisateur intuitive et une surveillance en temps réel des conditions internes du coffre-fort, telles que la température, l'humidité et la pression.

Composants Utilisés

•	Microcontrôleur STM32
•	Potentiomètre
•	Écran 7 segments (4 digits)
•	Boutons (BTN1, BTN2, BTN3, BTN4)
•	Capteurs environnementaux (pression, température, humidité)
Objectifs du Projet

Notre projet vise à :
•	Améliorer la sécurité des coffres-forts grâce au microcontrôleur STM32.
•	Assurer une interaction utilisateur intuitive avec la saisie et la validation du code.
•	Surveiller en temps réel les conditions internes du coffre-fort pour une protection continue.

Solution Technique
Le système utilise le microcontrôleur STM32, un potentiomètre, un écran 7 segments, des boutons et des capteurs pour ses fonctionnalités. La saisie et la validation du code sont réalisées via des boutons, tandis que les capteurs fournissent des données environnementales en temps réel. Les composants sont interconnectés pour offrir une solution complète et efficace.

Fonctionnement du Code
Le programme initialise les périphériques STM32, y compris les capteurs de mouvement et environnementaux, l'interface SPI pour l'écran 7 segments, et les boutons pour l'interaction utilisateur.
Le potentiomètre est utilisé pour entrer les chiffres du code, qui sont affichés sur l'écran 7 segments. Pour faciliter la saisie, des LEDs sont placées sous chaque digit de l'écran 7 segments pour indiquer le chiffre en cours de modification. L'utilisateur peut naviguer entre les chiffres du code en utilisant les boutons BTN1 et BTN2, permettant de passer au digit suivant ou de revenir au digit précédent, respectivement.
Une fois le code complet saisi, l'utilisateur appuie sur le bouton BTN4 pour valider le code. Si le code est correct, une animation LED est déclenchée pour indiquer le succès, et l'écran affiche "COOL". Si le code est incorrect, l'écran affiche "FAIL".
En appuyant sur le bouton BTN3, le système affiche les données environnementales (pression, température, humidité) sur le terminal Teraterm. Ces données sont fournies par les capteurs intégrés au système.
Des interruptions sont utilisées pour gérer les boutons et les capteurs en temps réel, assurant ainsi une réactivité optimale du système. Cela permet de capturer les entrées utilisateur et de lire les valeurs des capteurs de manière efficace et précise.

Défis et Problématiques
Les principaux défis ont été :
•	Intégrer divers périphériques avec le STM32 tout en gérant efficacement les interruptions.
•	Assurer une navigation fluide et un affichage précis sur l'écran 7 segments.
•	Garantir la sécurité et la précision de la saisie du code.

Résolution des Problèmes
Nous avons utilisé les interruptions pour gérer les boutons et les capteurs en temps réel. Le multiplexage a été employé pour un affichage efficace sur l'écran 7 segments. La communication des données environnementales a été réalisée via Teraterm, assurant une surveillance précise.

Conclusion
Ce projet améliore la sécurité des coffres-forts en utilisant le STM32, offrant une interaction utilisateur intuitive et une surveillance en temps réel des conditions internes. À l'avenir, nous envisageons d'ajouter des capteurs supplémentaires et d'intégrer des techniques de cryptage pour renforcer encore davantage la sécurité.

