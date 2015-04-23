###SWABATs

+ perform math with JS
+ declare JavaScript variables
+ declare JS constants
+ understand JS datatypes
+ execute string concatenate
+ utilize string methods
+ execute string concatenate
+ understand datatype conversion and why/when to use it
+ use different types of dialogue boxes like alerts and
+ display text in the console
+ understand comparison and logic operators
+ use conditional statements to control program flow (if/else and switch)
+ DOM - explain what the document object model is and how we can interact with it
+ DOM - understand the tree-like structure of the DOM
+ jQuery - use proper syntax
+ jQuery - how to use selectors and methods together to manipulate the DOM
+ jQuery - how to use jQuery selectors - they are essentially the same as CSS selectors
+ jQuery - understand what jQuery is - a library that helps us interact with the DOM
+ jQuery - set up a document with jQuery


###Motivation
You guys have all of the basics for creating fantastic, responsive web designs. Now for the icing on the cake - using jQuery to add animated and interactive elements.

###Lesson Plan
+ Before we launch right into jQuery there are a few fundamental principles of JavaScript that we are going to have to go over.
+ Variables
	+ A variable is like a bucket that we can store some data inside and then later change the data it stores.
	+ You need to declare variables explicitly in JavaScript with the var keyword like this:
		+ var x; 
		+ //var is a keyword that declares a variable
+ Naming variables: start with letter a-z A-Z remaining 0-9 a-z A-Z, you can also use _ never use spaces ' ' or or illegal characters (! % ?)
+ For variable names consisting of multiple words you should use camelCase or snake_case (camelCase is generally what JS developers use by convention)
+ Let's assign a value in x (remember we said var x; previously)
	+ x = 10;
+ I can refer directly to x and change its value using = symbol
+ We can also declare and assign a value simultaneously.
	+ var y = 20;
+ Declare multiple variables at once using comma separation.
	+ var a = 1,
	+ b = 2, 
	+ c = 3;
+ Perform math on variables
	+ var x = 10, 
	+ y = 20,
	+ 	myMath = x + y;|
+ What does myMath equal? 
	+ x = 5;
	+ myMath = x + y;
+ //What does myMath equal now?
+ Constants
	+ A constant is like a bucket with a lid that is glued shut, and once you store a value inside it, you cannot change that value again.
		+ const STAY_THE_SAME = 1;
	+ Just like var, const is a keyword that declares a constant
		+ STAY_THE_SAME = 2;	
	+ How much does STAY_THE_SAME equal now?
		+ Still equals 1… Always equals 1…
+ <b>What are the types of values that I can store inside of variables?</b>
+ JavaScript data types:
	+ Numbers: integers (whole numbers) like 2, floats (decimals) like 3.56789
	+ Strings: (text) like 'hello' or "hello"
	+ Boolean: true or false
	+ null (empty)
	+ undefined (not yet defined)
+ Checking the data type:
	+ typeof is a keyword that allows us to check the data type.
		+ const STAY_THE_SAME = 1;
		+ typeof STAY_THE_SAME; //reports type of number 
		+ var hamburger = 'Yumm';
		+ typeof hamburger; //reports type of string
+ Concatenation:
	+ JavaScript uses + symbol for math when surrounded by numbers, but when any content is a string, it will concatenate the text. If Boolean and a number: true = 1 and false = 0. So true + 2 = 3… weird huh? This can produce unexpected results unless we are careful how we use + symbol. It’s also good idea to be aware what data types are involved.
		+ var combineStuff = '10' + 5; //string concatenation	
		+ 'Adding a string to a number does this: 		+ '+combineStuff+' weird! ';
		+ This prints 105 weird!
+ String Methods:
	+ String methods can be called on a string to modify the string in some way. Usually you can figure out what a method is going to do just based on its name. Some examples:
	+ //toUpperCase
	+ "Foobar”.toUpperCase(); //returns "FOOBAR"

	+ //toLowerCase
	+ "Foobar".toLowerCase(); //returns "foobar"

	+ //replace
	+ "Foobar".replace("bar", "baz"); //returns "Foobaz"
	+ "Foobar".replace(/o/g, "x"); //returns "Fxxbar"

	+ //method chaining
	+ "Foobar".replace(/o/g, "x").toUpperCase(); //returns "FXXBAR"
