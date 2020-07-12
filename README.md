# jsNotes

Notes on Javascript

## Store values

``` javascript
var Age = 2;
let name = 'Lamby';
const isDog = 'true';

var userName = prompt('Whats your name?');
var confirmName = confirm('Did you put the correct name?');
```

## Parse a string and return an integer
``` javascript
var yourAge = prompt("Whats your age?"); 
parse(yourAge);
```

## IF / ELSE 

``` javascript
if(userName & confirmName) {
    alert(userName + ' would you like to adopt ' + userName + '?');
} else{
    alert('Refresh the page and enter the correct name');
} 
```

## Writing on the Page



``` javascript
//document.write() overwrites the entire page, so its not usually used.
document.write('Welcome to our page ' + userName);
```

## ARRAYS

``` javascript
//creates animal array
var animals = ["parrots", "cats", "dogs"];
//logs length of animal array
console.log(animal.length);
//log parrot
console.log(animals[0]);
//log dogs
console.log(animals[2]);
//log cats
console.log(animal[1]);
//logs the animal[3]. since theres no animal in that index, undefined is logged.
console.log(animals[animals.length]);
//logs the animal[2] which is dog.
console.log(animals[animals.length - 1]);
//logs the index position for bear. Since bear isn't in the array, -1 is logged.
console.log(animals.indexOf("bear"));
//logs the index position for parrot, which is 0.
console.log(animals.indexOf("parrot"));
```
### Array w/ Functions Example
```javascript
//array of animals
var animals = ["parrots", "cats", "dogs"];
//prompt user to get user's favorite animal
var userGuess = prompt("Which animal is your favorite?");
//converts users answer to lowercase
var userGuessLower = userGuess.toLowerCase();
//checks if its in the array we created 
if(animals.indexOf(userGuessLower) === -1) {
    alert("Nah they are pretty lame.");
} else{
    alert("OMG THEY ARE MY FAVORITE TOO!");
}
```
### Array Printing
``` javascript
var People = ["john", "arnold ", "will ", "esther", " curry", "steph"];

console.log(People[0]);
console.log(People[1]);
console.log(People[2]);
console.log(People[3]);
console.log(People[4]);
console.log(People[5]);
```

### Array value change
``` javascript
// Here we have created our drinks array.
var drinks = ["Coke", "Sprite", "Seltzer", "Pinneapple Juice"];
// We can either overwrite each element of the array to make it lowercase, or we can use the toLowerCase() method.
drinks[0] = "coke";
drinks[1] = "sprite";
drinks[2] = "seltzer";
drinks[3] = drinks[3].toLowerCase();
```
### Loopin Through Arrays
```javascript
var veggies = ["Carrots", "Peas", "Lettuce", "Tomatoes"];

for (var i = 0; i < veggies.length; i++) {
console.log("I love " + veggies[i]);
}
```
### Regular loop vs function version
Regular
``` javascript
var favAnimals = ["Zebra", "Rhino", "Giraffe", "Owl"];

for (var i = 0; i < favAnimals.length; i++) {
console.log(favAnimals[i]);
}
```
Function version
```javascript
// function version
function logArray(list) {
for (var i = 0; i < list.length; i++) {
    console.log(list[i]);
}
}

// same as above
logArray(favAnimals);
```
## Loops
### Loop
``` javascript

// from 0 to 4.
for (var i = 0; i < 5; i++) {
console.log("I can jump " + i "ft high");
}
```
### Hard-loop
```javascript
var myFridge = ["chickens", "pigs", "cows", "horses", "ostriches"];

// Creating a variable to hold our array length.
var arrayLength = myFridge.length;

// Looping through our myFridge array.
for (var j = 0; j < arrayLength; j++) {

// Console out the farm animal in the current index.
console.log(myFridge[j]);

// If the first character in the current animal is "c" or "o", alert the following message.
if (myFridge[j].charAt(0) === "c" || myFridge[j].charAt(0) === "o") {
    alert("Starts with a c or an o!");
}

}
```
## Events
```javascript
// Let's start by grabbing a reference to the <span> below.
var userText = document.getElementById("user-text");

// Next, we give JavaScript a function to execute when onkeyup event fires.
document.onkeyup = function(event) {
userText.textContent = event.key;
};
```
## Objects

```javascript
var info = {
    "city" = "Chicago",
    "state" = "Illinois",
    name = "Justin",
    Asian = true
}

```
### Accessing properties
```javascript
console.log(info["city"])
console.log(info.name)
if(Asian){
    console.log(name + " is Asian")
} else{
    console.log(name + " is not Asian")
}
```

### Property function
```javascript

var car = {

    // Properties of our car object.
    make: "Infiniti",
    model: "EX35",
    color: "Blue",
    mileage: 157000,
    isWorking: true,

    // Creating the driveToWork method.
    // A method is a function associated with an object.
    driveToWork: function() {

        // When we say "this" (as in this.mileage) we are referring to the object the method is a part of.
        // In this case, we will alert the mileage of the car object.
        alert("Old Mileage: " + this.mileage);

        // Adding 8 to the car's mileage.
        this.mileage = this.mileage + 8;

        // Alerting the car's new mileage.
        alert("New mileage: " + this.mileage);
    },

    // The driveAroundWorld method adds 24,000 miles to our car, sets isWorking to false, and makes some alerts.
    driveAroundWorld: function() {

        alert("Old Mileage: " + this.mileage);

        this.mileage = this.mileage + 24000;

        alert("New Mileage: " + this.mileage);
        alert("Car needs a tuneup!");

        this.isWorking = false;
    },

    // The getTuneUp method sets isWorking to true and alerts a message.
    getTuneUp: function() {
        alert("Car is ready to go!");
        this.isWorking = true;
    },

    // The honk method alerts a honking message.
    honk: function() {
        alert("Honk! Honk!");
    }
    };


    // How would we log...

    // The car's make?
    console.log(car.make);

    // The car's model?
    console.log(car.model);

    // The car's mileage?
    console.log(car.mileage);

    // How would we run the car's driveToWork function?
    car.driveToWork();

    // How would we run the car's driveAroundWorld function?
    car.driveAroundWorld();

    // How would we run the getTuneUp function?
    car.getTuneUp();

```