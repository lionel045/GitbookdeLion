# Propriété observatrice

Le swift dispose de propriété qui permette. de voir si  propriété à été modifié on utilise le mot le suivant <mark style="color:red;">WillSet et Didset</mark> on pourra voir si la propriété a ete mise à jour par exemple





```swift
    var age : Int = 0 {
    
       willSet(newValue) // Comme avec Set on met la valeur qu'on modifiera
    {
        
       print("Jai maintenant \(newValue)") // On affiche ce message si la valeur a été modifier
    
    }
        didSet
        {
          
          print("Avant j'avais \(oldValue)")   // On affiche la précédente valeur
        }
    
    }
    print(Personnage.age)
     // 0 sera retourner
     
     Personnage.age = 24
     // Un message retournera la nouvelle et l'ancienne valeur et la nouvelle
```
