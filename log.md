# 100 Days Of Code - Log

### Day 52: 27 September, 2020

**Today's Progress**: Continued learning Node.js from the Eloquent Javascript book.

**Thoughts**: Learnt about the Filesystem, HTTP and Streaming modules. Back-end programming is a much different paradigm than front-end programming where browser technologies are favourted as opposed to back-end where much more of the knowledge I have on basic computer science topics such as processes, threads, networking and the concept of streams. I've decided that the next application to be done is another common app: **budgeting app**.

**Link to work:** -

### Day 51: 26 September, 2020

**Today's Progress**: Started learning Node.js from the Eloquent Javascript book.

**Thoughts**: Currently reading the 3rd edition, there is a chapter on Node. Learnt the basic concept of Node (Javascript run-time that is single-threaded and based on Google's V8 engine), how it handles I/O and Events, and how it uses the CommonJS style of modules.

**Link to work:** -

### Day 50: 23 September, 2020

**Today's Progress**: Revised on the concept of Promises and went through the `async` and `await` features in Javascript.

**Thoughts**: Async and await applies synchronous paradigms to asynchronous codes, which sounds pointless but it's not and it's important I *promise*! Given that I've already finished all the asynchronous modules in MDN, the next session would be getting my hands dirty with Node.js.

**Link to work:** [Async & Await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)

### Day 49: 22 September, 2020

**Today's Progress**: Continued reading the MDN docs on Asynchronous Javascript, specifically on Promises.

**Thoughts**: Promises, a concept introduced in ES6, is a powerful and elegant way in handling asynchronous code. From having to deal with multiple callbacks, using the `.then()` keyword is a much more readable way of expressing chained asynchronous operations. This is definitely a broad topic and one that I will definitely have to master before diving into node.js.

**Link to work:** [Promises on MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises)

### Day 48: 21 September, 2020

**Today's Progress**: Continued reading the MDN docs on Asynchronous Javascript.

**Thoughts**: Learnt about the `setTimeout()` and `setInterval()` functions in Javascript. An interesting concept learnt today is the existence of the **event loop** in Javascript, which is things that will execute only when the main thread of Javascript has finished executing. Apparently it is a commonly used enough construct in computer science that it is easy to find resource on it.

**Link to work:** [Timeouts and Intervals on MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Timeouts_and_intervals)

### Day 47: 20 September, 2020

**Today's Progress**: Started reading on asynchronous Javascript as preparation to learn Node.js.

**Thoughts**: Asynchronous Javascript is interesting, with concepts like `Promises` and `Web Workers`. It is refreshing to learn about concurrency and how a piece of code gets executed rather than simply how something can and ought to be built.

**Link to work:** [Asynchronous Javascript on MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous)

### Day 46: 19 September, 2020

**Today's Progress**: Fixed the sidebar height and have it and the navbar fixed when scrolling for the Todo-App

**Thoughts**: Using `position:fixed` in CSS removes it from the normal document, which can cause some weirdness and overlaps when writing existing code. In this case, putting in the right margins for the content aligns the content correctly.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 45: 18 September, 2020

**Today's Progress**: Changed the look and feel of the checkbox and disabled the ability to press enter when editing any text for the To-do App.

**Thoughts**: CSS variables and SASS make life a lot easier when writing CSS code. Targeting modern browsers is of course the best developer experience what with all the enhancements in methods that are available to be used, but older browsers need some loving too (hence the fallback values and `@support`).

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 44: 17 September, 2020

**Today's Progress**: Fixed the hover bug from yesterday and added the editing function to the item descriptions for the To-do App.

**Thoughts**: Changing the `mouseover`/`mouseout` to `mouseenter`/`mouseleave` fixed the. I understand that it has something to do with event bubbling, but if I'm honest I do not fully grasp the concept yet. This will definitely be one of the topics study in my list of questions. The editing for the list items are also done similar to how the editing for the title was done (by focusing the element and then attaching an event listener upon blur). However, this would cause the code to run everytime a user clicks on the element and clicks away, which would be wasting cycles. This would be something to improve in the future.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 43: 16 September, 2020

**Today's Progress**: Continued working on the front-end scripting of the To-do App, specifically the Javascript adding the hover behaviour for the icon buttons and summary information.

**Thoughts**: There persists a bug on the hovering behaviour that will cause it to flicker whenever the user hovers over the icon's container element. Other than that, the summary information seems to be working fine, but again I am using a global variable to store the checked and total values and again am wondering if there are alternatives.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 42: 15 September, 2020

**Today's Progress**: Continued working on the front-end scripting of the To-do App, specifically the Javascript to handle the modals for the delete and adding a new list function.

**Thoughts**: Learnt about the `checked` property. I'm wondering if there's a reason that if there is a `checked` attribute on an `input` element, the value it holds is `checked` rather than true or false. Aside, not too happy with the use of a global variable to store the element that triggered the modal, and I am wondering if there are better ways to do it.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 41: 14 September, 2020

**Today's Progress**: Continued working on the front-end scripting of the To-do App, specifically the Javascript to handle the delete button and enable editing of line-items.

**Thoughts**: Learnt about `pointer-events` for paths and how setting it to none affects allows the clickable area to be the parent container element instead of being able to click on the individual paths. Mostly brushed up on existing knowledge (`.remove()` methods)and implementing the delete feature. A surprising feature that I've learnt today is that the querySelector method is able to be run on any child element and not just the document! In hindsight, this should've obvious as all elements in the page are child of the Document interface.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 40: 12 September, 2020

**Today's Progress**: Continued working on the front-end scripting of the To-do App, specifically the Javascript to handle the editable and add button.

**Thoughts**: Learnt theat the Query Selector works with *any* selector, including more complicated ones such as the Descendent Combinator. VS Code also has a nifty feature where there will be a popup detailing an example of the CSS Selector (specific to the HTML element types entered, even!) when hovering over the CSS selector in the stylesheet.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 39: 11 September, 2020

**Today's Progress**: Continued working on the front-end of the To-do App, specifically the editing of heading.

**Thoughts**: Learnt about the `contentEditable` attribute, along with accessing the `style` attributes programatically by going through the DOM.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 38: 10 September, 2020

**Today's Progress**: Continued working on the front-end of the To-do App, specifically, cleaning up some elements and applying some proper CSS.

**Thoughts**: The `calc()` function is a way to get a sidebar to be only the length of the screen, by inputting 100vh - amount of the navigation bar. Learnt this trick from the bootstrap docs website.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 37: 8 September, 2020

**Today's Progress**: Continued working on the front-end of the To-do App, specifically the sidebar.

**Thoughts**: The Collapse Bootstrap component combined with the Dropdown Bootstrap Toggle makes for a good way for a nested list.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 37: 7 September, 2020

**Today's Progress**: Continued working on the front-end of the To-do App.

**Thoughts**: Learnt about the `outline` CSS property and the difference between that and `border`. Surprised to learn that Bootstrap has its own icon set in SVG too. Dove a bit more in-depth on the difference between the pseudo-classes of `:active`, `:focus` and `:hover`.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 36: 6 September, 2020

**Today's Progress**: Learnt more on Bootstraps Components, especially Navs & NavBars and Dropdowns. Started work on a To-do App (what else would a first web project be!).

**Thoughts**: Bootstrap has some Javascript dependencies, especially on jQuery, which makes me favour Bulma more as it's a pure CSS framework. Bootstrap is a lot more opinionated and compelex then I thought, with the docs offering a really in-depth explanation of all the components. I just wish there was a quicker way to pick up Bootstrap than going through these documentations.

**Link to work:** [To-do App](https://github.com/RashidUjang/todo-app)

### Day 35: 5 September, 2020

**Today's Progress**: Learnt more on Bootstraps Grid system, and familiarized with the various Components.

**Thoughts**: Bootstrap seems to be useful for quickly mocking up a site what with only having to apply classes to common html elements go get a reasonable looking site, albeit a bit vanilla looking. Looking to create a dummy system with Bootstrap next.

### Day 34: 4 September, 2020

**Today's Progress**: Learnt the basics of Bootstrap, most notably its Container and Grid system.

**Thoughts**: As I'm already somewhat familiar with the Bootstrap system what with using MaterializeCSS for one of my projects before, learning more about how Bootstrap actually works with the Media Queries on the `min-width` and setting a set with for the container for two breakpoints was userful in understanding how to make a responsive layout.

### Day 33: 3 September, 2020

**Today's Progress**: Continued the Functional Programming module in freeCodeCamp

**Thoughts**: One of the challenges mentioned that `.reduce()` is simply a generalization of `.map()`, which is quite shocking to learn. I've to find out more about this.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 32: 2 September, 2020

**Today's Progress**: Started the Functional Programming module in freeCodeCamp

**Thoughts**: Functional Programming is an interesting topic that heavily emphasizes functions (of course!) and has concepts such as pure functions that do not introduce what is termed as *side effects* or changes to the state. Definitely excited to learn more and quite amazed that using the built-in functions in Javascript such as `.slice()` instead of `.splice()` which modifies the array is already following the Functional Programming paradigm. My idea of Functional Programming was something that could only be done with languages such as Clojure, Scala or Elixir.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 31: 31 August, 2020

**Today's Progress**: Spent more time working on the Product Landing Page, specifically in tidying up the margins, paddings and card look.

**Thoughts**: It is a smarter move to plan ahead the design so as not to waste time during the coding sessions. The fidelity of the mockup need not be up until the margins and paddings level, but a rough colour/page layout/images to use would be very beneficial so that I can straight away jump to the implementation.

**Link to work:** [Product Landing Page]()

### Day 30: 30 August, 2020

**Today's Progress**: Spent time working on the Product Landing Page.

**Thoughts**: Learned a lot about images and resizing them (`max-width` comes in handy when dealing with these images!) and also perhaps the best way I've found so far to resize images automatically. Creating these layouts is also a good refresher on all HTML & CSS. I am to start learning Bootstrap and Bulma for any future products other than this to be more efficient.

**Link to work:** [Product Landing Page]()

### Day 29: 29 August, 2020

**Today's Progress**: Finished the rest of the HTML and CSS Responsive Web Design Projects.

**Thoughts**: Next up would be to complete the Product Landing Page.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 28: 28 August, 2020

**Today's Progress**: Finished the Survey Form Challenge and Product Page Challenge and started work on the Technical Documentation challenge.

**Thoughts**: Currently for the sake of finishing the challenges on freeCodeCamp I've only set up the skeletons on the projects on Codepen and submitted it. However, after finishing all, I will choose one of five of the projects given to be expanded upon and to complete the front-end of it and possibly even the Javascript and backend.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 27: 27 August, 2020

**Today's Progress**: Finished the HTML Tribute Page Challenge and started on the Build a Survey Form challenge.

**Thoughts**: HTML has a lot of boilerplate code that needs to be entered all the time. The `max-width` property seems to be good for responsive layout. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 26: 26 August, 2020

**Today's Progress**: Completed the Intermediate Algorithm Challenge on freeCodeCamp and started on the HTML Tribute Page Challenge.

**Thoughts**: Regex is beginning to click, especially the capture groups and character classes. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 25: 25 August, 2020

**Today's Progress**: Continued doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: They're mostly done except for Regex challenges. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 24: 24 August, 2020

**Today's Progress**: Continued doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: I am wondering what use does Object-oriented Javascript have and if it is really necesssary if it used in a front-end context.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 23: 23 August, 2020

**Today's Progress**: Completed the CSS Grid and continued development on form validator.

**Thoughts**: Implementing the logic of the form validator is all fine, but obviously in a real world application the validation would have to happen server-side. The topic of user authentication is something I can look into in the future.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 22: 21 August, 2020

**Today's Progress**: Continued doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: The Array methods `.map()`, `.filter()` and `.reduce()` seems to be applicable to be used in most Javascript algorithm problems. They eliminate the need of looping through the array and I intend to exclusively use these methods when solving Javascript problems.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 21: 20 August, 2020

**Today's Progress**: Continued doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: Having to deal with primes, the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes) is an interesting topic. Some sort of visualizer for these would be a cool side project to learn the `canvas` elements on.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 20: 19 August, 2020

**Today's Progress**: Continued doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: Learnt the `.filter()` method. It's an elegent way of modifying an array without the need to use a `for` loop to iterate through the contents of the array. Also learnt some methods to convert to and from ASCII characters with some `String` methods.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 19: 18 August, 2020

**Today's Progress**: Started doing the Intermediate Algorithm Challenges on freeCodeCamp.

**Thoughts**: Learnt about the `.includes()` method for arrays. Also found that a better way to solve these algorithm challenges is to outline what needs to be done in a step-by-step way, and only then to think of the functions that would be useful to achieve those steps. Structured thinking is the enemy of inefficiency.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 18: 17 August, 2020

**Today's Progress**: Completed the Regex module on freeCodeCamp and started on the Intermediate Algorithm Challenges.

**Thoughts**: On my quest to complete the algorithm challenges, I've learnt about the `Set` and `Array.concat()` methods which help in manipulating arrays. Makes you wonder what is the efficiency of the methods that developers implement for replacement in languages that do not have these helper functions built-in.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 17: 16 August, 2020

**Today's Progress**: Completed the Object-Oriented Module from freeCodeCamp

**Thoughts**: Working backwords after learning ES6, the `class` and `constructor` keywords make Javascript a better object-oriented language and be more syntactically similar to the statically typed languages like C++ or Java of which I am more familiar with.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 16: 14 August, 2020

**Today's Progress**: Finished part 3 and halfway through part of TraversyMedia's DOM tutorial.

**Thoughts**: Events are an important part of respnsive Javascript and is anothe piece of the puzzle when sending/grabbing data from the front-end to send to the back-end.

**Link to work:** [Item List Adder and Deleter]()

### Day 15: 13 August, 2020

**Today's Progress**: Started work on a project to implement an application progress tracker from an available open source repository (found [here](https://github.com/NigelOToole/progress-tracker)) and converting it to fit my project's needs.

**Thoughts**: The design of the progress tracker has to be modified to include a curve if the number of progress markers exceed 6 and that the overflow would appear at the right instead of the left (as is the default behaviour of `flex-wrap`). This is also my first exposure to SASS, and right now it seems like a no-brainer to pick this up after getting used to the basics of CSS. Variables, mixins and able to define expressions to calculate a certain value are powerful features that CSS should have in the first place.

**Link to work:** [Progress Tracker with Curve]()

### Day 14: 12 August, 2020

**Today's Progress**: Finished 2 parts of the TraversyMedia's DOM tutorial.

**Thoughts**: DOM methods are straightforward and easy to use. Having the `querySelector` method in vanilla Javascript will allow me to work with my preferred syntax without having to include any external JQuery libraries. Learnt the difference on the `window`, `document` and `screen` objects in Javascript too.

**Link to work:** N/A

### Day 13: 11 August, 2020

**Today's Progress**: Finished the frontend for Form Validator and started going through [TraversyMedia's DOM tutorial](https://www.youtube.com/watch?v=0ik6X4DJKCc&list=PLillGF-RfqbYE6Ik_EuXA2iZFcE082B3s) on Youtube.

**Thoughts**: Happy with the outcome of the Form Validator's frontend (though I wish the form validation text could have a little more animation to it such as Airtable's registration page where it slides the other elements down when there's an error) and the DOM manipulation techniques will help in completing this mini-project. Looking around for the error in form validations at various major tech companies' landing pages shows that there is currently no best practice in displaying the error as they are all different. I've also started to thinking about hosting the mini-projects that I'm doing as a site, but I'm still considering the options as I may want to involve Django in the project and there's no free hosting for that.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)
[Form Validator]()

### Day 12: 10 August, 2020

**Today's Progress**: Went through about 75% of the Javascript Regex module and worked on the Form Validator project a little bit.

**Thoughts**: Basic regex as a concept is not a hard topic to grasp but requires some revising due to the amount of different meanings of common character symbols.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 11: 9 August, 2020

**Today's Progress**: Learnt about `border-box`, revised some elements on Forms to recreate the HTML & CSS [Form Validator](https://vanillawebprojects.com/projects/form-validator/) from the 20 Vanilla Web Projects.

**Thoughts**: Applying some of the previously learned materials from the freeCodeCamp modules to an actual mini-project is cementing them much better. My initial thought for the best way to perform the validation on the fields would be via regex. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)
[Form Validator]()

