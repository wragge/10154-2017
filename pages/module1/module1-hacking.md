---
title: Hacking the web
keywords: 
last_updated: July 19, 2017
sidebar: home_sidebar
permalink: module1-hacking.html
folder: module1
---


### Let's hack ASIO!

This thing we call 'the web' isn't a thing at all. We talk about 'web publishing' and 'web pages' as if they're products of the print world. But if you look underneath what's presented in your browser you'll see each 'page' is an assemblage of files, standards, protocols, and technologies, all pulled together and rendered in a human-readable version by your browser.

This is important because we can play around with these layers. We don't have to take the web we're given. We can change it.

Let's have a peek beneath the hood and see if we can break something...

(These instructions assume you're using [Chrome](https://www.google.com/intl/en/chrome/browser/desktop/index.html) as your web browser. All browsers provide a console, but the way you open it can vary.)

* Let's start by going to the [ASIO website](https://www.asio.gov.au/).

* Now open up your browser's Javascript console. In Chrome press `Ctrl+Shift+J` (Windows / Linux) or `Cmd+Opt+J` (Mac).

* Cut and paste the code in the box below into the console, then hit **Enter**.

``` javascript
document.getElementsByTagName('body')[0].innerHTML = '<h1>All your secret are belong to us!</h1>';
```

Congratulations you just hacked ASIO! The unmarked black vans are already pulling up outside...

Don't worry, it's ok. Nothing was actually changed on the ASIO site. All the various bits that make up the ASIO home page are stored in your browser in a thing called the [Document Object Model](http://eloquentjavascript.net/13_dom.html) or DOM. The Javascript console lets you play around with the contents of the DOM. 

* Reload the ASIO home page. See, it's still there!

* Cut and paste the code again. But this time change the text between the `<h1></h1>` tags before you hit **Enter**.

In this example we've replaced the contents of the page's `<body>` tag. But we can be more selective.

* Reload the page again.

* Cut and paste the following code and then hit **Enter**.

``` javascript
document.getElementsByTagName('img')[1].src = 'https://static.guim.co.uk/sys-images/Guardian/Pix/pictures/2014/9/26/1411702268561/firstdog-eggplant-620.jpg'
```

Hopefully, you should see [something like this](https://www.dropbox.com/s/py8lg9ak7ucok4b/asio-eggplants.jpg?dl=0).

In this example we're selecting an `<img>` tag and replacing the source of the image with the url for one of [First Dog on the Moon's cartoons](https://www.theguardian.com/profile/first-dog-on-the-moon). Much better!

* Reload the page.

* Cut and paste the code again, but this time try changing the `1` in the square brackets to `0` or another number. What happens?

### Hacking and hackers

Perhaps you're a bit nervous about using the work 'hack'. The media often equates 'hacking' with breaking into computer systems or stealing credit card details. But ‘hack’ has a number of definitions, both positive and negative. [Mark Olsen](http://learnonline.canberra.edu.au/pluginfile.php/1703281/mod_resource/content/1/Olson%2C%20Mark%202013%20Hacking%20the%20humanities%2C%20Belfiore%2C%20Eleonora%2C%20Upchurch%2C%20Anna%2C%20Humanities%20in%20the%20twenty-first%20century%20237-250.pdf) describes the ‘hacker ethos’ as:

> ‘a way of feeling your way forward through trial and error, up to and perhaps beyond the limits of your expertise, in order to make something, perhaps even something new. It is provisional, sometimes ludic, and involves a willingness to transgress boundaries, to practice where you don’t belong… Whether eloquent or a kludge, a hack gets things done.’

Olsen explores what hacking means in the context of the humanities, arguing not only that hacking has a legitimate place in humanities practice, but that the humanities itself needs to be hacked to foster the development of new skills and literacies.

I describe myself as a 'historian and hacker' -- I use code to 'get things done', to explore new ways of seeing digital cultural collections. 

### X-ray goggles

{% include image.html file="xray-goggles.png" url="https://goggles.mozilla.org/" alt="Screenshot of the XRay Goggle site" caption="Mozilla's X-Ray Goggles" %}

The Mozilla Foundation has created a tool called X-Ray Goggles that makes it easy to explore and change the content of any web page.

* Go to the [X-Ray Goggles page](https://goggles.mozilla.org/)

* Create an account with Mozilla so you can save your projects -- just click on 'Create an account' at the top of the page and follow the instructions.

* Now follow the instructions to install X-Ray Goggles in your browser. It's basically just a matter of dragging the pink button to your browser's bookmarks bar.

* Once you've installed X-Ray Goggles, click on the 'Sample activity page' button and follow the instructions.

* Note that once you've edited an element, you need to click **update** to save your change and move on to the next task.

Ok, so creating and naming cute animals is not terribly exciting. But now you know how to use X-Ray Goggles, you can remix any web page!

Perhaps you think that the websites of our national collecting institutions could benefit from an alternative perspective? Why not visit the [National Library](http://nla.gov.au), [National Museum](http://nma.gov.au/), [National Gallery](http://nga.gov.au), or [War Memorial](http://awm.gov.au) sites and make a few improvements?

* Go the site you want to hack.

* Click on the X-Ray Goggles button in your toolbar to activate the editor. You'll notice some buttons appear at the bottom right of the page.

* Just click any element (text or image) on the page to open it for editing. 

* Try changing the text. Replace images by substituting the `src` attribute with a url to an image somewhere on the web.

* Once you're happy with your remixed page, click on the **Publish** button. (You'll need to be logged in to your account.)

* Share the url of your 'published' version on Slack for others to see.

{: .bg-context .bg-warning}
**Portfolio alert!** Save a screenshot of your remixed page and the url to your 'published' version in your Portfolio.

### The people inside

There are other ways of modifying the DOM to hack the web. Userscripts are little Javascript programs that run in your browser, modifying the contents of selected pages. For example, I've created [a userscript](https://gist.github.com/wragge/2941e473ee70152f4de7) that inserts the faces of people subject to the restrictions of the White Australia Policy into relevant records in the National Archives of Australia's RecordSearch database -- instead of just metadata, you see [the people inside](https://storify.com/wragge/the-people-inside). You can [install it yourself]((http://timsherratt.org/digital-heritage-handbook/docs/installing-userscripts/)).

{% include image.html file="peopleinside-before.png" url="https://gist.github.com/wragge/2941e473ee70152f4de7" alt="Screenshot of RecordSearch without the userscript" caption="RecordSearch before my userscript" %}

{% include image.html file="peopleinside-after.png" url="https://gist.github.com/wragge/2941e473ee70152f4de7" alt="Screenshot of RecordSearch without the userscript" caption="RecordSearch after my userscript" %}

Browser extensions are similar -- they're just packaged and distributed in a more formal way. [Stop Tony Meow](http://stoptonymeow.com/) is a browser extension that replaces images of Tony Abbott with kittens. How do think it might work?

[Rehumanize](http://rehumanize.me/) is a browser extension that replaces words like 'boat people' and 'illegals' with 'humans'. A simple hack that is nonetheless both pointed and powerful.