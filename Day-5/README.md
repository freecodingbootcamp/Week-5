# Week-5 -- Day-5

## jQuery - The most Popular JavaScript Library

Simply put, jQuery makes JavaScript simpler and more pwerful at the same time. It's a little bit like saying "brb" instead of writing out "be right back". And just like with most libraries you need to import it first so let's start there.

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

That's it! It doesn't matter whether you load in the head or right before you close the body tag but I do recommend making it the first JavaScript file you load. That's just in case one of the other JavaScript files or libraries use jQuery.

## How to use jQuery

So now you got jQuery you are wondering how to use it. Well, if you are doing any sort of DOM manipulations which is just a fancy way of saying you are going to modify the HTML page using JavaScript (jQuery) you will need for the page to load before running your JavaScript. Here is how you can do it.

    $(document).ready(function(){
    	// Your JavaScript / jQuery code here
    }
You might also see this version of the same function above

    $(function(){  
	    // Your JavaScript / jQuery code here
    });

So whatever JavaScript file you have for you just put this in as the first line. Everything else goes inside of it.

## jQuery = $

jQuery is the $ sign. So when you see $ in JavaScript you should think jQuery.

## First jQuery Example

Here is a super simple jQuery statement that hides all "P" elements

`$("p").hide()`

So any p elements along with it's content will be hidden on the page.

Just like with CSS selectors you can also select elements by id or class names. So

`$(".foo").hide()`
`$("#bar").hide()`

 Simple right?

## More jQuery Examples

### Click event listener

So let's say you want to fire up some JavaScript but only when the user clicks on a button. It's simple:

    $("button").click(function(){
    	alert("You clicked on a button");
    }

The above code will show an alert box with the message "You clicked on a button" everytime somebody clicks on a button...any button!
