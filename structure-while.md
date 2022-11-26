# structure while

La structure de controle while fonctionne de la meme manière que les langage vu précédemment

comme ceci while condition { instruction dans la boucle }

voici un exemple :&#x20;

```swift
// Some codevar  anneedepoque = 1960
var madatedenaissance = 1998
while anneedepoque < madatedenaissance
{
    print("Tu n'est pas encore ne \(anneedepoque) ")
    anneedepoque += 1 // Incrementation 

}

```

Voici une variante avec <mark style="color:red;">repeat</mark> qui sera executer meme si la condition est fausse&#x20;

```swift
//var  anneedepoque = 1960
var madatedenaissance = 1998
repeat  // On passe obligatoirment dans la condition repeat apres on retourne vers le while
{
    print("on n'ait en \(anneedepoque) tu n'ai pas encore né")
    anneedepoque += 1
    
    
} while (anneedepoque != madatedenaissance)

```