### Day 10: 8 August, 2020

**Today's Progress**: Finished the CSS Flex and Responsive Web Design module and started on the CSS Grid module.

**Thoughts**: The freeCodeCamp modules on Media Queries, Flex and Grid seem to only teach the basics and not the real world use. Will have to explore real-world use cases on my own.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 9: 6 August, 2020

**Today's Progress**: Finished revising HTML & CSS from the video in Day 6. Learned about Media Queries briefly and started on the Flexbox module in CSS.

**Thoughts**: Creating a responsive website seems to be a lot more manual than I thought and requires a degree of experimentation and eyeballing. Flexbox is such a dynamic tool that it its enough to just use it to create beautiful and dynamic layouts without having to resort to frameworks.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 8: 5 August, 2020

**Today's Progress**: Finished the Algorithm Challenges in the Javascript module.

**Thoughts**: Learned about the `.sort()` function for arrays.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 7: 4 August, 2020

**Today's Progress**: Continued the Algorithm Challenges in the Javascript module.

**Thoughts**: `.splice()` methods are the easiest way to delete values in an array. Javascript has a concept of 'falsy' values, which is something foreign coming from strongly typed languages.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 6: 3 August, 2020

**Today's Progress**: Worked through 5 algorithm challenges in the Javascript module. Revised some HTML & CSS materials by going through [this](https://www.youtube.com/watch?v=ZeDP-rzOnAA) tutorial for a responsive website using vanilla HTML & CSS. 

