# 100 Days Of Code - Log

## Day 5: March 27, 2017

**Today's Progress**: Did the FreeCodeCamp jQuery exercises; Learned about grunt; Continued work on Portfolio.

**Thoughts**:

I did the FreeCodeCamp jQuery exercises.  All stuff I knew already so that
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

**Today's Progress**: Did the FreeCodeCamp Bootstrap exercises; Started work on Portfolio.

**Thoughts**:

Bootstrap is a godsend to artistically challenged people like myself.  I did
FreeCodeCamps bootstrap exercises to refresh my memory of how it works.  It
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

**Today's Progress**: Did the FreeCodeCamp HTML5 and CSS exercises;  Built a tribute page; Helped a Freecodecamper learn C.

**Thoughts**:

I started with the javascript algorithm stuff first because I thought that
would be more interesting and challenging and because, if you remember, I had
started and dropped FreeCodeCamp once before and I thought that I remembered
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

**Today's Progress**: Finished the rest of the Basic Algorithm Scripting Challenges from FreeCodeCamp; learned about git.

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

* [Challenge 6: Return Largest Numbers in Arrays](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms06.js)
* [Challenge 7: Confirm the Ending](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms07.js)
* [Challenge 8: Repeat a string repeat a string](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms08.js)
* [Challenge 9: Truncate a string](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms09.js)
* [Challenge 10: Chunky Monkey](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms10.js)
* [Challenge 11: Slasher Flick](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms11.js)
* [Challenge 12: Mutations](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms12.js)
* [Challenge 13: Falsy Bouncer](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms13.js)
* [Challenge 14: Seek and Destroy](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms14.js)
* [Challenge 15: Where do I belong](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms15.js)
* [Challenge 16: Caesars Cipher](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms16.js)

## Day 1: March 23, 2017

**Today's Progress**: First 5 Basic Algorithm Scripting Challenges from FreeCodeCamp

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

* [Challenge 1: Reverse a String](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms01.js)
* [Challenge 2: Factorialize a Number](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms02.js)
* [Challenge 3: Check for Palindromes](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms03.js)
* [Challenge 4: Find the Longest Word in a String](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms04.js)
* [Challenge 5: Title Case a Sentence](https://github.com/jaldhar/FreeCodeCamp/blob/master/Basic%20Algorithm%20Challenges/algorithms05.js)

Note due to a git mishap the date on the files is March 24 but I did them on the 23rd I swear! :-)
