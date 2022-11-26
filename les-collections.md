# Les collections

Il en existe 3 types de collections

Les tableaux(Array)&#x20;

Les dictionnaire(dictionnary)

Les ensemble((set)



Pour déclarer un <mark style="color:red;">tableau array</mark> vide voici la syntaxe



`var Nomdutableau : [Type] = []`&#x20;

pour déclaré un tableau avec des éléments :

var Nomdutableau : \[Type] = \[Index0,Index1,...]

Pour ajouter un élément dans notre tableau nous utiliseront <mark style="color:red;">append</mark> et <mark style="color:red;">insert</mark>

<mark style="color:red;">Voici un exemple :</mark>&#x20;

<pre class="language-swift"><code class="lang-swift"><strong>
</strong><strong>var montableau:String = ["Farine","Blé","Lait"] // Déclaration de notre tableau
</strong><strong>
</strong><strong>montableau.apend("sucre") // l'élément sucre sera ajouté au tout dernier index du tableau 
</strong><strong>                          // après le lait
</strong><strong>
</strong><strong> // Pour insert c'est beaucoup plus flexible car on choisis l'index ou notre élément sera ajouté                                             
</strong><strong>
</strong><strong>montableau.insert("Beure",at:0) // Le beurre sera ajouté a l'index 0 
</strong><strong>
</strong>
</code></pre>

<mark style="color:red;"></mark>

Pour supprimé un élément nous utiliserons la méthode <mark style="color:red;">remove</mark> qui nous permettra de choisir l'index qu'on souhaite supprimé

```
montableau.remove(at:1) // La farine sera supprimé
```

Pour parcourir un tableau nous utiliserons la boucle For qui comptera chaque élément de notre tableau voici un exemple

{% code lineNumbers="true" %}
```swift
var Famille : [String] = ["Frere","Soeur","Pere","Mere"]

for Iteration in Famille // Creation d'une variable de porter locale qui
                        // Itéra chaque élement du tableu
{
    print("Bonjour \(Iteration)") // Chaque élément sera parcouru avec préceder du mot Bonjout
} 
```
{% endcode %}

Les dictionnaires :&#x20;

Un dictionnaire fonctionne avec le principe de clé, valeur chaque clé est unique on ne peut avoir deux fois la même clé voici comment déclaré un Dictionnaire en swift :

```swift
var Famille : [String: Int] = ["Frere" : 26,"Soeur": 24,"Pere":62 ] 
 // Déclaration d'un dictonnaire avec pour clé une chaine de caractère et en valeur 
 // un Int
 
 // Déclaration d'un tableau vide
 
 var Dico = [CLé: Valeur]  =  [:]  // Déclaration d'un dictionnaire vide
 
 var DicoDeux = [Clé : Valeur] = () // Deuxieme manière pour déclarer un tableau vide
```

Pour ajouter un élément ou modifier un élément il nous suffis simplement de sélectionner la clé qu'on souhaite modifié

```swift

var Famille : [String: Int] = ["Frere" : 26,"Soeur": 24,"Pere":62 ] 
 Famille["Frere"] = 27 // Modification de la valeur de la clé frere
 
 Famille["Petit fils"] = 2 // Création de la clé petit fils qui n'exsite pas et sera
                           // donc insérez 

// Pour Supprimé une valeur

 Famille.removeValue(forKey: "Pere") // Nous supprimons la clé Pere



```

Pour parcourir chaque élément de notre dictionnaire on n'utilisera la boucle For

```
var Famille : [String: Int] = ["Frere" : 26,"Soeur": 24,"Pere":62 ] 

For (cle,valeur) in Famille
{

    print("Voici la valeur \(valeur)") // Cela affichera la valeur de la clé
    
    print("Voici la clé \(cle)") /// Cela affichera la clé
}



```
