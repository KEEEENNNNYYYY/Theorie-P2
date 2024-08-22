# Theorie-P2

# question:

A. Communications sécurisées (5 points)
Une communication sécurisée, du même style que sur HTTPS par exemple, est souvent
effectuée en deux temps : d’abord l’échange d’une clé partagée grâce à un chiffrement
asymétrique, ensuite l’utilisation de cette clé pour chiffrer les données utiles.
1. Quelle est la différence entre un chiffrement asymétrique et un chiffrement
symétrique ? (0,5 point)
2. Dans le cas d’un chiffrement asymétrique, la clé publique permet-t-elle de déchiffrer
un message ? (0,5 point)
Nous nous proposons d’effectuer un échange de clé en utilisant la version anonyme de
l’algorithme de Diffie-Hellman (DHa). Soient Alisy et Bôby deux personnes de clé secrète
respective a=6 et b=15. La clé publique est constituée du nombre premier p=23 et de la base
g=5.
3. Déroulez DHa et déterminez la valeur de la clé secrète s partagée entre Alisy et Bôby.
(2,5 points)
4. Eva est une personne malveillante qui souhaite également connaitre la clé partagée
s. Quelles est la valeur du message mab envoyée par Alisy à Bôby publiquement, et
donc lisible par Eva ? Et celle par Bôby à Alisy, mba ? (1 point)
5. Quel est le nom du problème mathématique qui fait qu’Eva aura beaucoup de mal à
dériver s malgré sa connaissance de p, g, mab et mba ? (0,5 point)
B. Les nombres de Javascript (5 points)
Un programmeur raisonne souvent en mémoire infinie.
1. Combien d’espace mémoire Javascript utilise-t-il pour stocker un nombre ? (0,5
point)
2. L’expansion binaire de π ε R peut-t-il tenir dans cet espace mémoire ? (0,5 point)
3. Le nombre Javascript Math.PI représente-t-il donc π ε R de manière exacte ? (0,5
point)
4. Donnez et expliquez l’évaluation de l’expression booléenne suivante en Javascript :
Number.MAX_SAFE_INTEGER + 1 ==
Number.MAX_SAFE_INTEGER + 2 (1 point)
5. Quelle est le nom du standard qui régit les nombres de Javascript ? Quel est le nom
du format que Javascript utilise dans ce standard ? (0,5 point)
Un programmeur raisonne souvent en base décimale.
6. Quelle est l’expansion binaire du nombre décimal n1=0.1 ? Est-il représentable
exactement dans le format binary64 ? (1 point)
7. Quelle est l’expansion binaire du nombre décimal n2=0.25 ? Est-il représentable
exactement dans le format binary64 ? (1 point)

1/2

Haute École d’Informatique de Madagascar

C. Recherche de données en temps logarithmique (5 points)
Soit une table, du même style que celles dans Postgresql par exemple, qui stocke les
prénoms de 1 million de personnes. Chaque entrée de la table contient exactement un
prénom. Supposons que n’importe quelle entrée de la table puisse être accédée avec le
même temps constant tread
.

1. Qu’est-ce qu’une relation d’ordre ? (0,5 point)
2. En supposant qu’aucun ordre n’a été établi sur les données, quel est le pire temps
d’accès tbozy pour savoir si la table contient Bozy ? (0,5 point)
3. En supposant que les prénoms sont stockés par ordre alphabétique, et en utilisant
l’algorithme dichotomique, quel est le pire temps d’accès tlita pour savoir si la table
contient Lita ? (1 point)
Nous décidons de stocker l’âge des personnes en plus de leur prénom. Au lieu du singleton
<prénom>, nous stockons désormais le couple <prénom, âge>. Les couples sont stockés dans
l’ordre lexicographique naturel.
4. Illustrez l’ordre lexicographique naturel en ordonnant les couples suivants : <Koto,
20>, <Bozy, 18>, <Bema, 21>, <Koto, 22> et <Zo, 17>. (1 point)
5. Dans la table de 1 million de <prénom, age>, et en utilisant l’algorithme
dichotomique, quel est le pire temps d’accès thasina30 pour savoir si la table contient
<Hasina, 30> ? (1 point)
6. Expliquez pourquoi il est en réalité plus intéressant d’ordonner le couple <âge,
prénom> plutôt que le couple <prénom, âge>. (1 point)
D. SLA de AWS (5 points)
Dans ses SLA pour EC2, AWS s’engage sur une disponibilité de 99,5% par instance.
1. Définir SLA. (0,5 point)
2. Qu’est-ce que le service EC2 ? (0,5 point)
3. Quel est le temps d’indisponibilité maximal par an que AWS s’autorise pour une
instance EC2 ? (1 point)
Supposons que nous exécutons le service Sclient d’un de nos clients sur EC2. Nous dupliquons
Sclient sur 2 instances pour tolérer les pannes. Un ALB reçoit les requêtes et les aiguilles vers
l’une d’entre elles en fonction de la santé des instances. AWS s’engage sur une disponibilité
de 99,99% par ALB.
4. Quel est le temps d’indisponibilité maximal par an de Sclient que AWS s’autorise à
causer ? (1 point)
5. Qu’est-ce qui augmenterait le plus la disponibilité de Sclient

: ajouter une instance EC2
supplémentaire ou ajouter un ALB supplémentaire ? Donnez le temps
d’indisponibilité

