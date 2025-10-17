# Lesson 12

## Overview

No overview provided

## Learning Objectives

Learning objectives will be defined as the lesson progresses.

## Topics Covered

Topics will be covered as the lesson progresses.

## Status

pending





## Subsections

### Lesson 12

In this lesson, you learn `EJS` (Embedded Javascript), a templating language for Express. The templates contain embedded JavaScript, which is executed on the server side. This constructs an ordinary HTML page, but with dynamic content. Because the embedded JavaScript runs on the server, before the page is sent to the client, dynamic content can be delivered, such as information from a database. This is called “server-side rendering”. Except for the embedded JavaScript, the templates are ordinary HTML pages, which may be combined with CSS and client-side JavaScript.

Server-side rendering is in some respects easier than writing first an API and then a front end for it, where the front end makes fetch calls to the API. On the other hand, if you don’t create an API, you can’t access the data via React or other front ends that run outside the application itself. There are other advantages and disadvantages. Frequently, an application will use both methods, using server-side rendering for the administrator user interface and front-end/back-end for the end-user interface.

In EJS, there are really only three kinds of embedded JavaScript statements:

```
<%- include 'filename' %>
<% code %>
<%= code %>
```

All are encased in the `<% %>` sequence.

The one with the minus in front does an “include” of another template, so that you can have headers, footers, and other partials.

The one with no minus or equals sign executes code but does not return any change to the HTML. This is used for logic statements, such as `if` statements and `for` loops.

The one with the equals sign executes code and returns the result in line as HTML.

---

Please be sure that you understand where each piece of JavaScript executes!

The JavaScript for your controllers, routes, middleware, etc. executes on the server side. If you do a `console.log` for this code, it appears in the server terminal. The code you put into an EJS file also executes on the server side, to customize the page with variable data before it is sent to the browser.

However, you can also put JavaScript into an HTML or EJS page, or load it from a script, where the JavaScript is _not_ within the EJS `<% %>` enclosure. That JavaScript is loaded by the browser and runs in the browser context, which means that it has access to the window and the DOM, but it does not have access to server side data and the database. Anything logged by `console.log` in thatcase would appear in the browser DevTools console.

**Video URL:** No video available

**Code Examples:**

No code examples available

**External Links:**

No external links available

**Quizzes:**

No quizzes available

## Supplemental Videos

No supplemental videos available

## References

No references available

## Resources

No resources available

## Additional Resources

No additional resources available

## Code Examples

No code examples available

## Discussion

No discussion topics available

## Podcast URL

No podcast available