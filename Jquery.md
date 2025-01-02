Jquery was borne out of disgust with too much typing Javascript commands.

It uses a short hand for 
    document.querySelector("h1) => $("h1")

In order to use jQuery, it needs to be incorporated in the HTML (just before the script tag for the Javascript) from a CDN:

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>

THe order matters a great deal - this script must be directly above the second script tag.

$("h1")            returns the h1 element
$("button")        returns all of the buttons

As far as changing values goes, we can pass the value to be set as the second value in the method call. FOr example,  

    $("button").css("color", "red")   - sets the value of all buttons' color to red
    $("button").css("color")          - returns the present color of the button

Changing CSS is not a great way to set styles and violates the principle of sepraration of concerns.\

A better way is to add the class to the element.

css:
    .big-text {
        font-size: 10rem;
        font-family: cursive;
    }

Then the jQuery method addClass will add it to the element.

    $("button").addClass("big-text);
    $("button").removeClass("big-text);

Multiple classes are defined in the addClass() declaration separated by spaces.

TO query for a class use hasClass(claz) method.

To change the text of an element use text(text) method:

    $("button).text("Don't click me")

OR use the html() method which allows html tag insertion

    $("button).html("<em>Don't click me</em>")

To add vent listeners, the methods are shorted.

    $("button").click(function () {});

In previous lessons, we set propreties of elements using for loops - e.g. with querySelectorAll. In jQuery this is not necessary as seen above. THus the Javascript used is shortened:

    for (var i=0; i < document.querySelectorAll('.drum').length; i++) {
        document.querySelectorAll('.drum')[i].addEventListener("click", function (event) {
            
            var buttonInnerHTML = this.innerHTML;

            associateKey(buttonInnerHTML);
        });
    }

becomes

    $("button").click(function () {
            var buttonInnerHTML = this.innerHTML;
            associateKey(buttonInnerHTML);
    })

The event listener is added to all buttons on the paege.

To listen for the 'keypress' (or 'keydown') event its done the same way but with the event name - 

    $("input").keypress(function (event) {
            console.log(event.key);
    })

To select the entire document instead of an element in jQuery, use 

    $(document)    WITHOUT THE QUOTATIONS.

https://developer.mozilla.org/en-US/docs/Web/Events

For all of these events you can write an on() listener, and listen to any events listed in the list.

To add elements to the page, use 
    -before()    //$("h1>").before("<button>New</button>") adds the element in front of the tag, e.g. <button>New</button><h1>Hello</h1>
    -after()     // $("h1>").after("<button>New</button>") adds the element after the tag, e.g. <h1>Hello</h1><button>New</button>
    -prepend()   // adds the element into the tag, e.g. <h1><button>New</button>Hello</h1>
    -append()   // adds the element into the tag, e.g. <h1>Hello<button>New</button></h1>

To remove buttons, $("h1>").remove("<button>") will take all buttons away.

Also there is a toggle switch which wil turn the feature on or off.