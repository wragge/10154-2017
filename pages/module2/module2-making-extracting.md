---
title: Making and extracting data
last_updated: July 19, 2017
sidebar: home_sidebar
permalink: module2-making-extracting.html
folder: module2
published: false
---

### #redactionart

Commonwealth government files more than 20 years old are supposed to be made available to the public. However, before they're released they go through a process known as 'access examination'. The contents of the files are checked against a list of exemptions -- things like privacy and national security. Depending on the results of the access examination process, files can be completely withheld from public access or opened 'with exception'. In the latter case, whole pages can be removed, or individual words or phrases can be blacked out -- these are called redactions.

I decided to try and find redactions in publicly available ASIO files held by the National Archives of Australia. Extended movie-like montage follows...

{: .img-example}
<div class="storify"><iframe src="//storify.com/wragge/redaction-art/embed?border=false&template=slideshow" width="100%" height="750" frameborder="no" allowtransparency="true"></iframe><script src="//storify.com/wragge/redaction-art.js?border=false&template=slideshow"></script><noscript>[<a href="//storify.com/wragge/redaction-art" target="_blank">View the story "Redaction art" on Storify</a>]</noscript></div>


And then there's the sequel where #redactionart escapes from my computer and unleashes havoc upon the world...

{: .img-example}
<div class="storify"><iframe src="//storify.com/wragge/redactionart/embed?header=false&border=false&template=slideshow" width="100%" height="750" frameborder="no" allowtransparency="true"></iframe><script src="//storify.com/wragge/redactionart.js?header=false&border=false&template=slideshow"></script><noscript>[<a href="//storify.com/wragge/redactionart" target="_blank">View the story "#redactionart" on Storify</a>]</noscript></div>

And of course there's the trailer...

{: .img-example}
<iframe src="https://player.vimeo.com/video/215976633" width="100%" height="500" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/215976633">The Redaction Zoo</a> from <a href="https://vimeo.com/wragge">Tim Sherratt</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

### Images as data

I thought I'd share my redaction art discoveries today because they're an example of how digital tools and techniques can lead you in all sorts of unexpected directions; but more importantly they also show how data can be used to generate new data. In this case I started with a set of digitised page images from ASIO files held by the National Archives of Australia. From those images I extracted the coordinates of redactions and created a new dataset containing [239,571 individual redactions](https://figshare.com/articles/Redactions_extracted_from_ASIO_surveillance_records_in_National_Archives_of_Australia_Series_A6119/4101765) that will enable me to look for patterns in redaction over time. But in the process of compiling that dataset I discovered redaction art, and traced the outlines of some of the creatures to create a [new collection of SVG files](https://github.com/wragge/diy-redactionart). Those SVG files have in turn been converted into [3D models](https://www.thingiverse.com/thing:2379810) (and cookie cutters).

Of course, we're currently doing the same sort of thing with our transcription project. We're starting off with a collection of images of documents, and we're extracting data from them. In this case humans are doing most of the work rather than machines, but the end result will be similar -- new datasets for research, exploration and analysis. Transcription projects like ours turn human-readable data (images) into machine-readable data.

Optical Character Recognition (OCR) is another familiar example of this process -- computers turn images into text. Current OCR software is pretty fussy, and will generate garbage if the imaged texts are not good quality. That's why Trove asks users to help them clean the OCR transcriptions of digitised newspaper articles. But in recent years there have been significant advances in [computer-aided transcription of handwriting](https://read.transkribus.eu/). 





Colours / hues

http://lab.softwarestudies.com/p/imageplot.html

### Seeing like a computer

Start to look for things IN images

Shapes / Features

Computer vision

they're an example of the use of computer vision in cultural heritage.

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

OpenCV includes a pre-trained face detection model based on many thousands of images, so you don't have to start from scratch. As a result it's surprising easily to create your own script and start finding faces.

Face demo http://wraggedemo.com/facedemo/

Not magic -- like my redaction finder breaking down a complex task into a series of simpler tasks.

TASK

### Creepy or compelling?

You've already seen the results of some of my early experiments in facial detection...


My work with faces goes back several years. I was looking at a collection of documents held by the National Archives of Australia that were used in the administration of the White Australia Policy. The documents were used for identification by people living in Australia, but deemed non-white -- if they wanted to travel overseas they needed these documents, or they would be refused entry on their return. They're visually compelling documents with portrait photographs on one side, and inky-black handprints on the other.

I explored this same sort of space in an earlier work, called [Eyes on the Past](http://eyespast.herokuapp.com/). For this work I found faces in Trove, and then found eyes in those faces -- yes OpenCV also includes an eye classifier! The result has been variously described as beautiful and creepy -- so I figure I must be doing something right. As with @facedepot, I'm using faces as a way of exploring the types of connections we make with the past.

{: .bg-info .bg-context}
I've now harvested a large collection of documents relating to the White Australia Policy and created a simple interface to browse them -- go to <http://iabrowse.herokuapp.com/> to explore.

Looking at the documents I wondered whether it might be possible to extract the portrait photographs from the larger images. So I googled 'facial detection'. Within a couple of days I'd built The [Real Face of White Australia](http://invisibleaustralians.org/faces/) -- a scrolling wall of thousands of faces. I still find it very moving. You can read more about it in [this draft chapter](https://www.dropbox.com/s/qflq77adawyobg0/The%20people%20inside_Sherratt%20and%20Bagnall_090615.docx?dl=0) Kate Bagnall and I wrote for a book on the use of computer vision in history.

My fiddling about with facial detection is all pretty basic. Nowadays there's money to be made in offering these sorts of image recognition services, so the tools are becoming much more sophisticated. If your business needs to process lots of photos, it can make use of custom APIs created by companies like [IBM](http://visual-recognition-demo.mybluemix.net/) and [Face++](http://www.faceplusplus.com/)

They do, however, provide some neat little demos that we can play around with.

* Go to the [Face++](http://www.faceplusplus.com/demo-detect/) demo site.

* There are a number of potted examples you can try, just click on a face.

* You can also supply a url, or upload an image. Find an image on the web and try it out.

* You'll notice that this service does more than just detect a face -- what other information does it provide?

{: .bg-info .bg-context}
How do you think businesses might make use of this sort of data? 

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

TASK ethical issues?

### Image tagging and classification

Another area in which neural networks having been making rapid advances is in adding subject tags or descriptions to images. Just the other week Google [released details](https://research.googleblog.com/2016/09/show-and-tell-image-captioning-open.html) of its latest image captioning system. Against a set of test images it achieved an accuracy of 93.9%. But not only does it detect the subjects of an image, it writes a caption in natural language. Once again, this model has been trained on a set of images manually captioned by human beings, but Google claims it can go beyong merely applying the same captions to new images, it can identify wholly new contexts.

It's easy to see how such technologies could be of immense value to cultural heritage organisations that never have enough money to describe all of their holdings. But once again we have to be wary. Last year Google's photo app [caused considerable controversy](http://blogs.wsj.com/digits/2015/07/01/google-mistakenly-tags-black-people-as-gorillas-showing-limits-of-algorithms/) when it's automatic tagging system labelled African-American people as 'gorillas'. It's not that the image recognition systems are racist, but there are always likely to be biases in the image sets we use to train them. We have to always be thinking about the judgements implicit in the development of these sorts of systems.

Women in the kitchen algorithm -- https://www.wired.com/story/machines-taught-by-photos-learn-a-sexist-view-of-women/?utm_source=MIT+Technology+Review&utm_campaign=da0dca2e77-The_Download&utm_medium=email&utm_term=0_997ed6f472-da0dca2e77-154448833


TASK on politics of algoritmhms

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


