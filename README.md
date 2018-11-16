# Intro to DOM Programming and Just Enough JavaScript

## Introduction

JavaScript can do many kinds of work, from building web servers, to creating
"infinite scroll" effects, but it was originally designed to do a type of
programming called **Document-Object Model (DOM) programming**. Understanding
DOM programming is the foundation of front-end development.

DOM programming is using JavaScript to:

1. Ask the DOM to find or `select` an HTML element or elements in the rendered
page
2. Remove and/or insert an element(s) 
3. Adjust a property of the selected element(s)

## Learning Goals

1. Explain the JavaScript / DOM relationship 
2. Explain "sight words" 
3. Explain "just enough JavaScript" concept 
4. Explain that JavaScript has things 
5. Explain that JavaScript has `variables` 
6. Explain that JavaScript can compare things 
7. Explain that JavaScript has `collections` 
8. Explain that JavaScript is object-oriented 
9. Explain that JavaScript has `loops` 
10. Explain that JavaScript `logs` with `console.log`

## Explain the JavaScript / DOM Relationship

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

## Explain "Sight Words"

When you learned to read, before you understood the process of joining letters
into sounds and sounds into words, you had a limited, but powerful vocabulary.
This vocabulary contained your "[sight words][sight]." These are also the words
you tend to memorize before you go on a trip abroad: MEN, WOMEN, WATER, FOOD,
HOSPITAL.

This lesson will provide you the "sight words" of JavaScript.  Some of these
lines of code you might not fully understand at first and that's OK. We'll
cover them all later in more depth.

## Explain "Just Enough JavaScript" Concept

We call the approach of learning JavaScript sight words "just enough
JavaScript." We learn so much better by working with technology than by merely
reading words.

We take this approach because it's just more fun, as well as being much more
effective. It's fun to change text on pages or update styling. Also, some of the
JavaScript concepts tend to sneak in along the way and make learning easier.

