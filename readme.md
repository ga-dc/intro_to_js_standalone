# Intro To JS

## Learning Objectives
- Describe the role Javascript plays in a web page.
- Add jquery as a dependency to an html page.
- Use jquery to manipulate elements in a web page.

## Admin
Please go to [http://deadsimplechat.com/](http://deadsimplechat.com/)
That way we can share links and such through this temporary chat room.

## Framing/Expectations
The concept behind this class is to give you exposure to Javascript and the cool things you can potentially do. We will write JS code. We won't learn all things JS. We have a full time 12 week all day web development immersive. Javascript is about 60% of the course material. Our students learn A LOT of JS. Upon leaving the course they'll go on to their jobs in the industry and STILL learn more about JS. This is why developers love the industry they're in, because you'll never know it all! That all said, we'll learn some cool things today to give you a taste of the different things JS can do. Remember the point of today is strictly exposure and NOT to be a JS developer.(though get with me after class if you want to be one!)

## Show a plain old HTML page.
(ST-WG) How many of you out there have worked with HTML/CSS? If so, were there any limitations?

Let's take a look at [this webpage](https://ga-dc.github.io/intro_to_js_standalone/)

Well this is boring. All I can do is read stuff and click on a link that sends me to a different webpage.

## Think-Pair-Share: Identify Javascript features in Cookie Clicker.
* 2 minutes: Go look at [Cookie Clicker](http://orteil.dashnet.org/cookieclicker/) . Play with it. Think about what's allowing these behaviors to exist.
* 2 minutes: Share with person next to you the features you think are being done leveraging javascript.

## Findings
- Interactivity
  - Click something, something happens.
    - Like: increment Like counter.
    - Comment: submit comment, appended to post.
  - Javascript defines what happens on a page depending on how you interact with it.
- No Refreshes / User Experience
  - When I click a cookie, CC is able to increment and update the counter on the page without a hard refresh.
  - When I comment on a post, Facebook is able to process my new comment and render it on the page without refreshing the entire page.
  - Gives the page a much smoother user experience compared to a static page that doesn't have this sort of functionality.
- Communication with a server
  - Javascript is somehow telling a server that (a) a user has done something, (b) save that interaction and (c) display the results of that interaction to all other users.

This is not an exhaustive list of Javascript properties, but we'll go over these and more in more detail later on in the course.

So, to sum up the main three components of front-end web development up in one word each...
- HTML: Structure
- CSS: Styling
- Javascript: Behavior

## A brief history of the web
A long time ago, there was this dude named Tim Berners Lee. He was working for a company called CERN(European Organization for Nuclear Research) at the time. He proposed and developed a system called ENRIQUE the predecessor to HTML. 10 years later HTML was born and became the standard for the world wide web.

Years later, people realized the web needed to be more dynamic. In 1995, Brendan Eich came along and created the Javascript programming language in 10 days.

## Whats a programming language?

- It let's us do things! It lets us act on information, manipulate it, display it, pretty much whatever we want.
- Javascript enables us to do all that in a browser.

## Why is it the dominant programming language of the web?
- Barriers to entry for learning Javascript are very low.
  - No additional software required to run it. Just a text editor and a browser.
- On top of that, it's supported by all web browsers.
- Javascript has evolved since its creation.
  - One of the biggest additions to JS was AJAX, which allows use to reload parts of a page without refreshing the entire thing (just like on Facebook, google maps). Big implications for User Experience.
- A lot of frameworks and libraries -- like backboneJS, reactJS, angularJS and jQuery -- have emerged that enable us to do so much more -- and do it quickly -- with Javascript.

## LES DO EET

### Setup

The first thing I'd like to do is go ahead and create the folder we'll be working in. Go to your finder and create a new folder.

Let's open up that folder in atom now. We can do this by opening atom then clicking on File then Open

Let's create three new files by clicking on File then New File. Save each of these files. The three file names should be `index.html`, `styles.css` and `script.js`.

Fill the index.html with this content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>This HTML</h1>
    <h2>And a bit of CSS</h2>
  </header>
  <main>
    <h3 class="header1">Here's the first block of content</h3>
    <p class="paragraph1">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto corporis tenetur minus quis, voluptates, fugiat consequatur eligendi quia velit unde quam similique, at dolor voluptatem temporibus nesciunt aperiam impedit ullam id dolore ex neque assumenda itaque. Asperiores, illum. Doloribus enim non, dolor asperiores nesciunt. Optio quam rem nulla modi itaque fuga laborum sunt, pariatur voluptates. Repudiandae aspernatur maiores dolore. Sit dolor magni asperiores culpa itaque, possimus ratione rem non sapiente sed et debitis delectus. Pariatur esse in expedita et natus mollitia, eaque, tenetur sapiente repellat eos ex odit veritatis iste corrupti animi non voluptate minima adipisci. Incidunt ea facere libero?</p>
    <h3 class="header2">Here's the second block of content</h3>
    <p class="paragraph2">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto corporis tenetur minus quis, voluptates, fugiat consequatur eligendi quia velit unde quam similique, at dolor voluptatem temporibus nesciunt aperiam impedit ullam id dolore ex neque assumenda itaque. Asperiores, illum. Doloribus enim non, dolor asperiores nesciunt. Optio quam rem nulla modi itaque fuga laborum sunt, pariatur voluptates. Repudiandae aspernatur maiores dolore. Sit dolor magni asperiores culpa itaque, possimus ratione rem non sapiente sed et debitis delectus. Pariatur esse in expedita et natus mollitia, eaque, tenetur sapiente repellat eos ex odit veritatis iste corrupti animi non voluptate minima adipisci. Incidunt ea facere libero?</p>
    <h3 class="header3">Here's the third block of content</h3>
    <p class="paragraph3">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto corporis tenetur minus quis, voluptates, fugiat consequatur eligendi quia velit unde quam similique, at dolor voluptatem temporibus nesciunt aperiam impedit ullam id dolore ex neque assumenda itaque. Asperiores, illum. Doloribus enim non, dolor asperiores nesciunt. Optio quam rem nulla modi itaque fuga laborum sunt, pariatur voluptates. Repudiandae aspernatur maiores dolore. Sit dolor magni asperiores culpa itaque, possimus ratione rem non sapiente sed et debitis delectus. Pariatur esse in expedita et natus mollitia, eaque, tenetur sapiente repellat eos ex odit veritatis iste corrupti animi non voluptate minima adipisci. Incidunt ea facere libero?</p>
  </main>
  <footer>
    <h3 class="header3">Here's a nice link to google.</h3>
    <a href="https://www.google.com"><img src="https://images.google.com/images/branding/googleg/1x/googleg_standard_color_128dp.png"/></a>
  </footer>
</body>
</html>
```

Fill in `styles.css` with this content:

```css
body{
  width: 70%;
  margin: auto;
}

header, footer {
  text-align: center;
  margin-right: 3em;
}

header {
  padding-bottom: 2em;
  margin-bottom: 3em;
  border-bottom: 1px solid black;
}

footer{
  margin-top: 3em;
  padding-top: 2em;
  border-top: 1px solid black;
}
```

Then finally in `script.js`:

```js
console.log("hello world")
var sentence = "this is a string!"
var number = 5 + 5
```

We might not know what this code is doing at the moment. But for now, let's open the index.html file in chrome! You can use another browser, but the developer tools will be slightly different from the ones I'll be using.

Next, let's open the developer tools by hitting `CMD` + `OPT` + `i`.

If your not operating on OSX or chrome, you'll have to google how to open dev tools for your respective Operating system and internet browser. If on windows, its most likely `CTRL` + `SHIFT` + `i` for chrome.

If we then click on console, we can see the words hello world.

- The "Console" is a REPL
  - “Read-Eval-Print Loop”.
  - Programming environment that lets us run Javascript code one line at a time.
  - What does it do?
    1. (R)eads our code.
    2. (E)valuates it.
    3. (P)rints it to the console.
    4. Then it (L)oops back to the beginning, ready to (R)ead the next line of code we feed it.

> The chrome dev tools(if you're using chrome...)are a developers best friend. Here you can do a bunch of stuff like inspect elements and look at the html. More importantly for this class though, is it allows you to access the console which interacts with the JS you loaded to your page.

The console is a wonderful sandbox where we can test out and play with JS code and see immediate results! If we look back at the code we wrote before:

```js
console.log("hello world")
var sentence = "this is a string!"
var number = 5 + 5
```

There are some things happening. Let's break it down.

First:

```js
console.log("hello world")
```

This function `console.log()` allows us to show some text in our REPL.

Next:

```js
var sentence = "this is a string!"
var number = 5 + 5
```

In these two lines of code we're using variables and storing some values in them. Variables are basically buckets in programming with which we can store data.

The first line, `var sentence = "this is a string!"` is storing a string in the variable `sentence`. If we type in sentence into our REPL, we'll see that string pop out! A string is just a sequence of characters delimited(started and ended) by quotation marks.

The next line, `var number = 5 + 5`, is storing the evaluation of `5 + 5`(or 10) into the variable `number`. The thing that's being stored is known as the number data type.

> Numbers and strings have different methods and get treated a bit differently in javascript. IE. there are things you can do with strings that you can't do with numbers and vice versa.

## You do - Try some math operations in the JS console.
Test this code:
```js
5 + 4 * (3 - 1)
```

What does this say about how JS does math operations? (ST - WG)

## User Input (Prompt)
There are many ways to get user input in JS. The easiest way(but probably least common) is to use the `prompt()` function.

Try this out:

```js
var age = prompt("How old are you?")
```

Then type an age into the dialog box. Let's see what happens when we type in `age` and hit enter afterward!

## jQuery

> One thing to note, we'll be using the REPL for alot of this stuff, but know that anything we run in the REPL can be written in our script file and will execute on load of the page!

Great, now that we know the basics, let's do some much cooler things! In order to do these things, let's use the jQuery library. Put this code above the existing script tag in your HTML, that part of your HTML should look something like this:

```html
<script src="https://code.jquery.com/jquery-2.2.2.min.js"></script>
<script src="script.js"></script>
```

> This loads the jQuery library before our script files. Note: All the things we're about to do with jQuery can be done in just plain 'ol JS, but jQuery makes it a bit easier. jQuery's motto is "write less, do more"

The idea of jQuery is very simple. Select something and then do something to it. There are many parallels with CSS and jQuery. We don't know HTML and CSS very well but we do see these `tags` in html. One example is the `<body></body>` tag. So in order to select things in jQuery it will look something like this:

```js
$("body")
```

This would select the body tags. We only have 1 so it will only select 1. If we did something like this:

```js
$("h1")
```

This would select all the `h1` tags.

> ST-WG how would i go about selected the `<h3>` tags?

You'll notice that we have 3 `<h3>` tags. How would we only select 1 of them?

Because these tags have classes we can select them individually by doing this:

```js
$("h3.header1")
```

So if we type this into the console. Something happens in the console but it doesn't DO anything in the actual browser. Let's actually do stuff.

## A quick aside about functions!
In javascript, there's these things called functions. We can call them on things, call them on their own. Some take arguments, others don't. There are lots and lots of rules about functions and honestly we could probably talk about functions for an entire month and still not be able to cover everything. The TLDR version of functions for this class, is that we can call them on things and sometimes we need to give them information. Like this function we're about to be introduced to!

## Changing Text(using `.html()` function)

Well, I guess that's cool, but how do we do stuff to it? Check this out:

```js
$("body").html("WHOA! You can do that!?!??!")
```

You sure can.

> This particular function requires 1 argument. The text that you want to be changed to, as a string

## You do - Change just a header's HTML
Leveraging what we just learned, Use JS/JQ to change the text of the `h2` in our html

## Changing CSS

I guess that kind of cool, but is there moar?! You betcha. Turns out, we can even change the CSS using JS/JQ.

```js
$("h1").css("color", "lemonchiffon")
```

AWWESSOMME!!

> This function takes 2 arguments. The first argument is the property you'd like to change. The second is the value you'd like it to be. Both strings!


> some of you may know CSS. In CSS there are lots of properties and corresponding values. In the case of the function above, the first argument ("color") is the property and the second argument("lemonchiffon") is the corresponding value

## You do - Change the css of a different element.

Select the `<p>` tag in the HTML and add or change a css property to it.

Here's a [list of CSS properties](http://www.blooberry.com/indexdot/css/propindex/all.htm)

## Events
This parts a bit tricky but bear with it, it's really cool! Event listeners are a way for us to add behaviors to a web application that makes it interactive. Let's see the basic syntax of one:

```js
$("h1").on("click", function(){
  console.log("this button got clicked!")
})
```

> We selected an element, in this case a `button`. Then we write this word `.on`(a function). Then some parentheses. The first thing we put in is the thing we want the `button` to listen for. In this case, a `click`. Then in the function block after we want to describe what we want to happen.

You'll notice that when I click the button, we see those words pop into our REPL.

(ST-WG) Are we limited to the types of code we can write in this block of code? IE. can i do other jQuery things in this block of code?

YES

```js
$("h1").on("click", function(){
  $("body").css("background", "blue")
})
```

Cool. This is great, but we barely scratched the surface of the true power of JS and jQuery. I hope you liked this taste!

If you're hungry for more check out these resources:

- [MDN JS Basics Tutorial](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/JavaScript_basics)
- [Tuts Point jQuery Tutorial](http://www.tutorialspoint.com/jquery/)
- [jQuery Documentation](https://api.jquery.com/)
