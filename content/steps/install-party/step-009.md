---
title: Step 9 - Ember
order: 9
---

## What is Ember?

Ember, or EmberJS is a program built on top of the programming language JavaScript and which will help us to build our very first website! We will talk more about what Ember is on the Workshop Day tomorrow - for anyone who's curious to know more, feel free to [check out the official project website](https://emberjs.com).

But to finalise the installation party and be ready for tomorrow, let's get Ember installed on our machines.

### Installing Ember

Because we installed Node in the previous step, we can now use a new program in our terminal, that comes installed with Node out of the box. This program is called `npm`. The `npm` program accepts text instructions from us via the terminal. One of these instructions allows us to install new programs with it. Let's install `ember-cli` to get Ember setup on our machine using the `npm install` command as follows:

```bash
npm install --global ember-cli
```

there is a shorter way to write this, too, to save you some time:

```bash
npm i -g ember-cli
```

The `-g` (`--global`) flag makes us install `ember-cli` - a program used with our Ember program - in a way that we can use it as its own command (similar to `npm`) in any folder of our computer. If you are curious to learn about what this means in more detail, feel free to reach out to the mentors.


### Creating an Ember app

Once you have installed `ember-cli` globally you should navigate to the directory you want to put your ember app (remember our `cd` step to change to the right directory or check out the [cheatsheet](http://www.pragtob.info/rails-beginner-cheatsheet/)). Now that you're in the right place you can run `ember new` as follows:

```bash
ember new awesome-app
```

this will take a while to install additional code in your project, so-called dependencies. Check out what's happening in your terminal!

The instruction `ember new` tells the `ember-cli` program that we had installed earlier that it should create a new application for us. This means, that it will

- download all the code for an Ember app
- create new directories in the app's folder
- download related code that is not from Ember itself, but which Ember requires to work (dependencies)
- configure our app with the default settings to work right off the bat


After the app creation process via `ember new` has finished, let's take a look if everything's working as expected.
Let's navigate into your new app using `cd` and run `npm start`

```bash
cd awesome-app

npm start
```

Alternatively, you can also use `ember serve` to start your ember app instead of `npm start`.

If all has gone well, you can navigate to http://localhost:4200 to see your very first Ember app running. You can do so by copy-pasting the url into the address bar of your browser Chrome and hitting Enter. See what it does live in action!


### Where is this website coming from?

Remember how we talked about websites living on servers, so that your browser can display them to us when we use the correct url? The Ember app you created can be visited via its address at [`http://localhost:4200`](http://localhost:4200) from your browser. But where does the website live?

In this case, we used the `npm start` (the same as `ember serve`) command to turn our own computer into a **server** which serves the website to the `localhost` address. You can confirm this by stopping your server (by hitting `Ctrl` + `C` while in the terminal) and visiting `http://localhost:4200` in your browser again. Now the website cannot be reached. If you start up your server again (run `npm start` in the terminal), it will be back up for you to view at the address mentioned above.

Now we don't only know how to use the terminal, install programs via `npm` and how to create an Ember app, but we even know how to run your own local server. Congrats to us and see you back tomorrow for the workshop!