+ Data Type Conversion
	+ var stringy = 12 + ' ';
	+ //concatenating empty string changes number to a string.
		
	+ typeof stringy; //prints “string”

	+ combineStuff = parseInt('10') + 5;
	+ //parseInt changes a string to a whole number.
	+ combineStuff; //prints 15

	+ //what the heck happens if I try converting text to a number?
	+ var userName = parseInt('bob'); //returns NaN
	+ //NaN stands for Not a Number!

	+ //what if I want to convert to a floating number instead of an integer?

	+ var gallonsGas = parseFloat('10.25');
	+ gallonsGas; //reports 10.25 as number

	+ //parseInt stops as whole number and ignores characters that are not numbers. 10xffffff same as 10.12345 becomes 10. Where as parseFloat maintains decimal values.
+ Dialog Boxes and JS Console
	+ //alert
	+ alert('warning do not attempt to cook food using this website!');

	+ //confirm
	+ var delete = confirm('Are you sure you want to delete this?'); //true or false

	+ //prompt
	+ var age = prompt('Please enter your age: '); //captures the value inserted.

	+ //log
	+ console.log(age); //reports the age they entered into the JS Console located in the developer too window.
+ Doing math with JavaScript: 
+ Operators
	+ Arithmetic
<img src= "https://s3.amazonaws.com/after-school-assets/jquery.png">
	+ Shorthand Operators
	+ shortcut		original
	+ x += y			x = x + y
	+ x -= y			x = x - y
	+ x *= y			x = x * y
	+ x /= y			x = x / y
	+ x %= y			x = x % y
+ Conditional Statements
	+ Who here has done if then statements in math class? This is a conditional statement.
	+ A conditional statement is a set of commands that executes if a specified condition is true. 
	+ JavaScript supports two conditional statements: if...else and switch.
	+ Use the if statement to execute a statement if a logical condition is true. Use the optional else clause to execute a statement if the condition is false. An if statement looks as follows:
		+ if (condition)
		  + statement_1
		+ [else
		  + statement_2]
	+ Example:
		+ var gasTank = 34; //gallons of gas

		+ if (gasTank === 34) {
		  +   console.log('Tank is full');
		+ } else {
		    +  console.log('Tank is not full');
		+ }
	+ You can see that there are a few syntax details that you’ll need to pay attention to. What is syntax? Syntax is like the grammar of a programming language. There are certain conventions that you need to follow in order for your program to run properly.
		+ JS requires that the conditions in your if statement be surrounded by ()
		+ You’ll need to encapsulate your conditional statement with {}
		+ (almost) every line of JS ends with a ;
