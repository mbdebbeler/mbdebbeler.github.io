---
layout: post
author: Monica Debbeler
title: What is functional programming?
---

Last August, I asked a developer for an example of a trendy topic in programming. “Functional programming” he said. “It’s the cool thing to say you’re into. It’s like putting that you love hiking in your Tinder profile."

It is true that languages that support functional programming show up among the most loved languages on the 2018 [Stack Overflow developer survey]( https://insights.stackoverflow.com/survey/2019#technology "Stack Overflow Developer Survey"), but functional programming is no fidget spinner. Its foundation is [lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus
 "Wikipedia | Lambda Calculus"), which was developed in the 1930s. The first functional-flavored programming language, Lisp, showed up in the early 1950s.

### So why is it called ‘functional’ programming? Don’t all languages have functions?

They do! Functional programming is a programming paradigm, or style, where functions are the star of the show. Functional languages tend to leverage first class functions (functions that take other functions as arguments), pure functions (functions that perform no side effects) and recursive functions (functions that call themselves). It’s [functions all the way down](https://en.wikipedia.org/wiki/Turtles_all_the_way_down, "Wikipedia | Turtles All the Way Down").

Some languages, like Elixir, Erlang, Elm, Haskell are specifically made for functional programming, but it’s possible to program in a functional style in other languages, too. For example, Javascript and Python both have first-class functions, and even Ruby, the queen of the object-oriented world, has lambdas.

For me, as a new dev, it’s easiest to understand functional programming when it’s contrasted with object-oriented programming, which I already know a little about.

### How is functional programming different from object oriented programming?


In object-oriented programming, we organize programs using the concept of “objects,” or data structures that contain both information (properties) and behavior (methods). Object-oriented programming believes that packaging information and behavior together in one place makes it easy to understand what a program does. Not everyone agrees:

> "The problem with object-oriented languages is they’ve got all this implicit environment that they carry around with them. You wanted a banana but what you got was a gorilla holding the banana and the entire jungle." _Joe Armstrong, author of Erlang_

By contrast, functional programming believes information and behavior should be kept separate.  Data is generally stored in plain arrays or hashes. These are then passed to tiny functions, which are stacked and sculpted like legos to create desired behavior. As a principle, combining bite-sized methods to get custom behavior isn’t unique to functional programming. It’s called composition, and object-oriented programming uses it too.

![Plush gorilla with sewn-on banana](https://github.com/mbdebbeler/mbdebbeler.github.io/tree/master/images/plush-gorilla.jpg)

_Joe Armstrong's metaphor..._

![Lego gorilla with detachable banana](https://github.com/mbdebbeler/mbdebbeler.github.io/tree/master/images/lego-gorilla.jpg)

_...extended. We can reuse the lego banana for our all of our fruit salad sculpture needs!_

Another core concept of functional programming is immutability, or the idea that, once stored, the contents of a variable should never be changed. If we need to transform those contents, we'll make a copy and if we’re going to need it later, we save the transformed copy in a new variable. That means there are essentially no variables in functional programming! There are only constants!

### So why do people like functional programming so much?

People like functional programming because they find it helps them write clean code. Small pieces are inherently more testable, which in turn helps with debugging, which in turn gives us the confidence to refactor. Because the data structures are immutable, it’s easy to manage state. In other words, if we know a function’s inputs, we can always predict its outputs, since the functions never mutate data. There are also a ton of business-y benefits about fault tolerance, scaleability and concurrency, which I’ll dive into more in my next post, which zooms in on Elixir.

Ultimately, spending some time in a functional paradigm forces us to examine our assumptions about how our code represents abstraction, and that’s a good thing.
