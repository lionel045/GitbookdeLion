# for Loop

en Swift nous pouvons instancier une boucle For pour parcourir nos élément mais elle fonctionne un peu différemment regardons :

<mark style="color:red;">Intervale ouvert</mark>

```
for i in 1...5 // Interval ouvert 1 à 5
```

cela fonctionne comme une boucle normal mais la différence c'est qu'il y a des intervals ce qu'il donne une flexibilité dans l'itération

Il y a cependant aussi les  interval semi ouvert comme ceci :&#x20;

`for i in 1 ... < 5 // Interval semi ouvert 1 à 4`

On peut également ne pas utiliser de variable pour l'itération en ajoutant le mot clé \_

&#x20;`for _ in i ... 5 // à la compilation le code s'executera 5 fois`



Nous pouvons effectuer également une for loop en rajoutant le petit mot clé <mark style="color:red;">**stride,**</mark> il nous permettra dans une boucle de passé d'une valeur à une en la spécifiant voici un exemple nous allons parcourir 50 élément et nous allons récupérer uniquement les nombres paires

for element in stride(from: 0, to: 100, by:2)

```swift
 for elementAparcourir in stride (from: 0, through: 50, by: 2)
 {
    
    print(elementAparcourir)
    
 }
 
```

Le <mark style="color:red;">from</mark> signifie a partir d'ou nous souhaitons parcourir la suite de nombre

Le <mark style="color:red;">to</mark>  signifera jusqu'à le dernier élément avant la fin de la valeur donnée

Le through permettra de contourner to et arrivera à la fin de l'ensemble &#x20;

Le <mark style="color:red;">by</mark> Définira dans quel sens nous souhaiterons filtrer dans notre exemple c'est par pair donc deux en deux en partant de 0&#x20;

``

<mark style="color:red;">For each</mark>

Nous pouvons parcourir une liste avec un For Each il est un peu différent d'une boucle for mais il fonctionne pareil mais c'est une méthode propre à chaque collection voici un exemple

```swift

 var montableauDelemnt = ["Ps4","Ps3","PS2","Ps1"]

 montableauDelemnt.forEach(){ Mesconsole in // Nous appelons la méthode ForEach
                                           // Nous nommons notre constante suivi de in comme dans un For classique
                                           
    print("Voici les consoles auquel j'ai joué \(Mesconsole)") // Nous affichons notre constante d'élément du tableau
 }
```

Les deux méthode se ressemble beaucoup prefère celle-ci
