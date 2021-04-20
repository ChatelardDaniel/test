# Développeur Full-Stack Skilleos 63h

## 1 Javascript 30h

### 1 Les fondamentaux 4h24

## <span style="color: yellow"> Les bases de Javascript </span>

### la console du navigateur

ctrl + shift + i

#### Où écrire Javascript ?

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="style.css">
        <title>Document</title>
    </head>
    <body>
        <!--Dans la balise script avant la balise de fermeture de </body>-->
        <script src="script.js"></script>
    </body>
</html>
```

#### Syntaxe et variable

```javascript
 var name = "John";

 console.log(name);
```

#### Number et Strings

```javascript
    var name = "John"; /* variable de type string, double guillement ou simple*/
    var x = 12; /* variable de type number */
    var xToString = x.toString(); /* passer une variable number en string */
    var nameLength = name.length; /* longueur de la variable */

    console.log(name);

    console.log(xToString);

    /* transforme une string en number avec parseInt()*/
    var xString ='12';
    var xNumber = parseInt(xString); /* ne fonctionne pas pour les décimales,retourne un entier */
    var xNumber = parseFloat(xString);/* pour les décimales */

    console.log(xNumber);

    /* Savoir la position d'une string avec indexOf() */
    var myString = 'Hello John';
    var position = myString.indexOf("John");
    console.log(position);

    /* Remplacer une string par une autre avec replace() */
    var myString = 'Hello John';
    var newString = myString.replace("John", "Tim");
    console.log(newString);

    /* Concaténer une chaine de caractère 'string' */
    var string1 = 'Hello';
    var string2 ='John';
    var myNewString = string1 + " " + string2;
    console.log(mynewString);

```

#### Les Opérateurs (operators)

```javascript
 var x = 5; /* égal est l'affectation de 5 à la variable x */

 var x = 10 % 3; /* % est égal au modulo, affichera le rest de la division */

 x++ /* incrémentation de 1, racccourci de x + 1 */

 x-- /* décrémentation de 1 raccourci de x - 1 */

 var x = 12;
 var y = 5;

 x += y /* Raccourci de x = x + y */ 
 x -= y /* Raccourci de x = x -y */
 x *= y /* Raccourci de x = x * y */
 x /= y /* Raccourci de x = x / y */
```

#### Les commentaires

```javascript
/* Les commentaires servent à expliqué le code ou pour ne pas executer certaines lignes de code*/
 // double slash, commentaire sur une seule ligne
 /* slash plus étoile,
  étoile plus slash, 
  commmentaire sur plusieurs lignes*/ 
```

#### Les booléens et comparaisons

```javascript
// Les Booleans
var myBoolean = true; 
console.log(myBoolean);

// Les Opérateurs de comparaison

// x est-il strictement égal à 5 avec '===', vérifie la valeur et le type de la variable
var x = 5;
var egal = (x === 5);
console.log(egal); // renvoie true

// x est-il strictement différent de 5 avec '!===', vérifie la valeur et le type de la variable
var x = 5;
var dif = (x !== 5);
console.log(dif);// renvoi false

// x est-il simplement égal à 5 avec '==', vérifie la valeur mais pas le type de la variable
var x = 5;
var egal = (x == "5");
console.log(egal); // renvoie true

// x est-il supérieur à 12 avec '>'
var x = 5;
var sup = (x > 12);
console.log(sup); // renvoie false

// x est-il supérieur ou égal à 12 avec '>='
var x = 5;
var sup = (x >= 12);
console.log(sup); // renvoie false

// x est-il inférieur ou égal à 5 avec '<='
var x = 5;
var inf = (x <= 5);
console.log(inf); // renvoie true

// x est-il strictement inférieur à 5 avec '<'
var x = 5;
var inf = (x < 5);
console.log(inf); // renvoie false

// x est-il supérieur à 5 et y est-il inférieur à 15 avec '&&' 'and'
var x = 5;
var y = 12
var supAndInf = (x > 3 && y < 15);
console.log(sup); // renvoie true si les deux conditions sont vrai, sinon il retourne false

true && true = true
true && false = false
false && true = false
false && false = false

// x est-il supérieur à 5 ou y est-il inférieur à 15 avec '||' 'or'
var x = 5;
var y = 12
var supAndInf = (x > 3 || y < 10);
console.log(sup); // renvoie true si l'une des deux conditions sont vrai

true || true = true
true || false = true
false || true = true
false || false = false

// 'Le Not' est l'inverse de quelque chose avec '!'
!true = false
!false = true

