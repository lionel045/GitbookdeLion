# Init constructeur

Un constructeur permet d'initialiser un objet ainsi que ses propriété&#x20;

En Swift pour initialiser un constructeur nous utiliserons le mot clé <mark style="color:red;">Init</mark>:

voici un exemple avec une déclaration d'une classe&#x20;

```swift
class perso 
{
    var nom: String

    var prenom: String

init(nom:String, prenom:String) // Déclaration du constructeur ainsi que les étiquettes
                                // Qui permettront d'initialiser les variables de notre objets
        
        
        self.nom = nom  // utilisation du self signifie

        self.prenom = prenom


    }

}
 
 var objet = perso(nom:"Diallo",prenom:"Sekou")  // Création de notre objet avec pour valeurs
                                                 // comme nom Diallo et comme prénom Sekou

 print(objet.nom)

```

