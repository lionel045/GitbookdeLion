# Propriété calculé et propriété privé

Pour bien comprendre la notion d'orienté objet en swift nous allons voir les propriétés calculés aussi appelé Accesseur dans les autre langage et nous permettra de respecter les principe d'encapsulation notamment lorsqu'on disposera d'une <mark style="color:red;">propriété privé</mark> que l'on souhaiterais afficher ou bien modifier nous utiliserons Get ou Set voici des exemples exemple :&#x20;

```swift
class perso {
     
     // Propriété
    private var _nom : String // Déclaration d'une propriété privé n'est pas accessible sur par l'utilisateur
     
   private var _prenom : String
     
     //Méthode 
     
     func Afficherprenom() -> Void
     { 
          print("Tu t'appel donc \(_prenom)")
     }

     // Propriété calculé (Getter et)
    
    var AfficherPrenomnom : String 
    {
    get 
    {
        return _prenom + " " + _nom. // Nous allons afficher le nom et le prenom dans notre exemple
    }
    }
```

Pour utiliser un setter nous seront obliger d'utiliser get en prefixe ou en suffixe&#x20;

```swift
class perso {
     
     // Propriété
    private var _nom : String // Ces variables seront initialisé à chaque création d'une instane d'objet
     
   private var _prenom : String
     
     
       // Propriété calculé (Getter et Setter)
   
        var modifierPrenom: String // On crée la propriété qui nous permettra de modifié notre propriété privé
        {
            set(newvalue) // Paramètre qu'on utilisera lorsqu'on modifira la propriété
                       {
                    _prenom = newvalue
                           
                           } 
            get
            {
             return (_prenom) // Cela nous permettra d'affchier la valeur de la variable en lecture 
            }
           
        }
        
    init(nom: String,prenom: String) //Utilisation du constructeur
    {
        
        self._nom = nom
        self._prenom = prenom
        
        
    }      
}
        

```

