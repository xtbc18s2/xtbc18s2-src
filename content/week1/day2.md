---
title: "Day 2: Functions and The DOM"
weight: 2
---

<date>Tuesday, June 5, 2018</date>

## Lecture Videos

Morning:

* [Playlist](https://www.youtube.com/watch?v=AxtgfBl_yIw&list=PLuT2TqJuwaY-wZ8GKN0bjgCwNVf1WpEGp) | [Day 2, part 1](https://www.youtube.com/watch?v=piSflVSmiOI&list=PLuT2TqJuwaY-wZ8GKN0bjgCwNVf1WpEGp&index=6)

Afternoon:

* [Playlist](https://www.youtube.com/watch?v=GOQvgEk9IBM&list=PLuT2TqJuwaY90mQ7meSdhHMX6FbfCaLNA) | [Day 2, part 1](https://www.youtube.com/watch?v=Olz7MncGYJA&index=8)

## Topics

### Functions
* Function Expressions
* Function Declarations
* Function Hoisting ([MDN](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting))

### Git

* [Git Guide](http://rogerdudler.github.io/git-guide/)
* [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)
* [Understanding Git (part 1): Explain It Like I'm Five] (https://hackernoon.com/understanding-git-fcffd87c15a3)

<div class="img github-flow"></div>

### DOM
* Creating elements with `document.createElement`
* Setting style properties with `someElement.style.stylePropertyName`
* Appending child elements with `someElement.appendChild`

### Other Topics

* [Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
* [Google Fonts](https://fonts.google.com/)
* Polyfills
  * [Definition from MDN](https://developer.mozilla.org/en-US/docs/Glossary/Polyfill)
  * [What is a Polyfill?](https://remysharp.com/2010/10/08/what-is-a-polyfill)
* [Placeholder attribute](https://www.w3schools.com/tags/att_placeholder.asp)
* [Child and Sibling Selectors](https://css-tricks.com/child-and-sibling-selectors/) 

## Examples

### Functions
{{< code js >}}
  // Function Declaration (use 'function' keyword)
  function aMostExcellentFunction() {
    console.log('This function is excellent!')
  }

  aMostExcellentFunction() // => 'This function is excellent!'

  // Function Expression (defines a function as part of a larger expression syntax - usually assignment to a variable)
  const anotherExcellentFunction = () => {
    console.log('This function is also excellent!')
  }

  anotherExcellentFunction() // => 'This function is also excellent!'
{{< /code >}}


### DOM
If we start with the following markup:
{{< code html >}}
&lt;div id=&quot;my-div&quot;&gt;&lt;/div&gt;
{{< /code >}}
We can add additional markup to it programmatically using JavaScript.  One way is to create new HTML elements using `document.createElement`, and adding them by using `appendChild`.  Styling of the element can even be changed by manipulating the element's `style` property.

{{< code js >}}
// create an h1 and modify text content and color
const heading = document.createElement('h1')
heading.textContent = "This is the best heading I've ever seen"
heading.style.color = "red"

// get a reference to the existing div and add the heading as a child element
const div = document.querySelector('#my-div')
div.appendChild(heading)
{{< /code >}}

This will produce the following markup:
{{< code html >}}
&lt;div id=&quot;my-div&quot;&gt;
  &lt;h1 style=&quot;color: red;&quot;&gt;This is the best heading I've ever seen&lt;/h1&gt;
&lt;/div&gt;
{{< /code >}}

## Presentations

* <a target="_blank" href="/day02.pdf">Review: HTML and the DOM</a>

## Projects

### Spellbook

[Morning](https://github.com/xtbc18s2/spellbook) | [Afternoon](https://github.com/xtbc18s2/spellbook/tree/afternoon)

## Homework

* Add a second field of your choice to the form.

### Bonus Credit

Look up `document.createElement` and `appendChild`, and try adding the list items that way, instead of with `innerHTML`.

### Super Mega Bonus Credit

Display each value in the list item (the name, whatever other field you add) in separate elements, and style them differently somehow.

For example:

```html
<li>
  <span class="spellName">Fireball</span>
  <span class="level">lvl 4</span>
</li>
```

### Super Mega Bonus Credit Hyper Fighting

* Build each new element (the `li`, each `span`, etc.) in separate functions.
