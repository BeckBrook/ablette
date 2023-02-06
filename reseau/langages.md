## Langages

### Menu

[Binaire](BeckBrook/ablette/blob/main/reseau/langages###Binaire)
[Héxadécimal]()
[Décimal]()
[Conversion binaire->héxa]()
[Conversion héxa->binaire]()
[Conversion décimal->binaire]()
[Conversion binaire->décimal]()
[Conversion décimal->héxa]()
[converion héxa->décimal]()



### Binaire

Exemple : 01001010 01101111 01110101 01101111 01101110 01110011 00100000 01100001 01110101 00100000 01000111 01010111 01011001 01001110 01010100 00100000 00100001 00100000

Les machines utilisent le langage binaire pour communiquer entre elles, fait de 1 et de 0, il se quantifie en bits (compression de "Binary Digits"). Il est appelé Binaire car seules deux valeurs peuvent apparaître, on dit qu'il est en base 2. 

## Comment compter en binaire ?

Pour convertir en binaire à la main, on peut dresser un tableau des puissances de 2, allant, de droite à gauche, de la puissance la plus élevée à 2^0. 

1. On récupère le nombre

2. On voit quelles puissances de 2 le constituent

3. Dans le tableau, on rajoute une ligne

4. A chaque fois que la puissance correspondante est comprise dans le nombre de base, on écrit 1. Si elle n'est pas comprise, on écrit 0. 

5. Une fois tous les bits écrits, on lit le nombre binaire de gauche à droite



(nota bene : les premiers 0 d'un nombre binaire sont optionnels, mais pas les derniers, c'est comme par exemple écrire 500 comme 000500.)



### Application

Je veux le nombre 192.

| 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| 1   | 1   | 0   | 0   | 0   | 0   | 0   | 0   |

2^7 + 2^6 = 128+64 = 192. Donc sont à 1 : 2^7 et 2^6. Le reste des chiffres sont à 0. 

Ainsi 192 = 11000000

Notez que la table range toujours les puissances de la plus élevée à 2^0 = 1. En théorie, elle contient **toutes** les puissances de 2, mais dans le cas de l'adressage ip, il nous suffit de renseigner jusqu'à 2^7.



### Notion de réseau - IP

Pourquoi ? notez que le nombre de cases équivaut à 8 données, ainsi un octet. Une adresse IP, elle est composée de 4 paquets de 8 octets 

- par exemple : 192.168.1.1 = un octet à 192 + un deuxième octet à 168 + un troisième octet à 1 + un quatrième octet à 1

le nombre maximum que peut atteindre un nombre binaire en 8 octets (càd, toutes les cases à 1 dans le tableau) est : 128+64+32+16+8+4+2+1 = 255
