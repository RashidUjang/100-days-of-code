# 100 Days Of Code - Log

## Day 100: 19 November, 2020

**Today's Progress**: Refactored notification handling for Budget App.

**Thoughts**: Today is the last day of the challenge and marks the final piece of code that I will push in to this app, at least as part of this challenge. Though the app has much, much more work to be done, namely in terms of the UI, the support for, I think it has come a long way. From being able to enter self inputs and switch between the two styles of input, to actually hooking up the web app to PostgreSQL and Express, this has been an amazing learning experience and I am a much much more able coder than I was when I started this. Popular doctrine states that it really is not about the technology chosen and language choice but more on software architecture, business logic, requirements and data models & API design. These language/technology-agnostic things are the real core of software engineering, and coding for 100 days have taught me the value of such things where before it was unclear what the actual importance and benefit of these things are.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 99: 18 November, 2020

**Today's Progress**: Cleared up unnecessary code for parents processing and created a script for resetting the table.

**Thoughts**: It turns out the parents processing part is unnecessary if the user adds in to the table itself. For now, it will be commented out until the input system is finalized, for which it may be necessary at that time. Also create a utility script for resetting the table, which makes use of some new keywords which I learnt which is `TRUNCATE` and `SETVAL`.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 98: 17 November, 2020

**Today's Progress**: Finished working on the parents processing part.

**Thoughts**: One of the mistakes found is actually in naming convention, where an improperly named variable caused the key lookup in an object to return empty and thus, not to trigger that branch of the program. It's important to maintain consistent naming conventions (which I admit, in this project I am not doing so well as I am forking the project) so that these things do not happen.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 97: 16 November, 2020

**Today's Progress**: Found the bug mentioned in the log of the previous day and started working on enabling the `amount` field to be sent into the `processingParents()` function.

**Thoughts**: Turns out the bug was simply a `.push()` inserted in the wrong place. I think we can avoid this kind of logic mishaps in the future by actually formalizing the logic and writing it down somewhere.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 96: 15 November, 2020

**Today's Progress**: Spent time trying debug the parent node

**Thoughts**: So far unable to find what is the problem, but I've narrowed down to the new function that had been created in `parseGeneralInputToFlows()` but was unable to find the root cause

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 95: 14 November, 2020

**Today's Progress**: Continued working on enabling parent nodes in the Sankeymatic flow.

**Thoughts**: I've come to realize that a lot of programming is planning before writing a single line of code. Dealing with the many many possible scenarios for adding the parents and the amount of checks that must be done to ensure all of the flows are accounted for correctly is simply overwhelming to be done WHILE coding. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 94: 13 November, 2020

**Today's Progress**: Started working on enabling parents of nodes inside the Sankeymatic flow.

**Thoughts**: Working on enabling at least 1 level of parents first (meaning, only 2 levels as a whole), and generalizing it later. I'm also just now realizing that I could be using a more object-oriented approach for my data structure, as I found having certain utility methods on the data itself would be useful such as, having `.hasParents()` as a property of an object instead of a utility method. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 93: 12 November, 2020

**Today's Progress**: Completed working on the delete button.

**Thoughts**: Turns out only a one-liner is required in enabling the delete button. Some bugs need to be fixed in regards to adding the category and enabling the parent category. A more thorough understanding of the inner workings of sankeymatic is required for this, which I am slowly beginning to understand.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 92: 11 November, 2020

**Today's Progress**: Continued working on the delete button.

**Thoughts**: One thing that I found would greatly benefit my project right now that is just simply not as easily doable with vanilla Javascript compared to using a front-end framework is by using the concept of row keys for tables. Without it, I am forced to insert an ID attribute to each of my table rows, which is functional, but I believe there are better ways to do it than this.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 91: 10 November, 2020

**Today's Progress**: Read up on some methods in keeping the table synced upon changes to it and started implementing the function to the delete button.

**Thoughts**: Implemented the live reload simply by fetching the list at the relevant points (update, delete). This is of course not ideal as there is some wastage in cycles by doing this, but I will keep the efficiency to when I'm starting to use a Javascript framework. Also discovered a neat trick to remove all childs from a parent node [here](https://stackoverflow.com/questions/3955229/remove-all-child-elements-of-a-dom-node-in-javascript).

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 90: 9 November, 2020

**Today's Progress**: Fixed the bug and successfully linked the add feature for both income and expenses to the backend.

