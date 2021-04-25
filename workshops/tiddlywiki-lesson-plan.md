# TiddlyWiki: Getting Started with digital gardens, networked thinking and non-linear research

4 April 2021<br>
Gavin Gamboa<br>
@gavcloud<br>

## Overview
We will be diving into the [Tiddlywiki framework (TW)](https://tiddlywiki.com/), which is an open-source tool great for compiling notes, research, bookmarking, and making non-linear and personalized knowledge maps. In my case I used it to build a virtual portfolio and bookcase for logging my reading notes and keeping track of my projects.

## Prerequisites

Some understanding of basic HTML and CSS is a plus, but not mandatory. TW is a very deep and complex system but luckily we don't need to know how all its innards interact with each other in order to start building our digital garden. Some tricks I've found that help me format tiddlers the way I want to are `<br>` which in HTML forces a line break in text, and `&nbsp;` which is a way of forcing a non-breaking space, which can come in handy in some cases. Later on we will also create a custom `<div>` class, to have more consistent and dynamic video embeds across devices and viewports. 

## Lesson Plan

- Review the Digital Garden concept. What is a digital garden ? What are the benefits ?
- Download the Tiddlywiki empty.html and begin exploring the interface
- Building a Table of Contents
- Familiarize ourselves with the ways in which new entries (or Tiddlers as they are called in TW) are created and modified
- Familiarize ourselves with WikiText, the Markdown-like syntax that allows uts to format text
- Learn about and decide upon on a tagging system to be implemented for our tiddlers
- Learn how to reference images externally in our tiddlers
- Execute some filter runs to manipulate our data
- Customize the interface by modifying the CSS, embedding videos, customizing fonts.

## Digital Gardens

I find [Anne-Laure Le Cunff's](https://twitter.com/anthilemoon) definition of a digital garden succinct and elegant: [a digital garden is a scalable way to transform seeds of information into original work](https://www.mentalnodes.com/a-gardening-guide-for-your-mind). There is also a burgeoning movement of people who adamantly want to learn things out in the open, and document the process of their learning in real-time. This is where a digital garden can be really handy. You plant **seeds** (ideas, notes, journal entries), which turn into **branches** (through making connections between them), which eventually yield **fruit** (a more substantial corpus, a novel, a research paper). Feel free to explore this [webring](https://dg-webring.netlify.app/) which features a few different flavors of what a digital garden can be.

## First Steps

### Downloading TW

We'll want to Download Empty from the [Getting Started](https://tiddlywiki.com/#GettingStarted) page of TW. This pulls a file called empty.html. This is essentially the entire TW framework encased in a single HTML file. There is no external database that is referenced, everything we add to our wiki will be saved into this file. (Since I run this page on the web at my domain root, I renamed empty.html to index.html. You can name it anything you want).

### Naming Our Wiki

Give a name (I'm calling mine `My Notebook` for this workshop) and the subtitle `babycastles workshop`.

### Quine 

TiddlyWiki is an unusual example of a practical quine: it is this ability to produce a copy of its own source code that lies at the heart of TiddlyWiki's ability to independently save changes to itself.

### Saving

It is important to make multiple redundant backups of your html file. The way we will be saving changes is through the built in Save button in the GUI of TW itself. Saving via Menu > File > Save is unsupported and **will not work**. As a first rule, it is recommended that you are aggressive with your [backup strategy](https://tiddlywiki.com/#The%20First%20Rule%20of%20Using%20TiddlyWiki) in case things go wrong.

## Build the Table of Contents

Let's click the plus sign to add a new tiddler to our notebook. 
* Title it `TableOfContents`
* Tag it with `$:/tags/SideBar` to add it to our Sidebar
* Place this code into the body:<br>
```
<div class="tc-table-of-contents">
<<toc-selective-expandable 'TableOfContents'>>
</div>
```
* Make sure the Content Type is set to `text/vnd.tiddlywiki`
* Add these Fields
  * `caption` in the `field name` and with `{{$:/language/SideBar/Contents/Caption}}` in the `field value`  
  * `list` in the `field name` and with `About Images Text [[Recent Discoveries]]` in the `field value`
  * `list-before` in the `field name` and with `$:/core/ui/SideBar/Open`

Don't worry too much about the technical aspects of the language here. What we are basically doing is adding a new tab to our sidebar called `Contents` and placing it before the open tab. We are also listing a series of tiddlers that we would like to display in a specific order, and then we are also saying making those tiddlers expandable.

## Creating and Modifying Tiddlers

Now we are ready to start making some entries to our wiki. We'll start by clicking the plus button again. Lets create a Tiddler with an image in it. We'll use Hieronymus [Bosch's Garden of Earthly Delights](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/The_Garden_of_Earthly_Delights_by_Bosch_High_Resolution.jpg/1920px-The_Garden_of_Earthly_Delights_by_Bosch_High_Resolution.jpg). We want to embed images externally so that we don't bloat the size of our empty.html file, so the way to do that is to create a separate tiddler for the image asset which loads the external image reference in the form of a url, and then we will reference that in the tiddler for the Garden of Earthly Delights itself.

### Create a Tiddler that externally references an image (jpg/png)

* name the new tiddler for the image `garden-of-earthly-delights`
* set the type to `image/jpeg`
* add a new field called `_canonical_uri` and set the `field value` to [this url](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/The_Garden_of_Earthly_Delights_by_Bosch_High_Resolution.jpg/1920px-The_Garden_of_Earthly_Delights_by_Bosch_High_Resolution.jpg).
* save the tiddler.

You should see the image asset load in the tiddler. Great. We can now reference this in our main tiddler for this artwork.

### Adding an image into a Tiddler

* Create a new tiddler by clicking `+`
* this time name it Garden of Earthly Delights
* tag it `Images` and `painting`
* add in the body `! Bosch`
* add underneath that our image tiddler: `[img [garden-of-earthly-delights]]`
* lets add a quote underneat the image by typing what is happening and then selecting it and choosing the double-quote formatting button. You should see the text enclosed between <<< >>>.

Now we should see our image asset loaded into the body of our main tiddler for this piece.

## Adding our newly created tags to the Table of Contents

So now that we have a tiddler tagged `Images` we want to display that in our `TableOfContents`. In order to do that we need to click on the tag for `Images` and select `Images` itself from the drop down menu. This will pull of an empty, yet-to-be-created tiddler. Let's tag it `TableOfContents` and add a simple piece of code to the body which will pull anything tagged `Images` and display it as a list in the body.

* In the `Images` tiddler, add the following to the body: `<<list-links "[tag[Images]]">>`

Great. Now our tiddler is displayed in the `TableOfContents` tiddler, which is mirrored in the sidebar, as well as the `Images` tiddler.

## WikiText

Now let's create a new tiddler by clicking `+` and calling it `WikiText` and tagging it `Recent Discoveries`. Then we'll add some text for each of the headers and observe how wikitext is working to format this text.<br>
<br>
```
! Header 1
!! Header 2
!!! Header 3

! Header 1\<br>with a line break\<br>preserving H1<br>

This is a link to [[Garden of Earthly Delights]]
This is a link to [[Baby Castles|https://babycastles.com]]
This is not a link to ~McDonalds
This is ''Bold'' text
This is a [[Rocket Ship|Mars Perserverance]]

This is a list

* one
* two
* three

[[Images]]
```
As we did for the `Images` tag previously, let's now edit our `Recent Discoveries` tag and tag it with `TableOfContents` and add `<<list-links "[tag[Recent Discoveries]]">>` to the body, and then save changes.

## Filter Runs

To effectively demonstrate filter runs in action, let's create two more tiddlers within our `Images` category.

* [Vanessa Nakate](https://upload.wikimedia.org/wikipedia/commons/0/0c/Vanessa_Nakate.jpg) and tag it `Images`, `people`
* [Perserverance Mars Lander](https://mars.nasa.gov/mars2020-raw-images/pub/ods/surface/sol/00031/ids/fdr/browse/zcam/ZLF_0031_0669690707_527FDR_N0030828ZCAM05000_0480LUJ01_1200.jpg) and tag it `Images`, and `mars`.

Now let's say we want to run a filter to list all images except paintings. To do that we'll create a new tiddler called `Not a Painting` and add this filter run to the body:`<<list-links "[tag[Images]!tag[painting]]">>`

This will display all `Images` tags and exclude anything tagged `painting`.<br>
<br>
Now let's create a filter for `paintings` and `mars` in a new tiddler called `Landscapes`. The filter run for this will be: `<<list-links "[tag[paintings]][tag[mars]]">>`

[further filter run examples](https://tobibeer.github.io/tw/filters/#Filter%20Examples)

## Customizing Tiddlywiki

### Custom CSS

We can create custom style rules for our wiki by creating a `custom-css` tiddler.<br>
* Create a new tiddler `+`
* name it `custom-css`
* tag it `$:/tags/Stylesheet`

and add this to the body:<br>
```
/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */<br>

/* Document<br>
   ========================================================================== */<br>
```
All of our custom css style rules go below this line.

### Create a custom video container class

Let's add the following to our `custom-css` for YouTube and Vimeo embeds, so that they scale proportionally and fit withing the bounds of our tiddler widths across devices.<br>
```
.video-container {
    position: relative;
    padding-bottom: 53%;
    padding-top: 35px;
    height: 0;
    overflow: hidden;
}

.video-container iframe {
    position: absolute;
    top:0;
    left: 0;
    width: 100%;
    height: 100%;
}
```
Now let's create a new tiddler called `Bird Techno` and grab the embed code from [this YouTube video](https://www.youtube.com/watch?v=6xyGXtOHOkE).

Now add the embed code inside a new div with the `video-container` class:<br>
```
<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/6xyGXtOHOkE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
```

### Custom Fonts

Let's add [Space Mono](https://fonts.google.com/specimen/Space+Mono) to our wiki by loading the font asset into the `<head>` of our page, and adding a rule to our `custom-css`

* Make a new tiddler called `space-mono-font`
* tag it `$:/tags/RawMarkup`
* add the Google Font `<link>` code to the body:
```
<link rel="preconnect" href="https://fonts.gstatic.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Mono&display=swap" rel="stylesheet">
```

Now lets add to `custom-css`:

```
.tc-site-title, h2.tc-title {
font-family: 'Space Mono', monospace;
font-style: normal;
font-weight: 300;
}
```

We have just changed our site title and the titles of each tiddler to our new font family Space Mono :)
