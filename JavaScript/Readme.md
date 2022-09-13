# JavaScript

## 1. Getting Started - 

### Versions of JavaScript

* ECMAScript 5 - Also known as ES5 [since 2012] 
* ECMAScript 6 - Also known as ES6 [since 2015]
* ECMAScript 6 and beyond

```
    Transpiler - babeljs.io
```

*** 

### Places to tinker with JavaScript

1. Browser-Console [shift+enter - For writting more than one line]
2. Terminal [node]
3. Cmd [node]

***

### Our Friend the text editor 

* Visual Studio Code
* Sublime Text
* Atom
* Brackets
* PhpStorm
* WebStorm
  
***

### Additional helpful resources

> 
    1. ELOQUENT JAVASCRIPT [http://eloquentjavascript.net]
    2. Exploring JS: JavaScript books for programmers [http://exploringjs.com]
    3. You-Dont-Know-JS [https://github.com/getify/You-Dont-Know-JS]
    4. JavaScript: The Good Parts [https://github.com/dwyl/JavaScript-the-Good-Parts-notes]
    5. JavaScript reference [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Refernce]
    6. Can I use [https://caniuse.com]

---


## 2. Variables and Types -

### Declaring and assigning variables

* define = value
* camelCase [eg. typeInfo]
```javascript
> var phone1 = "Apple iPhone 13", phone2 = "OnePlus 10T", phone3 = "Samsung Flip 4";
> phone1
"Apple iPhone 13"
> phone2
"OnePlus 10T"
> phone3
"Samsung Flip 4"
```

***

### Strings

```javascript
Example - "This is a string"
          'This is a string'
          `This is a string`
          "This is \"also\" a string"
          "This is \
           also \
           a string"
```

***

### String properties and methods

```javascript
> var myString = "This is my string";
> myString.length
17
> myString.toUpperCase()
'THIS IS MY STRING'
```

***

### Numbers 

* In JavaScript, all the numbers are same [eg. 15 and 15.0 is same]
```javascript
> 15
15
> 15.0
15
> -15
-15
> Infinity
Infinity
> -Infinity
-Infinity
> NaN
NaN
```

***

### Booleans and the quest for truth

```javascript
> true
true
> false
false
> buttonHasBeenClicked = false;
false
> buttonHasBeenClicked = true;
true
> var myLocation = "Indore", myOtherLocation = "Pune";
> myLocation === myOtherLocation
false
> myOtherLocation = "Indore"
> myLocation === myOtherLocation
true
```

---


## 3. Object, Arrays and More -

### Objects

* Object literal [{}]
```javascript
> {}
{}
> var myEmptyObject = {}
> myEmptyObject
{}
> var notEmptyObject = {
    'label': 'value',
    'label2': 'value2'
}
> notEmptyObject
{ label: 'value', label2: 'value2' }
```

***

### Object for modeling data

```javascript
> var bird = {
    genus: "corvus",
    species: "corvax",
    commonName: "raven",
    callType: "squawky",
    quote: "Nevermore",
    maxOffString: 5,
    noisy: true,
    deadly: false
 };
> bird
{
  genus: 'corvus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false
}
> var bookOfKnowledge = {
    "lunch time": "12:30 PM",
    "the ultimate answer": 42,
    bestSong: "Lonnie's Lament",
    earth: "Mostly harmless"
 };
> bookOfKnowledge
{
  'lunch time': '12:30 PM',
  'the ultimate answer': 42,
  bestSong: "Lonnie's Lament",
  earth: 'Mostly harmless'
}
```

***

### Manipulating Object

```javascript
> bird.quote
'Nevermore'
> bird["quote"]
'Nevermore'
> bird.color = 'black'
'black'
> bird['where it lives'] = 'in a tree';
'in a tree'
> bird
{
  genus: 'corvus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false,
  color: 'black',
  'where it lives': 'in a tree'
}
> delete bird.color
true
> delete bird['where it lives']
true
```

***

### Jargon: References and Objects

```javascript
> var animal = {
    genus: 'corvus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false
}
> animal
{
  genus: 'corvus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false
}
> var animal2 = animal;
> animal2
{
  genus: 'corvus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false
}
> animal2.genus = 'ursus'
'ursus'
> animal2
{
  genus: 'ursus',
  species: 'corvax',
  commonName: 'raven',
  callType: 'squawky',
  quote: 'Nevermore',
  maxOffString: 5,
  noisy: true,
  deadly: false
}
> animal2 = JSON.parse(JSON.stringify(animal));
```

***

### Arrays

```javascript
> var myArray = [];
> myArray
[]
> var daysOfTheWeek = ['S', 'M', 'T', 'W', 'TH', 'F', 'SA'];
> daysOfTheWeek
(7) ['S', 'M', 'T', 'W', 'TH', 'F', 'SA']
> myArray = [0, 1, 2, "string", true, false]
[ 0, 1, 2, 'string', true, false ]
> var arrayOfStuff = [
    {'name': 'value'},
    [1,2,3],
    true,
    'string',
    1
]
[ { name: 'value' }, [ 1, 2, 3 ], true, 'string', 1 ]
> arrayOfStuff.length
5
```

***

### Manipulating Array

```javascript
> var cities = [
    'Kurawar',
    'Indore',
    'Bhopal',
    'Ujjain',
    'Dewas',
    'Pune'
];
> cities
(6) ['Kurawar', 'Indore', 'Bhopal', 'Ujjain', 'Dewas', 'Pune']
> cities[0]
'Kurawar'
> cities[6] = 'Mumbai'
'Mumbai'
> cities[cities.length] = 'Delhi'
'Delhi'
> cities.push('Banglore')
9
> cities.pop()
'Banglore'
> cities.splice(3)
```

***

### Readability: Whitespace

`Prettier [https://prettier.io]`

***

### Readability: Comments

```javascript
Single-line Comments - //
Multiple-line Comments - /* */
```

*** 

### Regular Expression

> 
    Mastering Regular Expression [http://regex.info/book.html]

```javascript
> var string1 = 'This is the longest string ever.';
> var string2 = 'This is the shortest string ever.';
> var string3 = 'Is this the thing called Mount Everest?.';
> var string4 = 'This is the Sherman on the Mount.';

> var regex = /this/; [normal check]
> console.log(regex.test(string1));
  console.log(regex.test(string2));
  console.log(regex.test(string3));
  console.log(regex.test(string4));
false
false
true
false

> var regex = /this/i; [flag i = incencetive]
> console.log(regex.test(string1));
  console.log(regex.test(string2));
  console.log(regex.test(string3));
  console.log(regex.test(string4));
true
true
true
true

> var regex = /^this/i; [flag ^ = carate (check begining of the string)]
> console.log(regex.test(string1));
  console.log(regex.test(string2));
  console.log(regex.test(string3));
  console.log(regex.test(string4));
true
true
false
true

> var regex = /this$/i; [flag $ = dollar (check end of the string)]
> console.log(regex.test(string1));
  console.log(regex.test(string2));
  console.log(regex.test(string3));
  console.log(regex.test(string4));
false
false
false
false
```

---


## 4. Operations and Control Structures

### Simple comparisons

```javascript
> var one = 1, two = 2;
> one === one  //strict equality operator
true
> one === two
false
> one !== one //strict inequality operator
false
> one !=== two
true
> one == one //equality operator [but not strict]
true
> one == "1"
true 
> one != "1" //inequality operator
false
> one < two //relational operator
true
> one <= two
true
```

***

### Arithmetic operators

```javascript
> 1 + 2
3
> 5 - 1
4
> 5 - 9
-4
> 10 / 2
5
> 10 / 4
2.5
> 1 * 5
5
> 19 % 2 // % - Modulus Opertor
1
> 20 % 2 == 0
true
> var count = 0; 
> count = count + 1
1
> count += 1; // += - Addition Assignment Operator
2
> count++ // ++ - unary increment operator
2
> count += 5;
8
> count += -4;
4
> count -= 1; // -= - Subtraction Assignment Operator
3
> count--
3
> count *= 2;
4
> count /= 2;
2
> "aabhash " + "malviya" // + - Concatenate Operator
'aabhash malviya'
```

***

### Logical Operators

```javascript
> var animal1 = "monkey"
> var animal2 = "bear"
> var animal3 = "tiger";

> animal1 === "monkey" && animal2 === "bear" && animal3 === "tiger"  // && - Logical AND operator (return True only, if entire thing need to be true)
true
> animal1 === "ape" || animal2 === "bear" || animal3 === "tiger"  // || - Logical OR operator (return False only, if entire thing need to be false)
true
```

***

### Conditionals: if

```javascript
> var answer = window.confirm("Click OK, get true. Click cancel, get false.");
> answer
true
> var answer = window.confirm("Click OK, get true. Click cancel, get false.");
  
  if (answer === true) {
    console.log('You said true!');
  }
You said true!  // Click OK
> var answer = window.confirm("Click OK, get true. Click cancel, get false.");
  
  if (answer === true) {
    console.log('You said true!');
  } else {
    console.log('You said something else');
  }
You said something else  // Click cancel
> var answer = window.prompt("Type YES, NO, or MAYBE.  Then click OK");
  if (answer === "YES") {
    console.log('You said YES!');
  } else if (answer === 'MAYBE') {
    console.log("You said maybe. I don't know what to make of that.");  // Note the DOuble primes
  } else if (answer === 'NO') {
    console.log("You said no. :(");
  } else {
    console.log("You rebel, you!");
  }
You said YES! // YES
You said maybe. I don't know what to make of that. // MAYBE
You said no. :( // NO
You rebel, you! // else
```

***

### Conditionals: Switch

```javascript
> var answer = window.prompt("Type YES, NO, or MAYBE.  Then click OK");
  switch (answer) {
    case "YES":
      console.log('You said YES!');
      break;
    case "MAYBE":
      console.log("You said maybe. I don't know what to make of that.");
      break;
    case "NO":
      console.log("You said no. :("); 
      break;
    default:
      console.log("You rebel, you!");
      break;
  }
You rebel, you! // Any word other than YES NO MAYBE
```

***

### Terse ifs

```javascript
> var cherub = "Cupid";
> if (cherub === "Cupid") console.log("Ouch, an arrow!  Ooo, I'm in love!");
  else console.log("I feel nothing");
Ouch, an arrow!  Ooo, I'm in love!
```

***

### Ternary operator

```javascript
> var animal = "cat";   // animal = 'dog';
  animal === "cat" 
    ? console.log("You will be a cat herder")
    : console.log("You will be a dog catcher");
You will be a cat herder
var animal = "dog";   
  animal === "cat" 
    ? console.log("You will be a cat herder")
    : console.log("You will be a dog catcher");
You will be a dog catcher
```

***

### Type checking

```javascript
> var thing = 12;
> typeof thing
'number'
> thing = "twelve";
> typeof thing
'string'
> thing = false;
'boolean'
> thing = {}
'object'
> thing = [];
'object'
> typeof NaN
'number'
> typeof null
'object'
> typeof thing === 'object' && thing.hasOwnProperty("length");
true
```

---


## 5. Iterating with Loops -

### For loops: Sequential

```javascript
> for (var i = 0; i < 10; i * 2) {
  console.log(i)
 }
0
1
2
3
4
5
6
7
8
9
```

***

### For loops: Enumerative

```javascript
> var pageNames = [
  "Homes",
  "About Us",
  "Contact Us",
  "JavaScript Playground",
  "News",
  "Blog"
 ];
 for (var p in pageNames) {
  console.log(p, pageNames[p]);
 }
0 Homes
1 About Us
2 Contact Us
3 JavaScript Playground
4 News
5 Blog
> var pages = {
  first: "Homes",
  second: "About Us",
  third: "Contact Us",
  fourth: "JavaScript Playground",
  fifth: "News",
  sixth: "Blog"
 };
 for (var p in pages) {
  if (pages.hasOwnProperty(p)) {
    console.log(p, pages[p]);
  }
 }
first Homes
second About Us
third Contact Us
fourth JavaScript Playground
fifth News
sixth Blog
```

***

### While loops

```javascript
> var i = 0;
  while (i<10) {
    console.log(i + "... This will go until we hit 10");
    i += 1;
  }
0... This will go until we hit 10
1... This will go until we hit 10
2... This will go until we hit 10
3... This will go until we hit 10
4... This will go until we hit 10
5... This will go until we hit 10
6... This will go until we hit 10
7... This will go until we hit 10
8... This will go until we hit 10
9... This will go until we hit 10
> var myArray = [true, true, true, false, true, true];
  var myItem = null;
  while (myItem !== false) {
    console.log("myArray has " + myArray.length + " items now. This loop will go until we pop a false.");
    myItem = myArray.pop();
  }
myArray has 6 items now. This loop will go until we pop a false.
myArray has 5 items now. This loop will go until we pop a false.
myArray has 4 items now. This loop will go until we pop a false.
```

---


## 6. Functions -

### Basic Functions

```javascript
> function speak() {
  console.log("Hii");
  console.log("from");
  console.log("Functions");
}
> speak();
Hii
from
Functions
```

***

### Arguments in functions 

```javascript
> fuddify("Be very quiet, I'm hunting rabbits");
"Be very quiet, I'm hunting rabbits" 
> 
```

***

### More on arguments

```javascript
> function speakSomething(what, howMany) {
  var what = (typeof what !== "undefined") ? what : "Default speech";
  var howMany = (typeof howMany !== "undefined") ? howMany : 10;

  for (var i=0;i<howMany;i+=1) {
    console.log(what + " (" + i + ")");
  }
}

> speakSomething('hey hey', 5)
hey hey (0)
hey hey (1)
hey hey (2)
hey hey (3)
hey hey (4)

> speakSomething('hey hey')
hey hey (0)
hey hey (1)
hey hey (2)
hey hey (3)
hey hey (4)
hey hey (5)
hey hey (6)
hey hey (7)
hey hey (8)
hey hey (9)

> speakSomething()
Default speech (0)
Default speech (1)
Default speech (2)
Default speech (3)
Default speech (4)
Default speech (5)
Default speech (6)
Default speech (7)
Default speech (8)
Default speech (9)
```

***

### Objects, reference, and functions

```javascript
> function transmogrifier(calvin) {
  if (typeof calvin !== "object") {
    console.error("argument is of the wrong type");
    return;
  }

  var randomNumber = Math.floor(Math.random() * 5) + 1;

  switch(randomNumber) {
    case 1:
      calvin.form = "tyrannosaurus";
      break;
    case 2:
      calvin.form = "grey wolf";
      break;
    case 3:
      calvin.form = "bengal tiger";
      break;
    case 4: 
      calvin.form = "grizzly bear";
      break;
    case 5: 
      calvin.form = "canary";
      break;
    default:
      calvin.form = "human body";
      break;
  }
}

> var calvin = {
  name: "Calvin",
  bestFriend: "Hobbies",
  form: "human body"
};

> transmogrifier(calvin)
> calvin
{ name: 'Calvin', bestFriend: 'Hobbies', form: 'grey wolf' }
```

***

### Functions as objects

```javascript
> function speakSomething(what) {
  what = what || "Speaking";

  for (var i=0;i<10;i+=1) {
    console.log(what);
  }
}
hey
hey
hey
hey
hey
hey
hey
hey
hey
hey
> var speakSomething = function(what) {
  what = what || "Speaking";

  for (var i=0;i<10;i+=1) {
    console.log(what);
  }
};

> windows.setTimeout(speakSomething, 5000);

> var obj = { 
  sayHello: function() {
    console.log("hello");
  }
};
> obj.sayHello();
hello
```

***

### Jargon: Scope in JavaScript

```javascript
// Global variable and local variable
> "use strict"; // Global variable

> var // Local variable
```

***

### Variable scope in functions

```javascript
> var myNum = 32;
  var myResult = "Success!";

  function randomizer(limit) {
    var randomNumber = Math.floor(Math.random() * limit);

    var myNum = randomNumber;

    console.log("myNum is", myNum);
    console.log("Global myNum is", window.myNum);

    console.log("Our result is", myResult);

    return myNum;
  }
> randomizer(10)
myNum is 5
Global myNum is 32
Our result is Success!
5
```

***

### Jargon: Callback Function

```javascript
> function doubleIt(number) {
  return (number *= 2);
  }
  var myNumbers = [1, 2, 3, 4, 5];

  var myDoubles = myNumbers.map(doubleIt);
> myDoubles 
[ 2, 4, 6, 8, 10 ]

> myNumbers.forEach(function(number) {
  console.log("My array contains", number);
})
My array contains 1
My array contains 2
My array contains 3
My array contains 4
My array contains 5

> doubleIt = number => (number *= 2);
```

---


## 7. More Advanced Pieces -

### Asynchronous code: The waiting is the hardest part

***

### Promises, async, and await

```javascript
// Callbacks

// with one, it's simple enough
> jQuery.get("https://httpbin.org/get?data=1", function(response) { 
});

// callbacks get nested and infinitum [Callback Hell]
> jQuery.get("https://httpbin.org/get", function(response) {
    jQuery.get("https://httpbin.org/get", function(response) {
      jQuery.get("https://httpbin.org/get", function(response) {
      });
    });
});
```
```javascript
// Promises

// One Promises
> axios.get("https://httpbin.org/get").then(function(response) {
});

// Multiple promises in sequence, no nesting
> axios
    .get("https://httpbin.org/get")
    .then(function(response) {
      return axios.get("https://httpbin.org/get");
    })
    .then(function(response) {
      return axios.get("https://httpbin.org/get");
    })
```
```javascript
// Async / Await

// One request
> async function getOneThing() {
  var response = await axios.get("https://httpbin.org/get");
}

// Multiple request
> async function getLotsOfThings() {
  var response1 = await axios.get("https://httpbin.org/get");
  var response2 = await axios.get("https://httpbin.org/get");
  var response3 = await axios.get("https://httpbin.org/get");
}
```

***

### Object-oriented Javascript: Prototypes and classes

***

### Jargon: Strong vs loose typing

***

### Modern Javascript tooling


```javascript
// Dynamic Imports
import {myHelper} from helperFunction
```

>
  `Popular Modern JS tools-`
  1. Webpack 
  2. Rollup
  3. npm
  4. yarn
  5. babel
  6. typescript [transpiler]




