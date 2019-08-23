# Full Stack @ Advance
This is a test for candidates aiming for a position at Advance as a Full Stack developer.

## The task
We need you to implement the following interface using HTML, CSS and Javascript:

![The layout to implement](specs/00-DEFAULT.jpg)

You have to implement:
* A responsive layout based on the design above
* Real-time validation on the contact form
* Server-side validation of the same contact form data
* Data persistence by saving valid contact forms to a JSON file

You can **optionally** implement for bonus points:
* SSR using React, Vue or Angular

You can view all the page states and specifications on the `specs`
folder and download the source PSD* file
[here](https://drive.google.com/file/d/19-fXPrpgDyJMkdhVyL2dpXcvV09jbHXN/view?usp=sharing).
All the fonts used in the layout are available on Google fonts. Refer to
the specs file to find out which fonts to use.

\* *You don't need Photoshop to accomplish the task as all the image
assets were exported and are available in the `assets` folder.*

## User story
This is a restaurant contact page, and the user should be able send messages to the 
owners using a simple contact form. The user must input their name, email address
and a message. All fields are required. The data must be validated using 
the following rules:

* Name: Should contain at least 2 words and 7+ characters
* Email: Should contain the `@` character preceded and followed by at least 1 character
* Message: Should contain at least 4 words and 20+ characters

The user must be warned in real-time about any input that doesn't match the above 
rules in a clear way, following the proposed design.

When all fields are valid, the user should be able to press the send button. Pressing the
button should send the form data to an endpoint of the back-end you must create. The
back-end must respond with an HTTP code of 200 in case of success, or an HTTP code of 422
and a message in the response body indicating which fields are not valid in case of failure.

If the sent form fails to validate at the back-end, the message containing the invalid
fields must be shown to the user on the front-end.

If the sent form is valid, the back-end must **generate a unique id** for the given form and
save the form data as JSON in a file named `<form_id>.json`. You can generate the unique id
any way you want to. For instance, if the generated id was `aM2t52kml`, you should create a
file named `aM2t52kml.json` and save the form data as JSON in it. On success, simply return
an HTTP code of 200 to the front-end and show the user a nice success message, as proposed
on the [specs/02-SUCCESS.jpg](specs/02-SUCCESS.jpg) file.

*PS: although this double-validation strategy seems unnecessary for a simple test project,
we simply want to know how you'd handle this case in real life. When testing your project,
we will manually disable your front-end validation code to test how your back-end is
responding to invalid requests.*

## Using this repository
1. Fork this repo
2. Clone your fork
3. `npm install` it
4. Do your magic 🌈
5. Push your work
6. Reply your invitation email with the link to your repository

**There's no need to send us a pull request with your code. All tests should be sent to us
via email.**

This project has a minimal boilerplate set to help you start your work
quickly. It uses [Parcel](https://parceljs.org/) to post process and
bundle your code. This means you can use ES6 modules, SCSS, PostCSS,
etc. Feel free to customize it the way you want to, but you **won't get
any extra points** for doing so. You are free to write your code the way
you like to.

We're also providing a minimal [Express](https://expressjs.com/) setup. You **must**
implement your contact form endpoint on the single POST route we provided you on the
`server.js` file.

You can get more details on Parcel and Express on its documentation pages:
* [Parcel](https://parceljs.org/getting_started.html)
* [Express](https://expressjs.com/en/starter/installing.html)

You can start a development server by running `npm run dev` on your terminal after
installing the project's dependencies. Parcel will run as an Express middleware and will
watch and automatically hot reload `index.html` and all of its dependencies. You will need
to restart the server when you update the `server.js` file, however.


## What we expect
Long story short, we expect clean, maintainable, legible and well
organized code above everything else. However, we also expect you:

### HTML
* To make good use of semantic tags.
* To write HTML5 compliant code.
* To create a well structured DOM tree, without unnecessary elements.
* To make basic SEO optimizations.
* To optimize images used by the page.

### CSS
* **Not to** use CSS frameworks like Bootstrap, Foundation, Tailwind, etc. We don't use them
  for a myriad of reasons, so this is a no-go to us.
* To use a good CSS architecture.
* To use a good naming scheme.
* To use a CSS guideline (SMACSS, CSS guidelines, BEM, etc) when it makes sense to.
* To use modern CSS features like Flexbox, Grid, Custom properties, etc.
* To use CSS preprocessors **if and when** you feel it would be helpful to you. At Advance,
  although we use preprocessors like PostCSS on some projects, we tend to prefer using pure,
  modern CSS whenever possible. This means that you can use one if you'd like to, but **you
  won't get less or more points** by doing so. If you do, Parcel supports
  [many CSS preprocessors](https://en.parceljs.org/css.html) out of the box.

### Javascript
* To use vanilla Javascript (ES5, ES6/2015+) on most if not all of your code.
* To write your own validation logic. You can't use libraries to help you with this task.
* To have few dependencies on both front and back-end. Having no dependencies at all **will
  yield you extra points**.
* To put the browsers' native APIs to good use. Remember: Parcel 
  [will transpile your ES6+ code automatically](https://en.parceljs.org/javascript.html#default-babel-transforms)
  using Babel by default.
* To use an UI library or framework (like React, Vue, etc) if you feel that it makes sense
  to. Remember that using any of these libraries and providing SSR **will yield you extra
  points**.

### Layout/Design
* To make a responsive layout based on the original design. We provided a desktop-first 
  design above, and you should create a responsive layout based on it. We don't expect you
  to create new design elements to be shown exclusively on small and mobile devices, but
  rather an adapted layout that fits better on smaller devices that's based on the original
  design.
* To pay attention to the design's details. One of our UX Designers created it thinking 
  about every little aspect of the layout, such as margins, paddings, fonts, colors, etc.
  You should analyze the image and deliver a page that resembles the original design as much
  as possible.

### Git
* To use git. 👀
* To use meaningful yet short commit messages.

## Any questions?
[Create an issue](https://github.com/penseadvance/full-stack-test/issues/new) on this 
repository and we'll answer as quickly as possible.

Good luck! 🎉
