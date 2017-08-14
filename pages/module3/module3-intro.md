---
title: Introduction of Module 3
keywords: 
last_updated: July 19, 2017
tags: [introduction]
summary: ""
sidebar: home_sidebar
permalink: module3-intro.html
folder: module3
published: false
---

In this module you will...

By the end you should:

* Know this...
* And this...

### Tracking trends

We've already met one example of treating texts as data -- my [QueryPic](http://dhistory.org/querypic/) tool. As I mentioned, QueryPic visualises searches in Trove's digitised newspapers. To be honest, it's not really analysing the contents of the newspapers directly. Instead it's relying on Trove's built-in search index. QueryPic shows you the number of articles per year containing a particular word or phrase. It doesn't show you the number of times that word or phrase occurred in all those articles. But it's still useful for examining changes in language and technology.

Here's a [recent example](http://dhistory.org/querypic/gq/) someone created comparing the use of 'plumbago' to 'graphite' -- you can see a clear shift around the turn of the 20th century.

But as I warned in out first session -- these sorts of visualisations aren't arguments or proof, you need to remain sceptical.

Have a [look at this QueryPic](http://dhistory.org/querypic/43/) that explores when the Great War became World War I. Naturally enough, it shows that we only started talking about World War I sometime after World War II had started. However, if you hover over 1916 on the World War I line, you'll see there are 108 matching newspaper articles. What's going on? Is this evidence of time travel?

Click on the point to load results from Trove. Click on one of the results. Notice any references to 'World War I'? Have a look at the user tags. You might find the odd OCR error, but most of those 108 articles are there because some helpful Trove user has tagged them with 'World War I' and Trove helpfully searches user tags and comments along with the text! 

REMEMBER -- DON'T TRUST SEARCH!

While QueryPic doesn't let you explore the number of times words are used within articles, other tools such as Google's Ngram viewer do.

{: .bg-info .bg-context}
What's an [n-gram](https://en.wikipedia.org/wiki/N-gram)? It's a term from linguistics which usually refers to a series of consecutive words from a text, where 'n' represents the number of words. A single word is a 1-gram or unigram, a two word phrase is a 2-gram or bigram, three words gives you a trigram.

[Google's Ngram viewer](https://books.google.com/ngrams) has taken the content of millions of scanned books and split them up into 1, 2, 3, 4, and 5 grams. You can search on these words or phrases and view a visualisation of their frequency over time -- much like QueryPic.

Try typing a few words or phrases and see what you can find. You can change the corpus (the collection of texts that are being searched) from the dropdown list -- what difference does this make to your search?

One thing you might notice is that the Ngram viewer is case-sensitive. This may seem a bit annoying, but it allows you to look at interesting things like the [usage of 'aborigines' versus 'Aborigines'](https://books.google.com/ngrams/graph?content=aborigines%2CAborigines%2CIndigenous+Australians&year_start=1800&year_end=2000&corpus=15&smoothing=3&share=&direct_url=t1%3B%2Caborigines%3B%2Cc0%3B.t1%3B%2CAborigines%3B%2Cc0%3B.t1%3B%2CIndigenous%20Australians%3B%2Cc0). When does the change in usage seem to take place? Can you think of any similar shifts in language you could test?

There are also a lot of [advanced options](https://books.google.com/ngrams/info) that you can use, such as searching by parts of speech.

{: .bg-info .bg-context}
Note also that Ngram searches can be embedded in your blog or website like Plot.ly graphs.

But yet again -- DON'T TRUST SEARCH!

Do what everyone does when playing around with something like this -- search for rude words. In particular, search for ['fuck' from 1600 to 2000](https://books.google.com/ngrams/graph?content=fuck&year_start=1600&year_end=2000&corpus=15&smoothing=3&share=&direct_url=t1%3B%2Cfuck%3B%2Cc0). It seems writers were much more liberal in their use of the f-word up until the beginning of the 19th century. It then almost disappeared until the second half of the twentieth century. But what are we actually seeing here? [Read this article](https://jakubmarian.com/a-curiosity-about-the-f-word-in-google-ngram-viewer/) to find out.

People have pointed out a [number of problems](http://www.wired.com/2015/10/pitfalls-of-studying-language-with-google-ngram/) with the Ngram viewer -- such as OCR quality and bad metadata. Just like QueryPic you have to remain sceptical of the results it offers -- it's an interesting place to start an investigation, but it doesn't give you all the answers.

Bookworm.

### Counting words

One way of analysing individual books or documents is by just treating them as a ['bag of words'](https://en.wikipedia.org/wiki/Bag-of-words_model) -- don't worry too much about meanings or structures, just break them up into words and start counting the results. Strangely enough this often produces useful insights.

The Museum of Australian Democracy has a fun site that allows you to do some [basic frequency analysis of election speeches](http://electionspeeches.moadoph.gov.au/explore). Try searching for a few terms or try their potted examples.

* Who made the longest election speech?

* Who is the only leader to have given a speech that was understandable to a 7th grader?

One great thing about this site is that they provide all of their texts for others to analyse! Click on the **Download** button near the bottom of the page to save a copy of all the speeches for later.

While we're at it, let's download some more political speeches. Over the weekend I [havested 20,000 transcripts](https://github.com/wragge/pm-transcripts) of speeches, interviews and press releases from Prime Ministers since World War 2. The transcripts are all searchable on the [PM Transcripts](https://pmtranscripts.dpmc.gov.au/) site, but I thought it would be useful to make them available in bulk through my own repository. I've also aggregated the [transcripts by PM](https://github.com/wragge/pm-transcripts/tree/master/pms). Let's download the [combined speeches of Julia Gillard](https://github.com/wragge/pm-transcripts/raw/master/pms/gillard-julia-speech.txt). (If the file opens in the browser rather than downloading, just use **File > Save Page As** to save it to your computer.)

Databasic.io provide a simple tool called [WordCounter](https://www.databasic.io/en/wordcounter/) for, you guessed it, counting words. It's not terribly robust or configurable, but it's a fun first attempt at dipping into the bag of words.

* Go to [WordCounter](https://www.databasic.io/en/wordcounter/) and click on **upload a file**.

* Choose the Julia Gillard file you just downloaded and click on **Count**.

* A word cloud will load, as well as a list of the most frequent words, bigrams, and trigrams. What can you see?

Ok, so it's not very interesting or surprising that 'Australia' and 'people' figure prominently, but it's notable that 'work' is the next most frequent word. In the trigrams we see the continuing importance of 'the united states' and perhaps an indication of PM Gillard's rhetorical orientation in the frequent use of 'for the future'.

The main problem with this simple tool is that there's no way of hiding words like 'Australia' to reveal possibly more interesting patterns. The tool has filtered out many common words like 'the' and 'and' (these are known as 'stop words'), but there's no way of adding to this list of stop words.

{: .bg-info .bg-context}
If you want to test the impact of stop words, try loading the speeches again, but this time uncheck the **ignore stop words** box.

![Stop words]({{site.baseurl}}/images/stopwords.png){: .img-example .img-responsive}

Voyant Tools is a powerful text analysis suite freely-available over the web. It provides a lot more options than the simple tools we've seen so far. Let's have another look at Julia Gillard.

* Go to [Voyant Tools](http://voyant-tools.org/) click on the **Upload** button and select the Julia Gillard file. 

* The Voyant dashboard will open with information about the most frequent words. But this is just the beginning.

{: .bg-info .bg-context}
Voyant is a great tool, but it can be a bit flaky at times. If the interface stops responding or behaves strangely just try reloading the page.

On the dashboard you'll see a familiar looking word cloud. As in the WordCounter , 'australia' and 'people' dominate -- but in Voyant we can change this.

* Hover on the header bar above the word cloud -- a series of icons will appear. Move your cursor over them to find the one that says 'Define options for this tool' and click on it. The **Options** box will open.

* Look for the **Stopwords** setting and click on **Edit List**. A list of the most common stop words will open.

* Hit return to move to a new line and type in 'australia'.

* Do the same for some of the other most common words such as 'australians', 'australian', and 'people'. Click **Save** and then **Confirm** to apply your changes. What happens to the word cloud?

{: .bg-info .bg-context}
But did we really want to get rid of 'people'? Just because it's very common, doesn't mean that it's not interesting. In an analysis of gendered language we might want to compare use of 'people' and 'men' for example. Or we might want to compare against words like 'citizens'. Once again, the choices we make to exclude or include can make a big difference to the patterns we see.

* Feel free to add more terms to the stop words list. Once you're happy with the word cloud, hover over the header bar again and click on the 'Export a url' icon.

* Click **Export** to open your word cloud in its very own tab.

* Try adjusting the **Terms** slider in the bottom left-hand corner. What happens?

{: .bg-info .bg-context}
Yep, this cloud, like ALL of Voyant's tools can be embedded in your own website! Just click on the 'Export a url' icon, choose **Export view**, select the 'HTML snippet' option and click **Export**.

There are a lot of different tools and visualisations to play with in Voyant. Let's try another one:

* Hover over the header of you cloud and click the icon labelled 'Click to choose another tool'.

* From the dropdown box select **Grid Tools > Contexts**. This opens up the keywords in context tool.

* This tool lets you browse the different contexts in which particular words or phrases are used.

* You can change the selected term by using the input box in the bottom left-hand corner. Click on the down arrow in the input box to show the most frequent terms, select 'future'. (If you want to look for another term, just type it in the box.)

* You can now explore the different ways Julia Gillard spoke about the future.

Try playing around with some of the other tools. My current favourite is **Bubble Lines**!

There's all sorts of clever things you can do with Voyant to make use of it in your own site. For example, I've built it in to my [Historic Hansard](http://historichansard.net/) site -- just click on a link to automatically open a year of Hansard in Voyant. Check out the ['Embedding Voyant Tools'](http://voyant-tools.org/docs/#!/guide/embedding) page in the help documentation for more possibilities.

### Comparing texts

So we can use text analysis tools to explore a single document, but what about comparing miltiple texts?

Once again, Databasic.io offers a simple tools to get us started. This one's called [SameDiff](https://www.databasic.io/en/samediff/).

* If you haven't already, unzip the file of election speeches we downloaded from MoAD.

* Open up [SameDiff](https://www.databasic.io/en/samediff/) and click on **upload files**.

* Select two of the files from the election speeches folder and click **Compare**.

Note that at the top of the page you'll see a 'cosine similarity score' that gives you an indication of the similarity of the language in the two files based on word frequencies.

Underneath you'll see word clouds displaying the words that both documents have in common, as well as those that are only in one of the documents.

* Let's compare the speeches by Malcolm Turnbull and Bill Shorten from the recent election. Despite their political differences, these speeches are 'kind of similar' with a score of 0.61.

* Now lets's compare the earliest speech, by Edmund Barton, and the latest, by Malcolm Turnbull. These speeches are 'completely different' with a similarity score of just 0.19.

Unsurprising it seems that time has more of an impact on language than does political allegiance. But one thing that struck me in the Barton-Turnbull comparison is that the word 'Australians' only appears in Turnbull's speech. Really? How was Barton addressing the people of Australia? That seems like something worth exploring further.

Let's head back to Voyant to dig a bit deeper.

* Open Voyant and click on **Upload** as before. Another cool thing about Voyant is that it can process a variety of different file types -- even PDFs. In this case we can just upload the whole zip file of MoAD's election speeches and it will unpack it and process the individual files.
 
* Select the zip file and wait for the magic.

You'll see that some things about the dashboard are a bit different. In particular, the summary pane in the bottom left-hand corner provides some useful comparative data. Look at the list of 'Distinctive words'. These are words that are frequent in an individual speech, but much less so across the whole collection.

* Go to the 'Trends' panel in the upper-right corner and open it in a new tab as you did with the word cloud earlier.

* Type 'australians' in the input box and hit enter. We can now see how frequently the word 'australians' appears across the whole collection.

* Mouseover the points on the graph to see which speeches contain the most/least references to 'australians'. Do you notice anything interesting.

It seems that, in general, recent speeches talk more about 'Australians'. I only just noticed this while preparing for this lesson and I'm now quite intrigued. This is what happens when you start exploring texts!

* There are other ways we can compare the different speeches -- try opening the Document Terms tool to compare the frequencies of different terms across the collection.

* Once again, play around with some other tools. [MicroSearch](http://voyant-tools.org/?corpus=66eec14e3e2b971dbb0fd224991e776b&query=australians&view=MicroSearch) also gives a pretty nice visualisation of the occurrance of 'australians'.

Another useful tool for comparing texts is [Overview](https://www.overviewdocs.com/). This tool was developed primarily for use by journalists trying to make sense of large collections of documents (such as some of the recent 'leaks'). It offers a powerful way of exploring clusters of similar documents.

Here's a video that teaches you Overview in 90 seconds!

<iframe src="https://player.vimeo.com/video/77729177" width="100%" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/77729177">Learn Overview in 90 seconds</a> from <a href="https://vimeo.com/user3976784">Jonathan Stray</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

* Go to [Overview](https://www.overviewdocs.com/) and sign up for an account.

* Once your verified and logged in, click on the **Upload files** link from your dashboard. 

* Click on **Add all files in a folder** and select the unzipped folder of election speeches.

* Click **Done adding files** and wait... It can take a while to upload and process the documents.

Once it's done, you document set will open with yet another word cloud. Yay! But it's really the 'tree' view that is most interesting.

* Click on the **Tree** tab.

* The tree view starts with a box representing all of the documents, and provides examples of some words that are common across the collection. As you move down the tree you'll see it subdivides the collection into clusters based on the similarity of their language.

* Click on the plus sign on one of the boxes in the bottom row. You can keep going through increasingly narrow clusters until you get to a single document.

* What is similar about the documents? Try clicking on the big box in the second row. You'll see the list of documents on the right hand side updates to include only those in the selected cluster.

* Scan the list of documents in the selected cluster.

* Now select the smaller box in the second row and scan the results. Can you see any interesting differences between the two clusters?

Once again it seems that time plays a big factor in the nature of our political language. The two clusters on the second row break down remarkably cleanly along temporal lines. The big cluster is pre-1980, the little one is post 1990, and the 1980s appear in both. What happened to our political language in the 1980s? Another question to explore at a later date!

Overview bases its similarity measures on a statistical measure called TF-IDF (Term Frequency / Inverse Document Frequency). Instead of just telling you how many times a word appears in a document, TF-IDF tells you how many times a word appears in one single document compared to a whole collection of documents. This gives us a measure of that word's significance within the context of that document. A word that appears many times in a document, but only rarely across a collection, will receive a high TF-IDF value -- it's a marker of what's different about that document.

I use TF-IDF quite a lot in my own work as a way of getting an understanding of what makes a document different from its peers. For example, [In a word](http://inaword.dhistory.org/) takes descriptions from current affairs programs broadcast on ABCRN and extracts the word with the highest TF-IDF value for each month and program. The result is a word that gives us a sense of what was 'different' about that month (at least according to the ABC). There's [more documentation](http://inaword.dhistory.org/#data) about how I created it at the bottom of the page.

Another way of looking for clusters within collections of documents is a technique known as topic modelling. See [this tutorial](http://programminghistorian.org/lessons/topic-modeling-and-mallet) on the Programming Historian site for an introduction.

### Extracting information

Let's go back to Overview to see how we can extract additional information from texts.

* Click on the **Add View** and click 'Entities'.

* You'll see a list of names and places extracted from the speeches.

* Check the 'Geonames: countries' box on the left hand side to limit the list to country names.

Just like that we have a list of the countries mentioned most often in Australian election speeches. Can you see anything interesting? Once again the influence of the USA seems prominent.

Overview uses a technique known as Named Entity Extraction (NER) to look for names of things within a text. NER is built into lots of different tools -- it can be a bit hit and miss, as you'll see when you scroll through the list, but it's also pretty powerful. There's even a [Named Entity Extraction plugin](http://freeyourmetadata.org/named-entity-extraction/) for Open Refine.

Alchemy provides a number of (mostly paid) APIs for analysing texts. It's fun to play around with their [demo site](https://alchemy-language-demo.mybluemix.net/). Feed it texts and see what you can find.

### Data Visualisation

Where to start? Data visualisation is a popular topic at the moment and there's a rapidly growing number of guides, tools, and examples. It's all a bit overwhelming. Rather than get too bogged down in the possibilities, I thought I'd just look at a few basic types of chart and how you can create them. But you should explore further using the resources listed below, particularly if you're planning to use data visualisations in your project.

A good starting point is the video that I included in the readings for this week.

{: .img-example }
<iframe width="100%" height="500" src="https://www.youtube.com/embed/sb1UkU5rR90" frameborder="0" allowfullscreen></iframe>

We seen a number of types of visualisation already. For example:

* [A visual history of the Olympics](http://www.nytimes.com/interactive/2016/08/08/sports/olympics/history-olympic-dominance-charts.html?_r=0)
* [SA Census data in Plot.ly](https://timsherratt.org/digital-heritage-handbook/activities/creating-simple-charts-with-plotly/)
* [QueryPic](http://dhistory.org/querypic/) and the [Ngram viewer](https://books.google.com/ngrams)
* 'Generous interfaces' like [Prints and Printmakers](http://www.printsandprintmaking.gov.au/explore/)
* [MoAD's Election Speeches](http://electionspeeches.moadoph.gov.au/explore)
* Word clouds in [Voyant](http://voyant-tools.org/)

We'll continue to explore possibilities over the next few weeks. This week we'll be working with what we conventionally think of as 'data' -- numbers in spreadsheets. Next week we'll be looking at what we can do using timelines and maps. Later on we'll examine how we can treat images as data to reveal different patterns and possibilities. There's no one approach to visualisation in cultural heritage!

### Guides and catalogues

How do you tell a bar chart from a histogram? (That's one that I have trouble with...) The first challenge in working with data visualisations is just understanding the basic language, styles, and conventions. [A Tour Through the Visualization Zoo](http://homes.cs.washington.edu/~jheer//files/zoo/), which I included in readings for this week, provides an overview of the main categories of data visualisation and how they're used.

For a more detailed list of visualisation types have a look at the [Dataviz Catalogue](http://www.datavizcatalogue.com/index.html). It has good, concise descriptions of each type and a list of tools you can use to create them (although it doesn't include Plot.ly for some reason). In a similar way, the [Periodic table of visualisation methods](http://www.visual-literacy.org/periodic_table/periodic_table.html) gives a conceptual overview of how the different types of data visualisation are used.

But how do you choose? [How to design an excellent chart](http://www.verstaresearch.com/newsletters/how-to-design-an-excellent-chart.html#how-to-design-an-excellent-chart) provides a useful step-by-step guide. Alternatively you can jump straight to [Choosing a chart](http://extremepresentation.typepad.com/files/choosing-a-good-chart-09.pdf) -- a simple visualisation of visualisation options, that helps you choose a chart type based on your data and what you want to show.

### Looking critically

One of the continuing themes throughout the unit so far is that you can't trust what you see. Collections themselves are culturally constituted with significant gaps and silences. Search engines distort our experience. And visualisations don't show the 'truth', they argue a case.

A good way to start an exploration of data visualisation is to critically examine a few examples.

The list below presents a number of different types of visualisation. Either in groups or on your own, examine them closely.

* [Kindred Britain](http://kindred.stanford.edu/#)
* [The Preservation of Favoured Traces](https://fathom.info/traces/)
* [Mapping the Republic of Letters](http://web.stanford.edu/group/toolingup/rplviz/)
* [Mapping Police Violence](http://mappingpoliceviolence.org/)
* [The Instituional Harvest](http://institutionalharvest.net/)
* [A timeline of Earth's average temperature](http://xkcd.com/1732/) (xkcd)

Here are some questions you might want to consider as your exploring the visualisations:

* What is the data that's being presented?
* How easy is it to understand what you're seeing?
* What did you learn from it?
* What might be hidden or missing?

Which visualisations do you like? Which are most effective? Different visualisations will appeal to different audiences -- after all it's just another form of communication.

### Data and tools

I've prepared a few simple data sets for today. It's important to note that I've done a bit of cleaning up and reformatting already. Once you start playing around with data visualisation tools you'll realise that data doesn't always 'fit' the tool. There are assumptions built into the tools about the way the data will be presented. So you'll often find yourself going back to your spreadsheet to move cells or reformat data just so you can get it to work. This is one example of how our choice of tools can shape the stories we tell.

{: .bg-info .bg-context}
Don't forget about OpenRefine -- your swiss army knife for data cleanup and manipulation.

The datasets are all hosted on Google Drive. If you don't have a Google Account you might like to get one, so you can play around with the charting possibilities of Google Sheets and Fusion Tables.

* [Age groups accessing the Internet at home, 2010-11](https://docs.google.com/spreadsheets/d/1sakLzwrHYz5oAAdaU7JYxoHDKTx4XHRpA00li_1bvTY/edit?usp=sharing) (from [Culture and the Internet](http://www.abs.gov.au/ausstats/abs@.nsf/Lookup/4172.0main+features202014), Bureau of Statistics)
* [Attendance at cultural institutions by gender, 2013-14](https://docs.google.com/spreadsheets/d/1kq7nbQJ-tgAY6STY-KeE9_GgQSkvMD8on_LVqZhdxpg/edit?usp=sharing) (from [Arts and Culture in Australia: A Statistical Overview](http://www.abs.gov.au/ausstats/abs@.nsf/Lookup/4172.0main+features52014), 2014, Bureau of Statistics)
* [Trove work counts, 2010-2016](https://docs.google.com/spreadsheets/d/1T-bwyCLcG7W0PDIKWbOvG6FnmlkLmu8KE_CUgPRRXj8/edit?usp=sharing) (harvested from [Trove](http://trove.nla.gov.au/system/counts?env=prod&history=y))
* [Trove work counts, 2010-2016](https://docs.google.com/spreadsheets/d/1JhLTZFTH98sNddPLz5ByGjRqwKCIZnvb-PnMdvPhfv0/edit?usp=sharing) --reorganised for stream view (harvested from [Trove](http://trove.nla.gov.au/system/counts?env=prod&history=y))
* [Trove zones](https://docs.google.com/spreadsheets/d/1EP15Nv2K9pyONpFkghODUPWJwTrtDWeCN4iUDk3nD_E/edit?usp=sharing) -- with sizes 
* [Trove zones](https://docs.google.com/spreadsheets/d/1CtZCpS_gK5KbuDGV_Z42-utj07LQ8GHN5EbkwsLhdX8/edit?usp=sharing) -- hierarchy only
* [Tate artists](https://docs.google.com/spreadsheets/d/1KCcnbajjNiBjbHy31fQ9wJtlwzaUMrKqGpTXkvrN7g0/edit?usp=sharing) (via Mia Ridge's [excellent collection of resources](http://www.miaridge.com/resources-for-data-visualisation-for-analysis-in-scholarly-research/) for scholarly analysis of data visualisations)
* [Reasons for closing files in the NAA](https://docs.google.com/spreadsheets/d/1MKZjlRTbYxuK6Hxl_0Vrk9QIECA8ASNXhXFXmPeXTWU/edit?usp=sharing) (harvested for [Closed Access](http://closedaccess.herokuapp.com/))

The tools we're going to look at today are:

* Google Sheets -- charts can be created and then published for embedding elsewhere.
* [Google Fusion Tables](https://support.google.com/fusiontables/answer/2571232) -- a different way of looking at your spreadsheet data. Includes maps, charts, and network graphs.
* [Plot.ly](https://plot.ly/) -- a wide range of charting tools. Easy to create, easy to share and embed.
* [Raw](http://raw.densitydesign.org/) -- Raw allows you create types of  visualisations not available in conventional charting tools. Unfortunately the results aren't really able to be embedded.
* [Charted](http://www.charted.co/) -- creates one sort of chart but does it very well.

Other (more commercially oriented) data visualisation tools you might like to explore are:

* [Tableau](http://www.tableau.com/)
* [Silk](https://www.silk.co/)

As I noted above, I'm only going to step through a small number of examples using these tools and datasets. There are always alternatives! Try datasets with different tools. Try customising the charts. Try sharing and embedding the results. Find different datasets and try visualising them. Explore the possibilities!

### Displaying categories

One of my research projects is examining files in the National Archives of Australia with the access status of 'closed'. I describe it in [this paper](http://discontents.com.au/closed-access/). I've created a site that [displays the data](http://closedaccess.herokuapp.com/) I've harvested in a number of different ways -- mostly just using Plot.ly. Here's an example of displaying categories using bar charts -- in this case it's a [summary of the reasons](http://closedaccess.herokuapp.com/reasons/) why files have been closed. It's interactive! Click on one of the bars for more information.

Visualisations of categorised data allow us to make quick comparisons. Let's see how we can display data by category:

* Open up [Age groups accessing the Internet at home, 2010-11](https://docs.google.com/spreadsheets/d/1sakLzwrHYz5oAAdaU7JYxoHDKTx4XHRpA00li_1bvTY/edit?usp=sharing).

* Make a copy so you can play around with it. Select **File > Make a copy** from the menu. You'll need to have a Google account and be logged in.

This is a simple dataset with a small number of categories. A pie chart is probably a good way of visualising it. 

* Google Sheets (like other spreadsheet programs) has some charting tools built in. Find the icon that looks like a bar chart and click on it.

* Sheets scans your data and makes some suggestions for charts. Click on the pie chart.

* You should see a nicely formatted pie chart -- that was easy! Click on **Insert** to add it to your spreadsheet.

* Make sure the chart is selected and then click on the little down arrow in the top right-hand corner. You'll see you can do a number of things, including saving an image of your chart. Click on **Publish chart**.

* Click on the **Publish** button.

* You'll see you have options to link or embed. Grab a copy of the link and load it in your browser. You now have an [instant shareable chart](https://docs.google.com/spreadsheets/d/129TI0ly1qwmYcjuhoo2x4VFQX-ezRc47LGCboP-zTEM/pubchart?oid=1380538473&format=interactive)!

How else might we display this data? Use the charting tool to create a bar chart. When might a bar chart be a better option?

Now let's try comparing a couple of related datasets. We could have side by side pie charts, but a grouped bar chart is probably a better option.

* Open up [Attendance at cultural institutions by gender, 2013-14](https://docs.google.com/spreadsheets/d/1kq7nbQJ-tgAY6STY-KeE9_GgQSkvMD8on_LVqZhdxpg/edit?usp=sharing) and make a copy.

* Once again you can just click on the chart icon and Sheets will give you some visualisation options -- including a stacked bar chart (the values are stacked on top of each other) and a grouped bar chart (the values are next to each other).

* Let's try this one in [Plot.ly](https://plot.ly/). Make sure you're logged in, then click the **+Create** button and select **Chart**.

* Click on the **Switch back to Plotly 1.0** link at the top of the page.

* Select and copy the data (including the header row) from Google sheets.

* Click on the **+ New Grid** tab to open and empty grid.

* Click in the first cell then paste in the data.

* Click on the '1' on the left side of the grid to select the first row.

* Right-click on the first row (while it's selected) and choose **Use row as col headers**.

* Right click again on the first row and choose **Remove selected rows**.

* We're now ready to make a chart. Choose **Bar chart** from the dropdown list on the left side.

* 'Institution' will already be chosen as the source for the x axis, and 'Men' will be on the 'y'. Click on **Choose as y** in the 'Women' column to add them as well.

* Click on the blue **Bar Chart** button. You'll be asked to give your grid a name and save it. Do that.

* Plot.ly automatically displays the data as a grouped bar chart. You can change it to 'stacked' by clicking on the **Traces** button and selecting **Stack** under 'Mode'.

Which is most effective in displaying this data -- a stacked or grouped bar chart? Why?

You'll have noticed that were a few more steps involved in creating a chart in Plot.ly. But Plot.ly gives you more control than Google Sheets in styling, customising, and sharing your charts. Which should you use? It's a matter of thinking about what will work best for your project and your data.

{: .bg-info .bg-context}
Are you interested in the data we used in these examples? I copied only a small subset of the available data around attendance at cultural institutions. The full dataset breaks things down further by age, income, etc. Creating a series of data visualisation using the full dataset to show public engagement with cultural heritage institutions might be an interesting project!

### Change over time

Often we'll want to show how particular values change over time. There are lots of ways we can present this -- bar charts, line charts, scatter plots, stream graphs, and more. Look these types up in the [Dataviz Catalogue](http://www.datavizcatalogue.com/index.html) to get an idea of their strengths and weaknesses. What alternatives can you find?

QueryPic is an example of this sort of visualisation. It uses line charts to display the number of matches over time. Again on my Closed Access site, I've used Plot.ly to explore how time affects the fate of files in the National Archives. Here's a chart [showing the ages of closed files](http://closedaccess.herokuapp.com/ages/) -- can you find the peak year? (Hint -- try the Cold War!)

Charted is about as simple as you can get in data visualisation tools. It does one thing, but it does it very nicely. We'll use it to visualise changes in the contents of Trove:

* Open up [Trove work counts, 2010-2016](https://docs.google.com/spreadsheets/d/1T-bwyCLcG7W0PDIKWbOvG6FnmlkLmu8KE_CUgPRRXj8/edit?usp=sharing) and make a copy as before.

* This time click on the **Share** button to open the share options.

* Click **Get shareable link**. 

* Once the link has been generated click on **Copy link**.

* Now go to [Charted](http://www.charted.co/).

* Paste the link into the box and click **GO**.

That's it! I told you it was easy.

The [chart shows](http://www.charted.co/c/7a3e3af) steady growth in most parts of Trove, but there are a few oddities. What happened in October 2013? Why did the number of books drop by half in May 2011?

[![Trove work counts]({{site.baseurl}}/images/charted.png){: .img-example .img-responsive}](http://www.charted.co/c/7a3e3af)

One nice feature in Charted is the ability to extract one of the traces from the stacked chart and display it separately. Hover over one of the categories in the legend and click on the icon that appears. What happens? Why is this useful?

Charted makes very nice looking charts, but the customisation options are limited. Have a play around. Click on the gear icon to change a few settings. Click on one of the coloured dots to change its color. Try giving you chart a title.

{: .bg-info .bg-context}
And now a challenge -- without any more assistance from me, can you create the same sort of stacked bar chart in Plot.ly? Test your new dataviz skills!

Another way of representing change over time is using a streamgraph. Streamgraphs are a bit like stacked bar charts in that that show how the individual strands combine to make the whole, but the visual metaphor they use is that of 'flow'. They look much more attractive than your average bar chart -- is that a good thing or a bad thing?

Raw is a visualisation tool that allows you to create streamgraphs and other less familiar types of charts. Like a lot of visualisation tools, it's built on top of the [D3 javascript library](https://d3js.org/). But whereas you have to be a coder to use D3, anyone can make nice looking visualisations with Raw.

Let's have another look at that Trove data. This is a case where the tool is expecting to see the data in a particular way, so I've had to create a separate spreadsheet -- same data, just organised differently.

* Open up [Trove work counts, 2010-2016](https://docs.google.com/spreadsheets/d/1JhLTZFTH98sNddPLz5ByGjRqwKCIZnvb-PnMdvPhfv0/edit?usp=sharing) --reorganised for stream view. You don't need to make a copy in this case.

* Select and copy all of the data.

* Go to [Raw](http://raw.densitydesign.org/) and click on the **Use it now! button**

* In the text box just paste the data you copied. Raw will parse the data and let you know that it's all ok.

* Scroll down the page and find the 'Streamgraph' icon. Click on it.

* Scroll down to where it says 'Map your dimensions'.

* Drag 'Date' from the left-hand side to the 'DATE' box.

* Drag 'Zone' to 'GROUP' and 'Total' to 'SIZE'.

* Scroll a bit further and you'll see your streamgraph!

Note that unlike a lot of the tools we've been working with, Raw doesn't offer an easy way to share, or embed the original chart in your web page. You can download your chart as an image, or create the code necessary to render an SVG (Scalar Vector Graphic), which you can then edit in a graphics program or display in a browser.

{: .bg-info .bg-context}
Try Raw with some of the other datasets. What can you make?

### Trees and hierarchies

Sometimes our data represents a hierarchy, or a tree -- starting with the complete set and then subdividing into smaller and smaller categories.

Trove (yes Trove again) is divided into [zones](http://help.nla.gov.au/trove/using-trove/getting-to-know-us/inside-trove#anchor-1) -- like Books, Articles, Pictures. These zones are further subdivided into formats, and subformats. It can be a difficult structure to represent to users. Let's see if we can use Raw to help.

* Open up [Trove zones](https://docs.google.com/spreadsheets/d/1CtZCpS_gK5KbuDGV_Z42-utj07LQ8GHN5EbkwsLhdX8/edit?usp=sharing). No need to make a copy.

* Select and copy the data.

* Open up Raw (or reload the page) and paste the data into the box as before.

* Select Reingold-Tilford tree from the visualisation types.

* Drag 'Zone', 'Format', and 'Subformat' -- in that order -- to the 'HIERARCHY' box.

* View your lovely tree!

![Trove tree]({{site.baseurl}}/images/trove-tree.png){: .img-example .img-responsive}

Try this again with the 'Circular dendrogram'. Which do you prefer and why?

The tree view doesn't give any sense of how big the zones and their parts are. Let's try a slightly different approach:

* Open up [Trove zones](https://docs.google.com/spreadsheets/d/1EP15Nv2K9pyONpFkghODUPWJwTrtDWeCN4iUDk3nD_E/edit?usp=sharing) -- with sizes. This is the same hierarchical data, but with information about how many items are in each grouping.

* Select and copy the data.

* Open up Raw (or reload the page) and paste the data into the box as before.

* Select the 'Circle packing' visualisation.

* Drag 'Zone', 'Format', and 'Subformat' -- in that order -- to the 'HIERARCHY' box.

* Drag 'Total' to 'SIZE' and 'Zone' to 'COLOR'.

* View your new visualisation. What do you think? I think it's rather beautiful.

* Try clicking and dragging the circles for hours of entertainment!

<svg width="800" height="800" xmlns="http://www.w3.org/2000/svg" version="1.1"><circle style="fill: rgb(191, 105, 105);" cx="444.24149518140644" cy="511.72256524233984" r="105.3666833052016"></circle><circle style="fill: rgb(191, 156, 105);" cx="532.0766100948422" cy="426.1768787832118" r="7.24493986616605"></circle><circle style="fill: rgb(191, 156, 105);" cx="537.8291257395713" cy="433.4104711939468" r="0"></circle><circle style="fill: rgb(191, 156, 105);" cx="534.5206098479256" cy="436.538839516856" r="1.4008400461984416"></circle><circle style="fill: rgb(191, 156, 105);" cx="551.380828349898" cy="429.81401525601933" r="3.681440999439328"></circle><circle style="fill: rgb(191, 156, 105);" cx="539.5319808231394" cy="437.3736251717342" r="1.6797242498344036"></circle><circle style="fill: rgb(191, 156, 105);" cx="547.214072233948" cy="415.36729823762903" r="9.35534340960255"></circle><circle style="fill: rgb(191, 156, 105);" cx="550.5369333714477" cy="445.41606760734015" r="9.93848708526452"></circle><circle style="fill: rgb(191, 156, 105);" cx="542.9543109172266" cy="431.694755092598" r="2.9506534655453103"></circle><circle style="fill: rgb(191, 156, 105);" cx="584.4017369769376" cy="425.7240772513989" r="27.23547630136359"></circle><circle style="fill: rgb(174, 191, 105);" cx="502.3958952928656" cy="407.54413529266265" r="3.920499085983292"></circle><circle style="fill: rgb(174, 191, 105);" cx="515.038108487519" cy="409.1708236262846" r="6.828208017382634"></circle><circle style="fill: rgb(122, 191, 105);" cx="470.9163343367258" cy="308.2764878407179" r="1.082772833788334"></circle><circle style="fill: rgb(122, 191, 105);" cx="568.3405364836077" cy="195.59941543956165" r="116.2965356869891"></circle><circle style="fill: rgb(122, 191, 105);" cx="478.0184261386957" cy="290.5282484885578" r="12.741336132688737"></circle><circle style="fill: rgb(122, 191, 105);" cx="405.694741691476" cy="301.15871255013616" r="58.364654233471235"></circle><circle style="fill: rgb(122, 191, 105);" cx="502.51858389959307" cy="346.98406613419513" r="46.761662456185526"></circle><circle style="fill: rgb(105, 191, 139);" cx="304.0837087459932" cy="358.2956043320947" r="3.260268104295077"></circle><circle style="fill: rgb(105, 191, 139);" cx="339.1113528518112" cy="398.406843610651" r="25.76019203626724"></circle><circle style="fill: rgb(105, 191, 139);" cx="249.0299609889519" cy="266.65407581253874" r="92.04986960267114"></circle><circle style="fill: rgb(105, 191, 139);" cx="254.76129010770987" cy="417.76822161487576" r="57.18006134892492"></circle><circle style="fill: rgb(105, 191, 139);" cx="309.3307117350193" cy="378.13749776079464" r="8.264936811030157"></circle><circle style="fill: rgb(105, 191, 139);" cx="298.61885569008757" cy="367.22290100932156" r="5.022707233007831"></circle><circle style="fill: rgb(105, 191, 139);" cx="308.17133661315023" cy="365.1784310709827" r="2.7463048861033577"></circle><circle style="fill: rgb(105, 191, 139);" cx="329.7543363778363" cy="349.747478005235" r="21.789731614641976"></circle><circle style="fill: rgb(105, 191, 191);" cx="357.33338685920444" cy="431.9066659905935" r="2.376942182465128"></circle><circle style="fill: rgb(105, 139, 191);" cx="345.7178457145685" cy="439.35708612721453" r="1.4246824244263345"></circle><circle style="fill: rgb(105, 139, 191);" cx="342.021149524794" cy="437.3461402242485" r="0.7842253032848747"></circle><circle style="fill: rgb(105, 139, 191);" cx="340.2265748354562" cy="449.842128672731" r="5.105606487397413"></circle><circle style="fill: rgb(105, 139, 191);" cx="337.58775350407456" cy="442.10563533701406" r="1.0677256470386254"></circle><circle style="fill: rgb(105, 139, 191);" cx="342.02282317533985" cy="440.8424772640128" r="0.06597252226421338"></circle><circle style="fill: rgb(105, 139, 191);" cx="339.9425164194257" cy="439.6617072680252" r="0.32683694579938"></circle><circle style="fill: rgb(105, 139, 191);" cx="343.7618178627213" cy="442.93501491061994" r="0.6560578568991802"></circle><circle style="fill: rgb(105, 139, 191);" cx="340.72413777014935" cy="442.6324810174223" r="0.10961904974933433"></circle><circle style="fill: rgb(105, 139, 191);" cx="326.56829798072795" cy="440.7243114761214" r="7.686337413798791"></circle><circle style="fill: rgb(105, 139, 191);" cx="337.35594771491577" cy="436.15415388637626" r="2.030848876472447"></circle><circle style="fill: rgb(122, 105, 191);" cx="308.9118676017794" cy="487.10812290037217" r="4.1394114958501"></circle><circle style="fill: rgb(122, 105, 191);" cx="321.4579164025422" cy="471.70868519457474" r="13.721953661134219"></circle><circle style="fill: rgb(122, 105, 191);" cx="312.90372965332915" cy="492.53917981771025" r="0.5949466543292434"></circle><circle style="fill: rgb(122, 105, 191);" cx="308.2954565168764" cy="496.9271819388761" r="3.711669807492682"></circle><circle style="fill: rgb(122, 105, 191);" cx="323.5969025212145" cy="500.01396562822475" r="7.389133776793406"></circle><circle style="fill: rgb(122, 105, 191);" cx="317.3646048032504" cy="489.6632033658212" r="2.6930768759861365"></circle><circle style="fill: rgb(122, 105, 191);" cx="307.60844770525824" cy="514.8351660070192" r="12.214909187182524"></circle><circle style="fill: rgb(122, 105, 191);" cx="299.1161445399323" cy="477.73720460388364" r="7.416778972857076"></circle><circle style="fill: rgb(122, 105, 191);" cx="291.08933637552013" cy="496.1841378704727" r="10.701783596564683"></circle><circle style="fill: rgb(174, 105, 191);" cx="322.7701171508183" cy="543.4717087008654" r="10.19435815919671"></circle><circle style="fill: rgb(191, 105, 156);" cx="369.5882015032838" cy="607.1573498716258" r="5.793272400384256"></circle><circle style="fill: rgb(191, 105, 156);" cx="352.9812809820382" cy="612.051346534969" r="9.519757737052215"></circle><circle style="fill: rgb(191, 105, 156);" cx="326.77649730662563" cy="587.7192141536492" r="24.23544910110277"></circle><circle style="fill: rgb(191, 105, 156);" cx="365.0477952546063" cy="595.9058907693537" r="0.20542419883490798"></circle><circle style="fill: rgb(191, 105, 156);" cx="357.4134198644618" cy="595.6991108596139" r="5.4272522919761315"></circle><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="444.2398970280018" y="511.7233335517401"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="532.0775488168723" y="426.1760771063347"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="537.8312847938398" y="433.4114407670932"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="534.5217161838083" y="436.5379822212146"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="551.3803494602715" y="429.8135356064434"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="539.5330050582816" y="437.37323330615135"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="547.2147485450264" y="415.36582004142133"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="550.5407619461246" y="445.41493790821403"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="542.9546172424573" y="431.69393064563894"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="584.4044206376697" y="425.72097874710494"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="502.39460566418313" y="407.54399634787313"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="515.0385675713753" y="409.17050251625386"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="470.91724239834707" y="308.2751526715575"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="568.342097757707" y="195.5981535952917"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="478.0205538859303" y="290.532897037943"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="405.6935607400909" y="301.15757613977564"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="502.5196964090526" y="346.98370157077073"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="304.08302029079863" y="358.29520463244256"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="339.1107994772856" y="398.4060306730856"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="249.03000899922623" y="266.65146686542397"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="254.75873532397222" y="417.76785253688536"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="309.32938434013346" y="378.13758471508856"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="298.6179831515984" y="367.2231953392176"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="308.17005015878743" y="365.17862974812635"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="329.75293995320766" y="349.7460048255571"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="357.3345665765204" y="431.9057545231187"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="345.71851178243304" y="439.35580103301936"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="342.02110159998216" y="437.3462295032717"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="340.22914681687547" y="449.8411381084907"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="337.58735636390463" y="442.10558352347783"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="342.0228664816735" y="440.8421636728163"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="339.94230787209665" y="439.66162065771"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="343.7629822323942" y="442.93359282378225"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="340.72404013835836" y="442.6320754774849"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="326.56815758741243" y="440.72420895069024"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="337.35600911375496" y="436.15381537575024"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="308.91155729929505" y="487.10760851936965"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="321.45847128801006" y="471.71013471043574"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="312.9032976181101" y="492.5390287014501"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="308.295368649887" y="496.92790639717805"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="323.5964748489981" y="500.0149849218281"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="317.3643996052356" y="489.66408870873516"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="307.6067352690907" y="514.8363620271195"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="299.1155352402261" y="477.737002784301"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="291.0878910511176" y="496.18454305832546"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="322.7694360512278" y="543.4752442078119"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="369.58670892963255" y="607.1580941522188"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="352.9802833666539" y="612.05377005663"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="326.77530653601934" y="587.7227744229372"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="365.0470806835617" y="595.9062488454134"></text><text text-anchor="middle" dy="4" style="font-size: 11px; font-family: Arial, Helvetica;" x="357.41306031223644" y="595.7011598095621"></text></svg>

Here's [another way of visualising Trove's zones](http://dhistory.org/trove/zone-explorer/). In this case I used D3 directly to create a 'sunburst' visualisation. Try clicking on the segments. What happens?

### Network graphs

Network graphs allow you to explore relationships between things (or 'nodes' in graph speak). They're frequently used to visualise social networks -- the relationships within a group of people as revealed through activities like correspondence, communication,  collaboration. or co-authorship. Martin Grandjean, for example, has used network analysis to [explore the nature of the Digital Humanities community](http://www.martingrandjean.ch/network-analysis-mapping-digital-humanities-community-twitter/) by visualising their interactions on Twitter.

I used a network graph to examine clusters in the reasons cited for closing files in the National Archives. I used a tool called [Gephi](https://gephi.org/) and a [tutorial by Martin Grandjean](http://www.martingrandjean.ch/gephi-introduction/). You can [read about it](https://timsherratt.org/research-notebook/notes/relationships-between-reasons/) in my research notebook. Here's what I ended up with:

![Closed Access network graph](https://timsherratt.org/research-notebook/images/reasons_graph_labelled.png){: .img-responsive .img-example}

This was interesting because it indicated how commonly the national security exemption (33(1)(a)) has been used in combination with others -- it's sort of the go-to exemption for anything security-ish.

You can create a similar graph using my data and Fusion Tables:

* Open up [Reasons for closing files in the NAA](https://docs.google.com/spreadsheets/d/1MKZjlRTbYxuK6Hxl_0Vrk9QIECA8ASNXhXFXmPeXTWU/edit?usp=sharing) and make a copy.

As you can see each row in the spreadsheet is just a pair of reasons, indicating that these reasons have been cited together in an access decision. Unlike a letter sent from one person to another there's no directionality in this relationship. They just occur together. In some network graphs the direction of the relationships **is** important and can be visualised.

* From your Google Drive account click **New** then **More**, then choose 'Fusion Tables'. (Alternatively, go direct to [Fusion Tables](https://www.google.com/fusiontables/DataSource?dsrcid=implicit).)

* In the 'Import new table' box click on 'Google Spreadsheets' and select the file you just copied.

* Click **Next** and then **Finish** to complete the data import.

* Once the table is open, click on the little red **+** sign and select 'Add chart'.

* Fusion tables should recognise that your data can be visualised as a network graph and create one automatically.If not click on the network graph icon (at the bottom on the right-hand side).

* Use the plus and minus buttons to zoom in and out. Try clicking on a node and dragging it around. What happens? Hover over a node to highlight its relationships.


### The power of maps

Many years ago now [I was involved](http://discontents.com.au/local-heroes/) in a project called *Mapping Our Anzacs* at the National Archives of Australia. The plan was to build a map interface to 376,000 digitised WWI service records that enabled visitors to find records by the place of birth or enlistment of the service person. To do this I had to extract placenames from the file titles, find the coordinates of the places, and then figure out a way of displaying them on a Google map. We ended up with many thousands of places, and given the limitations of browsers at the time, it wasn't easy to put them on a map. If you tried to display them all at once everything would slow to a crawl. But still...

I remember the first time I got all those places to display -- no fancy interfaces or animations, just thousands of markers obliterating much of Australia. Thousands of places, large and small, that had sent their young people to war. Just seeing those markers crammed in the browser window was a powerful expression of the impact of the war on Australia.

I've still got one of the original data files, so you can try this for yourself. You'll need to install [Google Earth](https://www.google.com.au/earth/). Then just download the [anzacs.kml](https://www.dropbox.com/s/jbzpfuc29fab3xd/anzacs.kml?dl=0) file. Once it's downloaded, just double click on the file to open it in Google Earth. You might need to navigate your way round the globe to find Australia, once you do, zoom in, and in. You might also like to have a look at the UK.

![Google Earth screen capture]({{site.baseurl}}/images/anzacs.jpg){: .img-responsive .img-example}

Even simple maps can carry a powerful message.

### Do maps tell the truth?

Here's a pretty standard map of the world. Have a close look at it and answer one simple question -- which is bigger, Australia or Greenland?

![World map]({{site.baseurl}}/images/Mercator_projection_SW.jpg){: .img-example .img-responsive}

Judging from the map alone you'd think that Greenland was considerably bigger, but it's not. The land area of Australia is 7,692,024 km<sup>2</sup>, while Greenland is only 2,166,086 km<sup>2</sup> -- it's less that a third the size!

So what's going on? As you probably know, there's no simple way of displaying the surface of a globe in two dimensions. In fact cartographers have created many alternative projections, all with their own benefits and limitations. You can browse a [list of different projections](http://www.radicalcartography.net/index.html?projectionref) on the Radical Cartography site (you might need to click on 'Wall maps of the world'). Note the projections that are labelled 'Equal area' -- they represent the area of land masses accurately, though the shapes may be distorted.

The projection above is the Mercator projection, created way back in the 16<sup>th</sup> century to help sailors navigate the world. Despite its distortions, the Mercator projection is still widely used and, most importantly for anyone embarking on a digital mapping project, it forms the basis for just about all online mapping services, such as Google maps.

We put a lot of trust in online mapping applications. We believe them when they tell us to take the next exit on the freeway. We expect them to tell us the 'truth', but like other forms of visualisation, there are many assumptions built into the creation of maps. Maps can lie.

You may have seen a [story in the media recently](http://fusion.net/story/287592/internet-mapping-glitch-kansas-farm/) about a family in rural Kansas that have been accused of all manner of computer-related crimes. Why? Because investigators on the hunt for spammers and scammers try to find them by geolocating their IP addresses (the network address your computer uses to access the net). But when geolocation services don't have enough data for a precise fix, they just return an address in the geographic centre of the country -- and the centre of the USA just happens to be a farm in Kansas. People just assumed that geolocation services were telling the truth.

So once again we have reason to be sceptical of online services. But once again digital technologies can help us to see things differently, to break free of Mercator's grid.

[The True Size Of...](http://thetruesize.com/) is a fantastic digital project that compares the standard web Mercator projection with the real size of countries. It's easy and fun to use:

* Right click on any of the coloured outlines to remove them from the map.

* Enter 'Australia' in the search box.

* Once the coloured outline appears, drag it towards the north pole. What happens?

* Try layering Australia over Europe, or over Greenland!

### Starting simple with Google MyMaps

Let's start off by creating a simple map with Google's My Maps. You'll need to have a Google account to create and share maps.

To open up the My Maps editor you can either:

* go to [Google My Maps](https://www.google.com/maps/d/?hl=en), and then click **Create a New Map**;

* or go to your [Google Drive](https://www.google.com.au/drive/) account and choose **New** > **More** > **Google My Maps**.

![MyMaps]({{site.baseurl}}/images/mymaps.png){: .img-example .img-responsive}

Add a point to your new map:

* Click on the marker icon (the cursor will change from a hand to crosshairs)

* Click anywhere on the map.

* Add a title and description in the info box. Click save.

Search for a place to add to your map:

* Type a query in the search box to find a place -- try  'University of Canberra'.

* The map will recenter and a marker will appear.

* To add this marker to your map, click 'Add to map'.

* Click on the pencil icon to edit the content of the info box. You can also add a photo by clicking on the camera icon.

Try this:

* Draw an area or a line using the polygon tool. What might you use this for?

#### Add a layer

What if you already have data about places that you want to add to your map? It's easy to import data from a spreadsheet by creating a new layer. We're going to create a map of places on the Australian National Heritage List using a [dataset from data.gov.au](http://data.gov.au/dataset/national-heritage-list). 

* Download the [CSV file](https://www.dropbox.com/s/659cx7e912isj8x/heritage_places.csv?dl=0).

* Open up the CSV file and have a look at its contents. 

One thing you might notice is that although there are addresses for each site, there are no coordinates -- latitudes and longitudes. How will Google Maps know where to put the markers? As you'll see, Google Maps (and Google's Fusion Tables) will automatically attempt to turn addresses into coordinates. This process is known as geocoding or geolocation. We'll talk more about this below.

* In the My Maps editor click **Add layer**. A new layer will appear in the dialogue box.

* Click **Import** under your new layer.

* Select and upload the heritage places CSV file.

* You'll then be asked to choose the fields that will enable Google to position your markers. Scroll down the list and check 'address'. If you want to see an example of the contents of each field, just click on the little question mark.

* Click **Continue**.

* Now you need to select the field that contains the titles of your markers. Check 'name'.

* Click **Finish**.

Yay! A map appears with lots of little markers. Try clicking on the markers. Zoom in to see things more clearly.

But wait a minute -- you might have noticed that there's a message in the layer details saying that some of the places couldn't be located. Oh no!

* Click on the **Open data table** link under the warning to see what the problem is.

* At the top of the table you should see a number of rows highlighted in red. For some reason the `address` field didn't provide enough information.

* Find the row for 'Mawsons Huts'. You'll see that the `address` has 'EXT' instead of a state (presumably meaning 'external territory').

* Click on the `address` field and change the 'EXT' to 'Antarctica'. What happens?

See if you can find any other obvious problems and correct them. If we were doing this properly we'd obviously want to make sure that all our places appeared on the map.

* Close the data table.

* Let's try styling our map a bit to show some more information. Click **Uniform style** in the heritage places layer.

* In the 'Group places by' dropdown list choose 'class'. You'll see the markers will now have different colours representing the three classes -- 'Historic', 'Natural', and 'Indigenous'.

This is a simple example of how maps can represent not only locations, but data relating to those locations. My Maps abilities to display data are limited, so for more complex datasets you're probably better off using something like Carto (see below). 

There are other limitations as well. This is a [map of bus stops](https://drive.google.com/open?id=1BuM2waJ91XS8dw4inq-MSOHR0lE&usp=sharing) in Canberra. I've just imported a [dataset](https://www.data.act.gov.au/Transport/Bus-stop-locations-around-the-ACT/uwau-ie6v/data) provided by the ACT Government. But something's not right... Can you see a problem?

It seems that large areas of Canberra have no bus stops! Why? It's just because My Maps will only display 2000 points at a time. Once again -- beware of what online services hide!

Like the charts and visualisations we saw last week, Google's maps can be easily shared and embedded. Click on **Share** to change who can see your map and create a public link. Click on the three little dots next to the map's title to find the embed and export options.

### Maps and data

Increasingly maps are presented as ways of exploring complex datasets. Have a look at the series of maps created by the [American Panorama](http://dsl.richmond.edu/panorama/) project, such as [The Forced Migration of Enslaved Peoples](http://dsl.richmond.edu/panorama/forcedmigration). Examine the types of data being presented and the way the different visualisations interact. Excercise the critical skills we discussed last week -- What's missing? What's unclear? What do you learn?

Another interesting example of data-driven maps is [Orbis](http://orbis.stanford.edu/). This is an attempt to represent the experience of travel in the world of Ancient Rome. By adjusting the settings you can see how this experience changed depending on how much money you had, the transport options available, even the time of year. In this case the data is not really obvious, but clearly the map is based on much detailed research.

For more examples, ideas and inspiration have a browse through the [Carto gallery](https://carto.com/gallery/).

### Geocoding options

Depending on the source of your data you may or may not have coordinates for the places you want to map. As we saw, My Maps (and Fusion Tables) will automatically try to geolocate address data. However, there doesn't seem to be any way of getting the geolocated data back out of Google.

There are a large number of geolocation services about -- most are commercial, though some will offer a free or trial service that will allow you to locate a limited number of points. [Mappify](https://mappify.io/) is an Australian service that seems to offer a reasonable free allowance. Carto, which we'll explore below, only lets you geocode 100 points a month before you have to start paying.

If you're willing to make use of geocoding APIs there are more options available. You might have noticed that the [OpenRefine tutorial](https://github.com/IntersectAustralia/TrainingMaterials/blob/master/CleaningAndExploringYourDataWithOpenRefine/Tutorial.pdf?raw=true) we worked on a few weeks back includes a section on geocoding data. There's also a wholly free and open source geocoding API called [Nominatim](http://wiki.openstreetmap.org/wiki/Nominatim) made available by the Open Street Map community.

### Creating more complex maps using Carto

To introduce Carto (formerly CartoDB) we're going to work through the [Getting started with CartoDB](http://timsherratt.org/digital-heritage-handbook/activities/cartodb-getting-started/) tutorial. This shows you how to import data, create maps, and explore a variety of options for representing your data.

Once we've covered the basics, it's time to try some more advanced techniques in the tutorial [Merging data sources in CartoDB](http://timsherratt.org/digital-heritage-handbook/activities/cartodb-merge-datasets/).

If you want to play around a bit more with the possibilities of Carto, you could try loading the [anzacs.kml](https://www.dropbox.com/s/jbzpfuc29fab3xd/anzacs.kml?dl=0) file. How might you represent this data?

### Georectifying maps

So far the base maps we've been using are just the standard modern web maps we use every day. But if we're using historical data we might want to position our markers on a historical map. There are plenty of historical maps around, the problem is their coordinates might not match those of modern geospatial systems. The way we get around this is by georectification. Put simply, we match known points between the historical maps and modern maps and then distort or align the historical maps so that they can be used with modern geospatial systems. 

Have a look at the [NYPL Map Warper](http://maps.nypl.org/warper/) to browse a large collection of georectified historical maps.

We're going to make use of a public version of the NYPL Map Warper tool to georectify some Australian maps.

* Go to [MapWarper](http://mapwarper.net/)

* We're going to georectify this [1856 map of Melbourne](http://trove.nla.gov.au/version/22074297).

* Click through to the [digitised version](http://nla.gov.au/nla.obj-231730450/view) and then click on the 'Download' icon.

* This map is available as a high resolution tif. This would be the best version to use as it would allow us to zoom right in. But it's 112mb, so to speed things up let's use the jpg for now. Select the 'JPG' option and click **Start download**. You'll need to unzip the downloaded file.

* Go to MapWarper, login and click on the 'Upload Map' tab.

* Copy the basic bibliographic details from Trove to the MapWarper form -- title, publisher, date etc.

* Click on **Choose file** button to select the map we just downloaded.

* Once the form is complete, click on **Create**.

* Once the map has loaded click on the 'Rectify' tab. You'll see the map you loaded on one side, and a modern map on the other.

* Pan and zoom the modern map until you've found the location of your historical map.

* Now the fun begins! Identify points that you can see on both maps (such as the corners of streets). 

* Click on the pencil icon to 'Add a control point' to your historical map. Just click on the map at the point you identified.

* Repeat this process for the modern map.

* Once you're satisfied that you've identified a pair of matching points, click the **Add Control Point**.

* Repeat this at least three times with additional points.

* Once you've added your points, click the **Warp image!** button.

* Once it's done, click on the 'Preview' tab to view the results!

Now try on your own, here's a few searches that will find digitised maps in Trove:

* [Melbourne](http://trove.nla.gov.au/map/result?q=%22nla.obj%22+melbourne)
* [Canberra](http://trove.nla.gov.au/map/result?q=%22nla.obj%22+canberra)
* [Sydney](http://trove.nla.gov.au/map/result?q=%22nla.obj%22+sydney)
* [Adelaide](http://trove.nla.gov.au/map/result?q=%22nla.obj%22+adelaide)

Find, upload and geocode your own map and share the results on Slack.

How can you use these georectified maps? In the bottom left hand corner of your Carto maps you might have noticed an option to change the basemap. 

### Telling stories and mapping uncertainty

[Neatline](http://neatline.org/) is another mapping tool that allows you to incorporate a range of sources and use maps to tell complex and uncertain stories. See their [demos](http://neatline.org/demos/) for some fascinating examples of what's possible.

There are a number of tools available that enable you to create narratives using maps:

* [StoryMapJS](https://storymap.knightlab.com/)
* [OdysseyJS](https://cartodb.github.io/odyssey.js/)

You can even use your georectified maps in StoryMap to narrate a journey around your historical map!

### Timelines

* For a different slant on timelines try [Histography](http://histography.io/)

There are a number of timeline tools around, some free, some paid:

* [TimelineJS](https://timeline.knightlab.com/)
* [HSTRY](https://www.hstry.co/)
* [Dipity](http://www.dipity.com/)
