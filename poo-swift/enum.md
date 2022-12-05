# Enum

Un enum permet de définir plusieurs cas et peut s'utiliser comme une Structure voici comment déclarer un **Enum**&#x20;

{% code lineNumbers="true" %}
```swift
enum Etablissement {
    case eleve, professeur, parentdeleve, directeur 
}
```
{% endcode %}

La structure est similaire à un  switch pour déclarer une variable voici la syntaxe&#x20;

{% code lineNumbers="true" %}
```swift
enum Etablissement {
    case eleve, professeur, parentdeleve, directeur 
}
 let varecuperer : Etablissement = .Valeurducase // Fonctionne uniquement lorsque l'on connait le type
```
{% endcode %}

&#x20; Pour amélioré l'efficacité de notre code nous pourrons parcourir notre Enum

avec switch nous pourrons étudier plusieurs cas voici un exemple :&#x20;

```swift


var etablishement : Etablissement = .eleve // On initialise notre variable de type 
                                        //Etablissement                   

switch etablishement  { // On verifie  notre varibable par le biais du switch 
case .directeur: 
 print("Voici le directeur")

case .eleve:
print("Voici l'élève ")

case .parentdeleve:
print("Voila les parents d'élève")

case.professeur:
    print("Voici le professeur")
}
 // La variable par défaut de etablishement est donc  "Voici l'élève "

```
