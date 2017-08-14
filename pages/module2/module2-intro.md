---
title: Introduction of Module 2
keywords: 
last_updated: July 19, 2017
tags: [introduction]
summary: ""
sidebar: home_sidebar
permalink: module2-intro.html
folder: module2
published: false
---

In this module you will...

By the end you should:

* Know this...
* And this...

### Big data / small data

There's a lot of hype around about data. 'Big data' in particular is talked up as the source of new insights in research and business. But what is the 'data' that we're interested in as cultural heritage workers? [Miriam Posner's article](http://miriamposner.com/blog/humanities-data-a-necessary-contradiction/) explores some of the complexities of 'data' from a humanities perspective. She notes that humanities researchers are:

> not generally creating data through experimentation or observation — more often than not, we’re mining data from historical documents. You name it, we’ve tried to mine it, from whaling logs to menus to telephone directories.

Rather than working with the outputs of machines, we're usually working with artefacts created by people which, as Miriam notes are often 'eccentric, disparate, and historically and geographically uneven'. Nonetheless, working with this information in a digital environment allows us to do and see things differently. I wrote a bit about this in ['"A map and some pins": Open data and unlimited horizons'](http://discontents.com.au/a-map-and-some-pins-open-data-and-unlimited-horizons/).

This week we're going to look at some varieties of data that can be useful within the cultural heritage sector. Where do you find it? How do you get it in a useable form? How can you clean up some of the messiness?

### Sometimes it's as easy as cut and paste

Let's start off with something simple. The [Australian Data Archive](https://www.ada.edu.au/historical/home) provides historical census data from 1833 to 1901. The data is available in a variety of formats. Some of it is still locked up in scanned images, so you'd have to transcribe it before you could do anything interesting. But some of it is available as nicely formatted HTML tables.

Follow the instructions at [Making simple charts with Plot.ly](https://timsherratt.org/digital-heritage-handbook/activities/creating-simple-charts-with-plotly/) to grab some of this census data and display it as a chart. You'll need to create a free account with [Plot.ly](https://plot.ly/). 

### Exploring data repositories

The federal and most of the state governments maintain portals to help you find government datasets. This includes an increasing amount of data from cultural heritage organisations. Here's the ones I know about:

* [data.gov.au](https://data.gov.au/) -- it's the federal portal, but it also contains some data from state institutions, such as [LINCTasmania](http://data.gov.au/organization/linctasmania)
* [data.act.gov.au](https://data.act.gov.au/)
* [data.nsw.gov.au](http://data.nsw.gov.au/)
* [data.qld.gov.au](https://data.qld.gov.au/)
* [Data.SA](https://data.sa.gov.au/)
* [data.vic.gov.au](http://data.vic.gov.au/)
* [data.wa.gov.au](http://data.wa.gov.au/)
* [data.tas.gov.au](https://data.thelist.tas.gov.au/)

Have a poke around on these sites to see what you can find. If you're not sure where to start, try searching for things like 'archives', 'history', 'heritage', or 'library'. Here's a few examples:

* [Tasmanian Inquests (1828-1930)](http://data.gov.au/dataset/tasmanian-inquests-1828-1930)
* [Consumptive patients 1897 to 1902 (Queensland)](https://data.qld.gov.au/dataset/consumptive-patients-1897-to-1902)
* [Portraits and people](http://data.gov.au/dataset/portraits-and-people) from the National Portrait Gallery

Note that the first two of these are available as CSV (Comma Separated Values) files. CSV files are like spreadsheets and can be easily opened and used in tools like Excel, or many of the web services we'll be playing with in coming weeks. The 'Portraits and people' data is available as an XML file. XML enables you to represent hierarchies within your data, so you can have more complex structures than in a flat CSV file. Many of the tools we'll look at can also use XML.

{: .bg-info .bg-context}
Once you've found an interesting dataset, think about how you might use it in your project. Could you visualise the data as a chart? Locate it on a map? Link it to other sources of data?

### WTFCSV

If you have a CSV file, but you're not sure what to make of it, [WTFCSV](https://www.databasic.io/en/wtfcsv/) is a fun little tool that can provide some useful insights. Try one of their sample datasets, or upload your own. What does it tell you about the data?

### APIs

I've mentioned APIs (Application Programming Interfaces) before. They provide data in a form that computers can understand, and allow us to build new tools and interfaces such as [Headline Roulette](http://wraggelabs.com/shed/headline-roulette/). To make use of an API you generally need some coding experience, but not always. Yvonne Perkins has written a [great tutorial](https://stumblingfuture.wordpress.com/2014/03/13/using-the-trove-api-with-excel-spreadsheets/) to show how you can use Excel to harvest newspaper articles from Trove using its API. My DIY [exhibitions](https://github.com/wragge/diy-trove-exhibition) and [headline roulette](https://github.com/wragge/diy-headline-roulette) also allow you to make use of the Trove API without any coding.

To understand how the Trove API works, play around with my [Trove API Console](https://troveconsole.herokuapp.com/). Just click on a few of the examples and see what happens. Look for 'q=' in the query box and try changing the value that comes after it. Don't worry -- you can't break anything!

The Trove Help Centre [provides more information](http://help.nla.gov.au/trove/building-with-trove) about the API, including a number of examples and experiments.

### Trove Harvester

Would you like a dataset containing hundreds or thousands of newspaper articles on the topic of your choice? If you do then my Trove Harvester can help! It's a tool that uses to API to save data about newspaper articles to a CSV file for further analysis. There's [detailed documentation](https://timsherratt.org/digital-heritage-handbook/docs/trove-newspaper-harvester/) here -- it requires a bit of setup and the good old command line, but it's pretty simple to use.

### Scraping data

Sometimes the data you want isn't available in a convenient form like CSVs or APIs. But if it's on a web page, you might be able to extract it using a process called screen scraping. Remember how X-Ray Goggles showed you the structures underlying web pages. Screen scraping uses those structures to indentify the bits of data you want on a web page -- once you've identified them, they can be extracted and saved in a nice structured format, such as a CSV file.

I've spent a lot of time screen scraping data from sources such as the National Archives of Australia (here's [70gb worth of ASIO files](https://github.com/wragge/asio-files) for example). But fortunately there are a growing assortment of tools to make the process much less painful. Let's try one!

Follow the instructions in [Screen scraping with Import.io]({{site.baseurl}}/activities/screen-scraping-with-import-io/) to create your very own dataset of members of the House of Representatives.

### Cleaning data

As we noted, cultural heritage data can often be messy and inconsistent. Fortunately there's a great tool for cleaning up messy data -- [OpenRefine](http://openrefine.org/).

Intersect have prepared [a useful tutorial](https://github.com/IntersectAustralia/TrainingMaterials/blob/master/CleaningAndExploringYourDataWithOpenRefine/Tutorial.pdf?raw=true) to introduce you to the power of OpenRefine. In particular, its ability to cluster variations in spelling and standardise them all with a single click is just like magic. It can save you many hours of painstaking manual work.

To use OpenRefine you'll need to [download and install it](http://openrefine.org/download.html). Use the latest version '2.6-rc2'.

Once you have it installed work through [the tutorial](https://github.com/IntersectAustralia/TrainingMaterials/blob/master/CleaningAndExploringYourDataWithOpenRefine/Tutorial.pdf?raw=true). Try to at least complete up to section 7. If you're feeling adventurous, go on to try some geocoding in section 8. We'll cover geocoding in a few weeks when we play around with maps. Don't worry about section 9 as the State Records of NSW website is currently undergoing some changes and the examples probably won't work.

There's [another OpenRefine tutorial](http://programminghistorian.org/lessons/cleaning-data-with-openrefine) using collection data from the Powerhouse Museum on the Programming Historian site. 

### Seeing like a computer

I thought I'd share my redaction art discoveries today because they're an example of how digital tools and techniques can lead you in all sorts of unexpected direction; but more importantly they're an example of the use of computer vision in cultural heritage.

There's no pre-built tools for finding redactions (at least not that I know of), so I had to code my own. However, there is a very widely-used library of code called [OpenCV](http://opencv.org/) that meets most computer vision needs.

I'll save you all the coding details, but I did want to walk you through the process. If you've used image editing tools like Photoshop, some of these steps might be familiar.

* I removed the colour from the image (converted to grayscale).
* I blurred the image slightly to remove some of the background noise, but I used a technique that is supposed to maintain sharp edges.
* I applied [thresholding](https://en.wikipedia.org/wiki/Thresholding_(image_processing)) to reduce the image to black and white.
* I found all the black bits in the image.
* I traced the contours of all the black bits to find their shape.
* I looped through all the contours rejecting any that seemed too large, too small, or too close to the edge of the image.
* I found the centres of the contours that were left and checked that a 10px x 10px sample from the centre was all black.
* I then grabbed a rectangular box around each of the remaining contours and saved it as a new image.

This is probably not the best or most efficient way of finding redactions. I developed my script by trial and error against a set of test images. Even so, there's so much variation amongst the source images that I've ended up with 15-20% of false positives. I'd like to find a way to reduce that.

You might be thinking that it seems like a lot of work to find a little (or not so little) black blob. And it is. One of the things your constantly reminded of when working with computer vision applications is how good humans are at recognising patterns. It's a lot harder for computers!

### Finding faces

People are particularly good at recognising faces. In fact, we're so good at it that we tend to 'see' faces all over the place -- this is called [pareidolia](https://en.wikipedia.org/wiki/Pareidolia). Have a look at the photos shared by [@FacesPics](https://twitter.com/facespics?lang=en) on Twitter -- do you see the faces?

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Jazz hands bridge is happy! <a href="https://t.co/D5hnkI3IPA">pic.twitter.com/D5hnkI3IPA</a></p>&mdash; Faces in Things (@FacesPics) <a href="https://twitter.com/FacesPics/status/781584194946396160">September 29, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Faces don't matter much to computers, so they're not hardwired to recognise them in the way we are. However, facial detection is a very common computer vision task. So how do you do it?

First of all we need to distinguish between 'facial detection' and 'facial recognition'. Facial detection is just finding a face in an image -- it's what happens when your camera draws a box around faces as you're taking a picture.

Facial recognition means taking an image of a face and then matching it against a database of previously identified faces -- it aims to identify the owner of a face. We see facial recognition all the time on TV crime shows, though in the real world it's rather more complicated. Facial recognition is much harder than facial detection -- though the computers are learning fast!

Facial detection is one example of a broader category of computer vision tasks called object detection -- the ability to identify particular things in a image. The objects you're looking for might be faces, dogs, or bananas, the approach is basically the same. First you use a selected set of images to create a model of the thing you're looking for. Then you can use this model to detect instances of that thing in a new set of images. It's sometimes referred to as machine learning because you're training the computer to 'see' the thing you're interested in.

So to find bananas you'd train your machine with two sets of images -- one with bananas, and one without. It would gradually learn to spot the features that define a banana. But what makes a face? The models included with OpenCV are pretty basic and really just look for bands of contrast where the eyes nose and mouth should be. To demonstrate this I tested a facial detection script on a set of simplified faces. This, for example, was detected as a face:

![Sample face]({{site.baseurl}}/images/face-test.png){: .img-example .img-responsive}

This video shows how a basic face detection model or classifier analyses a new image. It moves a window across the image looking for matching features. If enough features are detected it saves the window as a possible match. If a number of these marked windows overlap, it's likely to have found a face.

<iframe src="https://player.vimeo.com/video/12774628" width="640" height="610" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/12774628">OpenCV Face Detection: Visualized</a> from <a href="https://vimeo.com/adamhrv">Adam Harvey</a> on <a href="https://vimeo.com">Vimeo</a>.</p>
 
It's simple, but it works pretty well, and it creates some interesting possibilities.

### Creepy or compelling?

OpenCV includes a pre-trained face detection model based on many thousands of images, so you don't have to start from scratch. As a result it's surprising easily to create your own script and start finding faces.

Let me introduce you to the [Vintage Face Depot](https://wragge.github.io/face-depot/). [@facedepot](https://twitter.com/facedepot) is a Twitter bot I created that offers specialised face replacement services. Tweet a photo of yourself (or someone else) to @facedepot, and the bot will respond with a new version of you, blended with a historical face drawn from Trove's digitised newspapers.

Try it! Just tweet a photo of a face (you or your favourite celebrity) to @facedepot. Some hints:

* The name of the bot @facedepot needs to be at the start of the tweet.
* Faces are most likely to be detected if the whole of the face is in frame, and there's some space around it. (So no extreme close ups.)
* Good even lighting also helps. 

Face swap applications are all over the place now. Indeed, there's a new service in development called [Dreambit](http://dreambit.xyz/) that is described as a 'personalised image search engine':

> Given one or more photos and a text query, it outputs versions of the input person in the query appearance. We let people explore a large variety of looks.

![Dreambit demo]({{site.baseurl}}/images/dreambit.jpg){: .img-example .img-responsive}

The Vintage Face Depot is much more basic. When it receives your photo, it:

* runs a facial detection script over your photo and saves the coordinates of up to four faces;
* searches a database of faces I've already extracted from Trove, looking for ones that are at least as big as you face;
* randomly selects one of the size-matches faces;
* resizes the Trove face to match yours, masks the shape to create an oval, blurs the edges, and reduces the opacity (to make it slightly transparent);
* pastes the new face on top of yours;
* tweets back the new image.

As you will have noticed, the Vintage Face Depot doesn't attempt a seamless transformation. You may also see little ghost faces popping up all over the place where the script has wrong detected a face (machine pareidolia?). It's very obvious the image has been tampered with!

However, by making the new face slightly transparent, you do get interesting and sometimes unsettling results. You may notice the colour of your own eyes or lips showing through the historical image. You may have sprouted a new moustache. The bot also includes a link to the original newspaper article in Trove where you can find out more about the person behind your new face. My hope is that this simple bot can enable people to make new connections to the past -- whether they're funny, disturbing, or tragic.

{: .bg-info .bg-context}
If you want to build something using my collection of faces from Trove you can use my special [Face API](http://faceapi.herokuapp.com/), or [download](https://figshare.com/articles/Faces_extracted_from_Trove_newspaper_photographs/1439432) the complete set.

I explored this same sort of space in an earlier work, called [Eyes on the Past](http://eyespast.herokuapp.com/). For this work I found faces in Trove, and then found eyes in those faces -- yes OpenCV also includes an eye classifier! The result has been variously described as beautiful and creepy -- so I figure I must be doing something right. As with @facedepot, I'm using faces as a way of exploring the types of connections we make with the past.

My work with faces goes back several years. I was looking at a collection of documents held by the National Archives of Australia that were used in the administration of the White Australia Policy. The documents were used for identification by people living in Australia, but deemed non-white -- if they wanted to travel overseas they needed these documents, or they would be refused entry on their return. They're visually compelling documents with portrait photographs on one side, and inky-black handprints on the other.

{: .bg-info .bg-context}
I've now harvested a large collection of documents relating to the White Australia Policy and created a simple interface to browse them -- go to <http://iabrowse.herokuapp.com/> to explore.

Looking at the documents I wondered whether it might be possible to extract the portrait photographs from the larger images. So I googled 'facial detection'. Within a couple of days I'd built The [Real Face of White Australia](http://invisibleaustralians.org/faces/) -- a scrolling wall of thousands of faces. I still find it very moving. You can read more about it in [this draft chapter](https://www.dropbox.com/s/qflq77adawyobg0/The%20people%20inside_Sherratt%20and%20Bagnall_090615.docx?dl=0) Kate Bagnall and I wrote for a book on the use of computer vision in history.

### Face detection as a service

My fiddling about with facial detection is all pretty basic. Nowadays there's money to be made in offering these sorts of image recognition services, so the tools are becoming much more sophisticated. If your business needs to process lots of photos, it can make use of custom APIs created by companies like [IBM](http://visual-recognition-demo.mybluemix.net/) and [Face++](http://www.faceplusplus.com/)

They do, however, provide some neat little demos that we can play around with.

* Go to the [Face++](http://www.faceplusplus.com/demo-detect/) demo site.

* There are a number of potted examples you can try, just click on a face.

* You can also supply a url, or upload an image. Find an image on the web and try it out.

* You'll notice that this service does more than just detect a face -- what other information does it provide?

{: .bg-info .bg-context}
How do you think businesses might make use of this sort of information?

### Recognising faces

I said that recognising faces was much harder than just detecting them. However, there's been significant advances over the last few years. The development of neural networks -- computer applications modelled on the brain -- have greatly improved the range and accuracy of machine learning.

Google and Facebook are investing a lot of effort to bring facial recognition up to human-like levels of accuracy. In 2014, Facebook [announced](https://research.facebook.com/publications/deepface-closing-the-gap-to-human-level-performance-in-face-verification/) that its 'DeepFace' system had reached an accuracy of 97.35% -- close to humans. What did they train their neural network on -- perhaps it was you! One advantage the FaceBook research team had was access to millions of identified photos of people -- Facebook users. Yep, that's one of the potential uses of your data you agreed to when you signed up.

But not to be outdone, in 2015 Google [announced](https://arxiv.org/abs/1503.03832) it's 'FaceNet' system had reached a new record accuracy of 99.63%! It should be noted that these accuracy figures are against one [particular set](http://vis-www.cs.umass.edu/lfw/) of celebrity images harvested from the web -- I'm not really sure how we're meant to interpret them.

There's a nice summary of facial recognition developments in this article from *Science* -- ['Facebook will soon be able to id you in any photo'](http://www.sciencemag.org/news/2015/02/facebook-will-soon-be-able-id-you-any-photo).

How might these sorts of technologies be used in cultural heritage? Last year it was [announced](https://www.theguardian.com/science/2015/feb/16/anne-boleyn-portrait-found-using-facial-recognition-software) that a research team had used facial recognition to 'identify' a new portrait of Anne Boleyn. Given that the recognition system was trained using this medal, the only undisputed image of Anne Boleyn, I can't help but be a bit sceptical.

![Boleyn medal]({{site.baseurl}}/images/boleyn-medal.jpg){: .img-example .img-responsive}

You can certainly see how large photographic collections could use this technology to find previously unidentified images of particular people. Can you think of other possibilities?

### Issues and dangers

Are you creeped out yet? There's certainly something disturbing about these technologies, particularly when it comes to rapid advancements in facial recognition. If Google and Facebook are doing it, I think we can safely assume that governments are investing in similar sorts of systems. Indeed, about a year ago the Australian government [announced](https://www.ministerjustice.gov.au/Mediareleases/Pages/2015/ThirdQuarter/9-September-2015-New-$18-5-million-biometrics-tool-to-put-a-face-to-crime.aspx) that its 'newest national security weapon' was a national facial recognition system linking up existing face-identified databases, such as car licences -- it's called 'the Capability'.

Never fear, if you want avoid identification on the street, you could adopt one of these [new fashion styles](https://cvdazzle.com/), specifically designed to confuse facial detection systems.

![CV Dazzle]({{site.baseurl}}/images/cv-dazzle.jpg){: .img-example .img-responsive}

But it's not just identification. You may have noticed that the Face++ demo returned information on your sex, whether you're smiling, and your race. There have been studies examining it's possible to detect a person's sexuality from their face. If we, in the cultural heritage sector, are going to make use of these sorts of technologies I think [we need to be aware](http://discontents.com.au/the-perfect-face/) of the political and social implications of using faces as a means of assigning people to categories.

Melissa Terras also [raises questions](https://melissaterras.org/2016/08/10/the-robots-enter-the-photographic-archive/) about how easy access to these powerful photo manipulation tools might change the historical record. There have always been fakes of course, but is it just becoming too easy, too seamless. What can we trust?

For the ultimate in creepiness watch this video demonstrating a live face-swapping system.

{: .img-example}
<iframe src="https://player.vimeo.com/video/29348533" width="100%" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/29348533">Face Substitution</a> from <a href="https://vimeo.com/kylemcdonald">Kyle McDonald</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

### Image tagging and classification

Another area in which neural networks having been making rapid advances is in adding subject tags or descriptions to images. Just the other week Google [released details](https://research.googleblog.com/2016/09/show-and-tell-image-captioning-open.html) of its latest image captioning system. Against a set of test images it achieved an accuracy of 93.9%. But not only does it detect the subjects of an image, it writes a caption in natural language. Once again, this model has been trained on a set of images manually captioned by human beings, but Google claims it can go beyong merely applying the same captions to new images, it can identify wholly new contexts.

It's easy to see how such technologies could be of immense value to cultural heritage organisations that never have enough money to describe all of their holdings. But once again we have to be wary. Last year Google's photo app [caused considerable controversy](http://blogs.wsj.com/digits/2015/07/01/google-mistakenly-tags-black-people-as-gorillas-showing-limits-of-algorithms/) when it's automatic tagging system labelled African-American people as 'gorillas'. It's not that the image recognition systems are racist, but there are always likely to be biases in the image sets we use to train them. We have to always be thinking about the judgements implicit in the development of these sorts of systems.

Once again, image tagging and recognition are being marketed to business as a way of extracting useful information. Let's try using these forces for good, and see if IBM's demo system can help me sort my redactions from the false positives.

I've prepared three zip files:

* [Positive examples](https://www.dropbox.com/s/x64k1sagztu4mua/positive.zip?dl=0) -- these are redactions I've checked
* [Negative examples](https://www.dropbox.com/s/ol5lrz4kkn6qoki/negative.zip?dl=0) -- these are false positives
* [Assorted examples](https://www.dropbox.com/s/vi7vmza0u9pwvhj/assorted.zip?dl=0) -- these are a mix we'll use to test our classifier

Download all the files. You can unzip the 'Assorted' examples, but you don't need to worry about the others as we'll upload the zip files directly.

* Go to the [IBM demo page](http://visual-recognition-demo.mybluemix.net/).

* Have a play with their potted examples to see the sorts of classifications that are possible.

* Now click on the 'Train' tab.

* Once again they have some potted examples that you can play around with -- feel free to try them out.

* Now let's make our own classifier! Click on the square under 'Use your own'.

* Under 'Positive classes' select and upload the `positive.zip` file.

* In the text box give your positive examples the name 'Redactions'.

* Under 'Optional negative classes' select and upload `negative.zip`. 

* In the text box give your negative examples the name 'Non redactions'.

* Click on the 'Train your classifier' and wait. It could take a minute or two.

* Once your classifier is ready you can feed it one of the images in the assorted file. Just select and upload it. 

* The classifier will tell you whether it thinks the image you uploaded is a redaction or not. Was it right?

### Other cool stuff

Keep your eye out for other interesting projects in the cultural heritage domain making use of computer vision.

* Here's [a project](http://www.dlib.org/dlib/july15/lorang/07lorang.html) which is trying to find poetry in digitised newspapers by looking at the characteristic shapes of poems -- jagged lines, white space etc.

* Here's a [cool experiment](https://ryanfb.github.io/etc/2016/08/17/animating_stereograms_with_optical_flow_morphing.html) that uses image morphing to bring old stereoscopic images to life.