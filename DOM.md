document //returns the whole document in Chrome developer tools

document.querySelector("h1") //selects the h1 element in DT

document.querySelector("h1").innerHTML="Michael" //set the HTML value to another

document.firstElement //property call

document.getElementsByTagName() //returns an array

document.getElementsByClassName() //returns an array

document.getElementById() //returns one item

document.querySelector("h1") //returns one item, arguments can be a class, id, or name. CSS style must be called with a "." prefixed.   

document.querySelector("li.link")

given the following html:

<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>My Website</title>
    <link rel="stylesheet" href="styles.css">

  </head>
  <body>

    <h1>Hello</h1>

    <input type="checkbox">

    <button style=":active color:red;">Click Me</button>

    <ul id="list">
      <li class="item">
        <a href="https://www.google.com">Google</a>
      </li>
      <li class="item">Second</li>
      <li class="item">Third</li>
    </ul>

  </body>

</html>

document.querySelector("#list")  //select by id 'list'
document.querySelectorAll("#list")  //select by id 'list'
document.querySelector("ul a").style.color='red'  //select by doc structure and set color

document.querySelector("button").style.add("invisible") // add class to the element
document.querySelector("button").style.remove("invisible") // removes class to the element
document.querySelector("button").style.toggle("invisible") // toggles class on the element

document.querySelector("button").textContent

document.querySelector("button").getAttribute

TO add an event listener to an element programmtically , use:

document.querySelector("button").addEventListener("click", handleClick)

assuming

function handleClick() {

}

Note that we do not use the () in the DOM call. Using the () will create a page reload immedialtely, which can result in an infinite loop. 

