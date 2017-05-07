# 100 Days Of Code - Log

## Day 45: May 6, 2017

**Today's Progress**: Debugging Calculator project

**Thoughts**:

I was going to continue with the tic-tac-toe project today but I got reports
thats there were still a couple of bugs in the calculator which I decided to
fix.  Unfortunately that used up all my available time.

**Links to work:**

* [Calculator](http://www.braincells.com/webdev/calculator/)

## Day 44: May 5, 2017

**Today's Progress**: Finished Calculator project

**Thoughts**:

I redid all the key handling code and reimplemented it as a state machine.  It's
much cleaner and bug-free now. The app is complete and has been submitted to
freeCodeCamp.

Next I'm going to do the Tic-tac-toe (or as I know it better, noughts and
crosses.) project.  I've already made a prototype which plays the game but not
intelligently.  This will be the next step along with UI improvements.


**Links to work:**

* [Calculator](http://www.braincells.com/webdev/calculator/)

## Day 43: May 4, 2017

**Today's Progress**: Continuing Calculator project

**Thoughts**:

The calculator is essentially complete but there are a couple of small logic
problems to be chased down and I'm too tired for that right now.

I couldn't resist one more UI improvement, namely an LCD font for the output.
I was surprised that [Google fonts](https://google.com/fonts) doesn't have on or maybe I couldn't find
it with their, ironically, horrible search.  [Font Squirrel](https://www.fontsquirrel.com) does.
They even have a service to convert it into a webfont which I did.

**Links to work:**

* [Calculator (WIP)](http://www.braincells.com/webdev/calculator/)

## Day 42: May 3, 2017

**Today's Progress**: Continuing Calculator project; Flexbox Zombies

**Thoughts**:

I didn't have a lot of time today. But I managed to improve the CSS for the 
calculator quite a bit.  I wrote some code for evaluating arithmetic.  But it 
turns out that is unnecessary because JavaScripts inbuilt eval function can do 
the job.  So I took it out again.  Some say eval is insecure but that is only 
if you feed it unfiltered user input.  We restrict input to that which comes 
from the buttons only.  Eval also does the right thing in regards to order of 
operations which I noticed the sample calculator does not.  I.e. 3+5*6 should 
be 33 not 48.

I also did another chapter of Flexbox Zombies.

**Links to work:**

* [Calculator (WIP)](http://www.braincells.com/webdev/calculator/)

## Day 41: May 2, 2017

**Today's Progress**: Started Calculator project

**Thoughts**:

I started the calculator project today.  I am going to use flexbox as it
makes this kind of tabular layout easy yet responsive.  I have the basic
key layout done.  I also spent some time reading about parsing and evaluating
arithmetic in javascript.

Speaking of flexbox, Dave "geddski" Geddes launched his free 
[Flexbox course](http://flexboxzombies.com/p/flexbox-zombies) yesterday.
I went through the first couple of chapters. So far it is pretty simple
but I hope I can learn more advanced flexbox usage through it.

**Links to work:**

* [Calculator (WIP)](http://www.braincells.com/webdev/calculator/)

## Day 40: May 1, 2017

**Today's Progress**: Finished Twitch.tv API project

**Thoughts**:

The Twitch.tv project is done and submitted.  I couldn't resist trying to do
the radio button toggle effect and I finally got it with a little help from
the internet.  It turns out you need both real radio buttons for the clicking
_and_ fake ones so you can style them.  Now it's onwards to the advanced
projects.  I think I will start with the calculator first.  It looks
interesting.

Also I attended a meeting of the New York Perl Mongers today.  It was an
interesting talk about XML.  I need to get back into Perl.  It is so much
better than JavaScript IMO.

**Links to work:**

* [Twitch.tv JSON API](http://www.braincells.com/webdev/twitch-api/)

## Day 39: April 30, 2017

**Today's Progress**: Continued work on Twitch.tv API project

**Thoughts**:

This log is very late because of an Internet outage which couldn't have come
at a worse time.  I was _this_ close to having the Twitch.tv project done and
shipped.  I still haven't figured out the radio button thing but that is just
cosmetic.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Day 38: April 29, 2017

**Today's Progress**: Continued work on Twitch.tv API project

**Thoughts**:

Being the weekend, household chores and dinner with my parents left little
time for coding but what I did have was very productive.  I got the CSS toggle
effect to work without going to stackoverflow or github or anyone elses code.
It turns out I did need radio buttons after all or atleast that is the most
straightforward way to implement this effect.  However a problem with radio
buttons is as far as I can see there is no way to style them.  I'll have to
think about this.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Day 37: April 28, 2017

**Today's Progress**: Continued work on Twitch.tv API project

**Thoughts**:

The javascript to access the API has been straightforward but getting the
filter buttons to toggle as in the example project has been an interesting
challenge.  Using javascript should be easy but it seems to me I should be
able to do it in pure css if I can just figure out how.

My first inclination was to have actual radio buttons and labels in a form.
But that didn't work because something (bootstrap?) kept leaving a space for
the label.  Normally you'd want that to make the radio buttons line up neatly
but this time I wanted the opposite.

So I've made fake radio buttons and labels out of divs and spans for what ought
to be more control.  But the same thing happens.

Oh well let me sleep on this mystery and maybe it will solve itself tomorrow.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Day 36: April 27, 2017

**Today's Progress**: Started work on Twitch.tv API project

**Thoughts**:

I started the next freeCodeCamp front-end certificate project.  Mainly, I did
a lot of reading to see how their API works so there is not much to see at the
moment.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Day 35: April 26, 2017

**Today's Progress**: Finished Wikipedia Viewer

**Thoughts**:

I forced myself to finish the wikipedia viewer.  I even improved my previous 
design a bit by using client-side templates using 
[Hogan.js](http://twitter.github.io/hogan.js/), Twitters version of the 
popular Mustache template system.  While there are probably some rough edges,
I think it is good enough to mark as done so I can move forward once again.

I should mention I didn't implement infinite scrolling in the end but I do want
to visit that at some point in the future.

**Links to work:**

* [Wikipedia Viewer](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 34: April 25, 2017

**Today's Progress**: No progress :(

**Thoughts**:

My new phone arrived from Amazon.  It's a ZTE Axion 7 that's miles ahead of my
old phone in every measure of power you can think off.  I installed LineageOS,
a custom build of Android on it.  That took a lot of my available time and as
a result, I did not work on the wikipedia viewer.  I did fulfill my one hour of
coding requirement by porting a little Android ggame I had made at an earlier
time but as that didn't really involve learning anything new, I consider the
day a loss.

And it has me worried.  It's been a week since I started the wikipedia viewer 
project and I really should have been done in half that time. I recognize this 
pattern in myself where I start doing something with enthusiasm and then 
slowly lose momentum eventually leaving it incomplete. The whole point of doing
this challenge was to break out that behavior so I'm a little depressed that
I can still be distracted that easily.  But I won't give up the fight just yet!


**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 33: April 24, 2017

**Today's Progress**: Continuing work Wikipedia Viewer

**Thoughts**:

I really ought to submit the wikipedia viewer and be done with the damn thing 
but I noticed something.  It should have been obvious but I only noticed now 
that the wikipedia API query only gives you a maximum of 10 items no matter 
how many hits a search term gets.  You are supposed to "page" through the 
results 10 at a time.  This is to reduce load I imagine.  The simple way to 
implement this would be to have a "next" button (and "previous" to go back in 
the result set) which would keep track of an offset and then get those items.
However modern sites seem to eschew this approach and have instead have an
"infinite scroll" effect where going to the bottom the page instantly loads the
next page of results.  So I researched how to implement this and soon ran out
of time.  If I can't get this working by tomorrow, I'm just going to submit it
as-is.  I've got to keep moving.

**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 32: April 23, 2017

**Today's Progress**: Success with Wikipedia Viewer searchbox

**Thoughts**:

Even though I was distracted by household chores and Amazon delivering a brand
new smartphone to me.  (ZTE Axon 7 if you're interested) I did manage to put in
some solid time today and I finally got the searchbox to expand and contract
properly.  Take a look at the linked codepen to see how I did it. I learned
more about CSS in the last few days than I have in my whole life so I'm very
proud of this though there are better ways of achieving this effect in a
real-life scenario. (e.g. jQuery and its various animation plugins.)

I ran out of time to finish the project but I hope to do so tomorrow.

**Links to work:**

* [A Searchbox That Expands From an Icon and Contracts Again](https://codepen.io/jaldhar/details/PmzdmY/)
* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 31: April 22, 2017

**Today's Progress**: Still working on Wikipedia Viewer

**Thoughts**:

The good news is that I can now make the search box expand as it should.  The
bad news is I don't seem to be able to make it contract again and I don't
understand why.  Please take a look at the codepen linked below and let me
know what I'm doing wrong.

**Links to work:**

* [Codepen illustrating my problem](https://codepen.io/jaldhar/details/PmzdmY/)
* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 30: April 21, 2017

**Today's Progress**: Continued Wikipedia Viewer; Learned CSS transitions and transformations

**Thoughts**:

I was hoping to finish the wikipedia viewer today but I got waylaid with
learning about CSS transitions and transformations.  I want to replicate the
way the search box expands like in the example project but I'm afraid I still
haven't got it right though I feel I am close.  So I am still resisting the
urge to peek at their code for now.

**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 29: April 20, 2017

**Today's Progress**: Continued Wikipedia Viewer

**Thoughts**:

Made progress on the wikipedia viewer.  Copying the functionality of the
example project without peeking at the code has been frustrating but enjoyable.

Take for example getting the close icon to appear at the right of the search
box.  Initially gave me a great deal of difficulty but then I had an epiphany;
instead of drawing a border around the input element and then somehow fitting
a close icon into it, I could just draw a border around the whole div that
wraps them both.

Recreating the rest of the UI was simple.  I haven't matched the color scheme 
and fonts 100% correctly but what I have looks good enough IMO.  Tommorow I 
will write the code to actually fetch results from the Wikipedia API.


**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 28: April 19, 2017

**Today's Progress**: Went to Android meetup; Started Wikipedia Viewer

**Thoughts**:

Today I went to a meetup organized by New York Android Developers. There were
two talks, one on using Exoplayer as a replacement for the MediaPlayer class 
and one on Android Lint and writing custom rules for it.

Android development is another interest of mine.  I have a few apps in the 
Play Store and some more in various stages of completion on my laptop.  It's a 
possible career too.  I actually started the Udacity NanoDegree program a 
while ago but didn't pursue it very far.  As I am actually paying money each 
month for it and after receiving the latest bill I thought that I should 
finish it once and for all and attending this meetup was to be the beginning 
of the process.

But this is another bad habit of mine.  I start things, sometimes get as far 
as 90% of the way through them and then drop them before completion.  As one 
of my reasons for doing the 100 Days of Code challenge is to improve my 
self-discipline,  I decided that I must complete the FreeCodeCamp front-end
certificate before I go to Android in earnest.

So even though I was tired and wanted to go to sleep, I forced myself to atleast
start the Wikipedia Viewer project today.


**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Day 27: April 18, 2017

**Today's Progress**: Finished Responsive Web Design course from The Gymnasium

**Thoughts**:

It turns out yesterdays problem was nothing to do with code.  I had
inadvertently corrupted the hamburger image.  I must remember to take this
into consideration when debugging in the future.

I finished the Responsive Web Design Course.  I learned a lot but the lectures
were recorded in 2014 and in web development terms that's ancient history.
For instance supporting Internet Explorer isn't a big deal anymore and HTML5
features such as the picture element are more widely supported.  Other
important topics such as flexbox were not covered at all. All in all I would
give it an 8/10.

**Links to work:**

* [Responsive Portfolio](http://www.braincells.com/webdev/responsive-portfolio/)

## Day 26: April 17, 2017

**Today's Progress**: Continued Responsive Web Design course from The Gymnasium

**Thoughts**:

I was hoping to have the Responsive Web Design course done today but I ran into
a problem which got me so engrossed I ran out of time. The problem is my
responsive layout is supposed to show a "hamburger menu" if the viewport gets
too small.  This collapses the navigation links into a drop down menu.  This
works well but for some reason the "hamburger" itself which is a background 
image in a label element just isn't showing up.  The exact same CSS is working
for other people.  I've been wracking my brains but I just can't figure it out.

Oh well I think I better call it a night and come back to it tomorrow.

**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)

## Day 25: April 16, 2017

**Today's Progress**: Continued Responsive Web Design course from The Gymnasium

**Thoughts**:

I am a quarter of the way through the 100 Days of Code challenge.

Today I did two more sections of the Responsive Web Design course on grids and 
forms.  I even implemented a fluid two-column layout of my own but you can't 
see it because I went back to the old layout to stay in sync with the course.

I really should try to wrap this up tomorrow if I can (there are 5 sections 
left) and get back to freeCodeCamp.


**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)

## Day 24: April 15, 2017

**Today's Progress**: Continued Responsive Web Design course from The Gymnasium

**Thoughts**:

Back to full strength but today was mostly dedicated to household chores. I did
the next section of the Responsive Design course which was about typography.
I learned a lot of new terminology which I'm not sure I've fully assimilated
just yet.  I can see how important it is to learn this stuff.  Design is my
weak point and I did not realize how much good use of type can improve a web
page.

**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)

## Day 23: April 14, 2017

**Today's Progress**: Continued Responsive Web Design course from The Gymnasium

**Thoughts**:

Feeling a bit better but not 100%.  I did a few more sections of the
Responsive Web Design course.  I learned a lot about media queries.  It's
really impressive how much work has to go into making a layout look good in
all possible dimensions. I really have to respect Bootstrap for hiding most of
that complexity.

**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)


## Day 22: April 13, 2017

**Today's Progress**: Started Responsive Web Design course from The Gymnasium

**Thoughts**:

It's official; I'm sick.  Being dissatisfied with just the canned solutions
Bootstrap gives you, I took a detour from [freeCodeCamp](https://freecodecamp.com) and started a Responsive Web Design course from [The Gymnasium](https://thegymnasium.com) which is centered around
building a responsive portfolio site from scratch.  I only got through the
first two chapters in my weakened state but I'm happy I atleast did something.


**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)


## Day 21: April 12, 2017

**Today's Progress**: Finished Advanced Javascript algorithm challenges

**Thoughts**:

My head was pounding all day today so I didn't feel like starting a new
project but I did do all the Advanced Javascript algorithm challenges.
 
**Links to work:**
* [Advanced algorithm challenge 1: Validate US Phone Numbers](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms01.js)
* [Advanced algorithm challenge 2: Record Collection](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms02.js)
* [Advanced algorithm challenge 3: Symmetric Difference](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms03.js)
* [Advanced algorithm challenge 4: Exact Change](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms04.js)
* [Advanced algorithm challenge 5: Inventory Update](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms05.js)
* [Advanced algorithm challenge 6: No Repeats Please](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms06.js)
* [Advanced algorithm challenge 7: Make a Person](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms07.js)
* [Advanced algorithm challenge 8: Map the Debris](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms08.js)
* [Advanced algorithm challenge 9: Pairwise](https://github.com/jaldhar/FreeCodeCamp/blob/master/Advanced%20Algorithm%20Challenges/algorithms09.js)


## Day 20: April 11, 2017

**Today's Progress**: Finished weather app!.

**Thoughts**:

Hooray! I finished the Local Weather app.  It required a lot of last minute
fiddling to get things looking right at different resolutions but I think I 
did it more or less.

By far the biggest stumbling block is that Lettering.js in the process of slicing
up a piece of text into spans does something to its container making it 0 width.
I don't know enough about JavaScript and the DOM to know if this is a bug in
the plugin or a natural consequence of the method used.  I'll see if I can
contact the maintainer and get some guidance.

**Links to work:**

* [Free Code Camp Weather App](http://www.braincells.com/webdev/local-weather/)

## Day 19: April 10, 2017

**Today's Progress**: Progress on round text in weather app; Finished JavaScript algorithms.

**Thoughts**:

If at first you don't succeed, move onto something else productive.  You can
always revisit the problem later.

I've given up on CSS shapes.  I have however managed to acheive circular text
with a combination of three jQuery plugins: lettering, roundType and fitText.
They work by the horribly hacky method of making each letter of text into a
span and using CSS transforms to rotate it to the desired angle.  CSS shapes
would have been a lot cleaner but atleast this does work.  Well, mostly; apparently
you cannot embed icon fonts into the rotated text.

I ran out of allotted time today but I think I will soon be able to make my 
design work.

Also, I finished the rest of the intermediate JavaScript algorithm challenges.

**Links to work:**

* [Free Code Camp Weather App (WIP)](http://www.braincells.com/webdev/local-weather/)
* [Intermediate algorithm challenge 11: Convert HTML Entities](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms11.js)
* [Intermediate algorithm challenge 12: Spinal Tap Case](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms12.js)
* [Intermediate algorithm challenge 13: Sum All Odd Fibonacci Numbers](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms13.js)
* [Intermediate algorithm challenge 14: Sum All Primes](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms14.js)
* [Intermediate algorithm challenge 15: Smallest Common Multiple](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms15.js)
* [Intermediate algorithm challenge 16: Finders Keepers](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms16.js)
* [Intermediate algorithm challenge 17: Drop It](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms17.js)
* [Intermediate algorithm challenge 18: Steamroller](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms18.js)
* [Intermediate algorithm challenge 19: Binary Agents](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms19.js)
* [Intermediate algorithm challenge 20: Everything Be True](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms20.js)
* [Intermediate algorithm challenge 21: Arguments Optional](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms21.js)

## Day 18: April 9, 2017

**Today's Progress**: Still stuck with CSS shapes; Did some JavaScript algorithms.

**Thoughts**:
Busy for most of the day with household chores but spent time trying to get
CSS shapes to work, this time with a different polyfill.  Still no dice.

Drowned my sorrows in some JavaScript algorithm challenges.

**Links to work:**

* [Free Code Camp Weather App (WIP)](http://www.braincells.com/webdev/local-weather/)
* [Intermediate algorithm challenge 2: Diff Two Arrays](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms02.js)
* [Intermediate algorithm challenge 3: Roman Numeral Converter](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms03.js)
* [Intermediate algorithm challenge 4: Wherefore Art Thou](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms04.js)
* [Intermediate algorithm challenge 5: Search and Replace](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms05.js)
* [Intermediate algorithm challenge 6: Pig Latin](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms06.js)
* [Intermediate algorithm challenge 7: DNA Pairing](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms07.js)
* [Intermediate algorithm challenge 8: Missing Letters](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms08.js)
* [Intermediate algorithm challenge 9: Boo Who](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms09.js)
* [Intermediate algorithm challenge 10: Sorted Union](https://github.com/jaldhar/FreeCodeCamp/blob/master/Intermediate%20Algorithm%20Challenges/algorithms10.js)

## Day 17: April 8, 2017

**Today's Progress**: Started Free Code Camp Weather App; Learned about CSS Shapes extension.

**Thoughts**:

The day started well. I started the next freeCodeCamp project which is to build
a local weather app.  I used the [OpenWeatherMap](http://openweathermap.org) API
for the data.  Instead of navigator.geolocation I used the [ipinfo.io](http://ipinfo.io) API to get the users location.  It seems less flakey that way.  There was a requirement to use icons to display the current weather type for
which I used [Erik Flowers' weather icon font](http://erikflowers.github.io/weather-icons).  And I also had to have a button that toggles between ~~normal~~ Fahrenheit and ~~foreign~~ celsius which was easy.

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
