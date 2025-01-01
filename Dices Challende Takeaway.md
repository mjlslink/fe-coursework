In this challenge I began by imagining how the images would be randomly chosen and 
took a look at the images/ inside the Dice Challenge+Starting+Files/. Them it was clear 
that a random number generator that chose +-6 appended onto the file name would role the dice 
and could be used to select the img.

So how to wire it up? My first error of judgment was to create a separate function. This had a side effect - it had to be called somehow. My first attempt was to use the onload() event of the DOM and to pass it the name of the function. BUT: 
     - the script had to have been loaded by the browser
     
        <script src="setDice.js" ></script>  

     - there must be a call to the script.
My submission involve including an onclick() to both images, which were initial set for player 1 to images/dice5.png and for player 2 to images/dice6.png. 

I wired the script using:

<script src="setDice.js" ></script>

and create a function 

function chooseRandomDice() {
    //choose a random number from 1-6
    var imgNum = Math.floor(Math.random() * 6) + 1;
    var img = document.getElementsByClassName("img1")[0];

    img.src = "./images/dice" + imgNum + ".png";

    //do this again so that both dice are kept in sync
    var imgNum2 = Math.floor(Math.random() * 6) + 1;
    var img = document.getElementsByClassName("img2")[0];

    img.src = "./images/dice" + imgNum2 + ".png";

    //make a judgement using the numbers
    if (imgNum > imgNum2) {
        document.querySelector("h1").innerHTML = "Player 1 Wins!";
    } else if (imgNum < imgNum2) {
        document.querySelector("h1").innerHTML = "Player 2 Wins!";
    } else {
        document.querySelector("h1").innerHTML = "Draw!";
    }
}

Two tags were included in the index.html using the onclick() event handler:

<div class="dice">
        <p>Player 1</p>
        <img class="img1" src="images/dice6.png" onclick="chooseRandomDice()"/>
      </div>

<div class="dice">
        <p>Player 2</p>src
        <img class="img2" src="images/dice5.png" onclick="chooseRandomDice()"/>
      </div>


In conclusion:

1)
<script src="setDice.js" ></script> should have been <script src="index.js" ></script> 
   -- does the script get loaded automatically when it is called index.js?

2) Using a function required the need to call it using a DOM event. I chose onclick().

3) The code using the document.getElementByCLassName call but it could have called document.querySelctorAll("img") on the img tag and then just referred using array notation. This would make the code DRYer.