**Thoughts**: Decided to make `addNode()` async after all, though it is something that perhaps can be improved on in the future. The next challenge is refreshing the table upon successfully initiating any change.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 89: 8 November, 2020

**Today's Progress**: Learnt about media types and started debugging on the add feature.

**Thoughts**: Quite a gnarly problem here that we have. After some time, trial and error using logging functions (I've learnt that the `catch` blocks should always be accompanied by a specific error message to know exactly where it failed!), I've narrowed it down to an async problem. Essentially, the `Promise` returned by `checkCategory()` is yet to be resolved when the code execution continues, ensuring that the DB only receives an empty value for the `categoryID`. Quickest fix would be to make `addNode()` async and have an await near the addNode code, but is that really the best way? 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 88: 7 November, 2020

**Today's Progress**: Continued working on the add feature.

**Thoughts**: Had to rethink some of the ideas that was implemented yesterday. The `checkCategory()` function should now check from the local list instead of the backend, and the checking to be done by name instead ID.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 87: 6 November, 2020

**Today's Progress**: Continued working on the add feature.

**Thoughts**: A lot of places to change in the code, especially in the modal popup where the checking and handling of new categories needs to be done, which results in a new API needed in the backend to handle such cases. This feature is incomplete as of now, though. Also learnt about the `.some()` method on arrays which is handy for checking existence.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 86: 5 November, 2020

**Today's Progress**: Started linking the add feature to the backend.

**Thoughts**: Learnt a new method, which is `JSON.stringify()`, which is used to convert objects in Javascript to a single JSON string to be used in the body. I will need to rethink of some enhancements to the add modal itself so as to make sure it adheres to the data structures that I have defined, namely the parent node field.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 85: 4 November, 2020

**Today's Progress**: Fixed the regression bug raised by adding the `record_type` indicator in the record data structure.

**Thoughts**: Although the bug has been fixed, (mostly by ensuring the data structure from the general-style and budget-style input are absolutely the same) I am actually left with more questions than answers from the exercise. One of my biggest questions is whether or not importing/exporting values between my `sankeymatic.js`, `main.js` and `util.js` files is a good idea? It seems that it is necessary, however it creates a web of dependency which from my time reading HN, is almost never a good idea. Another is on whether it is considered good practice to have an `export` statement in the `.onload()` function so that we are guaranteed to be able to accessed the fetched value from the DB or whether putting it at the end of the file is enough.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 84: 3 November, 2020

**Today's Progress**: Handled the parent category id case.

**Thoughts**: Added an indicator to the function to perform `matchCategory()` and recursively called `matchCategory()` inside to handle the parent category function. I still cannot commit this code though as there seems to be a regression bug which I have to fix first.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 83: 2 November, 2020

**Today's Progress**: Completed the category matching according to id for primary categories.

**Thoughts**: Found out that `.forEach()` doesn't support the `return` keyword as it's a delegated function. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 82: 1 November, 2020

**Today's Progress**: Rewrote the code for both the category and record API in a single function instead of two separate functions.

**Thoughts**: Learnt using `Promise.all()` in handling multiple `.fetch()` instances, and how ANOTHER `Promise.all()` is required when parsing the `Response` object using the `.json()` method as it returns a Promise instead of the actual parsed json (thanks to [this](https://gomakethings.com/waiting-for-multiple-all-api-responses-to-complete-with-the-vanilla-js-promise.all-method/) article for providing a clear example on the use-case!). This took an embarrasingly long time to figure out but this has been a great refresher on Promises and how it works.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 81: 31 October, 2020

**Today's Progress**: Created a script to refresh the DB with mock data and hooked up the front-end code by calling the API.

**Thoughts**: Finally able to see some visual progress on connecting the database to the front-end! Used the `fetch()` API to trigger the requests. It's obvious to me why the technical design of a certain piece of software is important. While badly-designed API/layers/database schema may get the job done in terms of functionality, it sure makes changing things much more difficult in the future. It's all part of dealing with complexity.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 80: 30 October, 2020

**Today's Progress**: Completed the CRUD operations via RESTful API in Express.

**Thoughts**: Similar to handling the `GET` requests, today's work has been on handling the `POST`, `PUT` and `DELETE` and its corresponding SQL operations of `INSERT`, `UPDATE` and `DELETE` respectively. The CRUD operations is now complete and the what we have now is a RESTful API on the `records` table.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 79: 29 October, 2020

**Today's Progress**: Added handling of POST requests for Budget App.

**Thoughts**: Had to brush up some concepts such as `async`, `await` and learnt about the `req` and `res` objects from the Express frameworks. They're simply implementations of the `IncomingMessage` and `ServerResponse` classes in Node.js. Successfully implemented the handling of POST requests for the record type.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 78: 28 October, 2020

**Today's Progress**: Created some dummy data and setup database connection for Budget App.

**Thoughts**: Learnt about the connection pooling concept as the `pg` library had to setup that. Also learnt how to manage users using PostgreSQL and refresh on the `INSERT` statement to create the dummy data. Looking forward to actually store and retrieve data from the front-end using the available database connection.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 77: 27 October, 2020

**Today's Progress**: Defined the database schema in PostgreSQL for the Budget App.

**Thoughts**: A blast of nostalgia just hit me when applying all these concepts learned in my first-year engineering classes! Working with databases is great fun and I find it rewarding when creating and maintaining a well designed schema that can make it long-lived and robust. Up next is to connect the database to Node.js using the [pg](https://www.npmjs.com/package/pg) package.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 76: 26 October, 2020

**Today's Progress**: Created the Budget App database and table.

**Thoughts**: Found out the cause of the previous issue of not being to find the proper role: it's actually not about roles in Postgres and more about users in Linux! I've learnt that the `sudo` command for Ubuntu is used mainly to run certain commands as other users, which when you run the `psql` command as the default postgres user it works flawlessly. Next activity is to actually define the schema as we have in the mock database.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

## Day 75: 25 October, 2020

**Today's Progress**: Worked on setting up the Linux environment and connection to PostgreSQL for the backend.

**Thoughts**: Set up the environment on Linux, mostly due to the ease of use with PostgreSQL and Docker. One thing to point out during the setting up of these environments is how easy it is `npm` has made to sync packages between development environments and that it "Just Works™" out of the box. Currently still setting up PostgreSQL and learning its CLI with the `psql` command as there are certain prerequisites that need to be set up before it can function and linked properly. Planning to follow [this](https://www.youtube.com/watch?v=ldYcgPKEZC8&ab_channel=freeCodeCamp.org) tutorial here, outlining the steps in creating a basic PERN stack app.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 74: 24 October, 2020

**Today's Progress**: Worked on the front-end of the Budget App.

**Thoughts**: Finally got the app to work with own input! Granted, there are still many things to be done but this a win that should still be celebrated as it is the first major enhancement made to the original Sankeymatic. Next would be to actually link it to a database, so it doesn't become a blocker for future features and enhancement. Some refactors are needed though, especially in passing the inputs to the `process_sankey()` function.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 73: 23 October, 2020

**Today's Progress**: Worked on the front-end of the Budget App.

**Thoughts**: Attempted and identified the areas to change to enable the budget-style of input. Most of it was sifting through the code to find that all that needs to be done is to push the good flows in the proper format to the `good_flows` array.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 72: 21 October, 2020

**Today's Progress**: Worked on the front-end of the Budget App.

**Thoughts**: Added the toast adding to the income and expense list functionality. Also made the `closePopup()` function to be generalized and able to open/close the popup even if it is not in the listener. Also added the success notifictation upon the success of an addition to the list. Fixed the model to also only have a `parentNodeID` but the category to be a name instead of an ID. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 71: 20 October, 2020

**Today's Progress**: Worked on the front-end of the Budget App.

**Thoughts**: In preparation for the actual backend, I've started trying to load the options programatically. Currently the roadblock seems to be what I want the structure of the node to be. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 70: 19 October, 2020

**Today's Progress**: Worked on the front-end of the input style and listing features for Budget App.

**Thoughts**: The `.toggle()` method for `classList` is really convenient. Planning to use Bulma's helper/utility classes to perform as much front-end as possible, instead of programatically hiding the element from the DOM.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 69: 18 October, 2020

**Today's Progress**: Standardized expenses to listing format and started work on programatically loading the listing for Budget App.

**Thoughts**: There's some really gnarly code in the programatically loading of the list that can turn into tech debt, but I'm going to live with it for now as my primary purpose is to ensure the new input style would work. Currently, the categories are simply strings but I have plans on having a mapping table and using IDs instead. Need to start looking into setting up PostgreSQL and hooking up to Node.js and start taking the tree structure into account for the DB schema.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 68: 17 October, 2020

**Today's Progress**: Changed the listing form to table and handled the closing of the popup for Budget App.

**Thoughts**: Pretty standard stuff today. Again, just wondering what is the best way to organize the code for Javascript handlers, whether to put all the DOM retrievals in one block, functions in one block or to segregate by feature. 

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 67: 16 October, 2020

**Today's Progress**: Changed the Add button for Income and Expense to become a modal instead of a duplicating an element.

**Thoughts**: Loving Bulma more and more over Bootstrap the more I use it. It being just a CSS framework and modernizing what Bootstrap set out to do by ensuring the implementation is even simpler (check out the `columns` implementation!) makes it much simpler and easier to use, especially with how intuitive some of the classes are. I now realize this is a much bigger project than the scope of the To-do App previously, but definitely one where I'm excited to work on everyday.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 66: 15 October, 2020

**Today's Progress**: Got the current version of Sankeymatic working with Node.js.

**Thoughts**: Apparently, the work done the previous few days were not in vain, as the HTML elements that were required to make the file work was still the same. Worked on enabling the new input style, which will require some technical design work on the data structure, so that I do not gimp myself in the future by not properly choosing the right data structures.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 65: 13 October, 2020

**Today's Progress**: Worked on getting the existing Sankeymatic App code to work wite Node.js.

**Thoughts**: Learnt about Ordinal Scales in d3, which can be accessed using the `.range()` and `.domain()` method. As this is already the third day in trying to glue Sankeymatic's code with the d3.js and I am currently looking to focus more on adding features and making progress on the Budgeting App, I've decided it is best to stash the work done on fixing the compatibility issues in the code and to revert to the d3.js v2. The goal of this exercise to learn things well and having to learn the complex d3.js along with Node.js and Bulma would simply slow my learning. From the next hour onwards, I will focus more on adding better UX while upgrading d3.js to v6 will be ticketed as a nice-to-have item and catered in the future where I can fully understand d3.js before implementing in the code.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 64: 12 October, 2020

**Today's Progress**: Worked on getting the existing Sankeymatic App code to work wite Node.js.

**Thoughts**: Attempting to rewrite `d3.scale.category20()` with new code as it had changed since d3.js v3 (Sankeymatic uses v2) and the project is currently using d3.js v6 as described [here](https://github.com/d3/d3/blob/master/CHANGES.md#scales-d3-scale). Learnt about ordinal scales and currently looking into replacing the color by using the new method described in the changes article with `d3-scale-chromatic`. Perhaps for the sake of moving the project, the colors of the graph could be set to only one colour by setting `node.color` be a single colour instead of accessing `d3_color_scale`.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 63: 11 October, 2020

**Today's Progress**: Worked on the front-end for the Budget App.

**Thoughts**: Successfully split modularized sankeymatic.js into util.js. There are several improvements that can be made to the sankeymatic code (using using the `async` keyword to trigger the rendering asynchronously and detect onchange programatically instead of using a HTML attribute) but I think the highest priority now is to ensure that the Generate button is able to spit out a Sankey diagram using the previous input styles to ensure the code is still working fine. Then perhaps I will move on to changing the input styles.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 62: 10 October, 2020

**Today's Progress**: Added the front-end code for the Add items functionality of the Budget App.

**Thoughts**: Reused some of the code from the previously made [To-do App](https://github.com/RashidUjang/todo-app) for the addition of items in a list. As the list now would seem to have parent and child relationships between each other and maintain its own category, trees would probably need to be used and to maintain a more robust data structure. Something I need to research before diving in the recursive behaviour of the tree.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 62: 9 October, 2020

**Today's Progress**: Attempted to split the modules for the Budget App.

**Thoughts**: Decided to fork the Sankeymatic project as I will be reusing most of the code and modularize it. However, currently unsuccessful in trying to split the utility functions and dealing with `import` & `export` functions from the main js file to a module js file.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 61: 8 October, 2020

**Today's Progress**: Attempted to split the modules for the Budget App.

**Thoughts**: Decided to fork the Sankeymatic project as I will be reusing most of the code and modularize it. However, currently unsuccessful in trying to split the utility functions and dealing with `import` & `export` functions from the main js file to a module js file.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 60: 6 October, 2020

**Today's Progress**: Set up the other dependencies required by Sankeymatic for the Budget App.

**Thoughts**: When trying to use `npm` as much as possible for managing packages, something I've learnt today is to be careful with using it as the package manager for your front-end package as it's possible for the packages to not be what you expect. Setting up the paths virtually using Express's `app.use()` to serve the files makes things simpler. CommonJS is also not available by default in the browsers. Next, I'll begin piecing up the Sankeymatic functions to be used in my own Javascript files. Makes me wonder if I should be forking the Sankeymatic project instead as I'll be using most of the components.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 59: 5 October, 2020

**Today's Progress**: Worked on setting up [Bulma](https://bulma.io/) as the front-end framework of the Sankeymatic.

**Thoughts**: Solved a bug on getting CSS files to work in a Node.js environment by linking the file virtually instead of providing the actual path. Also learnt the `path.join()` method, which joins the paths using the platform-specific path separator and the `__dirname` global, which points to the currently executing process's path. Learnt the basics of Bulma classes too.

**Link to work:** [Budget App](https://github.com/RashidUjang/sankeymatic)

### Day 58: 4 October, 2020

**Today's Progress**: Started performing groundwork on adapting the Sankey budget generator from [Sankeymatic](https://github.com/nowthis/sankeymatic) to be the first component of the Budget App.

**Thoughts**: Diagrammed the flow of the Sankeymatic function and thank god for the amount of comments in that repo. 

**Link to work:** -

### Day 57: 3 October, 2020

**Today's Progress**: Finished the Coding Train's tutorial up to the database and dove deeper into Node.js `Streams`.

**Thoughts**: Streams used mostly for I/O and network operations and can be manipulated with the events. Looking at using PostgreSQL as the database for the upcoming Node.js App.

**Link to work:** [Coding Train's Express](https://www.youtube.com/watch?v=Kw5tC5nQMRY&ab_channel=TheCodingTrain)

### Day 56: 2 October, 2020

**Today's Progress**: Started learning one of Node's most popular Express using Coding Train's tutorial video.

**Thoughts**: Learning an abstraction of a piece of code after learning the hard way of doing it is refreshing. Simply calling `app.post()` for the methods to handle the POST methods rather than defining handler methods for each method type manually puts more emphasis on the logic rather than handling structural cruft.

**Link to work:** [Coding Train's Express](https://www.youtube.com/watch?v=Kw5tC5nQMRY&ab_channel=TheCodingTrain)

### Day 55: 1 October, 2020

**Today's Progress**: Implemented the method.DELETE & method.PUT for the Node.js fileserver.

**Thoughts**: Learning how to handle requests has been an unexpectedly complex experience. Currently looking into studying the Stream and the related Event paradigms in Node.js more, as the fileserver makes heavy use of the `createReadStream()` and `createWriteStream()` methods.

**Link to work:** [Node.js Fileserver](https://github.com/RashidUjang/node-fileserver)

### Day 54: 30 September, 2020

**Today's Progress**: Brushed up on `async` and `await` keywords in Javascript and continued learning Node.js from the Eloquent Javascript book.

**Thoughts**: Back-end programming is a lot more interesting than I thought! Learnt about the `Stats` object in Node.js, MIME types, `url.parse()` and `path.resolve()` and I'm even amazed `path.sep` is even a thing, where the separator of path segments will be correctly entered into the path, depdending on whether you're on Windows or a POSIX based system.

**Link to work:** [Node.js Fileserver](https://github.com/RashidUjang/node-fileserver)

### Day 53: 28 September, 2020

**Today's Progress**: Continued learning Node.js from the Eloquent Javascript book.

**Thoughts**: The Eloquent Javascript book has me creating a HTTP fileserver from scratch, which is not an easy task and explains the various comments left in the files. Some new things I've learnt today is the concept of `stream.pipe()`, some nifty differences between `{}` and `Object.create(null)` and piece of code that stores corresponding functions into an object that when, depending on key that is used on the methods object, will make the handler function that calls the object call a different function.

**Link to work:** [Node.js Fileserver](https://github.com/RashidUjang/node-fileserver)

### Day 52: 27 September, 2020

**Today's Progress**: Continued learning Node.js from the Eloquent Javascript book.

**Thoughts**: Learnt about the Filesystem, HTTP and Stream modules. Back-end programming is a much different paradigm than front-end programming where browser technologies are favourted as opposed to back-end where much more of the knowledge I have on basic computer science topics such as processes, threads, networking and the concept of streams. I've decided that the next application to be done is another common app: **budgeting app**.

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
