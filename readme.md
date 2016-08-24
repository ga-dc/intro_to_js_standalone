# Intro To JS

## Learning Objectives
- Describe the role Javascript plays in a web page.
- Add jquery as a dependency to an html page.
- Use jquery to manipulate elements in a web page.

## Admin
Please go to [http://deadsimplechat.com/](http://deadsimplechat.com/)
That was we can share links and such through this temporary chat room.

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

Fill in `styles.css`
