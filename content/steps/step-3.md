---
title: Step 3
order: 3
---

# An Intro to Routing in Ember

## What is routing?

Our application allows us to navigate different parts of it via url. The url is the name of a sub page in our website, which we can type into the browser navigation bar to allow us to land on that part of our app. The url allows to access different `routes` of our Ember app.

Routing in web applications is important, since it enables users to share a specific part of the app with others. E.g. if you want a friend to take a look at your super-rentals overview page, you can just send them the link (a.k.a url) that opens that part of the application.

To create routes that can be accessed via certain urls, we use the Ember CLI and more specifically its **generator** s. Using the `ember generate` command we can create all kinds of things in our application, including routes.

<!--
- Exercise: Generate a Route (‘about’). What is a route? Investigate new page in browser.
- Exercise: Copy-paste template into route. Observe server reload and page in the browser.
- Primer: Objects in JavaScript. What are values and properties?
- Ember Object Model. What is an EmberObject, how does it look like? -->


### Exercise: Generate a new route in your Ember app

- Open your terminal
- Type in `ember generate route about` and hit enter. Ember CLI will create several JavaScript files for you and edit some of them automatically for you. Check out the changes in these files in your text editor!
- Open `app/router.js` and investigate the newly added route: `this.route('about')`
- Open your application in your browser to see the new route in action: `http://localhost:4200/about`
- In our app, a route is represented by a JavaScript file (`.js` file ending) and a template (`.hbs` file ending). Open the template `app/templates/about.hbs` in your text editor
- Copy-pasta the following into your template (`app/templates/about.hbs`)

```hbs
<div class="jumbo">
  <div class="right tomster"></div>
  <h2>About Super Rentals</h2>
  <p>
    The Super Rentals website is a delightful project created to explore Ember.
    By building a property rental site, we can simultaneously imagine traveling
    AND building Ember applications.
  </p>
</div>
```

- Save the file `app/templates/about.hbs` and go back to your app in the browser. What changed?


## What are JavaScript objects?

Objects in JavaScript are a special kind of data type. Each data type in JavaScript comes with its own characteristics in how you can store and access data. Data can come in many forms. E.g. the word 'tomster' in a JavaScript program can be a piece of data. If you wanted to use the word `tomster` in your JavaScript code, you'd need to do so using the `string` data type for example. The number 42 is of the `Number` data type.


In Ember most things that we work with revolve around objects though. An object is defined by having no, one or several properties, where each property has a specified value. An object can look for example like this:


```js
{ name: 'Marie Curie',
  job: 'Physicist',
  birthyear: 1867 }
```

The object allows us to store related information together one single piece of data. Similarly to Strings (words) and Numbers (numbers), objects can also be stored via variables. We can e.g. save the object above with the variable `scientist` as follows:


```js
let scientist = {
  name: 'Marie Curie',
  job: 'Physicist',
  birthyear: 1867
};
```


An object and its properties can be updated as follows:

```js
let scientist = {
  name: 'Marie Curie',
  job: 'Physicist',
  birthyear: 1867 };

scientist.name = 'Marie Skłodowska Curie';
console.log(scientist);
/*  This will log to your console the updated object:
{  name: 'Marie Skłodowska Curie',
  job: 'Physicist',
  birthyear: 1867  };
*/

```

## What is an Ember Object?

Objects in Ember are a specific type of object. They come with many different features that native JavaScript objects which we learned about in the previous section don't have. In the scope of this workshop we won't be able to cover the special things an EmberObject can do versus a normal object, but we want to take a look on how to create one and be able to recognize it later on in the course.

Learning about the EmberObject is also important for knowing that almost everything we create in an Ember app is based on an EmberObject. We'll come back to that notion later during the course.

You can create an EmberObject as follows:


```
import EmberObject from '@ember/object';

let programmer = EmberObject.create({
  title: 'Ada Lovelace',
  birthyear: 1815,
});

```


### Exercise: Creating and passing an EmberObject

In this exercise we want to create a new EmberObject which can be used in the `about` Route which we created earlier. We will use the EmberObject to carry information that will be displayed on the about page.

- Open the file `app/routes/about.js` in your text editor
- import the EmberObject from the `@ember/object` package as seen above in the previous example. You can put the import statement at the very top of the file
- inside of the `model() {}`, create the EmberObject with your application's name (you can choose one) as the object's `name` property and a descriptive text as the object's `text` property
- indicate that you'd like to pass the object down to your route's template by using the `return` keyword. Example on using `return` with an example object `myobject`:

```
model() {
  return myobject;
}

```

- Revisit your about page in your browser by visiting `http://localhost:4200/about` and see what has changed now


## How are routes and templates connected?

Earlier we created a new about route using the Ember CLI by typing `ember generate route about` into the terminal. This gave us two files, namely

- app/routes/about.js
- app/templates/about.hbs

In this part we want to take a look how templates and route files are interconnected. You already returned data from your route file to a template in the previous exercise. But how is it displayed there?

### Exercise: Update the sub title of the about page

- Open app/templates/about.hbs and find all the properties of your `model` that are displayed
- Go back into app/routes/about.js and add the missing property to the object returned from `model() {}`
- What happens in your application's `about` page in your browser?