```

#### Les conditions avec 'if' 'else if' 'else'

```javascript
// syntaxe du if seule 'si'
if(condition est vrai) {
    éxecute ce code;
}

// syntaxe du if avec else, 'si' condition est vrai, éxecute le code1 'sinon', éxecute le code2
if(condition est vrai) {
    éxecute le code1;
} else {
    éxecute le code2;
}

// syntaxe du if avec else if et else
if(condition est vrai) {
    éxecute le code1;
} else if(condition2){
    éxecute le code2;
} else {
    éxecute le code3;
}

// syntaxe du if avec else if et else, exemple
var speed = 80;
if(speed <= 80) {
    console.log("tu roule à la bonne vitesse");
} else if(speed === 100){
    console.log("il faut que tu ralentisse");
} else {
    console.log("tu roule trop vite !");
}
```

#### Les conditions avec 'switch'

```javascript
// syntaxe
switch(variable) {
    case1:
        break;
    case2:
        break;
    case3:
        break;
    default:
}

// exemple
var favoriteColor = "blue";

switch(favoriteColor) {
    case "blue":
        console.log("Le bleu c'est trop beau");
        break;
    case "red":
        console.log("Le rouge c'est beau");
        break;
    case "green":
        console.log("Le vert c'est jolie");
        break;
    default:
        console.log("Je ne connais pas t'as couleur");
}
```

#### Les boucles

```javascript
// La boucle 'while'
var number = 0;

while(number < 3) {
    console.log(number);
    number++; // incrémentation pour éviter une boucle infinie
}

// La boucle 'do while', on éxecute une première fois le 'do' puis le 'while'
var number = 0;

do {
    console.log(number);
    number++;
}
while(number > 0 && number < 3)


// La boucle 'for'
//syntaxe
for(initialisation; condition; incrémentation) {
    code à éxecuter;
}

//Exemple
for(var number; number < 5; number++) {
    console.log(number);
}
```

#### Les fonctions

```javascript
// syntaxe pour déclarer une fonction
function name(paramètre1, paramètre2, etc...) {
    code à éxecuter
    return result;// elle peut reourner ne valeur
}

//exemple
function multiply(number1, number2) {
    return number1 * number2
}

// Utiliser la fonction
var a = 5;
var b = 6;
// Appel de la fonction avec les arguments a et b
var result = multiply(a,b);
console.log(result);
```

#### Le scope

```javascript
// Le scope
function multiply(number1, number2, number3) {
    var resultMultiply = number1 * number2 * number3;
    return resultMultiply
}

var a = 5;// c'est une variable global, elle est connue dans toute la page
var b = 6;// cette variable est aussi global

var result = multiply(a,b,a);
console.log(resultMultiply);// renvoi une erreur, resulMultiply is not defined, parce que les fonctions on un scope local, étant donné que la variable 'resultMultiply' est déclarée dans la fonction, elle est connue que dans la fonction, pas à l'extérieur de la fonction

// si on enlève le mot clè 'var' dans la fonction alors 'resulMultiply' devient global, mais pas conseillé de faire comme ça
function multiply(number1, number2, number3) {
    resultMultiply = number1 * number2 * number3;
    return resultMultiply
}

var a = 5;// c'est une variable global, elle est connue dans toute la page
var b = 6;// cette variable est aussi global

var result = multiply(a,b,a);
console.log(resultMultiply);// elle est devenu global, suite à la suppréssion de 'var' dans la fonction 'multiply'

```

#### Les Tableaux 'arrays'

```javascript
// arrays
//syntaxe déclaration d'un array
var name =[valeur1, valeur2, valeur3, etc....]

//exemple
var fruits = ["Pomme", "Banane", "Orange", "Citron"];

// Savoir la taille d'un array avec 'length'
console.log(fruits.length); // affichera 4 puisque j'ai quatres valeurs dans le array 'fruits

//Accéder à une valeur dans un array avec '[index]
console.log(fruits[0]);// l'index d'un array commence toujours à zéro, il affichera Pomme
console.log(fruits); // affichera ["Pomme", "Banane", "Orange", "Citron"] tout le array

// Parcourir un array avec une boucle 'for'
for(var i=0; i < fruits.length; i++) {
    console.log(fruits[i]); // affichera Pomme Banane Orange Citron
}

// Ajouter une valeur à la fin d'un array avec la méthode 'push()'
fruits.push("Kiwi");
console.log(fruits); // affichera ["Pomme", "Banane", "Orange", "Citron", "Kiwi"]

