# Fonction

En swift nous allons voir la syntaxe pour déclarer une fonction&#x20;

voici un premier exemple d'une fonction qui ne renvoie rien

{% code lineNumbers="true" %}
```swift
func mafonction (parametre: Int) -> Void // Declaration de la fonction de type void 
                                         // Prenant en paramètre une variable de type void                     
{

 print("Tu as donc \(parametre) ans") 

}



```
{% endcode %}

Vous remarquerez que la syntaxe est un peu différente en swift on donne la possibilité dans les paramètre d'une fonction d'écrire au préalable une <mark style="color:red;">etiquette</mark> qui permettra de clarifier ce que prendra comme type et nom de notre fonction

{% code lineNumbers="true" %}
```swift
func mafonction (age: Int) -> Void 
{

 print("Tu as donc \(age) ans")

}

  var age = readLine() ?? "" // Recupération de l'age de l'utilisateur

   let deballage = Int(age) ?? 0 // Deballage de l'optionnel en le castant en Int

mafonction(age: deballage) // Utilisation de l'etiquette dans le code principale pour clarifier le code 

```
{% endcode %}





