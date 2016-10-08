#duckycss

duckycss is an unopinionated OOCSS framework; it is a fork of  [inuitcss](https://github.com/inuitcss/inuitcss) which is maintained by [Harry Roberts](https://twitter.com/csswizardry).

##Prologue
After spending a lot of time building my own OOCSS framework from scratch I found it becoming more similar to inuitcss as time went on.

With that in mind, I canned my own project and forked a copy of inuitcss to use as a starting point. This is the result.

##Installation
I think it's important I don't try to force people outside of their own workflow. So whether you use [Gulp](http://gulpjs.com/), [Grunt](http://gruntjs.com/), [Webpack](https://webpack.github.io/) or the latest task runner all the cool kids are using go nuts. Basically this is an 'Installation' section about how there is no installation section :)

##Getting Started
Either download the .zip or clone this repo to your local machine and ```cd``` into it. You'll notice 3 folders: ```css/```, ```less/``` and ```scss/```.

###Sass
[Sass](http://sass-lang.com/) is my CSS extension language of choice so this project is geared towards Sass users- in particular the SCSS (Sassy CSS) syntax.

###Less
Despite my penchant for Sass we use [Less](http://lesscss.org/) at [EKM](https://www.ekm.com/) hence my inclusion of a ```less/``` directory. Unfortunately Less doesn't quite include the same functionality as Sass in terms of logical and looping operators so the code in ```less/``` is more verbose than its big sister's.

###CSS
If pre-processing isn't your bag I've included both minified and un-minified CSS files in ```css/```. Because I'm nice like that. If you *are* using Sass or Less this is the directory your processed styles will end up in. We're talking about overrides, baby!

TL;DR pick your weapon of choice :)

##File Structure
Both ```sass/``` and ```less``` directories follow Harry Roberts' 'inverted triangle' ([ITCSS](http://itcss.io/)) methodology of CSS architecture.

Each 'layer' of styles gets progressively more specific and explicit the further down we go. When combined with a single class approach the result is a project free of specificity wars.

```
settings/
tools/
generic/
elements/
objects/
components/
utilities/
main.scss
```

###Settings
This is where our variables live both in terms of framework-specific variables and our project's base/global variables. This is where the party starts, basically.

###Tools
All our functions and mixins reside here- most of which are central to the way duckycss works. But some of them are for you to play with, lucky you!

###Generic
We define our wide-reaching styles like `box-sizing` and `clear-fix` here. They're kind of a big deal. The ```generic/``` also includes our resets in the form of [@necolas](https://twitter.com/necolas)'s [Normalize.css](http://necolas.github.io/normalize.css/) and our additional mini-reset. This layer lays out the foundation upon which the rest of our styles
are built. Like houses and shit.

###Elements
This is where we style un-classed HTML elements. This is a class-free zone, people. Respect the rules.

###Objects
Our objects and abstractions layer. This is where the [OOCSS](http://oocss.org/) magic happens and is where the real code-saving occurs. By using repeatable design patterns we can seriously reduce the amount of CSS we write. And we all hate writing CSS, right? Right!?

###Components
Project-specific chunks of UI live in this layer. While you will likely include similar components in here from project-to-project you will find they'll be styled on a strictly per-project basis.

There's an example button component included to get you started.

###Utilities
Whoever said you shouldn't use `!important`, eh? Because you'll find them by the sack-load in this layer. Utility classes have one specific job to do and should never be overwritten. NEVER. These incredibly useful helper classes will help you out of more than a pickle.

##Respek
Thanks to [Harry Roberts](https://twitter.com/csswizardry), [Nicole Sullivan](https://twitter.com/stubbornella), [Nicolas Gallagher][https://twitter.com/necolas] and [Hugo Giraudel](http://hugogiraudel.com/) for teaching me more about front-end development than any book or course could.

##Get in Touch
I like beer. We should go for a beer! [Hit me up](https://twitter.com/adam_duckett).
