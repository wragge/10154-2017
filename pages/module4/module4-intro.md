---
title: Introduction of Module 4
keywords: 
last_updated: July 19, 2017
tags: [introduction]
summary: ""
sidebar: home_sidebar
permalink: module4-intro.html
folder: module4
published: false
---

In this module you will...

By the end you should:

* Know this...
* And this...


### Making a difference

Here's something to try:

* Go to [asio.gov.au](https://www.asio.gov.au/) (of course)

* Right click somewhere on the page and select 'Inspect' or 'Inspect Element' from the menu. (You might need to use Chrome.)

* A complicated looking control panel opens up that tells you all about the innards of the web.

* Click on the 'Console' tab.

* Cut and paste the code in the box below into the console, then hit enter.

``` javascript
document.getElementsByTagName('body')[0].innerHTML = '<h1>All your secrets are belong to us!</h1>';
```

{: .bg-danger .bg-context alert}
Warning you've just hacked ASIO's website! (No not really... just reload to get it back.)

This takes us back to Week 1, when we were playing around with X Ray Googles. One of the points I was trying to make is that the web isn't 'published' like a book or a magazine -- we have the power to change what we're given, to be creators of our online experience, and not just consumers.

In week 1 I introduced userscripts as a way of playing around with the web. For me, they're a way of exploring alternate possibilities -- 'What would happen if...?' types of questions. It's also a way of making a point about what collection interfaces **don't** show.

So, for example, I created a userscript that puts the faces of people who lived under the restrictions of the White Australian Policy [back into RecordSearch](https://gist.github.com/wragge/2941e473ee70152f4de7). Instead of just metadata, you see [the people inside](https://storify.com/wragge/the-people-inside).

![RS faces]({{site.baseurl}}/images/rs-faces-after.png){: .img-example .img-responsive}

As I noted last week, I've created a new userscript that [puts information about redactions into RecordSearch](https://gist.github.com/wragge/b6d120a712ae7d598ab70e228f070bac) -- so you can see what you can't see.

Last week, I also pointed you to the work of [Documenting the Now](http://www.docnow.io/) project. They're developing archiving tools that will enable them to capture the voices and experiences of those who might not otherwise be documented in cultural institutions or the mainstream media.

Digital cultural heritage is not just about making cool things online (although it is pretty awesome). It's about using the tools and technologies at our disposal to make a difference.

### What's it all for?

While you're at it, you might want to read Mark Sample's ['A protest bot is a bot so specific you can't mistake it for bullshit'](https://medium.com/@samplereality/a-protest-bot-is-a-bot-so-specific-you-cant-mistake-it-for-bullshit-90fe10b7fbaa#.yx07w42ee). I refer to it in my talk -- it's powerful and thought provoking.

### Looking ahead

If you're interested in pursuing work in digital cultural heritage some and talk to me! There are a number of possibilities -- research projects, internships, perhaps even honours or postgrad work.

I'll be leaving the course content in my Digital Heritage Handbook, so feel free to dip back in at any time for links and information.

Happy hacking!

### Digital realities (AR, VR, 3D)

This week we're exploring multiple realities -- augmented reality, virtual reality, and even the amazing world of 3D! But I have to admit I'm a bit uncertain. With the other tools and technologies we've examined, I feel like I've had a pretty good understanding of their value and use. But while I think there are some exciting possibilities ahead for 3D imaging, I'm not sure about AR and VR in the cultural heritage setting. Perhaps it's because I feel like we've been there before. I remember playing around with VRML in the '90s; when Second Life was going to be the next big thing for museums; and when everybody was going round sticking QR codes on things. Are these technologies different? Will they change the way we experience cultural heritage?

I'd like to know what you think. Instead of trying to tie these things up in a neat bundle for you today, I thought I'd just offer examples and raise questions. As you explore each of the examples I'd like you to think about what they might contribute to the way we experience and understand cultural heritage. Are they gimmicks or groundbreaking? The future or mere fad?

### 3D imaging

As I said, I think 3D imaging is becoming an established part of the digitisation toolkit. Basic photogrammetry -- extracting spatial data from photographs -- has moved from research projects to consumer products. Indeed, if you have a smartphone you can try it for yourself. [Download 123Catch](http://www.123dapp.com/catch) and have a play. Unfortunately the documentation of the website seems to refer to an older version of the software, but it's very easy to use.

* Create a free account on the [123D site](http://www.123dapp.com/). This will enable you to save and share your models.

* Set up the object you want to image in an evenly lit space that you can easily move around (you need to be able to photograph it from all angles).

* Open the app and log in to your account. 

* Click on the '+' to start a new project.

* Move around the object taking photos from different angles.

* Also take some from above the object.

* Once you have about 20 to 30 photos you're ready for the next step. Click on the blue tick.

* You can then review your photos, deleting any that didn't work.

* Once you're happy click on submit.

* Your photos are then uploaded to the 123d server where they're magically stitched together. It can take quite a while, so be patient!

* Once your model is complete you can view it under your account on the 123D site.

The result will probably be a bit messy, with various bits of the background included. If you want to clean it up you can use tools like [MeshMixer](http://www.meshmixer.com/) (available for free from the 123D site) to select and delete the bits you don't want.

Here's a 3D model I created at home with my kids. You can [view the original version](http://www.123dapp.com/catch/Terry-the-pterodactyl-/5273824#) created with 123D Catch here. I then cleaned it up and uploaded to [SketchFab](https://sketchfab.com/), which has a great online 3D viewer.

<div class="sketchfab-embed-wrapper"><iframe width="640" height="480" src="https://sketchfab.com/models/86821f9c17a84cb6bc511462229a07cf/embed" frameborder="0" allowvr allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" onmousewheel=""></iframe>

<p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;">
    <a href="https://sketchfab.com/models/86821f9c17a84cb6bc511462229a07cf?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">Terry</a>
    by <a href="https://sketchfab.com/wragge?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">wragge</a>
    on <a href="https://sketchfab.com?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a>
</p>
</div>

Of course there are much sophisticated and accurate tools available for 3D imaging. Using technologies such as [LIDAR](https://en.wikipedia.org/wiki/Lidar) it's possible to create 3D models of complete heritage sites.

Cultural institutions are starting to make selected collection items available as 3D models:

* [Smithsonian's 3D gallery](http://3d.si.edu/browser)
* [MAAS (Powerhouse) 3D downloads](http://www.powerhousemuseum.com/collection/database/download.php)
* [Museum of Victoria](http://www.thingiverse.com/MuseumVictoria/designs)
* There are also a [lot of museums](https://sketchfab.com/members?segment=organization%2Fmuseum) posting models to SketchFab. They also have a [Cultural Heritage section](https://sketchfab.com/models/categories/cultural-heritage). Here's a very cool [3D anatomy book](https://sketchfab.com/models/03dded8f65934e26a37ae41122b1c804) from the 16th century.

Not only can you view the models online, you can download them and [feed them into a 3D printer](https://museumvictoria.com.au/about/mv-blog/may-2013/3d-printing-at-smartbar-/) to make your own physical copies. This seems to me to have important educational uses, particularly in remote areas -- what do you think? Does the ability to handle an item (even a 3D printed plastic version) add to our understanding of it?

### Virtual tours 

This is not really 3D and not augmented reality, but I thought it was worth mentioning here. As you may know, Google's StreetView technology has moved inside some institutions, allowing people to take virtual tours. Here's the [National Museum of Australia](https://www.google.com/culturalinstitute/beta/streetview/national-museum-of-australia-galleries/5wF161fenKUT5w?sv_h=350.6329158316756&sv_p=-28.80241873465554&sv_z=0.01656923402770183&sv_lid=13174458512189543304&sv_lng=149.12111414211688&sv_lat=-35.29381970840363).

The NMA also provides [laser-guided virtual tours](http://www.nma.gov.au/engage-learn/robot-tours) courtesy of two mobile telepresence robits.

I suppose one theme across all of the technologies we're looking at today is the attempt to create new understandings or experiences of space that blend the physical and the digital. But how new is this? How are technologies such as augmented reality different to old-fashined audio guides? Is access a key point -- the fact that these experiences can be delivered remotely?

### 3D worlds

As I noted above, 3D scanning technologies can be used to help build up models of complete sites. These can then be populated with reconstructed buildings, and even animated people.

The [Visualising Angkor](http://infotech.monash.edu.au/research/groups/3dg/projects/visualising-angkor.html) project is a particularly impressive example, where researchers have not only tried to reconstruct a site, they've tried to represent to rhythms of everyday life -- the sun rises and sets, people and animals move about their lives. All of this is based on detailed archaelogical evidence. Unfortunately the computing power required to run the simulation means it can't be accessed online, but you can find some videos on the [Google Cultural Institute page](https://www.google.com/culturalinstitute/beta/exhibit/visualising-angkor/AR6A-vMq).

How about a tour of ancient Rome? The Rome Reborn project has created a detailed 3D model of Rome in 320 CE.

{: .img-example}
<iframe src="https://player.vimeo.com/video/32038695" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/32038695">Rome Reborn 2.2: A Tour of Ancient Rome in 320 CE</a> from <a href="https://vimeo.com/frischer">Bernard Frischer</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

Distance in time is not the only reason to build 3D worlds. Sites can be inaccessible for a variety of reasons, and 3D models can provide a way of documenting and experiencing locations that might be at risk.

Researchers in Western Australia have created a 3D model of the wreck of the HMS Sydney. As you can see from this [ABC report](http://www.abc.net.au/news/2016-05-16/hmas-sydney-wreck-3d-reconstruction/7408688) it offers a powerful emotional experience.

You've probably also heard of attempts to use 3D modelling to document and possibly even reconstruct parts of Palmyra destroyed by ISIS. Recently a replica of the Palmyra Arch of Triumph, created using 3D modelling techniques, [was unveiled in London](http://www.bbc.com/news/uk-36070721). 

It's also possible to create models of places that never actually existed. Researchers on the Digital Panopticon project have created a [3D model of Jeremy Bentham's ideal prison](https://www.digitalpanopticon.org/?p=1188), designed in the 18th century, but never built. This them to think about how the space might have worked, and what the experiences of prisoners might have been within such a space.

But not everyone thinks these types of projects are a good idea. Critics of the reconstructed Palmyra arch, for example, have pointed to the [danger of creating](http://www.ibtimes.co.uk/palmyra-arch-london-unethical-reconstruction-disneyland-archaeology-criticised-1555659) a Disneyfied version of the past. Might such reconstructions obliterate memory rather than preserve it? How do we experience and document the processes of destruction and decay alongside such freshly-minted versions of the past? Are these reconstructions all a bit too clean?

### AR & VR

Nowadays if you want to explain augmented reality to someone it's easy -- you just say it's like Pokemon Go. AR is a blend of physical and digital, with new experiences, information and activities layered on top of our physical environment. There's some definitions and a good dash of added hype [in this article](https://medium.com/glam-bytes/augmented-museums-ad9f18d3ba8c#.4a6yzob4g) about 'Augmented Museums'. Clearly some people can see the business opportunities.

Location-enabled applications that present historical photographs based on your location have been around for a number of years. A couple of years ago the Museum of London created an iPhone app called [StreetMuseum](http://www.museumoflondon.org.uk/Resources/app/you-are-here-app/home.html) that blended past and present.

{: .img-example}
<iframe width="100%" height="500" src="https://www.youtube.com/embed/qSfATEZiUYo" frameborder="0" allowfullscreen></iframe>

Earlier this year the Art Gallery of NSW presented [an immersive 3D experience](http://paidcontent.smh.com.au/agnsw/art-gallery/article/pure-land-inside-mogao-grottoes-dunhuang/) that allowed visitors to explore intricate cave murals from the UNESCO World Heritage listed Mogao Grottoes in China. This work has been presented in a variety of forms around the world. It's not just a 3D reconstruction, because various elements of the paintings come to life. Here's a video showing it on display in HongKong.

{: .img-example}
<iframe width="100%" height="500" src="https://www.youtube.com/embed/BbU7LvPhLSE" frameborder="0" allowfullscreen></iframe>

Augmented reality apps can be used within a museum context to provide additional layers of information and interactity, as in this example.

{: .img-example}
<iframe width="100%" height="500" src="https://www.youtube.com/embed/v_cvAGUItU0" frameborder="0" allowfullscreen></iframe>

If you view this video on YouTube you'll see that the caption proclaims: 

> Visiting a museum is no longer a one-sided, passive experience, as we've developed an interactive exhibition tablet app using the newest innovative mobile technologies...

Does giving a visitor an iPad app make the experience less 'passive'? Isn't their experience still carefully curated? Clearly there's value in giving visitors access to more information, but is this a good way to do it?

Virtual reality, on the other hand, immerses you in a totally manufactured digital environment. And you have to wear funny-looking goggles. All the big players are working on VR technologies -- most notably FaceBook and Microsoft. (Let's not mention Google Glasses).

Microsoft is building up to the release of its HoloLens and there's much hype about the 'Minority Report' style of interactivity it will enable. It's interesting, however, that Microsoft has used the possibilities for cultural heritage as part of its pitch to potential developers:

<iframe width="100%" height="500" src="https://www.youtube.com/embed/pLd9WPlaMpY" frameborder="0" allowfullscreen></iframe>

One of the problems with VR is of ourse that you need special hardware for it to work. Videos don't capture the experience. If you'd like to explore some of the possibilities and you've got a smartphone handy you can order [Google Cardboard](https://vr.google.com/cardboard/). It's a simple VR viewer that uses your existing phone -- for $30 or so you can start experimenting.

The Google Cardboard app provides some fun examples, including museum exhibits. You can also search the App Store or Google Play for 'Google Cardboard' to find other VR apps. Beware -- the experience can be a bit unsettling!

You might we use this sort of technology? One of the nice features of SketchFab is that its 3D viewer is compatible with VR devices, including Google Cardboard. If you created a model with 123D Catch, you can easily upload to SketchFab and view using Google CardBoard. (Yes you'll need to create a free [SketchFab](https://sketchfab.com/) account.)

* Log in to the [123D site](http://www.123dapp.com/catch).

* Hover over 'ME' in the top menu and select 'Models'.

* You should see the model you created with 123D catch. Click on it.

* Click on the **Edit/Download** button and select 'Download 3D models'.

* In the list of downloads select the 'Mesh package' -- you can uncheck the other options.

* Once the file has downloaded, login to your [SketchFab](https://sketchfab.com/) account.

* Click on the **Upload** button and then select the file you just downloaded.

* Click **Continue** and wait while the file is processed.

* Once it's finished, click **Continue** again and wait some more.

* Eventually your model will open in the 3D viewer. Click on **Edit 3D settings** to play around with how it looks.

* To view in VR, just hover over the image and then click on the Google Cardboard icon. It will give you a link to open on your phone.

{: .bg-context .bg-info}
Note that the free SketchFab acount will only let you upload models that are less than 50mb.

If you didn't create a model with 123D catch you can still play around in SketchFab. Try downloading a 3D model from some of the collections mentioned above. This [jug](http://www.powerhousemuseum.com/collection/database/STLfiles/184995-campanian-askos.zip) from the Powerhouse and this [trilobite](http://www.thingiverse.com/thing:91832/#files) from the Museum of Victoria are both under SketchFab's free 50mb limit. Once you've downloaded the files, just upload them to SketchFab as described above.

For further experimentation download [Google's Street View](https://maps.googleblog.com/2015/09/introducing-new-street-view-app-from.html) app. You can use it to create 360 degree 'globe' images of any location that you can then explore in VR using Google Cardboard.

This is all a lot of fun. But how might you use this technology in a cultural heritage setting? Will we really want to spend our time immersed in a virtual museum? What sort of experiences do we want to create?

Perhaps the really exciting thing is not what cultural institutions will do with this technology, but what ordinary people will do with cultural collections using these sorts of tools.

### Games

There is a big overlap between VR/AR and the world of gaming. Indeed, the game creation platform [Unity](https://unity3d.com/) is often used as the platform for building and exploring 3D worlds.

If you're interested in the connection between cultural heritage and gaming, keep an eye on the [Play the Past](http://www.playthepast.org/) blog. Their most recent post is about creating interactive histories using [Twine](https://twinery.org/) (which I've mentioned previously).

One final video describes a project undertaken by the Auckland War Memorial Museum. Working with a local school they ['recreated' the Gallipoli campaign](http://www.aucklandmuseum.com/education/activities-and-resources/gallipoli-in-minecraft-learning-kit) using Minecraft.

<iframe width="100%" height="500" src="https://www.youtube.com/embed/Tpa7zyIiuSo" frameborder="0" allowfullscreen></iframe>

Would you be interested in such a project? 