// Enlever la dernière valeur dans un array avec la méthode 'pop()'
console.log(fruits); // affichera avant le pop() ["Pomme", "Banane", "Orange", "Citron"]
fruits.pop(); // ne prend pas de valeur entre les parenthèses
console.log(fruits); // affichera après ["Pomme", "Banane", "Orange"]

// La méthode slice()
var fruits = ["Pomme", "Banane", "Orange", "Citron", "Kiwi"];
var agrumes = fruits.slice(2,4); // (2 inclus, 4 non inclus)
console.log(agrumes);// affichera ["Orange", "Citron]

var agrumes = fruits.slice(2); // si je met qu'un seul argument, il affichera tout ce qui sera après la deuxième valeur
console.log(agrumes);// affichera ["Orange", "Citron", "Kiwi"]

// On peut mettre ce que l'on veut dans un 'array'
var myArray = ["Pomme", 15, true];
console.log(myArray); // affichera ["Pomme", 15, true]

// On peut faire un 'array' dans un 'array'
var myArray = [[0, 1], [5, 7, 8], [12, 18]];

// comment avoir la valeur 8
console.log(myArray[1][2])// [1] deuxième array, [2] troisième valeur du deuxième array 
```

#### Les Objets

```javascript
// Les Objets
// syntaxe d'une déclaration d'un Objet
var Object = {
    propertyName1: propertyValue1,
    propertyName2: propertyValue2,
    propertyName3: propertyValue3,
    method1: function() {
        code de la fonction;
    }
    };

// Exemple
var dog = {
    name: "Choupette",
    color: "white",
    age: 4
};

// Accéder à une propriété d'un objet
console.log(dog.name); // accés au name, affichera Choupette
console.log(dog.color); //  affichera white
console.log(dog.age); //  affichera 4
// ou bien
console.log(dog["name"]); // affichera Choupette
console.log(dog["color"]); // affichera white
console.log(dog["age"]); // affichera 4

// Comment faire une boucle pour lister toutes les propriété d'un objet
for(var property in dog) {
    conole.log(dog[property]); // affichera Choupette white 4
}

// On peut aussi créer un objet avec le constructor 'new Object()'
var dog = new Object();
dog.name = "Choupette";
dog.color = "white";
dog.age = 5;

for(var property in dog) {
    console.log(dog[property]); // affichera Choupette white 5
}

// Ajouter la méthode aboie
var dog = new Object();
dog.name = "Choupette";
dog.color = "white";
dog.age = 5;
dog.aboie = function() { // déclaration de la méthode aboie
    console.log("Wouaf Wouaf")
};

// Executer la fonction aboie
dog.aboie(); // affichera Wouaf Wouaf
```

#### Les prototypes

```javascript
// Les prototypes
// Création du prototype Dog
function Dog(name, color, age) {
    this.name = name;
    this.color = color;
    this.age = age;
}

// Utiliser le prototype pour créer une instance de Dog
var petitCaniche = new Dog("Choupette", "white", 4);

console.log(petitCaniche); // affichera, Dog {name:"Choupette", color: "white", age: 4}

// Créer un nouveau chien
var grosPitbull = new Dog("Rex", "black", 2);

console.log(grosPitbull); // affichera, Dog {name:"Rex", color: "black", age: 2}

// Ajouter une méthode à notre prototype
// Création du prototype Dog avec une méthode aboie
function Dog(name, color, age) {
    this.name = name;
    this.color = color;
    this.age = age;
    this.aboie = function() {
        console.log("Wouaf" + this.name);// this.name affichera le name qui aboie
    }
}
// Utiliser le prototype pour créer une instance de Dog
var petitCaniche = new Dog("Choupette", "white", 4);

// utilisation de la méthode aboie
petitCaniche.aboie(); // affichera, Wouaf Choupette
```

### 2 <span style="color: yellow"> Techniques avancées</span> 9h18

### Les différents types de variables

```javascript
// Les Booleans
console.log(true);
console.log(false);

// Les nombres
console.log(5);

// Strings
console.log("Hello Word !");
console.log('Hello Word !');

// undefined
console.log(undefined);

// Null
console.log(null);

// Object
console.log({name: "John"});
```

### Les différences entre undefined, null et is not defined

```javascript
// undefined
var a;

console.log(a); // affichera undefined, la variable existe mais aucune valeur ne lui est assignée

// null

var selectedObject = {
    name: "John"
};
console.log(selectedObject);
selectedObject = null; // pour mettre à zéro une variable par un codeur
console.log(selectedObject);// affichera null

// is not defined
console.log(b); // affichera, b is not defined,  la variable n'est pas déclarée

