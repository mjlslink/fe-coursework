Objects in Javscript are structured datasets.

var Dog = {
    name: "Spot",
    age: 3,
    breed: "Dalmation",
    isHungry: true,
    favoriteToys: ["bone", "ball", "squeaky toy"]
}

Names must be capitalized.

Constructors can also be used:

function Dog(name,age,breed,isHungry, favoriteToys) = {
    this.name = name;
    this.age=age;
    this.breed=breed;
    this.isHungry=isHungry;
    this.favoriteToys = favoriteToys;
    fetch: function () {
        alert("Fetching);
    }
}

var dog1 = new Dog("Spot",3,"Dalmation",true,["stick", "chew toy", "ball"]); 

Methods can also be added to the object:


function Housekeeper(name, occupation, salary, favoriteAnimal) {
    this.name = name;
    this.occupation = occupation;
    this.salary= salary;
    this.favoriteAnimal=favoriteAnimal;
    this.clean = function  () {
        alert("Cleaning");
    }
}

var housekeeper2 = new Housekeeper("Filda", "Housekeeper", 33455, "Dog");

THere are some caveats - in Chrome, this is not retroactive. Only new objects created after the 
method addition have the method available. Also note that the method is defined as a proprty of 
the object with an anonymous function.





