# 100 Days Of Code - Log

## Day 17: April 8, 2017

**Today's Progress**: Started Free Code Camp Weather App; Learned about CSS Shapes extension.

**Thoughts**:

The day started well. I started the next freeCodeCamp project which is to build
a local weather app.  I used the [OpenWeatherMap](http://openweathermap.org) API
for the data.  Instead of navigator.geolocation I used the [ipinfo.io](http://ipinfo.io) API to get the users location.  It seems less flakey that way.  There was a requirement to use icons to display the current weather type for
which I used [Erik Flowers' weather icon font](http://erikflowers.github.io/weather-icons).  And I also had to have a button that toggles between -normal- Fahrenheit and -foreign- celsius which was easy.

Trouble started when I decided it looks a little drab so I wanted to put the
data inside a circle which would have a picture of the planet Earth as a
background.  It turns out there is no standard way to display text in anything
other than a straight line in CSS.  There is a shapes extension that does what
I want but it is not well supported yet.  There is a polyfill but so far I have
been unable to get it to work.  I'll try again tomorrow.

**Links to work:**

* [Free Code Camp Weather App (WIP)](http://www.braincells.com/webdev/local-weather/)

## Day 16: April 7, 2017

**Today's Progress**: Finished building Random Quote Machine.

**Thoughts**:

Finished off converting the Random Quote machine to plain javascript.  It wasn't
that hard really though the DOM has some quirks that jQuery smooths over nicely.
Though doing without has been a very educational experience, I think I'll keep
using jQuery.  Ditto for Bootstrap.

I also learned about CSS filters though in the end I decided not to use them.


**Links to work:**

* [Random Quote Machine](http://www.braincells.com/webdev/random-quote-machine/)

## Day 15: April 6, 2017

**Today's Progress**: Continued building Random Quote Machine.

**Thoughts**:

Another light day.  In the time I could spare, I fixed some bugs concerning
responsiveness in my flexbox-based layout.  I also converted a lot of jQuery
into plain javascript but the task is not complete.

**Links to work:**

* [Random Quote Machine (WIP)](http://www.braincells.com/webdev/random-quote-machine/)

## Day 14: April 5, 2017

**Today's Progress**: Started building Random Quote Machine.

**Thoughts**:

Converted my existing Random Quote Machine design to use flexbox instead of 
Bootstraps' grid.  It basically works but there is more to be done to make it
responsive.  I also need to remove jQuery from the javascript code.

I didn't have time for anything else.

**Links to work:**

* [Random Quote Machine (WIP)](http://www.braincells.com/webdev/random-quote-machine/)

## Day 13: April 4, 2017

**Today's Progress**: Learned about Flexbox.

**Thoughts**:

I got some feedback about my portfolio project.  Mostly positive I'm happy to 
say.  I'll gather it up for now and wait a bit until I revisit it.

The next freeCodeCamp project is a random quote generator.  I had already
attempted this the last time I tried fCC but reviewing it, I see that I used
Bootstrap an jQuery.  I wonder how hard it would be to do it with just css and
vanilla javascript?

To prepare, I learned all about flexbox.  A fun tutorial is [Flexbox Froggy](http://flexboxfroggy.com).

Just to keep my toe in the water I did one of the intermediate algorithm challenges.

**Links to work:**

* [Intermediate algorithm challenge 1: Sum All Numbers in a Range](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms01.js)

## Day 12: April 3, 2017

**Today's Progress**: Finished the portfolio project.

**Thoughts**:

Phew!

Ok in greater depth; some of the things I learned doing this project include:

* How to customize bootstrap with LESS.
* How to minify images, stylesheets and javascript to prevent page bloat.
* How to use Grunt to automate all these.
* Establishing a workflow (dev -> staging -> production) powered by git.
* Web standards and conventions such as ARIA, microformats, and humans.txt
* Letting go of perfection in order to actually get things done.

Now I just need some content to put in it.

**Links to work:**

* [Portfolio](http://www.braincells.com/webdev/)

## Day 11: April 2, 2017

**Today's Progress**: Finished freeCodeCamp JSON APIs and AJAX exercises; The tide is turning in the war on Bootstrap.

**Thoughts**:

I finished all the freeCodeCamp JSON APIs and AJAX exercises which wasn't very
hard because they were all cut-and-paste and there weren't even that many.  It
is definitely a part of the curriculum that needs to be strengthened IMO.

My Bootstrap customizations are looking a lot better as I understand its' 
structure in greater depth.  I'm still not done yet.

I learned a nifty CSS trick.  Given HTML like this:

```
<span class="fa fa-envelope"><span class="hidden-text">Contact</span></span>
```

This CSS will make it so only the icon shows up in a graphical browser but the
text will be displayed in a text-mode browser such as w3m or lynx.

```
.hidden-text {
    display: none;
    text-indent: 100%;
    white-space: nowrap;
    overflow: hidden;
}
```

Ok, maybe the general public rarely need or use something like that but I do
and I know a lot of my fellow Linux users do too so I definitely wanted to
make my site usable in text-mode.  I imagine that would also help e.g. blind
people using screen-readers etc.  (There is a specification called ARIA which
I have been reading about and partially implemented though there is more work
to be done on that front.)

**Links to work:**

* [Portfolio (WIP)](http://www.braincells.com/webdev/)

## Day 10: April 1, 2017

**Today's Progress**: Finished freeCodeCamp Functional and OOP exercises; More Bootstrap aggravation.

**Thoughts**:

I did all the freeCodeCamp object-oriented and functional programming exercises..

I try to keep reminding myself that the perfect is the enemy of the good but
this I think is too important not to fix.  I mentioned previously that I have
some icons in my navbar.  As the navbar is responsive, it collapses into a 
"veggie burger button" (this is what I am choosing to call a ["hamburger button"](https://en.wikipedia.org/wiki/Hamburger_button) :-) with a dropdown menu if the screen width gets too narrow.  The problem is that the menu looks
bad if there are only icons on it.  There ought to be text labels too IMO.  But
I don't want those labels when the navbar is full size.  Figuring out how to do
this in CSS and Javascript has been quite difficult.  However I'm sure this is
the kind of scenario real front-end developers have to deal with so I'm 
determined to figure it out.  I did get the color problem from yesterday sorted
out so I'm confident I can solve this one too.

**Links to work:**

* [Portfolio (WWWWWWWWIIIIIIIIIIIIIIIIIPPPPPPP)](http://www.braincells.com/webdev/)

## Day 9: March 31, 2017

**Today's Progress**: Finished freeCodeCamp javascript exercises; struggled with Bootstrap.

**Thoughts**:

I finished the freeCodeCamp basic javascript exercises.  Now it's onwards to
object-oriented and functional programming.

I had hoped to finish my portfolio today but ran into an unexpected snag.  I
have a set of icons in my Bootstrap-produced navbar.  I wanted to change their
color.  Easy right?  Somehow I can't get the right sequence of CSS classes to
override in order to make this happen.  The Firefox developer tools were very
useful but I still didn't get it.  Bootstrap is wonderful for the design-challenged
like me but there is a lot of magic under the hood which makes it hard to 
understand exactly what's going on.

No codefights today either.

**Links to work:**

* [Portfolio (alas, still WIP)](http://www.braincells.com/webdev/)

## Day 8: March 30, 2017

**Today's Progress**: More freeCodeCamp javascript exercises; Worked on Portfolio a bit more.

**Thoughts**:

Today I did even more of the freeCodeCamp javascript exercises.  I also did
more work on my portfolio including some interesting experiments in making it
responsive.  I didn't put up the current state publically yet but I think that
by tomorrow I'll be ready to mark this as done.  For now.

I should have done some codefights but got lazy.  I am suitably ashamed.

**Links to work:**

* [Portfolio (WIP but not for much longer!)](http://www.braincells.com/webdev/)

## Day 7: March 29, 2017

**Today's Progress**: More freeCodeCamp javascript exercises; Learned about less; Started doing exercises from Codefights.

**Thoughts**:

I'm sad to say I've just been treading water today.  I did do some more of the
freeCodeCamp javascript exercises.  Also via the FCC forum I learned of a site
called [CodeFights](https://codefights.com/) where you can practice algorithmic
problems in a variety of languages.  (I'm using Perl with C++ as a backup.)  The
first few problems were easy but this one had me stumped for a long time:

Given a sequence of integers as an array, determine whether it is possible to
obtain a strictly increasing sequence by removing no more than one element
from the array.

Eventually I was forced to look at [Stack Overflow](http://stackoverflow.com/questions/43017251/solve-almostincreasingsequence-codefights) for help.
I was relieved to see that I was basically on the right track but it shows I
need more practice in this sort of thing.

**Links to work:**

* [Portfolio (WIP still)](http://www.braincells.com/webdev/)

## Day 6: March 28, 2017

**Today's Progress**: Did some freeCodeCamp javascript exercises; Learned about less; Continued work on Portfolio.

**Thoughts**:

I did some of the freeCodeCamp javascript exercises mostly just to keep my
activity streak going more than anything else. 

Today I learned about LESS.  This is a language for generating CSS so there is
less boilerplate you actually need to write. (As usual in the Javascript world
there are alternatives like SASS and Compass.  I haven't looked at them yet.)
Bootstrap is generated from LESS files.  So I found out how to change
parameters like default colors and recompile bootstrap.  (A Grunt task comes
in handy for that.)  Flat-UI which I mentioned yesterday is created just like
that.  I forgot to mention in yesterdays log that I had been looking for
themes to use as inspiration.  I found one for portfolios at
[startbootstrap](https://startbootstrap.com/template-overviews/freelancer/)
called Freelancer that seemed nice.  From
[bootswatch](http://bootswatch.com/superhero/) came Superhero which was more
basic but had the kind of color scheme I wanted.  Finally, I replaced the
glyphicons font that came with Flat-UI with
[Font Awesome](http://fontawesome.io/) for the icons.  All of these are
distributed with LESS files so I integrated them into my custom bootstrap.

So now my portfolio is looking much better&mdash;apart from the woeful lack of content.

**Links to work:**

* [Portfolio (WIP)](http://www.braincells.com/webdev/)

## Day 5: March 27, 2017

**Today's Progress**: Did the freeCodeCamp jQuery exercises; Learned about grunt; Continued work on Portfolio.

**Thoughts**:

I did the freeCodeCamp jQuery exercises.  All stuff I knew already so that
didn't take long.

After the nth iteration of writing files, uploading them to the server, and then
moving them into place I wondered if there was a way to automate it all and the
answer is, yes there is.  In fact as is usual in the javascript world there
are several incompatible ones, no one agrees which is standard, and the
"coolest" keeps changing every few months.  I settled on grunt mainly because
a book I'm reading has a chapter on it.

With grunt, you can set up various tasks.  I currently have:

* htmlhint: which checks your HTML syntax for things like missing end tags etc.
* imagemin: which compresses images so loading them will not use as much bandwith.
* cssmin: which does the same but for CSS.  It can also concatanate all your CSS files into one so you get one big but efficient download instead of several smaller but slower ones.
* uglify: compresses and concatenates javascript.
* copy: moves files around so you can arrange them as you need in a destination directory.

This destination directory is a git repository which tracks a repository on my
server.  So after running 'grunt build' I commit any changes that occured and
then do a 'git push' to upload everything in one go.

It was suggested to me on gitter that I put all my work on github so potential
employers etc. can inspect it.  I haven't set it up yet but with this setup
I can easily set up github as another push target and use it as a mirror
(and backup!) with only one extra command.

With all this going on there was little time to actually work on the portfolio
(I must be careful about this.)

**Links to work:**

* [Portfolio (WIP)](http://www.braincells.com/webdev/)

## Day 4: March 26, 2017

**Today's Progress**: Did the freeCodeCamp Bootstrap exercises; Started work on Portfolio.

**Thoughts**:

Bootstrap is a godsend to artistically challenged people like myself.  I did
freeCodeCamps bootstrap exercises to refresh my memory of how it works.  It
seems they are based on version 3 and there is a Bootstrap 4 out.  Last time
aound what finally sunk me was agonizing over getting the portfolio (which
is the second Basic Frontend Development Project in the FCC curriculum) just
right and eventually losing all momentum.  So this time I'm not going to worry
just yet and stick with 3.

However I am going to ditch my previous attempt and start from scratch.  One
thing I will be keeping is the [Flat-UI toolkit](https://github.com/designmodo/Flat-UI), a theme for Bootstrap which gives it a more modern "flat" look.

I did the basic framework of the portfolio page but ran out of time to add content
today.


**Links to work:**

* [Portfolio (WIP)](http://www.braincells.com/webdev/)

## Day 3: March 25, 2017

**Today's Progress**: Did the freeCodeCamp HTML5 and CSS exercises;  Built a tribute page; Helped a Freecodecamper learn C.

**Thoughts**:

I started with the javascript algorithm stuff first because I thought that
would be more interesting and challenging and because, if you remember, I had
started and dropped freeCodeCamp once before and I thought that I remembered
the basics of JavaScript, HTML5, CSS, jQuery, and Bootstrap well enough from
then.  However today I decided that it might be prudent to review it once more.
It being the weekend, there were domestic things to attend to but I did get
through all the HTML5 and CSS exercises.

I also took some time to help a camper who is learning C which I know well. I
am still wondering if I should go into web development or C/C++.  Whichever
results in big $$$$ first I guess.

Lastly I took the old tribute page I had done as the first Basic Frontend
Development Project from the last time and gave it the once over.  I think it
is good so I submitted it.  The only difference is last time I had it up on
codepen, which no offense, is a wonderful service but a little inflexible
unless you pay for the pro features.  I have a server of my one so I just put
it up there instead.

**Links to work:**

* [A Tribute to the Sinclair ZX Spectrum](http://www.braincells.com/webdev/tribute-to-spectrum/)

## Day 2: March 24, 2017

**Today's Progress**: Finished the rest of the Basic Algorithm Scripting Challenges from freeCodeCamp; learned about git.

**Thoughts**:

Today almost ended in disaster when I somehow messed up my git repository.
Luckily I had not pushed my local changes to github so there was still a chance
I could fix things up without having to blow away the repository and start over
which is my usual remedy for git problems.  This is what I did.

First of all you should checkout a new branch.  Call it backup or something.  As
the name suggests, this is a backup just in case you mess things up.  Now go
back to your master branch and use git reset --hard [commit] where [commit] is
the value of your last good public commit on github.  Now all your latest work
seems to have disappeared but don't worry all the commits are still there on the
backup branch.  You can reimport some or all of them back into the master
branch with the git-cherry-pick command (See the man page for details.)  Then
when everything is shipshape again push to github as usual and delete the
backup branch.  Phew! Disaster averted.

**Links to work:**

* [Basic algorithm challenge 6: Return Largest Numbers in Arrays](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms06.js)
* [Basic algorithm challenge 7: Confirm the Ending](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms07.js)
* [Basic algorithm challenge 8: Repeat a string repeat a string](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms08.js)
* [Basic algorithm challenge 9: Truncate a string](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms09.js)
* [Basic algorithm challenge 10: Chunky Monkey](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms10.js)
* [Basic algorithm challenge 11: Slasher Flick](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms11.js)
* [Basic algorithm challenge 12: Mutations](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms12.js)
* [Basic algorithm challenge 13: Falsy Bouncer](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms13.js)
* [Basic algorithm challenge 14: Seek and Destroy](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms14.js)
* [Basic algorithm challenge 15: Where do I belong](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms15.js)
* [Basic algorithm challenge 16: Caesars Cipher](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms16.js)

## Day 1: March 23, 2017

**Today's Progress**: First 5 Basic Algorithm Scripting Challenges from freeCodeCamp

**Thoughts**:

It's not like I'm completely new to programming.  In fact I've been coding for
over 20 years and I've been employed professionally in the field for most of
that time.  However for many years I've just been treading water.  I've let my
skills stagnate and I probably haven't been making as much money as I could have
been.  Yesterday was my birthday.  I've decided that this is the year this
is going to end and I'm going to get back into full-time professional software
development.  100 days should be more than enough to get back up to speed so I'm
taking up this challenge starting with the [Free Code Camp](https://www.freecodecamp.com/)
curriculum.  I had started this last year but kind of ran out of steam.  Not this time!


**Links to work:**

* [Basic algorithm challenge 1: Reverse a String](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms01.js)
* [Basic algorithm challenge 2: Factorialize a Number](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms02.js)
* [Basic algorithm challenge 3: Check for Palindromes](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms03.js)
* [Basic algorithm challenge 4: Find the Longest Word in a String](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms04.js)
* [Basic algorithm challenge 5: Title Case a Sentence](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms05.js)

Note due to a git mishap the date on the files is March 24 but I did them on the 23rd I swear! :-)