**Thoughts**: The myriad of ways that you can solve the same problem is interesting. The `.map()` and `.reduce()` functions are seemingly often used in these kinds of challenges and I'm going to look more into that. Flexbox's `align-items` and `justify-content` seem to be its most important properties.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 5: 2 August, 2020

**Today's Progress**: Finished up the data structures module on the Javascript track.

**Thoughts**: I'm wondering what the performance are for these atomic operations such as `slice`, `splice` and `indexOf()` and if there are any downsides to using the built-in methods.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 4: 1 August, 2020

**Today's Progress**: Finished up the ES6 modules covering string literals, classes, Promises and exports, the entire debugging module and also some data structures.

**Thoughts**: Promises are a stand out to me as something to delve deeper into. Exports seemed to have been born out of a necessity to cater for server-side Javascript logic. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 3: 31 July, 2020

**Today's Progress**: Finished up the freeCodeCamp recursion lessons, and started learning ES6 Javascript syntax such as arrow functions, let and const keywords and destructuring syntax.

**Thoughts**: Made some good progress on understanding recursion (it's starting to 'click'!) and ES6 seems to have many features that revolve around manipulating objects and arrays and generally a good addition to make any web developer's life easier. Being able to use the destructuring assignment in the parameter of a function seems shockingly easy. Loving that flexibility to manipulate an object's representation.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 2: 29 July, 2020

**Today's Progress**: Continued more freeCodeCamp challenges focusing on loops, recursion and the ternary operator.

**Thoughts**: Good refresher on all the content, as the syntax is mostly as it is in Java. Going to study more on some prerequisite knowledge on recursion (from [this](https://forum.freecodecamp.org/t/freecodecamp-challenge-guide-use-recursion-to-create-a-countdown/305925) freeCodeCamp forum post) before continuing on to the next challenge to ensure I'm well equipped to tackle the problem.

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 1: 28 July, 2020

**Today's Progress**: Did some freeCodeCamp challenges for Javascript from the Basic Javascript track from "Golf Code" to "Record Collection". Learned mostly on `switch` statements, Javascript object notations, access and property notations.

**Thoughts**: Javascript has an easily confusable way to access its objects either via the dot notation (e.g. myObject.myProperty) and the more robust square bracket notation (e.g. myObject\[myProperty\]), which lead to some difficulty when tackling "Record Collection". Specifically, what's important for me to remember is that variable names are not accessible via the dot notation and only by the square bracket notation. 

**Link to work:** [freeCodeCamp Portfolio](https://www.freecodecamp.org/rashidujang)

### Day 0: 27 July, 2020

**Today's Progress**: Started the 100 Days Of Code Challenge by forking the repo and updating the log. Learned how to push changes in using VS Code and created a tentative roadmap of the challenge in Notion.

**Thoughts:** The Markdown syntax is pleasant to deal with (the simplicity of the heading hierarchy is simple yet effective). VS Code is a lot more robust than I thought what with its ability to handle version control. Hope I can make it through this challenge! I've always had a lot of trouble sticking and committing to my self-learning initiatives and projects so when I heard about a challenge that's specifically for people who tend to shift focus like me. The premise of the challenge is simple and its easy enough to get started.

**Link to work:** [Learning Roadmap](https://www.notion.so/6718fff81f0e4e699563a22e05826eef?v=d92ae18b60424512b9be5b0614b5d1bd)

<!--### Day 0: February 30, 2016 (Example 1)
##### (delete me or comment me out)

**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts:** I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link to work:** [Calculator App](http://www.example.com)

### Day 0: February 30, 2016 (Example 2)
##### (delete me or comment me out)

**Today's Progress**: Fixed CSS, worked on canvas functionality for the app.

**Thoughts**: I really struggled with CSS, but, overall, I feel like I am slowly getting better at it. Canvas is still new for me, but I managed to figure out some basic functionality.

**Link(s) to work**: [Calculator App](http://www.example.com)


### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence)-->