+ You can also see that we have a funny looking triple equals. This is how we compare the values of two things. One equal to assign value, triple equals to compare values.
+ Here is a list of all of JS comparison values and what they do
+ COMPARISON Operators
<img src="https://s3.amazonaws.com/after-school-assets/jquery2.png">
	+ We can add additional branches to a conditional statement with the else if keywords like this:
		+ if (gasTank === 34) {
		    + console.log('Tank is full.');
		+ } else if (gasTank > 34) {
		 +     console.log('Oops, tank is overfilled!');
		+ } else {
		  +   console.log(’Tank refill mandatory!');
		+ }
	+ We can also make more complex conditional statements with logical operators, like this:
	+ if (gasTank === 34) {
	  +   console.log('Tank is full.');
	+ } else if (gasTank > 34) {
	 +     console.log('Oops, tank is overfilled!');
	+ } else if (gasTank < 34 && gasTank > 5) {
	 +    console.log(’Tank refill suggested.');
	+ } else {
	  +   console.log(’Tank refill mandatory!');
	+ }
	+ Here is a list of all the Logical Operators and what they do:
<img src="https://s3.amazonaws.com/after-school-assets/jquery3.png">
+ What do I do with my JavaScript. You write out your JS in a .js file and require it in your html files like this:
	+ `<script src="js/myScript.js"></script>`
+ <b>Go to Learn.co and get some practice using js with the Donut App lab.</b>

<b>jQuery</b>
+ Now that you are a little bit familiar with JavaScript it’s time to launch into using jQuery.
+ BUT before we do that we need to talk about something called the DOM. This stands for document object model and it is a structural representation of our HTML in tree form. Like this:
<img src="https://s3.amazonaws.com/after-school-assets/jquery4.png">
+ This model enables us to modify the content and visual presentation on our HTML document with scripting languages such as JavaScript.
+ What kind of things can we do with JS + DOM.
	+ Add/remove/hide/show HTML elements in the page.
	+ Add/remove/change HTML attributes.
	+ Add/remove/change  CSS styles.
	+ Listen for key presses or mouse events upon Elements
	+ Create events in the page.
+ We can select elements on the page like this:
	+ // using “plain old” JavaScript
	+ document.getElementsByTagName("p");

	+ // using jQuery
	+ $("p");
+ And manipulate content like this:
	+ // using “plain old” JavaScript
	+ document.getElementById("foo").innerHTML("hello world");

	+ // using jQuery
	+ $("#foo").text("hello world");
+ You can probably already see how jQuery is going to help simplify your life. Let’s dive right in to learning more about it.
+ So what is jQuery?
	+ jQuery is a JavaScript library
+ What is a library?
	+ A library is a  collection of code that extends the abilities and features of a core programming language, offering additional methods and often simplifying the process to build in that native language.
+ Why use jQuery?
	+ It just works everywhere! jQuery has been written to solve many cross browser issues that exist in core JavaScript.
	+ Terse code. You can often write fewer lines of code than you would in using core JavaScript to accomplish the same thing. Hence jQuery’s slogan “Write Less Do More”.
	+ Popularity. jQuery is currently at the time of writing this by far the most popular JavaScript framework. That means more forums, more code sharing, and more plugins.
	+ Easy extending methods. Coders can create and share their own custom plugins easily.
	+ Familiar DOM selectors. If you already know CSS you’re a step ahead as jQuery uses all our familiar CSS selector statements.
+ Are their other JS libraries out there?
	+ Yes, there are a lot each with their strengths and weaknesses and some are broad, while others suit specific purposes.
	+ At the time of writing this, here are some other popular JS libraries and frameworks:
	+ MooTools, YUI, Prototype, Backbone, Cappuccino, Sammy, Angular, Ext JS, Knockout, Dojo, MochiKit, The M Project, Embed JS, MobilizeJS…etc
+ To setup a document to run jQuery we must link to the jQuery core library first! Imagine that JavaScript is like a pet dog. On it’s own it knows how to eat, sleep, and play. Loading jQuery is like teaching the dog new tricks such as roll over, fetch, etc… Imagine what would happen if we gave the command for our dog to fetch before we had taught it this trick (linked to jQuery). Therefore, we always link to the jQuery core library first.
+ Remote link:
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>`
+ Local link (downloaded from jquery.com):
`<script src=”js/jquery-1.8.2.min.js"></script>`
+ Both using local as fallback solution:
`<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>`
`<script>window.jQuery || document.write('<script src="js/jquery-1.8.2.min.js"> <\/script>')</script>`
+ jQuery syntax	
+ Here is an example of the syntax for using a jQuery method
	+ $(selector).method(parameters);
	+ '$' refers to the jQuery object.
+ 'selector' asks jQuery to go out into the DOM (Document Object Model) web page and select an element(s). In jQuery we can use all of the familiar selectors we use in CSS yay!
+ 'method' these are various actions and commands attached to the jQuery object that allow us to do things like fade elements in an out or change the content of the DOM and much much more
+ 'parameters' are options we can set for each method.
+ An example of real code:
	+ $('h1').css({'background':'yellow'});
	+ '$' refers to the jQuery object.
	+ ’h1' asks jQuery to go out into the DOM (Document Object Model) web page and select all `<h1>`.
	+ ’css' method applies some CSS upon the selected element(s).
	+ '{'background':'yellow'}’ changes the background color to yellow.
+ A few more examples of jQuery selectors:
	+ Select Elements
	 	+ $('h1')
	+ Select ID
		+ $('#nav')
	+ Select Class
		+ $('.celeb')
	+ Select Attribute
		+ $('a[href^=http://]')
	+ Select Descendent(s)
		+ $('#nav li')
	+ Select Child(ren)
		+ $('#nav > li')
	+ Select Sibling(s)
		+ $('h3 + p')
	+ Select by position
	+ $('li:eq(1)') //selects the second list item
+ A few examples of jQuery methods
	+ Effects
		+ animate(), fadeTo(), show(), hide(),  slideToggle()
	+ Events
		+ click(), hover(), focus(), blur(), keypress()
	+ Manipulation
		+ addClass(), clone(), empty(), attr(), val()
	+ Traversing
		+ eq(), each(), has(), closest(), find()
+ If you want to do something to your DOM jQuery probably has a method for it. 
+ YOU DO NOT HAVE TO MEMORIZE ALL OF THE METHODS
+ Having an idea of what possibilities are available is useful, and familiarizing yourself with some that you will use from day to day is useful, unless you’re a jQuery guru you probably will not memorize every method. Fortunately we can look them up and see their usage at sites like:
	+ API: http://api.jquery.com/
	+ Documentation: http://docs.jquery.com/
	+ Or nifty cheatsheets like: http://oscarotero.com/jquery/
	+ and http://overapi.com/jquery
+ How will I know when to use jQuery versus core JavaScript?
	+ Firstly, jQuery is written in JavaScript so you can think of them as variations of the same thing instead of two separate things. To help answer this, jQuery methods are useful for many things; however there are certain fundamental parts of JavaScript that we still need in order to make flexible web applications. For example jQuery on its own does not have method for declaring variables, functions, if statements, or doing math…
	+ This means that we can get a lot more mileage by integrating jQuery with core JavaScript.
+ An example of JS and jQuery working together:
	+ var x = 12, 
	  +     y = 5,
	   +   total = x + y;

	+ If (total === 17) {
	  +    $(’p').text('Correct!');
	+ } else {
	  +    $(’p').text('Incorrect.');
	 + }
+ Set up steps for using jQuery in your websites:
	+  Include link to jQuery core library:
	 `<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>`
	+ Link to your custom js file
	`<script src=”./js/app.js"></script>`
	+ Start your app.js with document ready command:
		+ $(document).ready(function() {
	    	+	// your app code goes here.
		+ });
+ You’ll notice that here we are calling the ready method on the $(document) object and that ready function takes an argument that is another function. This happens a lot in jQuery. One jQuery method that you will probably be using a lot is the .click() method.
+ The .click() method also takes a function as an argument - a function that describes what should be done when that particular part of the dom is clicked. Here is an example (demo this in jsFiddle):
	+ `<button id="alert">Push to Alert</button>`

	+ $(document).ready(function(){
	 +    $('#alert').click(function(){
	  +      alert('hello there');
	   + });
	+ });
+ You can see that we have a button in our dom and when we click that button the .click method performs the action within the function that we’ve given as an argument.
+ We can get even fancier and include jQuery methods within the function. 
+ For instance - what if we want to add some text to our page every time the button is clicked? 
+ We can use a very handy jQuery append method. The append method will add HTML to any piece of the DOM indicated. 
	+ For example if I add `<div id="alert-tracker"></div> `to my dom I can append “alert clicked!” every time the button is pushed and keep track of how many times the alert button has been pushed like this:
	+ `<button id="alert">Push to Alert</button>`

	+ $(document).ready(function(){
	   +  $('#alert').click(function(){
	      +  alert('hello there');
	       + $('#alert-tracker').append("<p>alert clicked!</p>");
	    + });
	+ });
+ Pretty cool, huh! 
+ Now go get some practice with the labs on Learn.co!