It's OK to come back here if you get confused or forget something. You might
want to bookmark this page or keep it open in a tab as you move along. This is
all OK in the "just enough" approach. In the following sections we list several
"sight words" of JavaScript. If you want to know more about a sight word, feel
free to consult [MDN's JavaScript Reference][ref].

## Explain that JavaScript Has Things

It might sound a bit weird to say, but there are "Things" in JavaScript. Most
programming languages call these "types." For the moment we're going to call
them **Things**.

One type of Thing is a `number` like `2` or `3.14`.

Another type of Thing is an arrangement of characters, called a `string` like
`"Byron"` or `'Please feed the dog'`. Strings are written inside of `"` **or** `'`.
Strings are quoted because `if` might mean something very special to
JavaScript but it also might be the beginning of a bit of
text "if you can keep your head when all about you are losing theirs..." `if`,
in this case is a _reserved word_ &mdash; something special to JavaScript. The
String is, well, just some text.

## Explain that JavaScript Has Variables

Sometimes you want to hold a `String` or a `Number` under another name.

> **TYPOGRAPHICAL NOTE**: The `//=>` means "What JavaScript would return back".
> For now, think about what's "returned back" as an answer to a question that
> you're asking JavaScript. Sometimes, too, you tell JavaScript a fact and it
> will just return it to you.

_Any time we give you a JavaScript example, feel free to try it out in the Chrome JavaScript console that is included in the DevTools yourself! To open the console, you can use the keyboard shortcut of command + shift + c, or go to View, then Developer, and Developer Tools. Make sure the Console tab is selected at the top. Copy the first part of the example - the part after the // is showing you what the return value will be, which you will see in the console!_

```javascript
3.14 //=> 3.14
var pi = 3.14 //=> `undefined`
pi //=> 3.14
```

JavaScript also lets you say:

```javascript
3.14 //=> 3.14
let pi = 3.14 //=> `undefined`
pi //=> 3.14
```

or

```javascript
3.14 //=> 3.14
const pi = 3.14 //=> `undefined`
pi //=> 3.14
```

When JavaScript first came out it had only `var`. Now it has `let` and `const`
too. We'll cover the differences between these later. They all tell JavaScript,
"Hey this is a name that I'm going to associate with some bit of information."

## Explain that JavaScript Can Compare Things

```javascript
1 < 3  //=> true
3 == 3 //=> true
3 != 4 //=> true
5 > 2  //=> true
```

Be careful here, `=` means "assign to," like we did with `var` just above. For
comparison we use `==` and `===`.

We can build on our previous example:

```javascript
3.14 //=> 3.14
const pi = 3.14
pi //=> 3.14
pi == 3.14 //=> true
```

## Explain that JavaScript Has Collections

Sometimes a `variable` might point to a Thing which actually has multiple Things
inside of it. In programming vocabulary, these collection Things are called
`arrays`. So technically, `Array` belongs with `String` and `Number`.

```javascript
slytherins[0] //=> "Salazar Slytherin"
slytherins[1] //=> "Bellatrix Black"
slytherins[2] //=> "Draco Malfoy"
```

In JavaScript, `arrays` start at `0`. In America, the floor where you walk in is
called the `1` floor (or first floor). In most of Europe and the rest of the
world, the floor where you walk in is called something else. Arrays are like
that, they start at `0`.

As seen above, we can get one of the elements of a collection by putting `[]` after a
collection's name and putting a number inside of the `[]`. In the example we get
the `String` names of some wizards stored in a collection of wizards identified
by the name `slytherins`.

## Explain that JavaScript is Object-Oriented

When working with the DOM in JavaScript, many of the Things are you meet are
objects. `Objects` are bits of code you can talk to that know state and
behavior. `Objects` should round out our universe of JavaScript Things along
with `arrays`, `strings`, and `numbers`.

When talking to an `object` you can ask it for a bit of state by using a `.`
and then that state's name. You can trigger behavior by using a `.` and then
the behavior's name followed by `()`. Due to the `.` being the separator
between the object-name and the state or behavior name, we call writing code
this way "dot-notation."

The thing that holds a bit of state is known as a property. This all sounds a
bit confusing, but it's a bit more simple than it sounds. To ask, say, an
adorable poodle its `name` state, you would do it like so:

``` javascript
poodle.name //=> "Byron"
```

If you ask an object for a property it doesn't have, JavaScript says
`undefined`

``` javascript
poodle.favoritePainter //=> undefined
```

When asking an object to do something (a behavior),  you use a `.` and a
behavior-name (usually a verb) followed by `()`. Behaviors on objects are
called `methods`.

```javascript
poodle.bark() //=> An ear-splitting bark is heard
```

`Objects'` `methods` have access to all of that `object's` properties.

```javascript
poodle.introduceYourselfFormally() //=> "Hello, my name is Byron the poodle"
```

In this case the `method` `introduceYourselfFormally` presumably looks at
`poodle`'s `name` property and adds some text around it. We might imagine that
it's making `"Hello, my name is " + this.name + " the poodle"`. As it turns out,
that is entirely valid JavaScript and it is probably what's happening!

Finally, `methods` can take arguments. Arguments change the `method's`
operation.

```javascript
poodle.eat(1) //=> "Byron eats 1 can of food"
poodle.eat(2) //=> "Byron eats 2 cans of food"
```

`Methods` can take multiple arguments.

```javascript
poodle.eyeEnviously("Shack Burger", "$", 9.57)
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

## Explain That JavaScript Has Loops

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

## Explain That JavaScript Logs With `console.log`

In the examples that follow, and in much of the technical documentation of
JavaScript, you will see the following `method` used: `console.log()`. This
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

We'll discuss this `method` in more detail later, but it's a way to get
JavaScript to "talk to our screen."

## Conclusion

In this lesson you've learned the "sight words" of basic JavaScript. You should
be able to reason about what code is doing when it works with the DOM in the
subsequent lessons.

Don't forget the power of imagination! By looking at these bits of code, you can
imagine that the code, written by humans just like you probably does
something like.... Professional developers try to make their code's function as
"guessable" as possible.

Guesses and imagination are a vital part of your toolkit!

[sight]: https://en.wikipedia.org/wiki/Sight_word
[ref]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference 