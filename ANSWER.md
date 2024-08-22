# +vA. Cryptographie
## 1. Quelle est la différence entre un chiffrement asymétrique et un chiffrement symétrique ? (0,5 point)

    Chiffrement symétrique : Utilise une seule clé pour chiffrer et déchiffrer les
    données. La même clé est partagée entre l’expéditeur et le récepteur, ce qui
    nécessite que la clé soit secrète et partagée en toute sécurité.
    Chiffrement asymétrique : Utilise une paire de clés distinctes, une clé publique pour
    chiffrer les données et une clé privée pour les déchiffrer. La clé publique peut être
    partagée librement, tandis que la clé privée reste secrète.

## 2. Dans le cas d’un chiffrement asymétrique, la clé publique permet-t-elle de déchiffrer un message ? (0,5 point)

    Non, dans le chiffrement asymétrique, la clé publique est utilisée pour chiffrer un message.
    Seule la clé privée correspondante permet de déchiffrer le message. La clé publique ne peut
    pas déchiffrer les messages qu’elle a chiffrés.

## 3. Déroulez DHa et déterminez la valeur de la clé secrète s partagée entre Alisy et Bôby. (2,5 points)

    Voici le déroulement de l'algorithme de Diffie-Hellman :
    •
    Données : p=23p = 23p=23, g=5g = 5g=5, a=6a = 6a=6 (clé secrète d’Alisy), b=15b =
    15b=15 (clé secrète de Bôby).

### 1. Calcul des clés publiques :

    o Alisy calcule sa clé publique AAA7* :
    A=gamod p=56mod 23A = g^a \mod p = 5^6 \mod 23A=gamodp=56mod23
    Nous avons déjà calculé 56mod 23=25^6 \mod 23 = 256mod23=2, donc
    A=2A = 2A=2.
    o

    Bôby calcule sa clé publique BBB :
    B=gbmod p=515mod 23B = g^b \mod p = 5^{15} \mod
    23B=gbmodp=515mod23
    Nous avons déjà calculé 515mod 23=25^{15} \mod 23 = 2515mod23=2, donc
    B=2B = 2B=2.
### 2. Calcul de la clé secrète partagée :

    o Alisy calcule la clé secrète partagée sss en utilisant la clé publique de Bôby :
    s=Bamod p=26mod 23s = B^a \mod p = 2^6 \mod 23s=Bamodp=26mod23
    26=64mod 23=182^6 = 64 \mod 23 = 1826=64mod23=18Donc, s=18s = 18s=18.
    o
    Bôby calcule la clé secrète partagée sss en utilisant la clé publique d’Alisy :
    s=Abmod p=215mod 23s = A^b \mod p = 2^{15} \mod
    23s=Abmodp=215mod23 215=32768mod 23=182^{15} = 32768 \mod 23 =
    18215=32768mod23=18
    Donc, s=18s = 18s=18.
### 3. La clé secrète partagée est donc s=18s = 18s=18.
### 4. Quelle est la valeur du message mabm_{ab}mab envoyée par Alisy à Bôby publiquement, et donc lisible par Eva ? Et celle par Bôby à Alisy, mbam_{ba}mba ?

    •
    Message envoyé par Alisy à Bôby (mabm_{ab}mab) :
    mab=A=2m_{ab} = A = 2mab=A=2
    •
    Message envoyé par Bôby à Alisy (mbam_{ba}mba) :
    mba=B=2m_{ba} = B = 2mba=B=2
    Donc, les messages envoyés sont tous les deux 222.
### 5. Quel est le nom du problème mathématique qui fait qu’Eva aura beaucoup de mal à dériver sss malgré sa connaissance de ppp, ggg, mabm_{ab}mab et mbam_{ba}mba ?

    Le problème mathématique est le problème du logarithme discret. Il consiste à déterminer
    l'exposant (ou clé secrète) à partir de la base, du modulo, et du résultat de l'exponentiation.
    C'est un problème difficile à résoudre efficacement sans connaître la clé secrète.
# B. Les nombres de Javascript
## 1. Combien d’espace mémoire Javascript utilise-t-il pour stocker un nombre ? (0,5 point)
    Javascript utilise 64 bits (8 octets) pour stoc
    ker un nombre. Cela correspond au format double précision de IEEE 754.
## 2. L’expansion binaire de π peut-elle tenir dans cet espace mémoire ? (0,5 point)
    Non, l’expansion binaire de π est infinie et non périodique, donc elle ne peut pas être
    représentée exactement dans un espace mémoire limité à 64 bits.
## 3. Le nombre Javascript Math.PI représente-t-il donc de manière exacte ? (0,5 point)
    Non, le nombre Math.PI en JavaScript est une approximation de π. Il est stocké en double précision, ce qui ne permet pas une représentation exacte de π.

### 4. Donnez et expliquez l’évaluation de l’expression booléenne suivante en Javascript :
    Number.MAX_SAFE_INTEGER + 1 == Number.MAX_SAFE_INTEGER + 2 (1 point)
    Number.MAX_SAFE_INTEGER est la plus grande valeur entière que JavaScript peut représenter
    de manière exacte, soit 253−12^{53} - 1253−1. En raison des limites de précision des
    nombres en double précision, Number.MAX_SAFE_INTEGER + 1 est égal à
    Number.MAX_SAFE_INTEGER + 2 car l’espace de représentation ne peut pas différencier ces deux
    valeurs. L’évaluation de l’expression sera donc true.
### 5. Quelle est le nom du standard qui régit les nombres de Javascript ? Quel est le nom du format que Javascript utilise dans ce standard ? (0,5 point)

    Le standard est IEEE 754.
    Le format utilisé est double précision (64 bits).
### 6. Quelle est l’expansion binaire du nombre décimal n1=0.1 ? Est-il représentable exactement dans le format binary64 ? (1 point)

    Le nombre décimal 0.1 en binaire est une fraction périodique :
    0.000110011001100110011...0.000110011001100110011...0.000110011001100110011.... Il
    ne peut pas être représenté exactement en format binary64. La représentation est donc une
    approximation.
### 7. Quelle est l’expansion binaire du nombre décimal n2=0.25 ? Est-il représentable
    exactement dans le format binary64 ? (1 point)
    Le nombre décimal 0.25 en binaire est 0.010.010.01, ce qui est exactement représentable
    en format binary64. La représentation est exacte.
# C. Recherche de données en temps logarithmique
### 1. Qu’est-ce qu’une relation d’ordre ? (0,5 point)
    Une relation d’ordre est une relation qui permet de comparer des éléments dans un
    ensemble en établissant un ordre entre eux. Par exemple, dans une liste triée, chaque
    élément est comparé à un autre pour déterminer sa position relative.
### 2. En supposant qu’aucun ordre n’a été établi sur les données, quel est le pire temps d’accès tbozyt_{bozy}tbozy pour savoir si la table contient Bozy ? (0,5 point)
    Si aucun ordre n’a été établi, il faudrait effectuer une recherche linéaire. Le pire temps
    d’accès est donc O(n)O(n)O(n), où nnn est le nombre total d’entrées dans la table, soit 1
    million.3. En supposant que les prénoms sont stockés par ordre alphabétique, et en utilisant
    l’algorithme dichotomique, quel est le pire temps d’accès tlitat_{lita}tlita pour savoir si la
    table contient Lita ? (1 point)
    Avec les prénoms stockés par ordre alphabétique, une recherche dichotomique (ou binaire)
    peut être utilisée. Le pire temps d’accès est O(log⁡n)O(\log n)O(logn). Pour 1 million de
    prénoms, cela donne log⁡21,000,000≈20\log_2 1{,}000{,}000 \approx 20log21,000,000≈20.
### 4. Illustrez l’ordre lexicographique naturel en ordonnant les couples suivants : <Koto, 20>, <Bozy, 18>, <Bema, 21>, <Koto,22> et <Zo, 17>. (1 point)
    L’ordre lexicographique naturel trie d’abord par prénom, puis par âge en cas d’égalité :
    1.
    2.
    3.
    4.
    5.
    <Bozy, 18>
    <Bema, 21>
    <Koto, 20>
    <Koto, 22>
    <Zo, 17>
### 5. Dans la table de 1 million de <prénom, âge>, et en utilisant l’algorithme dichotomique, quel est le pire temps d’accès thasina30t_{hasina30}thasina30 pour savoir si la table contient <Hasina, 30> ? (1 point)
    Avec les couples <prénom, âge> triés lexicographiquement, la recherche dichotomique
    donnera un temps d’accès de O(log⁡n)O(\log n)O(logn). Pour 1 million de couples, cela
    donne log⁡21,000,000≈20\log_2 1{,}000{,}000 \approx 20log21,000,000≈20.
### 6. Expliquez pourquoi il est en réalité plus intéressant d’ordonner le couple <âge, prénom> plutôt que le couple <prénom,âge>. (1 point)
    Ordonner par <âge, prénom> permet de regrouper les personnes ayant le même âge, ce qui
    est souvent plus utile dans les requêtes qui filtrent ou trient par âge. Cela permet une
    recherche plus efficace par âge et évite de faire des recherches dans des segments de
    données non pertinents. Le tri par <prénom, âge> est plus adapté pour des recherches
    alphabétiques et peut être moins efficace si la recherche se fait principalement par âge.
    Voici les réponses à vos questions :
