# Switch et Where

Le switch permet d'eviter d'utiliser des condition else if il est pratique lorsque qu'on a plusieurs choix et on souhaite simplement récupérer un résultat voici un exemple



{% code lineNumbers="true" %}
```swift
var Semaine = readLine() ?? "" // Déclaration d'un optionnel avec 
                              // Une entré saisi utilisateur


switch Semaine // On declare notre structure switch avec la valeur de l'utilisateur saisis
{
case "Lundi": // Si la saisis correspond à Lundi 
    print("On est \(Semaine)") // Ce message sera alors affichier
    
case "Mardi":
    print("On est \(Semaine)")
    
default:
    print("Salut") // Si aucune saisis correspondante a ete faite ce message sera renvoyer
}
```
{% endcode %}

Nous allons essayer de découvrir le mot clé <mark style="color:red;">**where**</mark> il nous permettra de parcourir un sous ensemble d'élément et nous fera gagner du temps lorsque qu'on voudra récupérer un sous ensemble dans une collection

{% code lineNumbers="true" %}
```swift
let names = ["Tom Jedusor", "Taylor Swift", "Tom  Cruise", "Chris Hemsworth", "Tom Hiddleston"]

for name in names where name.hasPrefix("Tom") // On parcour normalement notre tableau
//On rajoute apres le in le 'where' dans notre exemple on veut parcourir tout les élément portant en suffixe Tom
{
    print(name) // Chaque élément ayant pour préfixe tom sera itérez
}

```
{% endcode %}

&#x20;on peut aussi utilisé <mark style="color:orange;">**Where**</mark> dans la structure switch

```swift
let age  = readLine() ?? "" // On recupère l'age de l'utilisateur


let conversionage = Int(age) ?? 0 // La valeur de l'utilisateur sera un optionnel
                                 // On convertis la chaine de caractère en Int 



switch conversionage    // On teste plusieur cas en fonction de la saisi de l'utilisateur
{
case 1...19 where conversionage  < 20:  // On test plusieur cas par le biais ...
                                        // on cherche toute les valeurs en dessous de 20
    print("Tu as donc moin de 20 ans")
    
case 20...24 where conversionage < 25: // on verifie toute les valeurs entre 20 et 24
    print("Tu est un jeune adulte décidéments")
    
default:
    print(conversionage)
}

```

Pour résumé:&#x20;

* `Where`  filtre facilement les valeurs :
  * `for where`  permet de filtrer une liste.
  * `switch where`  permet de vérifier des conditions supplémentaires.