```

### Hoisting

```javascript
// hoisting, ça veut dire hisser vers le haut, quand javascript fait une première lecture du code , il voit les déclaration de fonction et les hissent en haut donc dans sa deuxième lecture c'est comme-ci la déclaration de la fonction était écrite avant son utilisation.
addition(5, 7);

function addition(a,b) {
    console.log(a + b); // affichera 12 le résultat de 5 + 7
}

//On a mis une fonction anonyme dans une variable, là ça ne fonctionne pas car ce n'est pas du hoisting de fonction.il faudra éccrire l'appel de la fonction addition(5,7) après son assignation dans la variable addition.
addition(5, 7);// pas bon

var addition = function(a,b) {
    console.log(a + b); // affichera une erreur, addition is not a function
}
addition(5, 7);// ok, maintenant ça marche.

// Le hoisting de variable

console.log(x); // affichera undefined
var x = 5;
//javascript à fait
var x;// il a pris que var x; la déclaration mais pas l'assignation de la valeur
console.log(x);// c'est pourquoi il affiche undefined
x = 5;
```

### Types primitifs et objects

```javascript
// Les Types primitif, sont copié par valeur
boolean
number
string
undefined 
null
// Exemple
var x =5;
console.log(x);
// dans la mémoire, il crée une boite nommé 'x' et met dedans '5'

// Exemple2
var x = 5;
var y = x;
console.log(x);// affiche 5
console.log(y); // affiche 5
// maintenant il crée une boite nommé 'y' et met la valeur de la boite 'x' dedans

// Exemple3
var x = 5;
var y = x;
y = 8;
console.log(x); // affiche 5
console.log(y); //affiche 8

// Les Objects, sont copiés par références
array
object

// Exemple
var x = { name: "John" };
console.log(x);
// javascript crée deux boites, dans une il met l'objet et dans l'autre il met la référence à l'objet grâce à un pointeur qui pointe vers l'objet.

// Exemple2
var x = { name: "John" };
var y = x;// 'y' aura un pointeur vers le même objet que 'x'

console.log(x); // affichera John
console.log(y); // affichera John

// Exemple3
var x = { name: "John" };
var y = x;// 'y' aura un pointeur vers le même objet que 'x'
y.name = "Codeur";
console.log(x); // affichera Codeur
console.log(y); // affichera Codeur
// On a changer la propriété name de l'objet, comme ils pointent toutles deux vers la même référence cela modifiera 'x' aussi.

// Exemple3
var x = { name: "John" };
var y = x;// 'y' aura un pointeur vers le même objet que 'x'
y = { name: "Codeur" };
console.log(x); // affichera John
console.log(y); // affichera Codeur
// 'y' va créer un nouvel espace mémoire pour cet objet, donc 'y' ne pointera plus vers 'x' mais vers le nouvel objet.
```

### Let et const (ES6)

```javascript
// let
let x = 5;
console.log(x); // affichera '5'

// const doit obligatoirement assigner à une valeur lors de sa déclaration, elle ne peut pas être réassigné.
const x = 7;
console.log(x);

const x = { name: "john" };
x.name = "Codeur";
console.log(x); // affichera Codeur, car nous pouvons modifier les propriété d'un objet

const x = { name: "john" };
x = { name: "Codeur"}; // je veux lui donné un nouvel objet
console.log(x); // affiche une erreur car on ne peut pas lui assigner un nouvel objet

// le hoisting ne fonctionne pas avec let et const
```

### let, const et var

```javascript
// Rêgles
// 1 ne plus utiliser le 'var'
// 2 toujours utiliser le 'const'
// 3 si on réassigne une valeur à une variable utilisé le 'let'
```

### Contexte d'exécution

il y a la phase de création et la phase d'éxectution.
il est constitué de trois choses.

1.Objet des variables, c'est toutes les variable, les fonctions qui vont être défini dans se bout de code dans ce contexte d'éxecution.
2.La chaine des scopes, c'est toutes les variables auquel pourra accéder notre bout de code.
3.Le this, c'est l'objet qui sera associé à notre bout de code.

### L'objet des variables

 L'objet des variable on le crée et l'initialise pendant la phase de création du contexte d'exécution.
 Que va t'il contenir ?
 1.Les arguments de la fonction qu'on exécute.
 2.il va chercher les déclarations de fonction avec la règle du hoisting. il va mettre les fonctions dans l'objet des variables.
 3.Les déclarations de variables avec la règle du hoisting.

```javascript
 // Exemple
