# Intro to DOM Programming and Just Enough JavaScript

## Introduction

JavaScript can do many kinds of work, from building web servers, to creating
"infinite scroll" effects, but it was originally designed to do a type of
programming called **Document-Object Model (DOM) programming**. Understanding
DOM programming is the foundation of front-end development.

DOM programming is using JavaScript to:

1.  Ask the DOM to find or `select` an HTML element or elements in the rendered
    page
2.  Remove and/or insert an element(s)
3.  Adjust a property of the selected element(s)

## Learning Goals

1.  Explain the JavaScript / DOM relationship
2.  Explain "sight words"
3.  Explain "just enough JavaScript" concept
4.  Write experimental code in Chrome DevTools
5.  Explain that JavaScript has things
6.  Explain that JavaScript has `variables`
7.  Explain that JavaScript can compare things
8.  Explain that JavaScript has `collections`
9.  Explain that JavaScript is object-oriented
10.  Explain that JavaScript has `loops`
11. Explain that JavaScript `logs` with `console.log`

### Explain the JavaScript / DOM Relationship

JavaScript changes are made through a middle layer called the DOM, the
Document Object Model. The DOM only knows how to be spoken to in JavaScript.
JavaScript and the DOM have been there, together, since the beginning.

Because they're twins, learning about the DOM will require us to write some
JavaScript &mdash; which we don't know yet! And learning all the details of
JavaScript language won't tell us anything about the DOM. It would just tell us
how to write valid JavaScript code. It's a chicken-and-egg situation.

To get around this problem we start by learning some basic structures of
JavaScript called "sight words." We're going to learn "just enough JavaScript"
so that we can start working with the DOM &mdash; the best way to understand it.

### Explain "Sight Words"

When you learned to read before you understood the process of joining letters
into sounds and sounds into words, you had a limited, but powerful vocabulary.
This vocabulary contained your "[sight words][sight]." These are also the words
you tend to memorize before you go on a trip abroad: MEN, WOMEN, WATER, FOOD,
HOSPITAL.

This lesson will provide you the "sight words" of JavaScript. Some of these
lines of code you might not fully understand at first and that's OK. We'll
cover them all later in more depth.

### Explain "Just Enough JavaScript" Concept

We call the approach of learning JavaScript sight words "just enough
JavaScript." We learn so much better by working with technology than by merely
reading words.

We take this approach because it's just more fun, as well as being much more
effective. It's fun to change the text on pages or update the styling. Also,
some of the JavaScript concepts tend to sneak in along the way and make
learning easier.

