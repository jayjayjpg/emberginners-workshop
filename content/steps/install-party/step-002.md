---
title: Step 2 - The Browser
order: 2
---

## What is a browser?

A browser is a program running on your laptop or desktop computer that allows you to browse the internet and visit websites online. Examples for commonly used browers are Google Chrome, Firefox, Safari and Edge.

At the top of the browser window we find an address bar that lets us enter so-called **URLs**. An example for an url is `https://emberjs.com`. Colloquially urls are also known as "links".

When we type or copy-paste a url (a "link") into the address bar of our browser and hit the `Enter` key, the browser takes note of what we typed and will redirect us to the website.

![Chrome Address Bar](/images/google-address.png)

When we get redirected to the website, the browser then displays the website to us in the browser window and allows us to interact with it.

### What happens in the browser when we visit a website

When we enter a url into the address bar of a browser, the browser tries to find the location of the website that refers back to the url it has been given. The url functions as an address for the website.

You may wonder: how can a website have its own address?

Not only humans, but also websites need a place to live. In general, websites live on so-called **servers**.

![Analogy Server and Website. Servers may host websites, just like houses host people.](/images/ember-workshop-install-export-p1-a.jpg)

A website may be found and retrieved by its address, its so-called **IP** address (Internet Protocol Address). An IP is a unique label consisting of numbers that is assigned to devices connected to the internet, e.g. also to servers.

![Analogy IP and Websites. Websites can be located on a particular server by their unique IP address](/images/ember-workshop-install-export-p1-c.jpg)

As internet users we usually don't deal with IPs very much, but instead rely on more human-friendly urls consisting of words to navigate the web. Yet, every url for a website that is live relates to a unique IP which is a descriptive address for a particular server in which a website lives.

![Analogy IP and Websites. Websites can be located on a particular server by their unique IP address](/images/ember-workshop-install-export-p1-b1.jpg)

A server is usually a computer that is running in some other part of the world, which is connected to the internet and will _serve_ a website back to anyone who requests it (e.g. a user visiting the website using their browser). There are other ways than using a browser to ask a server to return a website. We will learn more about different methods later.


### What else can a browser do?

Browsers allow you to not only view websites which are online and living on far-away server that you do not own (e.g. when visiting `https://emberjs.com`), but also websites that are **running on your computer** and that you have full control over. It is possible to make your own computer act as a server -  a home for website you want to build! We call a server that lives on our computer a **local server** or sometimes also a **localhost**. We will see how we can run our own local server during the course of this workshop.

Finally, apart from letting you visit, view and interact with websites, a browser also comes together with a toolbox of useful features that allow you to write small programs right in your browser.

Professional and hobbyist developers oftentimes use browsers to view and inspect the websites they are developing while they are running on their computer (=on their local server) or they make use of the browser's toolbox to write programs to manipulate those websites.

For now, all you need to know is, that a browser will help you to follow the exercises in this workshop in which we will also run and develop a website locally (=on our computer). This way you as a programmer will be able to bring your website to life and review it even before it is online.

#### Installing a browser

Several browsers provide us with tools that help us to develop our web application. In the scope of this workshop we'd like to use **Google Chrome**.

![Chrome Download Page](/images/chrome-dl.png)

If you haven't got it on your computer yet, you can download and install it over [here](https://www.google.com/chrome/).