// VOglobal = Objet des Variable( On cherche les arguments des fonction, puis on cherche les déclarations de fonction, ensuite on cherche les déclarations des variables)
// avant de commencer la première ligne, je crée le contexte d'exécution global, puis je liste en fonction des règles (1, 2, 3) vu plus haut.
 var name = "John";// (2) 'name' dans VOglobal phase de création (initialisé à undefined) (3)phase d'exécution de VOglobal ('name' contient John).
// (1) fonction first dans VOglobal
 function first() {//  pas d'argument, pas de déclarationde fonction, déclaration de variable (oui).
     var a = "Hello";// (5) 'a' dans VOfirst phase de création (initialisé à undefined), (7)phase d'exécution de VOfirst (a contient 'Hello').
     second();// (8) nouveau contexte d'exécution, on crée un objet des variable 'VOsecond'
     var x = a + name;// (6) 'x' dans VOfirst phase de création (initialisé à undefined),(20)phase d'exécution de VOfirst (x contient 'Hello John').
 }// (19) fin du contexte d'exécution first

// (1a) fonction second dans VOglobal
 function second() {
     var b = "Hi";// (9) phase de création, on met 'b' dans 'VOsecond' et et il est initialisé à 'undefined', (11)phase d'exécution de VOfirst (b contient 'Hi').
     third();// (12) nouveau contexte d'exécution, on crée un objet des variable 'VOthird'
     var y = b + name;// (10) phase de création, on met 'y' dans VOsecond et il est initialisé à 'undefined', (18)phase d'exécution de VOfirst (y contient 'Hi John').
 }// (19) fin du contexte d'exécution second
 
// (1b) fonction third dans VOglobal
 function third() {
     var c = "Hey";// (13) phase de création, on met 'c' dans 'VOthird'  et il est initialisé à 'undefined', (15)phase d'exécution de VOfirst (c contient 'Hey').
     var z = c + name;// (14) phase de création, on met 'z' dans 'VOthird' et et il est initialisé à 'undefined', (16)phase d'exécution de VOfirst (z contient 'Hey John').
 } // (17) fin du contexte d'exécution third

 first();// (4) lorsqu'on exécute une fonction, on crée un nouveau contexte d'exécution 'VOfirst', que contient t-il? voir la fonction first.

 ```

### Chaine des scopes

Une fonction enfant peut accéder au scope de la fonction parent déclarer.

```javascript
// scope global
var name = "John";

// function first() est déclaré dans le scope global, il aura accès au scope 'VOglobal' et 'VOfirst'
function first() {
    var a = "Hello";
    second();
    var x = a + name;
}

// function second() est déclaré dans le scope global, il aura accès au scope 'VOglobal' et 'VOsecond'
function second() {
    var b = "Hi";
    third();
    var y = b + name;
}

// function third() est déclaré dans le scope global, il aura accès au scope 'VOglobal' et 'VOthird'
function third() {
    var c = "Hey";
    var z = c + name;
}

first();

// Exemple2
//VOglobal
var a = "Hello";
first();
// scope VOfirst t VOglobal
function first() {
    var b = "Hi";    
    second();
    // scope VOsecond et VOfirst et VOglobal
    function second() {
        var c = "Hey";
        console.log( a + b + c );
        third();
    }
}
// scope VOthird et VOglobal, mais pas aux autres
function third() {
    var d = "Hola";
    console.log( a + b + c + d );// on ne peut pas avoir accès à 'b' et 'c'
}


// une fonction déclarée dans un autre fonction à accès à son scope, c'est le principe de la chaine des scopes

// L'ordre dans la chaine des scopes, il part du scope courant jusqu'au scope global.

```

### Scope de bloc ES6

```javascript

// Les variable avec let et const respectent le scope de bloc, un bloc commence et se termine par une accolade. { bloc }

//Exemple
function first {// bloc
    let a = 5;
}

if(true) {// bloc
    let a = 5;
}

for(let i=0; i < 0 ; i++) {// bloc
    console.log(i);
}

//Exemple2
 function first() {// bloc parent
     let a = 5;
     if(a > 3) {// bloc enfant
         conole.log(a);
     }
 }

 first();

var // à un scope de fonction
let // à un scope de bloc

// le bloc enfant connaît les variable du bloc parent, mais le bloc parent n'a pas accès aux variables qui sont déclarer dans un bloc enfant.

```

### Fonction première classe

### 3 Rendre un site interactif 6h57

### 4 ES6 et ES7 6h21

### 5 Introduction aux frameworks 1h46

## 2 Angular 4h59

## 3 React JS 8h01

## 4 Node.js 3h18

## 5 VueJS 3h53

## 6 MongoDb 2h53

## 7 MEAN Stack 8h41
