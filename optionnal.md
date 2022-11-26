# Optionnal



* Un optionnel est un type qui permet à une variable d’être utilisée sans valeur.
* Si l'optionnel n'a pas de valeur on dis qu'il détient la valeur nil
* Il faut se représenter un optionnel comme un paquet cadeau qui contient :
  * soit une valeur du type indiqué ;&#x20;
  * soit rien.

Voici deux méthode recommander permettant de déballer un optionnel&#x20;



La première avec la condition <mark style="color:red;">**If let**</mark>&#x20;

```swift
var ValeurdeLoptionnel : String? = "Je suis un optionnel " 
// Déclaration d'une variable de type optionnel 


print(ValeurdeLoptionnel)
if let deballage = ValeurdeLoptionnel // Création d 'une variable local qui p
                                       // permettra de deballer l'optionnel 
                                        
{
    print(deballage)    
    
}
```

L'utilisation de cette technique est assez simple pour déballer un optionnel mais la variable qui permettra de déballé l'optionnel aura une portée local et ne pourra pas être utilisé dans tout le code.



Deuxième méthode l'utilisation de <mark style="color:red;">guard let</mark>

```swift

var ValeurdeLoptionnel : String? = "Je suis un optionnel "

print(ValeurdeLoptionnel)

func deballetoi( Valeuradeballer: String?  ) -> String? 
// Création d''une fonction qui déballera les optionnel de type String?
{
   guard let deballage = Valeuradeballer  // Creation d'une constante qui recupéra
                                      // La valeur de l'optionnel si il n'est pas vide 
    else{
        return nil // Si l'optionnel est vide on retournera alors nil
    }
    print(deballage) // On affiche notre optionnel deballer
    return deballage
}

deballetoi(Valeuradeballer: ValeurdeLoptionnel) // Notre optionnel. sera déballer

```

Cette méthode permet de crée une variable qu'on pourra réutiliser <mark style="color:red;">**guard**</mark> permet de vérifié si la condition est correcte des son Initialisation elle est plus recommandé lorsqu'on veut déballé plusieurs optionnel

&#x20;

Voici d'autre méthode non recommandés

```swift
                         
var ValeurdeLoptionnel : String? = "voila" 

if ValeurdeLoptionnel != nil  // On vérifie que l'optionnel ne vaut pas nul
                             
{
    print("la variable n'est pas vide ")
    print("l'optionnel contient \(ValeurdeLoptionnel!)") //  et on la deballe avec !
}


```

Une autre méthode avec la <mark style="color:red;">**ternary**</mark> (if,else) expression elle a l'aire différente mais elle est similaire au autre

```swift
var ValeurdeLoptionnel : String? = "voila" // Déclaration de l'optionnel


let valeurdeballe = ValeurdeLoptionnel != nil ? ValeurdeLoptionnel! : ""

// On declare une constante qui est égale a l'optionnel si (?) celui n'est pas vide 

// Sinon (!) nous retournons une chaine vide

```

Cette méthode nous permettra de convertir notre variable optionnel en structure et pourra être réutiliser dans le code



Voici la dernière méthode avec l'utilisation d'un opérateur <mark style="color:red;">**nil-coalescing**</mark>

```swift
var ValeurdeLoptionnel : String? = "Nonvide"




let recuperation = ValeurdeLoptionnel ?? "" // ?? est l'opérateur nil-coalescing
                                           // Si la valeur est nil il attribuera lui meme la valeur ""                    
```



* Un optionnel est un type qui permet à une variable d’être utilisée sans valeur.
* Dans le cas où l’optionnel ne contient pas de valeur, on dit que sa valeur est  `nil`  .
* Il faut se représenter un optionnel comme un paquet cadeau qui contient :
  * soit une valeur du type indiqué ;&#x20;
  * soit rien.
* Un optionnel doit donc être déballé, selon de différentes méthodes :
  * Une première méthode sécurisée  et recommandée qui permet d’accéder à la variable par la création d’une nouvelle variable.
  * Une deuxième méthode sécurisée  et recommandée qui permet d’accéder à la variable par la création d’une nouvelle variable, et qui sera réutilisable en dehors de la scope.
  * D'autres méthodes existent, mais ne sont pas recommandées.
* Lorsqu’on accède aux valeurs d’un dictionnaire avec une clé, le dictionnaire renvoie un optionnel et non la valeur directement.
