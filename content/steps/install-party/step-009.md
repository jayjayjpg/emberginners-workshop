---
title: Step 9 - Ember
order: 9
---

Now that we have Node installed we can use `npm` to install `ember-cli`

```bash
npm install --global ember-cli
```

there is a shorter way to write this too which can help to save you precious seconds

```bash
npm i -g ember-cli
```

Once you have installed `ember-cli` globally you should navigate to the directory you want to put your ember app (remember our `cd` step to change to the right directory). Now that you're in the right place you can run `ember new` to crate your ember app:

```bash
ember new awesome-app
```

this will take a while to install all the dependencies.

Next up you just need to navigate into your new app using `cd` and run `npm start`

```bash
cd awesome-app

npm start
```

You can also use `ember serve` to start your ember app.

If all has gone well you can navigate to http://localhost:4200 to see the Ember demo app running
