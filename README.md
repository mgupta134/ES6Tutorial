Note: This is imcomplete and examples are not tested yet. 
This information is not intended to teach anyone yet. 
This is just me putting my thoughts together while I commute in train to work. 
Once I have complete information here then I will remove this note.

#ES6 tutorial

Introductory to ES6 features. ES6 or ECMAScript 2015 is a significant update from its last version since 2009. 

##Features
1. Varibales
2. Template Literals
3. Arrow Functions
4. Modules
5. Classes 
6. Computed Properties

##Variables  
###const
Constant variables are immutable variables, whose values can't be changed. 
The value of constant variable will remain the same through out its lifeline. 
When trying to assign the value of constant varibles, you will get run time error.    

`const PI = 3.14;`

###let
let keyword allows you to declare block variables. Scope of this variables are 
limited to the block its declared in. 

```
//TODO: Example
(function(){
    let foo = 'foo';
    if (true) {
        let bar = 'bar'; 
    }
    console.log(bar); //undefined
})

```

##Template Literals
 

```
TODO: Example

console.log(`Hello World!!!
                ES6 is awesome!!!`);
```

```
var a = 5;
var b = 10;

console.log(`My first number is ${a}`);
console.log(`My second number is ${b}`);
console.log(`Sum of these numbers is ${a + b}`);

```

##Arrow Functions

```
TODO: Example

```


##Modules

```
TODO: Example

```


##Classes

```
class Animal{
    constructor(){
        //Properties
        this.legs = 4;
    }

    speak(){
        console.log('I am speak method in Animal class');
    }
}

```

###Inheritance

```
class Cat extends Animal(){
    constructor(){
        super() // Calling constructor method of parent class
        
        //Note: Direct call to super can only be made from constructor method.
    }

    speak() {
        console.log('I am speak methos in cat class');
        //Calling speak method of parent class
        super.speak();

    }
}
```

###Getters Setters
 
 ```
 class Person{
     constructor(name){
         this.name = name;
     }

     get name(){
         console.log('Accessing name...');
         return this.name;
     }

     set name(name){
         console.log('Changing name...');
         this.name = name;
     }
 }

 let person = new Person('Mayank');
 console.log(person.name); //person.name will call get method
 // Accessing name...
 // Mayank

 this.name = 'Gupta'; //This will call set method
 //Changing name...

 console.log(person.name); //person.name will call get method
 
 // Accessing name...
 // Gupta


 ```

##Computed Properties

```
TODO: Example
let foo = 'hello';
let bar = 'world';

let [foo+bar] = 'Hello World!!!';
//Above will create a variable named helloworld

console.log(foo); // hello
console.log(foo); //world
console.log(helloworld); //Hello World!!!

```

```
TODO: Example
let foo = 'hello';
let bar = 'world';

let world = {
    [foo+bar] : 'Hello World!!!'
};
//Above will create a property named helloworld in world object

console.log(foo); // hello
console.log(foo); //world
console.log(world.helloworld); //Hello World!!!
```