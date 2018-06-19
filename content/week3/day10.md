---
title: "Day 10: React & Firebase Cont'd"
weight: 2
---

<date>Tuesday, June 19, 2018</date>

## Lecture Videos

Morning:

* [Playlist](https://www.youtube.com/watch?v=AxtgfBl_yIw&list=PLuT2TqJuwaY-wZ8GKN0bjgCwNVf1WpEGp) | [Day 10, Part 1](https://www.youtube.com/watch?v=_u204Lp---Y&list=PLuT2TqJuwaY-wZ8GKN0bjgCwNVf1WpEGp&index=127)

Afternoon:

* [Playlist](https://www.youtube.com/watch?v=GOQvgEk9IBM&list=PLuT2TqJuwaY90mQ7meSdhHMX6FbfCaLNA) | [Day 10, Part 1](https://www.youtube.com/watch?v=FvzgFZrY-Ww&list=PLuT2TqJuwaY90mQ7meSdhHMX6FbfCaLNA&index=133)

## Topics

#### [React Select](https://github.com/JedWatson/react-select)
#### [Refs and the DOM](https://reactjs.org/docs/refs-and-the-dom.html)
#### [Moment.js](https://momentjs.com/)
#### [Firebase Database Rules](https://firebase.google.com/docs/database/security/)
#### [Element.scrollIntoView()](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView)

## Examples

#### Firebase Database Rules
Again, you can set database rules in Firebase for your application. In our Chatarang app, we made a certain endpoint public while others are private based on whether or not a user is authenticated.

{{< code >}}
{
  "rules": {
    "users": {
      ".read": "true",
      ".write": "auth != null"
    },
    ".read": "auth != null",
    ".write": "auth != null"
  }
}
{{< /code >}}


## Projects

* Chatarang: [Morning](https://github.com/xtbc18s2/chatarang) | [Afternoon](https://github.com/xtbc18s2/chatarang/tree/afternoon)

## Homework

Only list public rooms, and rooms in which the current user is listed as a member.

### Super Mega Bonus Credit

Don't allow users to load non-public rooms of which they're not members.

### Super Mega Bonus Credit Hyper Fighting

Make a separate UI for direct messages.

* List them separately in the sidebar.
* Make a new form (or at least a new button that presents the same form differently).
