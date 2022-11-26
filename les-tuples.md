# Les tuples

Un tuple est utilisé pour regrouper plusieurs valeurs dans **une seule valeur composée**

Ils sont couramment utilisés pour renvoyer plusieurs valeurs à partir d'un appel de fonction, et sont devenus très populaires dans la plupart des applications utilisées en production, car ils permettent de regrouper un ensemble de données connexes, telles que le nom d’une personne, son âge et son genre, par exemple. Il faut voir cela un peu comme un dossier où l’on souhaiterait **regrouper des informations de différentes natures.**

**L’idée c’est de se dire qu’on va s’en servir pour pouvoir retourner plusieurs valeurs avec une seule fonction**

Nous allons aborder Les tuples anonyme,Les tuples nommée

Voici un **tuple anonyme**

```swift

let ami = ( "Mete", 25, "Jonathan", 24) // Declaration du tuple

let premierelement = ami.0 // On attribue une constante a chaque index du tableau
let deuxiemeelement = ami.1
let troisieme = ami.2

print(premierelement) // Affichera Mete
```

On les appel tuples anonymes car les élement du tuples sont uniquement accessible par <mark style="color:red;">index</mark> et non par <mark style="color:red;">label</mark>

**Les tuples nommés**

```swift
let ami = ( nom : "Mete" ,age: 25) // création d'un tuple avec des label     
                                   // nom et age
let age = ami.age                // création d'une constante sur le label age
print("Ton frero est \(ami.nom) et il a \(age) ans") 

```

Les tuples nommés par le le biais des labels assurent une meilleurs lisibilité du code&#x20;

On peut également utilisé une fonction pour retourné l'ensemble du tuple

```swift
func retourneTuple()->(name: String,age: Int) //Déclaration de la fonction
                                              // avec le type de retour String et Int
{
    return(name: "Sekou",age: 28) // On retourne l'ensemble de notre tuple
}

let result = retourneTuple() // On initialise une constante sur le tuple
print(result.name) // Et on affiche la valeur qu'on souhaite à partir de la constante
```

* Les tuples permettent à une fonction de pouvoir retourner plusieurs valeurs, et de types différents (ou pas !).
