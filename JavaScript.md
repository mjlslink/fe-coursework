
splice(begin, end);

Math.floor(num);

Math.round(num);

Math.pow(base, exponent);

MAth.random() //16 place decimal, 0 inclusive
   - Math.round(2.345 *100) / 100 = 2.35

=== / !=== cares about datatyle, 1 === "1" yields false

== does not care about data type

&&, ||, !

Lists
  - [] denote a collection
     e.g. var guestList = ['Michael', 'Angela', 'Jack']
- guestList.length: number of elements in array 
- guestList.includes('Alisa') gives false.
- guestList.push('Ryan') adds this item to the end of the array

So if I have arbitrary DOM operations in my script file(call it index.js), the only thing necessary to get them to run is to include the script in a script tag:

  <script src="index.js" charset="utf-8"></script>

When this tag is executed the script's content will also execute.

higher order functions take a function in their parameter list, 
that is used for further calculation.

In Chrome, use 'debugger' command to enter debug mode.

function add(num1, num2){
    return num1+num2;
}
function subtract(num1, num2){
    return num1-num2;
}
function multiply(num1, num2){
    return num1*num2;
}
function divide(num1, num2){
    return num1/num2;
}
function modulo(num1, num2){
    return num1%num2;
}
function calculator(num1,num2,operator) {  //higher order function
    return operator(num1,num2);
}