It's OK to come back here if you get confused or forget something. You might
want to bookmark this page or keep it open in a tab as you move along. This is
all OK in the "just enough" approach. In the following sections, we list several
"sight words" of JavaScript. If you want to know more about a sight word, feel
free to consult [MDN's JavaScript Reference][ref].

### "But Wait, Where's the (Boring) Basics Chapter on Data Types and Stuff Like That?"

You might have looked at other programming languages' courses that start with
(boring) introductory, contrived examples to teach you basics of the language.

We _could_ tell you, for example:

> An `Array` is a data structure that holds a series of memory-contiguous data elements which can be accessed via an index, an integer, which starts at `0`. Here's an example: `arrayOfDogs = ["Byron", "Boo", "Luna"];` `"Boo"` is at index `1` and we can retrieve that value with `arrayOfDogs[1]`"

We'd then go on to list all sorts of things you need to know about `Array`s. How to get their length, how
to iterate over their members, etc.

Then, sometime later, we'd then expect you to understand that when we say
"`document.querySelectorAll()` returns an `Array` of DOM nodes" that you should "re-load"
and re-apply all those previously seen lessons onto the results of this method call.

But we _don't_ do that here. That's not the way human brains work.

We want you to work with an `Array` &mdash; not a contrived example with a list of Flatiron
team's dogs' names. We want you to see _for yourself_ what it's good for in the environment you'll
most often need it in. You'll see what it can help you do _first_ and _then_ cover the theory. If
you've learned programming languages elsewhere, this might feel a bit funny at first. Try
out this approach!

### Write Experimental Code in Chrome DevTools

It's impossible to overstate how important practice is when you're learning a
new programming language. You can read the READMEs and watch the videos, but the
true education is in writing code — _lots_ of it.

As you move through the JavaScript curriculum, you should almost always have a
browser console open, either on the lesson page or in a separate window. Code
along with every example. Get used to the syntax and familiarize yourself with
the errors that arise when you mistype something. Clear the console or simply
refresh the page whenever you need a clean slate. Code, code, **code**,
**code**, ***code***.

Every major browser comes with a built-in set of developer tools that you can
use to inspect, modify, and debug the content of a web page.

***NOTE:*** To ensure that instructions and screenshots match up with your
experience, use [Google Chrome](https://www.google.com/chrome/index.html) browser.

To [open the dev tools in Chrome](https://developers.google.com/web/tools/chrome-devtools/console/#open_as_panel
), press `Ctrl+Shift+J` (Windows / Linux) or `Cmd+Opt+J` (Mac). Chrome ships with a whole suite of useful dev tools, but the only one we care about for now is the JavaScript console.

The console is an environment in the browser where we can type and run arbitrary
JavaScript code in the context of the current browser window. The console is
_sandboxed_, meaning the only resources it has access to are those loaded on the
current page. Once we start declaring variables and functions in separate
JavaScript files, we'll be able to access and play around with them in the
console. The console is the single best tool for debugging JavaScript in the
browser, so start familiarizing yourself with it now.

The `Ctrl+Shift+J` / `Cmd+Opt+J` command should open up straight into the
console. If for whatever reason, it doesn't, you can always click on `Console`
in the dropdown (when the dev tools are collapsed) or in the list of tabs:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" alt="Opening the console">
</picture>

To access the Chrome dev tools settings — for example, to change the theme from
light to dark — click the three vertical dots:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" alt="Changing the theme">
</picture>

If at any point the console becomes cluttered with errors, warnings, or anything
else, click the `Clear console` button:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" alt="Clearing the console">
</picture>

Okay, okay, enough background and setup. Let's write some code!

### Coding

We'll start off with some simple math. In the console, type `1 + 1` and press
enter. You should see the number `2` appear.

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" alt="Math in the console">
</picture>

You just wrote and ran your first line of JavaScript code!

The code you wrote, `1 + 1` is an _expression_. In JavaScript, an expression is **[a valid unit of code that returns a value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Expressions)**. The value that it returned, `2`, is aptly referred to as the **return value** of the expression. Try out some more mathematical expressions and see what they return!

Next up, let's write some text. To make sure the JavaScript engine knows that we're trying to write some literal text, we need to wrap it in quotation marks, like so:

```js
"This is some literal text in JavaScript!"
```

Go ahead and type that classic phrase, `"Hello, world!"`, into the console and
press enter. It returned `"Hello, world!"` right back to us. Try typing some
more literal text into the console, such as your name. Don't forget the
quotation marks!

<img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/text_in_console_300.gif" alt="Text in the console">


### Explain that JavaScript Has Things

It might sound a bit weird to say, but there are "Things" in JavaScript. Most
programming languages call these "types." For the moment we're going to call
them **Things**.

One type of Thing is a `number` like `2` or `3.14`.

Another type of Thing is an arrangement of characters, called a `string` like
`"Byron"` or `'Please feed the dog'`. `String`s are written inside of `"` **or** `'`.
Strings are quoted because `if` might mean something very special to
JavaScript but it also might be the beginning of a bit of
text "if you can keep your head when all about you are losing theirs..." `if`,
in this case is a _reserved word_ &mdash; something special to JavaScript. The
`String` is, well, just some text.

### Explain that JavaScript Has Variables

Sometimes you want to hold a `String` or a `Number` under another name.

> **TYPOGRAPHICAL NOTE**: The `//=>` means "What JavaScript would return back".
> For now, think about what's "returned back" as an answer to a question that
> you're asking JavaScript. Sometimes, too, you tell JavaScript a fact and it
> will just return it to you.

_Any time we give you a JavaScript example, feel free to try it out in the
Chrome JavaScript console that is included in the DevTools yourself! To open the
console, you can use the keyboard shortcut of command + shift + c, or go to
View, then Developer, and Developer Tools. Make sure the Console tab is selected
at the top. Copy the first part of the example - the part after the // is
showing you what the return value will be, which you will see in the console!_

```javascript
3.14; //=> 3.14
var pi = 3.14; //=> `undefined`
pi; //=> 3.14
```

JavaScript also lets you say:

```javascript
3.14; //=> 3.14
let pi = 3.14; //=> `undefined`
pi; //=> 3.14
```

or

```javascript
3.14; //=> 3.14
const pi = 3.14; //=> `undefined`
pi; //=> 3.14
```

When JavaScript first came out it had only `var`. Now it has `let` and `const`
too. We'll cover the differences between these later. They all tell JavaScript,
"Hey! This is a name that I'm going to associate with some bit of information."

#### Explain that Mathematic Operations Can Be Performed on Numbers

`Number`s can be added, subtracted, multiplied and divided, and the
results of these operations can be stored in variables:

```javascript
1 + 1; //=> 2
let result = 1 + 1; //=> `undefined`
result; //=> 2
let pi = 3.14; //=> `undefined`
let radius = 2; //=> `undefined`
let circumference = pi * (radius * 2); //=> `undefined`
circumference; //=> 12.56
10 / 4; //=> 2.5
```

JavaScript also has a symbol for finding the remainder when one `Number` is
divided by another:

```javascript
10 % 4; //=> 2
13 % 5; //=> 3
```

#### Explain How Strings Can Be Manipulated

Just as `number`s can be added together, it is possible to add `string`s
together as well:

```javascript
'Ya got trouble, folks, right here in ' + 'River City';
//=> 'Ya got trouble, folks, right here in River City'
let poolTable = 'Trouble';
poolTable + ' with a capital T';
//=> 'Trouble with a capital T'
```

Dynamically combining `string`s and variables is very common in JavaScript, so
much so that multiple methods exist for combining `String`s. Another method
is to use `concat`:

```javascript
'And that rhymes with '.concat('P');
//=> 'And that rhymes with P'

let lyric = 'And that stands for ';
let trouble = 'pool!';
lyric.concat(trouble);
//=> 'And that stands for pool!'
```

You can also use what are known as [Template Literals][literals]:

```javascript
let pool = 'trouble';
//=> undefined
`Ya got ${pool}, ${pool}, ${pool}, ${pool}, ${pool}...`;
//=> 'Ya got trouble, trouble, trouble, trouble, trouble...'
```

To use Template Literals in your `string`s, you _must_ wrap the entire `string`
in _backticks_, not quotation marks. Instead of using `+` to combine, a variable
is wrapped in brackets preceded by a dollar sign, `${}`, then included _within_
the backticks. Inside these brackets, you can include variables or any other
Things that can be converted into a `string`.

```javascript
`Adding two and two equals ${2 + 2}`;
//=> 'Adding two and two equals 4'
```

### Explain that JavaScript Can Compare Things

```javascript
1 < 3; //=> true
3 == 3; //=> true
3 != 4; //=> true
5 > 2; //=> true
```

Be careful here, `=` means "assign to," like we did with `var` just above. For
comparison we use `==` and `===`.

We can build on our previous example:

```javascript
3.14; //=> 3.14
const pi = 3.14;
pi; //=> 3.14
pi == 3.14; //=> true
```

### Explain that JavaScript Has Conditionals

With the ability to compare things, we are able to build logic into our
code using `if` statements:

```javascript
let test = 1;
test; //=> 1

if (test < 2) {
  // test is less than 2.
  // this statement is true so the code within the brackets is executed
  test = test + 1;
}

test; //=> 2

if (test < 2) {
  // test is NOT less than 2.
  // this statement is false so the code within the brackets is ignored
  test = test + 1;
}

test; //=> 2
```

The code inside an `if` statement's brackets will only be executed if the
statement, in this case `test < 2`, is `true`.

We can expand our `if` statement to do one thing or another using `else`:

```javascript
let test = 1;
test; //=> 1

if (test < 2) {
  test = test + 1; // test is less than 2
} else {
  test = 0;
}
test; //=> 2

if (test < 2) {
  test = test + 1;
} else {
  test = 0; // test is NOT less than 2
}
test; //=> 0
```

### Explain that JavaScript Has Collections

Sometimes a `variable` might point to a Thing which actually has multiple Things
inside of it. In programming vocabulary, these collection-Things are called
`Array`s. So technically, `Array` belongs with `String` and `Number`.

```javascript
slytherins[0]; //=> "Salazar Slytherin"
slytherins[1]; //=> "Bellatrix Black"
slytherins[2]; //=> "Draco Malfoy"
```

In JavaScript, `arrays` start at `0`. In America, the floor where you walk in is
called the `1` floor (or first floor). In most of Europe and the rest of the
world, the floor where you walk in is called something else. Arrays are like
that - they start at `0`.

As seen above, we can get one of the elements of a collection by putting `[]` after a
collection's name and putting a number inside of the `[]`. In the example, we get
the `String` names of some wizards stored in a collection of wizards identified
by the name `slytherins`.

### Explain that JavaScript is Object-Oriented

When working with the DOM in JavaScript, many of the Things you encounter are
objects. `Objects` are bits of code you can talk to that know state and
behavior. `Objects` should round out our universe of JavaScript Things along
with `arrays`, `strings`, and `numbers`.

When talking to an `object` you can ask it for a bit of state by using a `.`
and then that state's name. You can trigger behavior by using a `.` and then
the behavior's name followed by `()`. Due to the `.` being the separator
between the object-name and the state or behavior name, we call writing code
this way "dot-notation."

The thing that holds a bit of state is known as a property. This all sounds a
bit confusing, but it's a bit simpler than it sounds. To ask, say, an
adorable poodle its `name` state, you would do it like so:

```javascript
poodle.name; //=> "Byron"
```

If you ask an object for a property it doesn't have, JavaScript says
`undefined`

```javascript
poodle.favoritePainter; //=> undefined
```

When asking an object to do something (a behavior), you use a `.` and a
behavior-name (usually a verb) followed by `()`. Behaviors on objects are
called methods.

```javascript
poodle.bark(); //=> An ear-splitting bark is heard
```

`Objects'` methods have access to all of that `object's` properties.

```javascript
poodle.introduceYourselfFormally(); //=> "Hello, my name is Byron the poodle"
```

In this case, the method `introduceYourselfFormally` presumably looks at
`poodle`'s `name` property and adds some text around it. We might imagine that
it's making `"Hello, my name is " + this.name + " the poodle"`. As it turns out,
that is entirely valid JavaScript and it is probably what's happening!

Finally, methods can take arguments. Arguments change the method's
operation.

```javascript
poodle.eat(1); //=> "Byron eats 1 can of food"
poodle.eat(2); //=> "Byron eats 2 cans of food"
```

`Methods` can take multiple arguments.

```javascript
poodle.eyeEnviously('Shack Burger', '$', 9.57);
// ==> "Byron eyes your Shack Burger enviously, hoping you will drop some,
// ==> not caring the least that it cost you $9.57."
```

<figure>
  <img src="https://curriculum-content.s3.amazonaws.com/jsdom-mod/jsdom-mod-intro-dom-and-just-enough-js/poodle2.jpg" alt="Picture of IG:@byron_poodle_darling, who would like a snack" width="640" height="480">
  <figcaption><em>I'm more than behavior and state, I'm a burger-eating machine!</em></figcaption>
</figure>

<br><br>
Here we can imagine JavaScript doing some calculations to turn the `Number`
`9.57` and `String` `$` into the new string `$9.57`. We can also imagine it
using the property of `name` to supply `Byron`.

**A very important object when working with the DOM is called `document`.**

### Explain That JavaScript Has Loops

Sometimes you don't want to manually type something out multiple times, but you
want to perform some action "for each" element in a collection. That's where
looping comes in.

In this module, we'll be using a very common loop structure that's found in C,
C++, Java, PHP, and many other languages: The `for` loop.

Let's pull together several of the concepts of this lesson by coding:

"for each" character in the `slytherin` collection (or "`Array`"), we would like
the `harry_potter` object to invoke its `expelliarmus` method on the wizard or
witch who is passed in as an argument:

```javascript
for (let i = 0; i < slytherins.count; i = i + 1) {
  harry_potter.expelliarmus(slytherins[i]);
}
```

The important thing to take away is the ability to "sight read" that `for`
invokes the idea of doing some repeating action for each element in a
collection.

### Explain That JavaScript Logs With `console.log`

In the examples that follow, and in much of the technical documentation of
JavaScript, you will see the following method used: `console.log()`. This
method is used to print something. Often it's used to print out a `variable` or
some bit of data to make a point or to debug something.

Let's build on the loop example. Let's say we want to know who `harry_potter` is
defending against:

```javascript
for (let i = 0; i < slytherins.count; i = i + 1) {
  console.log(`Harry is about to disarm ${slytherins[i]}`);
  harry_potter.expelliarmus(slytherins[i]);
  console.log(`${slytherins[i]} is defenseless!`);
}
```

We'll discuss this method in more detail later, but it's a way to get
JavaScript to "talk to our screen."

## Conclusion

In this lesson, you've learned the "sight words" of basic JavaScript. With
those, you can reason about what code is doing when it works with the DOM in
future lessons.

Don't forget the power of imagination! By looking at these bits of code, you can
imagine that the code, written by humans just like you probably does
something like.... Professional developers try to make their code's function as
"guessable" as possible.

Guesses and imagination are a vital part of your toolkit!

[sight]: https://en.wikipedia.org/wiki/Sight_word
[ref]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
[literals]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals

<p class='util--hide'>View <a href='https://learn.co/lessons/fewpjs-introducing-the-dom-and-just-enough-javascript'>Introducing the DOM and Just Enough JavaScript</a> on Learn.co and start learning to code for free.</p>
