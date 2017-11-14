# 100 Days Of Code - Log

## Round 3, Day 12: November 12, 2017

**Today's Progress**: Editor

**Thoughts**:

I've added methods to buffer to search backwards and forwards.  Using that,
I added methods in Subeditor (and bindings in Evaluate) to go to the beginning
of a line, end of a line, up a line or down a line.  However, the editor remains
resolutely single-line for now so you can't actually move up or down.

Oh and it looks like go to the beginning of a line is causing a segfault.
Back to the drawing board! :(

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)


## Round 3, Day 11: November 11, 2017

**Today's Progress**: Editor

**Thoughts**:

Now that my const iterators work properly, it is easy to add support for reverse
iterators too.  I'm going to need this for e.g. moving up a line.  I would
have to find the last newline and go past that.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)


## Round 3, Day 10: November 10, 2017

**Today's Progress**: Editor

**Thoughts**:

I solved my problem from yesterday by completely redoing the implementation
of BufferIterator.  Articles by Pete Goodliffe in the ACCU journal Overload ([part 1](https://accu.org/index.php/journals/389) and [part 2](https://accu.org/index.php/journals/383))
were very helpful in improving my understanding of how this is all actually supposed to work.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)


## Round 3, Day 9: November 9, 2017

**Today's Progress**: Editor

**Thoughts**:

So with full-screen multiline support on the way I thought I would implement
operations such as move to the beginning of the line, end of the line, top of
the text, end of the text and so on.  It seemed pretty straightforward then
all hell broke lose.  The problem it turns out is that I have implemented const
iterators incorrectly but thats' not what the compiler told me.  Instead it
spewed out hundreds of lines of gibberish.  Is it really necessary to give a
full expansion of each template every time?  Can we have the option to turn
off the notes which suggest every single class in the STL could be a candidate
for the right definition but never is?  I supposes it is a better policy to give
too much information rather than risk not giving enough but it makes things
really difficult especially if, like me,  you are not a C++ expert. A bit of
googling suggests that g++ doesn't have an option to control this.  It really
should.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)


## Round 3, Day 8: November 8, 2017

**Today's Progress**: Editor

**Thoughts**:

So adding multiline support to the editor is proving to be a _little_ bit harder
than I made out yesterday but it is almost there.  It's on a local branch for
now not uploaded to github.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)


## Round 3, Day 7: November 7, 2017

**Today's Progress**: Editor; Calculator

**Thoughts**:

I fixed the problem in the calculator and in the process, simplified the code
a little bit.

On the editor front, I did most of the infrastructure to make it multiline. It
isn't yet because I don't handle newlines but that will be easy to do tomorrow.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)
* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)


## Round 3, Day 6: November 6, 2017

**Today's Progress**: Editor; Calculator

**Thoughts**:

Hooray! I got an answer on Stack Overflow which solves my operator+= problem.
And in hindsight it was so simple.  I made a few other changes notably move
support and I now consider the Buffer and BufferIterator classes complete. The
next step is to actually make the editor multiline and able to load and save
files.

The indefatigable Jens Grabner popped up again after three months with a report
of another bug in the calculator I made for the freeCodeCamp front-end certificate.
I am really grateful to him for the amount of effort he has put into QA'ing this.
Unfortunately it is going to require a bit more detective work to figure out
exactly where the problem lies. I made some minor cosmetic changes while I was
at it.

**Links to work:**

* [Editor](https://github.com/jaldhar/editor)
* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)


## Round 3, Day 5: November 5, 2017

**Today's Progress**: Editor

**Thoughts**:

The time drought continues.  The main work today was to rename the member variables
in BufferIterator to be more descriptive.  I gave in on operator+= and asked
on Stack Overflow how to fix it.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 3, Day 4: November 4, 2017

**Today's Progress**: Editor

**Thoughts**:

Another day with more distractions than time to code. I implemented all the
other recommendations from the code review.  I just have one annoyance remaining
in the buffer code namely the implementation of operator+= (which is the basis
for all the iterator arithmetic functions really.)  This seems like it could
be made simpler but I am just not getting how.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 3, Day 3: November 3, 2017

**Today's Progress**: Editor

**Thoughts**:

I didn't get a lot of time today but in the moments I did have, I made more
of the changes recommended in the code review and asked for clarification of
some of the others.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 3, Day 2: November 2, 2017

**Today's Progress**: Editor

**Thoughts**:

I decided to submit my Buffer class to [codereview.stackexchange.com](https://codereview.stackexchange.com/) and
I got some good feedback.  The good news is that it seems my code is basically sound.
But there are lots of C++ stylistic things I can improve.  I only comitted one
today; some of the others will require more study.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 3, Day 1: November 1, 2017

**Today's Progress**: Editor

**Thoughts**:

After taking one days' break (from logging, not coding.)  I'm back for round 3.

I took a step back from implementing new features in the editor to do some
refactoring.  Further departing from the Finseth book. I changed the names of
some of the methods in Subeditor to be more in line with what EMACS uses.
I also removed the BufferStart and BufferEnd methods.  They are useful for a
C interface not a C++ STL based one.  I also seperated out the code for the
Buffer and BufferIterator methods from their class definitions.  An annoying
defect in C++ is that all the code for a templated class effectively has to
go into the header file.  There is a kludgy workaround which is to put the methods
into another file and then include that in the header which is what I did but
I don't like it.

With all that out of the way I could get back to adding features.  The biggest
is that the Buffer will now resize if the gap gets filled up.  If your terminal
supports it, it will beep if an error occurs such as trying to move past the
end of the buffer.  And in Evaluate there is support for giving subeditor commands
arguments (so you can do things such as move left 5 characters.)  This is not
fully implemented yet. 

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 100: October 30, 2017

**Today's Progress**: Round two finished! Editor

**Thoughts**:

Looking back on the last 100 days I feel I have started a bunch of things and
not completed them.  So the focus of round three (there will be a round three!)
will be to complete them.  Namely, the roguelike game, Perdu, the interpreter,
learning React, and learning Perl6, Swift, and Kotlin.  I also want to build
some Android apps but this will be my "day job" and may or may not be part
of my 100 days of code challenge.

As for the editor, todays progress was in making the Buffer expandable. This is
the crucial step before the editor can be used for anything longer than one line.

I still need a name for it.


**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 99: October 29, 2017

**Today's Progress**: Editor

**Thoughts**:

Hooray! I fixed the bug.  After last nights log entry I went to sleep and I
had a dream about it.  The next morning I implemented the idea I had dreamed of
and lo and behold it worked!  The solution seems a bit hacky to me so perhaps
dreams are not the next software engineering breakthrough. :-)

I also implemented a few more methods and changed the signatures of some others
to make the Buffer class a proper STL container.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 98: October 28, 2017

**Today's Progress**: Editor

**Thoughts**:

Did next to nothing today except change the signature of Buffers constructor
to perhaps solve the delete first character display bug.  Didn't work and
had to revert it.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 97: October 27, 2017

**Today's Progress**: Editor

**Thoughts**:

The problem with Ctrl-d turned out to be something obvious in hindsight.  The
Curses getch() function which gets a character from the keyboard returns an int.
I was casting that to a char because I am only dealing with ASCII characters so
who needs a whole int right? Turns out if you want to properly distinguish
between control keys and extended keys such as delete or left-arrow, you do need
the whole int.  Changing char to int had to be done in a number of places. I
should abstract that into a typedef in the event I  ever need to do it again,

Also did more cleanup work in bounds checking etc.  This has revealed a new
problem.  I can now sucessfully delete a character at the beginning of the 
buffer (It didn't work before.) but the display shows the old character and
deletes the one next to it.  I know what the problem is I think but fixing it
might be rather difficult.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 96: October 26, 2017

**Today's Progress**: Editor

**Thoughts**:

Very productive day today with a lot of free time in between the usual real-life
activities.  I implemented backspace and delete.  One minor annoyance is that
I wanted delete to be bound to the Ctrl-d key as well as the DEL key.  But somehow
Ctrl-d is being "eaten" by something&mdash;the console, shell or I dont know what&mdash;and is
not getting through to my program.  I don't understand why.  I also made more
changes to the API of the Buffer and BufferIterator classes.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 95: October 25, 2017

**Today's Progress**: Editor

**Thoughts**:

I added back all the operators I took out on day 90 and added some missing ones.
So BufferIterator is a fully functional RandomAccessIterator again. I am not
really using that functionality right now but I will need it later on.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 94: October 24, 2017

**Today's Progress**: Editor

**Thoughts**:

One remaining annoyance is that if the point goes beyond the beginning or the
end of the buffer, the program freezes.  (It refuses to take further input.)
Today I finally debugged and fixed this.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 93: October 23, 2017

**Today's Progress**: Editor

**Thoughts**:

HOORAY! Incrementing and therefore insert finally work the way they should.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 92: October 22, 2017

**Today's Progress**: Editor

**Thoughts**:

I realized I do not need a count member in the Buffer class as that can be
calculated on the fly as needed.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 91: October 21, 2017

**Today's Progress**: Editor

**Thoughts**:

It was the use of std::distance() that was messing things up.  When I changed
the gap and user coordinate conversion methods to just subtract
gapEnd - gapStart a lot of bugs went away.  But not all.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 90: October 20, 2017

**Today's Progress**: Editor

**Thoughts**:

All this operator nonsense is too complicated so I'm ditching it for now. I'm
only keeping enough bits to make BufferIterator a ForwardIterator.  Hopefully
that will make it easier to debug.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 89: October 19, 2017

**Today's Progress**: Editor

**Thoughts**:

The point ironically does not need to be a pointer; it is just an offset into
the buffer so it can be an integral type. (size_t.)

It's still not working unfortunately.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 88: October 18, 2017

**Today's Progress**: Editor

**Thoughts**:

Things are going to be slow for the next few days because of Diwali and the
Gujarati New Year.

I did some messing around with the operators in BufferIterator which didn't
really seem to help.  It seems a conceptual mistake I've made is treating
the point and gap start and end as BufferIterators when they should just be
iterators to the underlying container or even just pointers.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 87: October 17, 2017

**Today's Progress**: Editor

**Thoughts**:

I thoroughly reviewed all the operators and I think I now have them set up the
way they are supposed to be.  Also I changed back all the internal iterators
(point, gap start and end) in the Buffer back to plain pointers.  This prevents
the kind of circular references that were causing my segfault before.

Maddeningly, the program still doesn't work properly.  Is it because I'm using
std::copy with pointers instead of iterators?  I hope to find out tomorrow.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 86: October 16, 2017

**Today's Progress**: Editor

**Thoughts**:

No it turns out it is operator== in the Buffer class.  It in turn calls the
BufferIterators operator== but BufferIterator as it is currently designed holds
a reference to the buffer.  So I end upwith a segfault.  Now to figure out how
to get around this...

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 85: October 15, 2017

**Today's Progress**: Editor

**Thoughts**:

I've narrowed down the problem to operator- and operator+ (and their related
operations such as ++, --, +=, and -=) haven't been implemented correctly. But
I have not, despite a lot of reading, understood how to do that.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 84: October 14, 2017

**Today's Progress**: Editor

**Thoughts**:

Didn't get much free time today.  I readded debug information to the editor
display and made an attempt to figure out what is going wrong but no luck yet.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 83: October 13, 2017

**Today's Progress**: Editor

**Thoughts**:

The great redesign is done.  C++ templates are as awkward to deal with as ever.
(And woe beside you get something wrong because the compiler will spew out a
couple of pages of totally useless and incomprehensible garbage in lieu of a
proper error message.)  The operator and iterator stuff was also not very
well documented in my opinion.  I have probably got things wrong there.

And sure enough, while the program compiles without errors, it segfaults whenever
you try and insert a character.  I can't immediately tell why.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 82: October 12, 2017

**Today's Progress**: Editor

**Thoughts**:

I have decided to mostly abandon the API from the Finseth book.  It was designed
for C and I want to try and make my editor use as many modern C++ idioms as
possible.  For example I have a custom iterator and overload several operators.
But this requires a lot of boilerplate and I still have some left to go.

So I am not checking my current work into Github today.  Hopefully it will be
done by tomorrow.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 81: October 11, 2017

**Today's Progress**: Editor

**Thoughts**:

I moved all the buffer stuff into its own class.  Well most of it.  Wrestling
with C++ took up some time so there are still a few more methods that need
to be moved.  I'll also have to partially redo the Redisplay class to deal
with the changed API.  Still I think I accomplished quite a bit today.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 80: October 10, 2017

**Today's Progress**: Editor

**Thoughts**:

I missed a day due to a lot of demands on my time in real life.  Today I 
implemented the gap part of the buffer-gap algorithm.  It still needs work
though because it causes the editor to lock up if you try and edit in the
middle of the buffer.  I haven't done the refactoring I mentioned in the last
entry and I am regretting it.  There are subtle errors in this code I need to
track down.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 79: October 8, 2017

**Today's Progress**: Editor

**Thoughts**:

Now you can move backwards and forwards in the edit buffer.  This is not the
full buffer-gap algorithm though.  I am going to refactor my current code to
better use advanced C++ features so there is no point in comitting it publically
right now.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 78: October 7, 2017

**Today's Progress**: Editor

**Thoughts**:

I did an implementation of the buffer-gap algorithm from the Finseth book but
I haven't committed it yet because I have a sneaking suspicion there is a memory
leak.

There are also two minor improvements.  One, I read an interesting article about
[portable Makefiles](http://nullprogram.com/blog/2017/08/20/) and made a few minor changes in mine.
Second, the cursor now follows the point which looks better aesthetically.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 77: October 6, 2017

**Today's Progress**: Editor

**Thoughts**:

My editor is finally able to edit.  Well insert characters not quite edit them.
I've been reading about the buffer-gap algorithm and I think I finally get it
but I'll wait until tomorrow to implement it.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 76: October 5, 2017

**Today's Progress**: Editor

**Thoughts**:

More scaffolding work on the editor.  Today I set up a class that evaluates
commands and dispatches them to the part of the editor that actually stores
and manipulates text.  Which it doesn't yet.  However you can now quit from the
editor by pressing q instead of having to break out with ctrl-c.

**Links to work:**

[Editor](https://github.com/jaldhar/editor)


## Round 2, Day 75: October 4, 2017

**Today's Progress**: Editor

**Thoughts**:

I started writing a text editor.  It is written in standard C++14 with ncurses
so it should be fairly portable though it is only tested on Linux for now.  It
turns out I own a copy of Craig Finseths book about text editors which was mentioned
on Hacker News.  There is also an online version available [here](http://www.finseth.com/craft/).  I've used it
as a basis for designing my editor.  Today I did the view and input framework.
Tomorrow I'll do the actual editting bits.


**Links to work:**

[Editor](https://github.com/jaldhar/editor)

## Round 2, Day 74: October 3, 2017

**Today's Progress**: Giving up on Hackintosh; Editor

**Thoughts**:

I spent reinstalling the Hackintosh and all the apps, my backed up files etc. and
by the end I didn't have the energy to continue with swift.  Reading some articles on 
[Hacker News](https://news.ycombinator.com/) about editor data structures got
me interested in the topic.  Perhaps I shall have a go at writing one of my own.

**Links to work:**


## Round 2, Day 73: October 2, 2017

**Today's Progress**: Hackintosh disaster continues

**Thoughts**:

The Mac OS X recovery is useless.  It keeps insisting the disk cannot be repaired
though I can mount it and see that all the files are there.  Atleast  I found
out how to boot into single user mode and run fsck (Thank God there is Unix underneath.)  Even this is resolving the problem as for some reason the
disk is considered "write locked" and I don't know how to unlock it.

If worst comes to worst I will have to wipe and reinstall the whole thing.  I have belatedly made a backup of all my personal files so I won't quite be
back to square one but It will still be a collossal pain and waste of time though.


**Links to work:**


## Round 2, Day 72: October 1, 2017

**Today's Progress**: Hackintosh disaster!

**Thoughts**:

I've not being having good luck lately.  Today as I was working I must have
accidently kicked out my laptops power cord.  This model doesn't beep when the
battery is low like my old laptop.  (Or if it does, I haven't figured out how.)
So I was merrily working away on my swift when the power gave out and the 
laptop suddenly went dead.  I put the power cord back in and a long but uneventful
fsck later, I was back in Linux.  Unfortunately it seems VMWare does not react
well to being ungracefully shut down.  When Mac OS X restarts, it finds that
the virtual disk drive is corrupt and tries and fails to fix it.  The loss of 
some work is bad enough but if I can't get this working again I'm sunk as I don't
have access to a real mac.

**Links to work:**


## Round 2, Day 71: September 30, 2017

**Today's Progress**: Swift

**Thoughts**:

Built another real app today albeit a very simple one. I think they went a little
too fast with this lab.  Not a big deal for me but I can imagine programming
newbies getting lost.  Spllitting it into two labs would help in my opinion.

**Links to work:**

* [Simpn Says](https://github.com/jaldhar/swift-outlets-lab-swift-intro-000)

## Round 2, Day 70: September 29, 2017

**Today's Progress**: Swift

**Thoughts**:

Now we're getting to the good stuff.  Today I learned about using XCodes Interface
Builder.  It was a little hard to grasp at first but compared to Android Studio,
it is superior in my opinion.

**Links to work:**

* [Interface Builder: Basics](https://github.com/jaldhar/swift-interfaceBuilder-lab-swift-intro-000)
* [Roll the Dice](https://github.com/jaldhar/swift-viewLifeCycle-lab-swift-intro-000)

## Round 2, Day 69: September 28, 2017

**Today's Progress**: Swift

**Thoughts**:

I was very busy with real life today but I got some swift practice in.  There is no github commit though.

**Links to work:**


## Round 2, Day 68: September 27, 2017

**Today's Progress**: Swift

**Thoughts**:

Very productive day today. I learned how to use XCode though not for an actual app yet.

**Links to work:**

* [Math, Booleans, and Conditionals](https://github.com/jaldhar/swift-conditionals-lab-swift-intro-000)
* [Math, Booleans, and Operators](https://github.com/jaldhar/swift-mathBoolOp-lab-swift-intro-000)
* [Switches](https://github.com/jaldhar/swift-switchLab-lab-swift-intro-000)
* [Fun with Basics!](https://github.com/jaldhar/swift-switchLab-lab-swift-intro-000)

## Round 2, Day 67: September 26, 2017

**Today's Progress**: Swift

**Thoughts**:

One more lab about functions. I think I've beaten this topic into the ground now.

**Links to work:**

* [All About Functions](https://github.com/jaldhar/swift-allAboutFunctions-lab-swift-intro-000)


## Round 2, Day 66: September 25, 2017

**Today's Progress**: Swift

**Thoughts**:

More swift today.  The main feature of functions in Swift that feels novel is that
parameters have to be named.  The extra typing is a little annoying but overall
I think I like the idea.  It makes the code a little more self-documenting.

**Links to work:**

* [Functions with Multiple Arguments](https://github.com/jaldhar/swift-functionLab-lab-swift-intro-000)
* [Functions](https://github.com/jaldhar/swift-funcMultipleArg-lab-swift-intro-000)


## Round 2, Day 65: September 24, 2017

**Today's Progress**: Swift

**Thoughts**:

I've been out of action for a week due to a painful hand injury which left me
unable to type.  I'm slowly ramping up again.  I still intend to finish Perdu
but for the moment I'm taking a break and concentrating on the Swift course
from Flatiron School for now.

**Links to work:**

* [Variables](https://github.com/jaldhar/swift-firstTask-playground-swift-intro-000)


## Round 2, Day 64: September 18, 2017

**Today's Progress**: Perdu cleanup

**Thoughts**:

One of the reasons why the JS13K version of Perdu was so unplayable was
because the Chickens moved too fast compared to the player.  It should be more
manageable now in my local branch.  Still not uploaded to github though.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 63: September 17, 2017

**Today's Progress**: Perdu cleanup; Swift

**Thoughts**:

Internet is back, whew.  The refactoring of the model, controller  and a basic
2d view is essentially complete (but still not on github.)  I have to shake
out a few bugs and then make the raycasting work again.

If you have been following me on twitter you may have seen that I am also doing
the #BackToCode, 21 day challenge from a bootcamp called [FlatIron School](https://flatironschool.com).
They have a free course on Swift which I was going to rush through this weekend.
Unfortunately my "Hackintosh" (Mac OS X Sierra running in a VMWare VM under Linux) stopped working.  By the time I had fixed it and upgraded everything
I only had time to do a few of the lessons. I'm going to try and spend some time
on this over the next few days.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 62: September 16, 2017

**Today's Progress**: Perdu cleanup

**Thoughts**:

I got a lot further in refactoring today (probably because I lost Internet access
at home.) though it is on a local branch and not uploaded to github yet.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 61: September 15, 2017

**Today's Progress**: Perdu cleanup

**Thoughts**:

Today I began refactoring the code using my tried and tested MVC layout.  Didn't
get very far though because of a lack of time.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 60: September 14, 2017

**Today's Progress**: Perdu cleanup

**Thoughts**:

I implemented a minimap so I could see how movement is taking place.  One problem
that immediately springs to mind is that most times you will have a chicken
right next to you on the first turn which spells instant death.  I will 
either have to redo placement so the player starts of in a safe zone or do as
in the [hivolts](https://github.com/jaldhar/hivolts) game I based this off of
and implement a "teleport" command.


**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 59: September 13, 2017

**Today's Progress**: Perdu: cleanup begins.

**Thoughts**:

Didn't do much as I am still decompressing after last nights marathon. I took
a look at the Perdu code and identified two major areas of concern.  First
the ray casting of chickens doesn't work right.  Sometimes they merge with the
walls and there is no sense of distance.  Secondly, it is far too easy to die.
This suggests to me that collision detection is still not correct.  And overall,
the code is a mess.  These are things to look at starting tomorrow.
 
**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 58: September 12, 2017

**Today's Progress**: Perdu: complete!

**Thoughts**:

As usually happens in these situations something came up at the last minute so
I was not able to have the free time I had hoped for.  So I ended up pulling an
all-nighter and finally with barely half an hour left before the deadline, I
made it!  Perdu is not going to be on anyones top 10 lists I guarantee you but
it is playable.  I am exhausted right now but I'll do a post-mortem soon.
 
**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 57: September 11, 2017

**Today's Progress**: Perdu.

**Thoughts**:

Really biting my nails wondering if I can get everything finished in time.  The
latest obstacle is collision detection.  Sometimes the player goes right through a chicken.
Happily it looks like I will be able to dedicate a lot more time to this tomorrow and if I can
solve this I should be in a decent position to submit.
 
**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 56: September 10, 2017

**Today's Progress**: Perdu.

**Thoughts**:

It's not committed to git yet but I did a lot of work on gameplay.  My initial
idea of a roguelike is too ambitious.  Instead the game is going to be something
like [Robots](https://en.wikipedia.org/wiki/Robots_(computer_game)) I had actually
written a [similar game](https://github.com/jaldhar/hivolts) before albeit in C++ so I can atleast use that as a model.
 
**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 55: September 9, 2017

**Today's Progress**: Perdu.

**Thoughts**:

Found an excellent [SVG optimizer](http://petercollingridge.appspot.com/svg-optimiser) It reduces file sizes by upto 60%.
This means I can keep my nicer looking graphics and still have room for the
actual game code.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 54: September 8, 2017

**Today's Progress**: Perdu.

**Thoughts**:

I am wasting way too much time trying to make good looking graphics that will
fit into 13k.  I'll give it one more day then settle for whatever I have because
I need to work on the gameplay and I'm running out of time.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 53: September 7, 2017

**Today's Progress**: Perdu.

**Thoughts**:

I finally got it working!  What I did was to use [a converter](http://professorcloud.com/svg-to-canvas/) to turn
the SVG file into a function made up of equivalent canvas operations.  Then I
created a canvas used the function to draw the image on it and used canvas.toDataUrl('image/png') to convert it into a PNG.  Possibly this is an
overly convoluted way of doing things and the converter didn't do a perfect job
of reproducing the SVG but it works and that's the main thing.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 52: September 6, 2017

**Today's Progress**: Perdu.

**Thoughts**:

Still haven't got SVG's working properly.  I try and load e.g. the wall texture
inline via a data URI but the slicing and dicing the raycasting code does makes
it look horrible.  If I replace it with a bitmap format such as .gif it looks
much better but then the size is too big.  It must be possible to load an SVG
and convert it to a bitmap on the fly but I've yet to figure out how.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 51: September 5, 2017

**Today's Progress**: Perdu.

**Thoughts**:

For the first time, the game is actually under 13k.  I did this by replacing
the default graphics I got from the raycaster tutorial with simple GIFs.  It
doesn't look very good but that's going to be the next step.  One obvious solution
is to use SVGs and I tried it but it looked weird for some reason so I backed
out for now.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 50: September 4, 2017

**Today's Progress**: Perdu.

**Thoughts**:

More vaccilating back and forth with frameworks.  Now I've decided to do without
one altogether.  Times running out I really need to work on the actual game 
instead of messing about like this.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 49: September 3, 2017

**Today's Progress**: Perdu.

**Thoughts**:

Spent my time playing with micro frameowrks for games.  I even wrote one (not
very good) of my own.  All I really need is a game loop and canvas/image
manipulation.  I've settled on [Rat.js](https://github.com/keyten/Rat.js) we'll
see how that goes.  One thing is for sure, I'm in over my head with all this
but it's fun to learn about.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 48: September 2, 2017

**Today's Progress**: Perdu.

**Thoughts**:

Converting my maze generation code from C++ ran into a couple of snags but I 
think I have them worked out now.  I still need to add the code into Perdu.

I've gone back and forth a couple of times on using ga.  Now once again I've
thinking about ditching it.  I've found a couple of other small frameworks and
I'll try them tomorrow.

In the process of porting to JavaScript I noticed some bad code in my C++
version.  I was creating an essentially unchanging vector within a loop.  By
taking it outside, it is probably much faster though as it happens, the test
program is very fast and simple so it doesn't make any real world difference.
In a browser it probably will though.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)
* [Maze generation algorithm demo](https://github.com/jaldhar/Maze)


## Round 2, Day 47: September 1, 2017

**Today's Progress**: Maze generation

**Thoughts**:

Back to Perdu.  I want the map to be a maze so I implemented an algorithm to
generate a random maze.  The code is in C++ because that's easier for me to
understand so tomorrow I will convert it to JavaScript and integrate it.

**Links to work:**

* [Maze generation algorithm demo](https://github.com/jaldhar/Maze)


## Round 2, Day 46: August 31, 2017

**Today's Progress**: freeCodeCamp beta Product Landing Page

**Thoughts**:

It turns out it only took one line of CSS to get it working properly on chrome.
(If you specify the height for a child element, you need to specify it for the
parent also.)
 
Still haven't gone back to the game.  Hopefully the Labor Day long weekend will
give me some more free time.

**Links to work:**

* [Product Landing Page](http://www.braincells.com/webdev/landing-page/)


## Round 2, Day 45: August 30, 2017

**Today's Progress**: freeCodeCamp beta Product Landing Page

**Thoughts**:

The status now is that the landing page looks good in firefox but not in chrome,
either the desktop Linux version or on my Android phone.  I had no idea that
making your own framework would be this difficult.  Luckily I do feel I know
where things might be going wrong so one more day should crack it.

I've got to get back to my game if I ever hope to finish it.

**Links to work:**

* [Product Landing Page](http://www.braincells.com/webdev/landing-page/)


## Round 2, Day 44: August 29, 2017

**Today's Progress**: freeCodeCamp beta Product Landing Page

**Thoughts**:

I wanted to work on the game today but I wasted so much time fiddling with CSS
I ran out of time.  The page is looking better now but I'm still having difficulty
getting flexbox to behave the way I want it too in some places.

It really makes you appreciate a framework like bootstrap.

**Links to work:**

* [Product Landing Page](http://www.braincells.com/webdev/landing-page/)


## Round 2, Day 43: August 28, 2017

**Today's Progress**: freeCodeCamp beta Product Landing Page

**Thoughts**:

Due to time constraints the great comeback hasn't quite happened yet.  I did
do the Product Landing Page project and got all the tests passing but it looks
pretty ugly at the moment.  I'm trying to make my own responsive flexbox based
grid framework rather than rely on something like e.g bootstrap.  I hope to be
finished by tomorrow and get back to Perdu.

**Links to work:**

* [Product Landing Page](http://www.braincells.com/webdev/landing-page/)


## Round 2, Day 42: August 27, 2017

**Today's Progress**:

**Thoughts**:

The library is closed today but the good news is my laptop is back from the
repair depot.  (I am impressed by the quick turn around time.)  Apparently it
came yesterday while I was out and my downstairs neighbor signed for it but
forgot to tell me.

Everything works as it should.  However I wasn't able to get anything done on
it as restoring the backup is agonizingly slow.

One of the reasons I started this challenge is because I know I have a
character flaw of quickly losing motivation to complete a  task if I suffer
any kind of setback.  I had hoped by now, almost half way through the second
round, I would have cured myself of this tendency but after the laptop
incident, here I am with energy and interest flagging.  Tomorrow, if nothing
else, I will aim for an easy win to get me moving once again.

**Links to work:**


## Round 2, Day 41: August 26, 2017

**Today's Progress**: freeCodeCamp beta Technical Documentation Page; Perdu (sort of)

**Thoughts**:

In between shopping and other errands I was able to spend some time at the
library today.  This last failing test in the Technical Documentation Page
project has really got me stumped.  It checks to see if you have fullfilled the
requirement to have "sticky" navigation i.e. which doesn't scroll when the rest
of the page does.  The problem is I'm using flexbox and the only way I know
to make this effect in CSS is to use position: fixed which breaks the flex
layout.  I'm going to have to ask for help with this one.

I haven't forgotten about Perdu.  I've been reading about maze generation but
I haven't integrated it into the game just yet.

**Links to work:**

* [Technical Documentation Page](http://www.braincells.com/webdev/tech-doc/)


## Round 2, Day 40: August 25, 2017

**Today's Progress**: freeCodeCamp beta Technical Documentation Page; Quicksort in C.

**Thoughts**:

Hooray for my local public library!  They have wifi and computers you can use.
The storage gets wiped after every session but that's ok because I want to use
a Debian GNU/Linux live CD and save my work to a USB key anway.  I explained
this to the librarians and after I assured them I was not some nefarious hacker
type they allowed it.  It's a little bit slow but I have git and all the
command line tools I'm used to. The only downside is that most days if I rush
over after work I'll barely get one hour before they close.

Today (Friday) however, they are open later so I used my time to complete the
freeCodeCamp beta Technical Documentation project.  I chose to document the
quicksort algorithm and in the process I wrote a version of the standard C
Library qsort(3) function.

All the tests now pass except one but I'll look at that the next time I can
go to the library.

**Links to work:**

* [Technical Documentation Page](http://www.braincells.com/webdev/tech-doc/)


## Round 2, Day 39: August 24, 2017

**Today's Progress**: freeCodeCamp beta Survey Form

**Thoughts**:

I connected the laptop up to an external monitor and did a little bit of work
on polishing the mostly complete Survey Form project before sending the machine
off for repair.  (Luckily it is still under warranty.)

Work have given me a loaner laptop but I do not want to do any of my personal
stuff on it.

I tried to see if I could use an iPad with a terminal app to connect to my
server to see if I could code directly on there but I'm finding it very awkward
and really not worth the time and effort.  I'll have to stick to reading for
now.


**Links to work:**

* [Survey Form](http://www.braincells.com/webdev/survey-form/)


## Round 2, Day 38: August 23, 2017

**Today's Progress**:

**Thoughts**:

Disaster!  I was walking home from work and my backpack must have been open because
I heard a clatter and saw that my laptop had fallen out.  The screen had cracked
but it did turn on so I hastily put it back in the bag and went home.  That's
when I found out the wifi was not working either.  That pretty much dispirited
me from doing anything further so instead I spent my time backing everything
up to an external USB hard drive.

**Links to work:**


## Round 2, Day 37: August 22, 2017

**Today's Progress**: Perdu

**Thoughts**:

Didn't get a lot of time today.  I did more work to integrate ga and perdu.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 36: August 21, 2017

**Today's Progress**: Perdu; freecodecamp beta

**Thoughts**:

Today was the day of the solar eclipse and the last day of the month of Shravana
so I took the day off to concentrate on religious activities which happily also
left some time for me to work on my code during the day time.  I went through
nearly all the exercises in the new FreeCodeCamp Responsive Web Design certificate and looked over the projects.  Two I've already done, the tribute page
and the portfolio.  Both only needed minor tweeks to pass the new test suite.
I will have to do three more, a survey, product landing page, and a technical 
documentation page.  I started all three of these but didn't completely 
finish any.  This is a bad habit of mine.  There isn't a lot left to do so I should
be done tomorrow but I need to learn how to get things done.

In Perdu I reintegrated the ga framework.  Now I have to go through the code
line by line and replace it with functions from ga.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 35: August 20, 2017

**Today's Progress**: Perdu

**Thoughts**:

I have decided that I've wasted too much time trying to OOPize the raycaster.
So I ripped it all out and reimported the original prototype-based code.  Bar
a few quickly fixed typos, it all works fine.  Now I can begin the real task
of adapting it for my game.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 34: August 19, 2017

**Today's Progress**: Perdu; freeCodeCamp Beta

**Thoughts**:

I made a little more headway in solving the recursion problem but no solution yet.
So I got depressed and gave up for the night.

Instead I looked at the new testing framework for projects in the freeCodeCamp
beta which is going to go live soon.

Mostly make the tests pass for my existing projects simply involved adding or
changing ids so the test suite could recognize things.  For the calculator, I
actually had to implement some features which was fairly easy to do and ended
my session with a win which makes me feel good.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)
* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)


## Round 2, Day 33: August 18, 2017

**Today's Progress**: Perdu

**Thoughts**:

I was wrong it turns out the real problem is that somehow when I downloaded the
images, they got corrupted.  Now they are fine and rendering mostly works correctly
except for columns.  The function that is supposed to draw them is complaining
it is being called too many times recursively.  So that's the problem I need to
investigate tomorrow.

It's been interesting but at this rate it look I'm never going to finish the
actual game. :-(

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 32: August 17, 2017

**Today's Progress**: Perdu

**Thoughts**:

I've discovered what the problem in rendering is.  For some reason it is not finding the images. Unfortunately I
haven't yet figured out how to fix this and I've run out of time for today.  So I'll try again tomorrow.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 31: August 16, 2017

**Today's Progress**: Perdu

**Thoughts**:

I've decided to strip out ga for now and focus on getting the raycaster to run
properly.  So I ported the few remaining bits from the original source.
Instead of just cutting and pasting the code I've tried to structure it my own
OOPish way.  This made it easy to decouple from ga but unfortunately along the
way I've made some mistakes which are causing errors so for now I have disabled
rendering until I can debug it.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 30: August 15, 2017

**Today's Progress**: Perdu

**Thoughts**:

Work continues on Perdu.  Today I ported most of the rest of that raycaster to ga.
However it is not displaying properly.  I think this has something to do with
how it hooks into the ga game loop but I need to look into it further.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 29: August 14, 2017

**Today's Progress**: Perdu

**Thoughts**:

I spent some time playing with the [ga framework](https://github.com/kittykatattack/ga) It seems very powerful in an
extremely tiny package and the documentation is excellent.  I also found code
for a [tiny raycaster](http://www.playfuljs.com/a-first-person-engine-in-265-lines/) Together, these should be enough to power my game graphically.

At the moment however all I have to show is a white rectangle.  Never fear it's
going to look much better over the coming days.

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 28: August 13, 2017

**Today's Progress**: JS13KGame: Perdu

**Thoughts**:

The great beginning of my JS13KGames entry turned out to be anticlimatic.  The
sudden illness of a close relative meant I spent most of the day in a hospital
room with no wifi.  I have however set up a basic project structure on Github and
thought about what my game is going to be like.  (See the README.)

**Links to work:**

* [Perdu](https://github.com/jaldhar/perdu)


## Round 2, Day 27: August 12, 2017

**Today's Progress**: More Preparation for JS13KGames; Perl6

**Thoughts**:

Very little time today so I mostly spent it on reading about game architecture
and algorithms.  Unfortunately most of what you can find on the web is not in
JavaScript but hopefully the concepts will transfer well.

I did one more Think Perl6 exercise to keep the commit streak going.

**Links to work:**

* [Think Perl6 Exercise 10.2](https://github.com/jaldhar/perl6-scripts/blob/master/ackermann2.p6)


## Round 2, Day 26: August 11, 2017

**Today's Progress**: Preparation for JS13KGames; Perl6

**Thoughts**:

I spent some time looking through the various tools available online for building
very small javascript games. I also looked at some of the previous entries
which are really impressive.  I will consider myself lucky if I can finish this
challenge.  I certainly can't hope to win.

I did another Think Perl6 exercise from chapter 10.

**Links to work:**

* [Think Perl6 Exercise 10.3](https://github.com/jaldhar/perl6-scripts/blob/master/hasduplicates2.p6)


## Round 2, Day 25: August 10, 2017

**Today's Progress**: Refactoring freeCodeCamp Calculator and Twitch API; Perl6

**Thoughts**:

I gave the Calculator and Twitch API projects the once over to use the module
pattern and in the case of the latter, promises. Twitch API doesn't use jQuery,
so I had to do a bit more work to get the promises working right and I feel
I might have broken it a bit on the way.  So I need to look at that carefully
tomorrow.

I did a little bit of Perl6 to keep my github streek going.  This time I skipped
ahead to chapter 10 which is about hashes.

The [JavaScript 13K game challenge](http://js13kgames.com/) is starting soon. I'm
going to try and take part.

**Links to work:**

* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)
* [Free Code Camp Twitch API Project](http://www.braincells.com/webdev/twitch-api/)
* [Think Perl6 Exercise 10.1](https://github.com/jaldhar/perl6-scripts/blob/master/hashsearch.p6)


## Round 2, Day 24: August 09, 2017

**Today's Progress**: freeCodeCamp Local Weather App (Again!)

**Thoughts**:

After reading [Todd Mottos' excellent article](https://toddmotto.com/mastering-the-module-pattern/) I realized
I've been doing the JavaScript module pattern wrong all this time.  So I went
back to the local weather app and fixed it, learning some lessons about
JavaScript scope along the way.

I also read [The Promise of a Burger Party](https://kosamari.com/notes/the-promise-of-a-burger-party) by Mariko Kosaka which is about JavaScript promises
which promise (haha) to be a better way to organize asynchronous code.  As the
weather app has two AJAX calls which have to complete in order, I looked into
adding promises here. But actually as I am using jQuery in this project it already
does everything for you behind the scenes so I didn't really have to change much.

**Links to work:**

* [Free Code Camp Weather App](http://www.braincells.com/webdev/local-weather/)


## Round 2, Day 23: August 08, 2017

**Today's Progress**: Perl6

**Thoughts**:

The idea was to refactor another web project today and I did get started on one
(the random quote machine) but I ended up spending most of my time on Perl6.
Exercise 9.10 involves implementing the binary search algorithm.  As practicing
algorithms is also one of my goals for the 100 days of code I was eager to see
if I knew this one.  Happily I do, but I took too long to get all the details
right in my opinion and that does not bode well for the more complex algorithms.

**Links to work:**

* [Think Perl6 Exercise 9.10](https://github.com/jaldhar/perl6-scripts/blob/master/binarysearch.p6)


## Round 2, Day 22: August 07, 2017

**Today's Progress**: Perl6

**Thoughts**:

Things are still crazy in real life so again, just a few Think Perl6 exercises.

**Links to work:**

* [Think Perl6 Exercise 9.5](https://github.com/jaldhar/perl6-scripts/blob/master/sorted.p6)
* [Think Perl6 Exercise 9.6](https://github.com/jaldhar/perl6-scripts/blob/master/anagrams.p6)
* [Think Perl6 Exercise 9.7](https://github.com/jaldhar/perl6-scripts/blob/master/hasduplicates.p6)
* [Think Perl6 Exercise 9.9](https://github.com/jaldhar/perl6-scripts/blob/master/buildwordsarray.p6)


## Round 2, Day 21: August 06, 2017

**Today's Progress**: Perl6

**Thoughts**:

Another day where I couldn't get a lot done so I just did some Perl6 exercises.
I've skipped ahead to chapter 9.


**Links to work:**

* [Think Perl6 Exercise 9.1](https://github.com/jaldhar/perl6-scripts/blob/master/nestedsums.p6)
* [Think Perl6 Exercise 9.2](https://github.com/jaldhar/perl6-scripts/blob/master/cumulsums.p6)
* [Think Perl6 Exercise 9.3](https://github.com/jaldhar/perl6-scripts/blob/master/middle.p6)
* [Think Perl6 Exercise 9.4](https://github.com/jaldhar/perl6-scripts/blob/master/chopit.p6)


## Round 2, Day 20: August 05, 2017

**Today's Progress**: FreeCodeCamp Twitch API Project

**Thoughts**:

With a lot of family stuff going on today I had little time for coding.  What
I did have, I spent on refactoring the Twitch API project.  Now I understand
the MVC design pattern thoroughly, it was a piece of cake.

It turns out one of my github commits from my last set is dated today so I didn't
have to bother doing anything else in order to maintain my one commit a day goal..

**Links to work:**

* [Free Code Camp Twitch API Project](http://www.braincells.com/webdev/twitch-api/)


## Round 2, Day 19: August 04, 2017

**Today's Progress**: FreeCodeCamp Calculator, Perl6 and Perl5

**Thoughts**:

Fixing the parentheses problem was not quite as simple as I made out yesterday
but still but not too difficult either.  What I do is start at the end of the
input string which is at that point a ')'.  I keep a counter initially set to 1.
Then I go backwards through the string and every time I see a ')' increment the
counter and every time I see a '(' decrement it.  I stop when the counter = 0
that's the character from where I want to start a substr() to eval().  If I
reach the start of the string and the counter still isn't 0, it means the
parentheses are unbalanced which is an error.  lastIndexOf() is no longer used
at all.

I also took the opportunity to improve the CSS so it actually looks more like
a calculator.  It's really slick now if I do say so myself.

I still haven't returned to Think Perl6.  Instead I ported a C++ program I had
done in Round 1 day 92.

I also briefly dealt with Perl 5. I had a written a module long ago which was
up on CPAN and I got a pull request on Github for it.  Just fixing a trivial
typo but it's nice to know there are people actually using my code.

**Links to work:**

* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)
* [Fold a string into a triangle (Perl6 version)](https://github.com/jaldhar/perl6-scripts/blob/master/string2triangle.p6)
* [CGI::Application::Plugin::REST](https://github.com/jaldhar/CGI-Application-Plugin-REST)

## Round 2, Day 18: August 03, 2017

**Today's Progress**: FreeCodeCamp Calculator and Perl6

**Thoughts**:

I was already to tell you how clever I am but then I noticed a bug. Let me explain.

I was not looking forward to implementing a stack to deal with intermediate
answers in parentheses.  Then I hit upon an idea.  Why not separate out the
string from the end paren to the preceding start paren and eval that then display
it?  It's simple to do with JavaScripts lastIndexOf() and substr() functions
and it works for a single level of parentheses i.e.:

```
  5 X ( 3 + 5 )
```

...but alas it fails for something like:


```
  5 X ( 3 + (10 - 5) )
```

I think I know how to fix this: count the total number of left parens, subtract
the current number of right parens and call lastIndexOf in a loop that many
times.  I'm too sleepy to trust myself to do it right at the moment so I will
try tomorrow.

For Perl6, I didn't do an exercise from the book per se.  I was idly wondering
how many words in the list the author has been using in this chapter are
palindromes.  A question I was able to answer with a mashup of Exercises 5.3 and
8.2.  (The answer is surprisingly few.  Only 91 or 0.08%.)


**Links to work:**

* [Free Code Camp Calculator App](http://www.braincells.com/webdev/calculator/)
* [List all palindromes in words.txt](https://github.com/jaldhar/perl6-scripts/blob/master/allpalindromes.p6)

## Round 2, Day 17: August 02, 2017

**Today's Progress**: FreeCodeCamp Calculator and Perl6

**Thoughts**:

The Calculator app is working again and looks more responsive. Now I can look
at the flaw reported by Jens which is that after an end parentheses, 0 is
displayed instead of the intermediate answer.  Fixing this might not be easy; I
may have painted myself into a corner because I don't actually do much parsing
accept at the simplest level e.g. do I have a number, operator etc.  JavaScripts'
eval() function does all the heavy lifting.  I think I will have to implement
some kind of stack.  That sounds like a big task so I am postponing it until
tomorrow.

I did one Think Perl6 exercise just to keep the momentum going.

**Links to work:**

* [Think Perl6 Exercise 8.3](https://github.com/jaldhar/perl6-scripts/blob/master/avoid.p6)

## Round 2, Day 16: August 01, 2017

**Today's Progress**: FreeCodeCamp Calculator and Perl6

**Thoughts**:

I have decided that I am going to try and have atleast one commit to github
every day this month.  Things didn't get off to a good start; It was 11:45pm and
I suddenly realized the refactoring of the Calculator app was all in pieces.
So I quickly did some of the chapter 8 exercises from Think Perl6. I hope to have
the calculator usable again tomorrow so I can fix that bug I mentioned on day 13.

**Links to work:**

* [Think Perl6 Exercise 8.1](https://github.com/jaldhar/perl6-scripts/blob/master/longerthan20.p6)
* [Think Perl6 Exercise 8.2](https://github.com/jaldhar/perl6-scripts/blob/master/hasnoe.p6)

## Round 2, Day 15: July 31, 2017

**Today's Progress**: FreeCodeCamp Local Weather App

**Thoughts**:

I did not have a lot of time today but I got the Local Weather App ship-shape
again and possibly looking better on mobile devices.  Or possibly worse.  It
looks good on chromium on android but not on safari on an ipad mini.  Maybe
it could be because caching issues from earlier tests.  I'll spend a little time
on it tomorrow but I really should be getting on with the calculator (and Perl6!)

**Links to work:**

* [Free Code Camp Weather App](http://www.braincells.com/webdev/local-weather/)

## Round 2, Day 14: July 30, 2017

**Today's Progress**: FreeCodeCamp Local Weather App

**Thoughts**:

I was going to start on the calculator today when I looked the weather app and
noticed that somewhere along the way, I had lost the ability of converting from
Celsius to Fahrenheit.  That was one of the key requirements of the project spec
so I had to try and fix it.

What turned out to be the problem is that I have the banner Free Code Camp Weather
App in an H1 element which I bend into a circle using a jQuery plugin called
CircleType.  The Weather information is in a DIV called contents which is a
sibling of the H1 but appears inside the circle thanks to CSS positioning. There
is an image of the planet Earth which is set as the background of the contents
DIV in CSS. However this covers up the banner. Ok, the easy CSS solution is to
make the z-index of the banner bigger than that of the contents.  Looks good.

But unexpectedly, this had the side-effect of swallowing clicks on the anchor
which toggles Celsius/Fahrenheit conversion.  I tried increasing the z-index of
the anchor which was not that straightforward as it is dynamically generated
after I get the weather information.  I played with the CSS pointer-events property
but that didn't work either.  Finally I hit upon moving the background image
from the contents div to the banner.  That way I didn't have to mess around with
z-indexes and the conversion worked again.  It looks slightly different but I
can live with that.  The more pressing issue is that all my careful responsive
CSS positioning has gotten messed up and will have to be redone.  That'll be
my job for tomorrow.

**Links to work:**

* [Free Code Camp Weather App](http://www.braincells.com/webdev/local-weather/)

## Round 2, Day 13: July 29, 2017

**Today's Progress**: FreeCodeCamp Local Weather App (again)

**Thoughts**:

Today I took a detour back to frontend JavaScript for two reasons.  One, I read
an article on SitePoint entitled ["The MVC Pattern in Plain JavaScript"](https://www.sitepoint.com/mvc-design-pattern-javascript/).
When I did my front-end projects I was concentrating on getting the job done
quickly  and they are not in the best of shape especially if I want to show them
to an employer.  So I knew they needed to be refactored and reading this article
gave me an impetus to try that using the local weather app as a test case.  The
principles shown work well though this is really just a waypoint to doing a
rewrite in ES6.  While I was at it I also made the CSS more responsive and
replaced the planet Earth graphic with something easier on the eyes.

The second reason is that Jens Grabner who has been giving me a lot of valuable
feedback about my calculator project in the FreeCodeCamp forums noticed another
little flaw.  I want to see if I can fix that.  The calculators design needs
to be overhauled to look nicer and be more responsive too.  So that will be
my agenda for tomorrow.

**Links to work:**

* [Free Code Camp Weather App](http://www.braincells.com/webdev/local-weather/)

## Round 2, Day 12: July 28, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

Algorithm::DawkinsWeasel was accepted into the ecosystem...and failed to
install.  The problem was that in the META6.json file (which contains metadata
for a module distribution) I had given the URL to my github repository but
forgot to put .git on the end of it.  With that little fix everything was
good once again.  I also took the opportunity to add continuous integration
with Travis which was a lot easier than I thought it might be.

With that my little adventure in modules is over and it's back to the exercises
in Think Perl6.  Unfortunately with all that, I only had time left to do one.

**Links to work:**

* [Think Perl6 Exercise 7.3](https://github.com/jaldhar/perl6-scripts/blob/master/caesar.p6)

## Round 2, Day 11: July 27, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

I was able to work on my code during the daytime today so I got a lot done.

The problem with my Perl6 module is solved.  Apparently the correct thing to
do is not implement the Iterator role at all but to return an array.  You might
think this potentially very inefficent but Perl6 has a construct called
gather/take that can do "lazy" evaluation that only gives the next entry as it
is needed.  The upshot is now you can call the module like this:

```
  my $weasel = Algorithm::DawkinsWeasel.new;

  for $weasel.evolution { say .current-phrase; }
```

I must thank the people in the #perl6 channel on the FreeNode IRC network for
this and other insights which have made my code more idiomatically Perl6ish.

I also polished up the documentation and tests and submitted a pull request
to have Algorithm::DawkinsWeasel included in the Perl 6 Ecosystem (as the
module repository is known.)  It's not been approved yet but hopefully will
be tomorrow.

**Links to work:**

* [Algorithm-DawkinsWeasel](https://github.com/jaldhar/Algorithm-DawkinsWeasel)

## Round 2, Day 10: July 26, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

I was hoping to be able to tell you I had uploaded my Perl6 module but I had
to go and try to add one more feature.

Right now you use it like this:

```
  my $weasel = Algorithm::DawkinsWeasel.new;
  
  repeat {
      say $weasel.current-phrase;
  } until $weasel.evolve;
  say $weasel.current-phrase; # The last phrase.

```

That seems a little verbose and it's annoying that you have to repeat the
loop contents one more time in order to get the last phrase.  I tried all kinds
of loop constructs but the only way around it seems to be something like:

```
  my $weasel = Algorithm::DawkinsWeasel.new;

  my Bool $ended = False;
  repeat {
      $ended = $weasel.evolve;
  } until $ended;

```

...which hardly seems like an improvement.  In my original C++ version I had
gotten around this by making the class iterable.  (By implementing operator++
etc.) It seems like I could do the same in Perl6 by implementing the Iterator
role.  (A role is like an interface in Java or a pure abstract class in C++.)

Then I would be able to do something like:

```
  my $weasel = Algorithm::DawkinsWeasel.new;

  say $weasel.current-phrase while $weasel;

```

Much better eh? But as of right now I can't get it to work right.  I've asked
on the #perl6 channel on IRC but the experts don't seem to awake at the moment.
Let's see if I get any answers tomorrow.

**Links to work:**

* [Algorithm-DawkinsWeasel](https://github.com/jaldhar/Algorithm-DawkinsWeasel)

## Round 2, Day 9: July 25, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

As I suspected, once I added some tests problems were uncovered in Algorithm::DawkinsWeasel.
Perl (and now Perl6) has a the best infrastructure for test-driven development of any language IMO.

One by one the problems were easily fixed until the last one which was big.
Somehow I was ending up in an infinite loop and I spent over an hour trying to
figure out why.  Then I noticed one place where I had a '.' when I should have
had a '!' DOH!

I fixed up the POD documentation and other files needed for publication but I
haven't done so yet.  I still want to tinker a little bit.

**Links to work:**

* [Algorithm-DawkinsWeasel](https://github.com/jaldhar/Algorithm-DawkinsWeasel)

## Round 2, Day 8: July 24, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

I tried to get Rakudo 2017.07 to build again and this time it worked without
any problems.  So now I can play with the new module manager, zef.  Apparently
there are already 858 modules which is impressive.

Naturally I had to write one of my own.  This involved skipping ahead in the
book once again and learning about classes.  I took my weasel script from day
3 and have converted it enough that it passes the basic test of loading.  It
remains to be seen whether it is actually usable; I'll find out tomorrow.

**Links to work:**

* [Algorithm-DawkinsWeasel](https://github.com/jaldhar/Algorithm-DawkinsWeasel)

## Round 2, Day 7: July 23, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

I finished the chapter 5 and 6 exercises in Think Perl6.  They were math-heavy
which forced me to think a little harder than I would otherwise have needed to
but nothing I can't handle.  I also read the next chapter which is about strings
so should be more interesting.

**Links to work:**

* [Think Perl6 Exercise 5.4](https://github.com/jaldhar/perl6-scripts/blob/master/power.p6)
* [Think Perl6 Exercise 5.5](https://github.com/jaldhar/perl6-scripts/blob/master/gcd.p6)
* [Think Perl6 Exercise 6.1](https://github.com/jaldhar/perl6-scripts/blob/master/sqrt.p6)
* [Think Perl6 Exercise 6.2](https://github.com/jaldhar/perl6-scripts/blob/master/pi.p6)

## Round 2, Day 6: July 22, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

Had to go to a birthday party so I didn't get much coding done but I took my
Think Perl6 with me and read some of it.  (Yes I am a collosal nerd.)  And I
got one more exercise done.  I was pleased I got the recursion bit right but I
didn't do the part about adding a signature constraint.  I don't see how that
could work unless there is something about constraints I haven't learned yet.

This is one frustrating thing about Think Perl6 I find; it sometimes jumps ahead
and uses concepts/syntax it hasn't introduced yet.  I understand that Perl6 is
complicated and overall I do like the book but that's an area that could use
some improvement IMO.

**Links to work:**

* [Think Perl6 Exercise 5.3](https://github.com/jaldhar/perl6-scripts/blob/master/palindrome.p6)

## Round 2, Day 5: July 21, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

Rakudo perl6 has monthly releases.  I am currently using last months but I want
the July release as it has the module system.  I thought it would be 
straightforward to build having done so once before but again I ended up 
spending a lot of time on it (and eventually gave up for the time being.)  So
I only got to do one exercise from chapter 5 of Think Perl6.  The rest will have
to wait until tomorrow.

**Links to work:**

* [Think Perl6 Exercise 5.2](https://github.com/jaldhar/perl6-scripts/blob/master/ackermann.p6)

## Round 2, Day 4: July 20, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

Did the exercises for Chapter 4 of Think Perl6.  Fairly straightforward stuff.

**Links to work:**

* [Think Perl6 Exercise 4.1](https://github.com/jaldhar/perl6-scripts/blob/master/seconds.p6)
* [Think Perl6 Exercise 4.2](https://github.com/jaldhar/perl6-scripts/blob/master/fermat.p6)
* [Think Perl6 Exercise 4.3](https://github.com/jaldhar/perl6-scripts/blob/master/triangle.p6)
* [Think Perl6 Exercise 4.4.1](https://github.com/jaldhar/perl6-scripts/blob/master/fibonacci1.p6)
* [Think Perl6 Exercise 4.4.2](https://github.com/jaldhar/perl6-scripts/blob/master/fibonacci2.p6)

## Round 2, Day 3: July 19, 2017

**Today's Progress**: Perl 6.

**Thoughts**:

Read a few more chapters of Think Perl6 today.  I am going to do the exercises
I promise but I can't help skipping ahead.  I wrote an implementation of a
genetic algorithm called [Dawkins' Weasel](https://en.wikipedia.org/wiki/Weasel_program) based off an earlier C++ version I
had done.  In comparison, the Perl6 version is lot more succint yet still IMO
readable.


**Links to work:**

[Dawkins' Weasel](https://github.com/jaldhar/perl6-scripts/blob/master/weasel.p6)

## Round 2, Day 2: July 18, 2017

**Today's Progress**: More Perl 6.

**Thoughts**:

Read through Chapter three of Think Perl6 and did the exercises.  The book
starts from the very basics such as what is a function, what is a loop etc.
which isn't very interesting for me except for learning the Perl6 syntax.  So
I skipped ahead a little and did a one-liner for determining Harshad numbers
which are Integers divisible by the sum of their digits.  E.g. 72 is a
Harshad number because 7 + 2 = 9 and 72 is divisible by 9.  51 is not.
(Incidently Harshad is my patronym hence the interest :-) Despite being a one
liner, my code does validation. (Input is an integer, not 0 etc.)  Perl6 makes
it impressively easy.

**Links to work:**

* [Think Perl6 Exercise 3.1](https://github.com/jaldhar/perl6-scripts/blob/master/rightjustify.p6)
* [Think Perl6 Exercise 3.2](https://github.com/jaldhar/perl6-scripts/blob/master/dotwice.p6)
* [Think Perl6 Exercise 3.3](https://github.com/jaldhar/perl6-scripts/blob/master/drawgrid.p6)
* [Determine if Harshad Number](https://github.com/jaldhar/perl6-scripts/blob/master/harshad.p6)

## Round 2, Day 1: July 17, 2017

**Today's Progress**: Started round 2; Perl 6.

**Thoughts**:

Being forced to maintain a steady schedule of coding and tweeting about it has
been good for me so I'm going to start the 100 days of code challenge a second
time.

This time I want to concentrate on algorithms and data structures.  I shall
concentrate on C++ and Perl 6 as my languages of choice.  I'm still going to
be doing the android and web dev stuff I was doing before -- in fact I hope to
spend more time on it but the minimum daily one hour of coding will be
dedicated to the topics mentioned above.

Today there doesn't seem to be much result but a lot went on behind the scenes.
The version of Rakudo perl 6 in Ubuntus package repositorys was about 8 months
old.  So I build packages for the latest version.  Unfortunately it took a lot
of time but now I have an up to date base for my future explorations.

**Links to work:**

[Print my name in Gujarati](https://github.com/jaldhar/perl6-scripts/blob/master/jaldhar.p6)

## Round 1, Day 100: June 30, 2017

**Today's Progress**: 100 days! Finished adding features for javascript calculator.

**Thoughts**:

I did it!  100 days of atleast one hour of coding along with a daily tweet and
link to commit on github.  (Well, the last I didn't always manage because of
e.g. multiday tasks but overall I did make more than 100 commits during this
time period so I'm counting it.

Day 100 itself was a bit anticlimactic.  I just had the minimum time available
and that was by forcing myself.  In that hour though I completely overhauled
the logic of the calculator and added support for parentheses.

What's next?  The goal was to be ready for job hunting by this point but I feel
I''m not quite there yet.  The android stuff is going great but it is not 
finished.  Working on the calculator reminded me that I will need to polish up
these projects if I really want to go into webdev.  (And I have completely
forgotten about react.)  I've done some interesting c++ stuff but I'll need
to sharpen my skills in algorithms and data structures if I want to make a
career of that.

So maybe I'll continue this by commiting to the 301 days of code challenge but
in any case I will definitely keep learning and coding.

**Links to work:**

[Calculator](http://www.braincells.com/webdev/calculator/)

## Round 1, Day 99: June 29, 2017

**Today's Progress**: Android; More features for javascript calculator.

**Thoughts**:

More android work but again, nothing you can see at the moment.

So the person who reported the bug asked me to add a 1/x button to the
calculator.  And I did.  But to keep the layout looking good I had to add
four more buttons.  I decided to fill them with percent, sign change and
parentheses.  The first too were pretty straightforward though it made me
see I needed to refactor some code.  But the parentheses did not work right.
Ironic because I had been shown how to implement that in the "Let's Build a
Simple Interpreter" tutorial.  (Which I need to get back to.)  Or perhaps I
can say it is because of the tutorial that I know it is not working right.

**Links to work:**

[Calculator](http://www.braincells.com/webdev/calculator/)

## Round 1, Day 98: June 28, 2017

**Today's Progress**: Android; Fixing a javascript bug.

**Thoughts**:

Work continued on my Udacity android nanodegree but nothing to show at the moment.

Unexpectedly, I got a bug report about the javascript calculator I did at
freeCodeCamp.

The problem is calculations like 1 / 7 don't work because the answer is an
irrational number.  I limit the length of the answer to thirteen digits including
the decimal point and give an overflow error if it is longer.  Obviously
that's not going to work for a number that continues for ever.

So I amended the code to check if the result is not an integer. If so I 
used the Number objects toPrecision() method to limit the result to 10 places.

It turns out that's not enough. E.g. 6.2 / 2 becomes 3.1000000000. It's 
technically correct but unsightly. So to get rid of the trailing zeros, I used 
parseFloat() to turn it back into a number and then called toString on it. 
Like this:

```
    if (result === Math.floor(result) )) { // is it an integer?
        my.answer = result.toString();
    } else {
        my.answer = parseFloat(result.toPrecision(10)).toString();
    }
```

It's a bit convoluted but does the trick. And it is gratifying to know that
people are actually looking at my work.

**Links to work:**

[Calculator](http://www.braincells.com/webdev/calculator/)

## Round 1, Day 97: June 27, 2017

**Today's Progress**: Learned about OOP design patterns

**Thoughts**:

There's another Android meetup in New York, Android NYC  which has been
moribund for a while but just restarted with new organizers.  The first event
took place today.  We were to do hands on learning about design patterns by
splitting into small groups which would each implement one pattern in a small
demo app and then explain it to everyone else.  The group I was in was
assigned the factory pattern.  Here is the demo app I made.  It was kind of a
hackathon like atmosphere (which I thoroughly enjoyed.) so there was time
pressure and as a result the demo is a bit rough around the edges.  Maybe
tomorrow I will polish it up a little bit.

**Links to work:**

[Factory pattern demo](https://github.com/jaldhar/factorydemo)

## Round 1, Day 96: June 26, 2017

**Today's Progress**: Finished cocos2d-x game.

**Thoughts**:

Yep.  Using an older NDK (13b) did the trick.  The game is playable though it
needs some more polish.  Things like sound effects or some kind of visual signal
that you have won.  The help and documentation hasn't been implemented.  And
there are probably some minor bugs lying around in there somewhere.  I can
also think of some additional features that might be nice like being able to
select your own picture or maybe even AI that solves it for you.  The upshot
is I'm not putting this up in the play store just yet.

I'm feeling upbeat.  After the doldrums of the past couple of days I needed a
win.

**Links to work:**

[LOLCatsPuzzle](https://github.com/jaldhar/LOLCatsPuzzle)

## Round 1, Day 95: June 25, 2017

**Today's Progress**: Further along with cocos2d-x game but still fails to build.

**Thoughts**:

I really should have left well enough alone particularly because I didn't have
much time today but I had received some advice about my compile problems so
I tried to get my game working.  Android Studio is still a no go but I can
get a lot further by running gradle from the command line.  It fails before the
end though.  It seems that what my problem is, is a too new version of the NDK.
If I downgrade it to an older version, it should work.  But I'm not going to
try it out today.

**Links to work:**

LOLCatsPuzzle: Haven't bothered uploading it yet.

## Round 1, Day 94: June 24, 2017

**Today's Progress (or lack thereof)**: Failed to build a game with cocos2d-x.

**Thoughts**:

I had found a free Udemy course about the cocos2d-x game library which I took
today.  I like cocos2d-x because it is open source (truly, not with restrictions
like Unity,) uses C++ and is multi-platform. I have a very simple game in the
Play Store which I made using this library a long time ago but this course
brought me up to date with the latest version and got me understanding it on a
much higher level than I had before. So I used it to write a more complex (but
still relatively simple. My magnum opus still lies in the future) scrambled
puzzle game.

So far so good but then Android Studio happened.  The latest versions of
cocos2d-x are supposed to support it.  But both 2.3.3 and the latest 3.0 beta
give some sort of null pointer exception in gradle and refuse to build further.
I could build from the command line but I recall that used to be somewhat messy
so I am just giving up for now.  The downside of this library is that it is more
popular in Asia so the English documentation is not that great.  Their forum
is pretty active though or perhaps I could ask the course teacher.

Anyway I'm disappointed but I remind myself tomorrow is a new day.

**Links to work:**

LOLCatsPuzzle: Haven't bothered uploading it yet.

## Round 1, Day 93: June 23, 2017

**Today's Progress**: Android; roguelike shelved for now.

**Thoughts**:

I found the bug in my dungeon generating code but that also uncovered other
problems.  What I have uploaded today implements corridors but not rooms etc.
That will be trivial to add in but some other time, I have to get back to
Android now.
  
**Links to work:**

[dungeon](https://github.com/jaldhar/dungeon)

## Round 1, Day 92: June 22, 2017

**Today's Progress**: Folding a string into a triangle

**Thoughts**:

I got offered an interview today which was unexpected because I'm not actively
looking just yet.  This means tonights coding session is off as I have to make
sure I get a good nights rest for tomorrow.  The roguelike, android etc. will
have to wait.

In order to fulfill the terms of the 100 days of code challenge I have done
something though.  I came accross an interesting algorithm problem on
Stack Exchanges' code golf site.  Instead of trying to make my version really
small (the objective of code golf) I have kept it easy to read and follow.
  
**Links to work:**

[Fold a string into a triangle](https://gist.github.com/jaldhar/5c24443fb3a5d34e1778962d17d53135)


## Round 1, Day 91: June 21, 2017

**Today's Progress**: Continued C++ roguelike project

**Thoughts**:

I've uploaded the code that implements the features I mentioned yesterday but
maddeningly I still can't figure out why the dungeon generation is going wrong.
I need to get back to android so I've resolved to fix this tomorrow or forget
about it.

**Links to work:**

[dungeon](https://github.com/jaldhar/dungeon)


## Round 1, Day 90: June 20, 2017

**Today's Progress**: Continued C++ roguelike project

**Thoughts**:

At this point the roguelike displays a title and an (empty) window.  It accepts
input from the keyboard (only the Q key to quit really.) and it has a game loop.
The actual dungeon building code has a bug I need to track down so I will
add it tomorrow.

**Links to work:**

[dungeon](https://github.com/jaldhar/dungeon)


## Round 1, Day 89: June 19, 2017

**Today's Progress**: Started C++ roguelike project

**Thoughts**:

Having submitted the Popular Movies app I wanted to take a little break from
Android stuff so I started playing about with C++ by reimplementing the 
dungeon building algorithm from Rogue -- the original roguelike.  I've done this
before but this time I want to implement all the C++ best practices.  It won't
become a full game; I should work on one of my several incomplete roguelikes
for that.  Right now the github repository only has the details of the algorithm
itself.  I'll put up the rest of the code tomorrow when its fully finished.


**Links to work:**

[dungeon](https://github.com/jaldhar/dungeon)


## Round 1, Day 88: June 18, 2017

**Today's Progress**: Continued Popular Movies.

**Thoughts**:

I'm ready to call this complete.  As it is late I'll give it a final once over
and submit it tomorrow.

**Links to work:**

[Popular Movies](https://github.com/jaldhar/PopularMovies)


## Round 1, Day 87: June 17, 2017

**Today's Progress**: Continued Popular Movies.

**Thoughts**:

I think the network status broadcast receiver is working properly now but I am
facing a new problem with updating the database when the status changes.  It
could potentially happen lots of times in rapid succession if the wifi goes
in and out so I don't want react every time.  Perhaps I should just inform the
user and leave it up to him to start the sync instead of doing it automatically.
I'll think about that tomorrow.

**Links to work:**

[Popular Movies](https://github.com/jaldhar/PopularMovies)


## Round 1, Day 86: June 16, 2017

**Today's Progress**: Continued Popular Movies.

**Thoughts**:

A feature I wanted to add to Popular Movies is to check if the user is online
before trying to fetch movie details from the cloud as the cool kids call it.
So today I learned about setting this up via a broadcast receiver.  The code
doesn't quite work but I think it is almost there. I'll debug it tomorrow.

**Links to work:**

[Popular Movies](https://github.com/jaldhar/PopularMovies)


## Round 1, Day 85: June 15, 2017

**Today's Progress**: Continued Popular Movies.

**Thoughts**:

After rethinking my database schema, things are moving forward once again in the
rewrite of Popular Movies to use architecture components.  There is still a lot
of work to do however.

I attended a meetup of the New York Android Developers group in the evening.
There were two talks; one about navigation design patterns, and the other which
I was more looking forward to, about the architecture components.  But it 
turned out not to tell me much I hadn't figured out myself these past few days.
I actually learned some things from the navigation talk.

**Links to work:**

[Popular Movies](https://github.com/jaldhar/PopularMovies)


## Round 1, Day 84: June 14, 2017

**Today's Progress**: Continued interpreter tutorial.

**Thoughts**:

I spent a lot of time upgrading various computers to the next version of Debian
GNU/Linux, "stretch" which is going to be released this Saturday.  And if I have
to be honest, a lot of time playing a game called [Little Alchemy](https://play.google.com/store/apps/details?id=com.sometimeswefly.littlealchemy).

But neither of those activities count for this challenge.  What I did do was
add parentheses to my interpreter which was the exercise in part 5 of the
tutorial.  It took me a long time but I finally figured it out all by myself
and I was pleased to see it was basically the same solution as Ruslan gives in
part 6.

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 83: June 13, 2017

**Today's Progress**: Continued interpreter tutorial.

**Thoughts**:

I was only able to do the bare minimum today; part 5 of the Interpreter
tutorial and even then not the exercises.

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 82: June 12, 2017

**Today's Progress**: Continued Popular Movies and interpreter tutorial.

**Thoughts**:

Now that XYZ Reader is in the reviewers hands, I continued converting Popular
Movies (the first project in the Udacity Android nanodegree.) over to the new
architecture components this might be a bigger job than I had anticipated.

I also did part 4 of the Interpreter tutorial.

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 81: June 11, 2017

**Today's Progress**: Continued XYZ Reader

**Thoughts**:

Today I just put the finishing touches on XYZ Reader.  Little adjustments to
make it look good on a tablet etc.  I will submit it tomorrow.

**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)


## Round 1, Day 80: June 10, 2017

**Today's Progress**: Continued XYZ Reader

**Thoughts**:

Work contains apace on XYZ reader.  I was having a bit of a problem with
collapsing toolbars but I was pleased to be able to solve it myself without
having to ask on a forum or Stack Overflow etc.  It did waste a lot of time
though.
 
**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)


## Round 1, Day 79: June 9, 2017

**Today's Progress**: Continued XYZ Reader

**Thoughts**:

I didn;t have much time today but I did manage to get some solid work done on
XYZ reader.  It looks a lot more like a Material app now though I still need to
make sure all the little details are taken care of.  Nevertheless I'm going to
go out on a limb and say I will have it finished this weekend.

**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)


## Round 1, Day 78: June 8, 2017

**Today's Progress**: Continued interpreter tutorial and XYZ Reader

**Thoughts**:

Did part 3 of the Interpreter tutorial.  The exercises were mostly on theory.
The only part that needed code was to reimplement the interpreter on your own
which I'm doing anyway.

A bit of forward progress with XYZ reader.  It looks better but still doesn't
conform entirely to the Material Design spec.

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 77: June 7, 2017

**Today's Progress**: Continued interpreter tutorial

**Thoughts**:

Did part 2 of the Interpreter tutorial.  I am enjoying this one a lot more and
learning a lot too.

I Watched some more of the Google IO videos.  I think I understand the new
architecture components now more or less. However I haven't implemented them
yet because my layouts in XYZ reader got messed up somehow and I ended up
having to backtrack to yesterdays state of affairs.  Thank God for git.

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 76: June 6, 2017

**Today's Progress**: Started new interpreter tutorial

**Thoughts**:

I feel bad about giving up on Crenshaws' compiler tutorial but it isn't the
right material for me and would have wasted my time which is in short enough
supply as it is.  Happily, today I came across another, similiar, tutorial.
This one is [by Ruslan Spivak](https://ruslanspivak.com/lsbasi-part1/) It's in
Python not Pascal so it should be easier to translate to C++.  Ruslan says
that you should formally commit to learning about interpreters and compilers
so here is my pledge:

I, Jaldhar H. Vyas, of being sound mind and body, do hereby pledge to commit
to studying interpreters and compilers starting today and get to a point
where I know 100% how they work!

Signature: Jaldhar H. Vyas

Date: June 06, 2017

**Links to work:**

[Let's Build A Simple Interpreter](https://github.com/jaldhar/Lets-Build-a-Simple-Interpreter)


## Round 1, Day 75: June 5, 2017

**Today's Progress**: Continuing with Android XYZ Reader; Revisiting Popular Movies

**Thoughts**:

Three Quarters of the way through the 100 Days of Code challenge!

After watching some videos from this years Google I/O conference I am excited 
about the new architecture components they have introduced for lifecycle management,
ORM, etc.  As I haven't proceeded far with my udacity projects yet, I am 
investigating how to integrate them into atleast Popular Movies and maybe
XYZ Reader too.

**Links to work:**

[Popular Movies](https://github.com/jaldhar/PopularMovies)
[XYZ Reader](https://github.com/jaldhar/xyz-reader)


## Round 1, Day 74: June 4, 2017

**Today's Progress**: Android XYZ Reader overhaul continues.

**Thoughts**:

Although I had a good amount of free time for coding today, it was Nirjala
Ekadashi a Hindu fast day where you do not eat or drink even a drop of water.
I can manage that fine for most activities but not highly intellectual ones
like programming.  After the fast has gone on for a while you feel foggy and
unable to concentrate.  So I focused on reading about Android and Material
Design and went over the code in XYZ Reader but didn't make any permanent
changes.

**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)


## Round 1, Day 73: June 3, 2017

**Today's Progress**: Built Solitaire game in Kotlin; small improvements to ;#

**Thoughts**:

Limited time for coding today with family stuff to attend to but I finished off
the two remaining Kotlin videos and I received a response to my Stack Overflow
question from a couple of days ago suggesting some improvements to my assembly
code which I implemented.
 
**Links to work:**

* [Solitaire in Kotlin](https://github.com/jaldhar/Solitaire)
* [;# interpreter](https://github.com/jaldhar/semicolonhash)

## Round 1, Day 72: June 2, 2017

**Today's Progress**: Built Solitaire game in Kotlin.

**Thoughts**:

A slow day at work meant I had a lot more time for coding than usual.  I used it
to finish watching all but two of the Treehouse Intro to Kotlin videos and
followed along in code.

Still no react.  I should devote a day to that.

**Links to work:**

* [Solitaire in Kotlin](https://github.com/jaldhar/Solitaire)

## Round 1, Day 71: June 1, 2017

**Today's Progress**: Learned about Kotlin, Perl 6, and Assembly.

**Thoughts**:

Today was Alternative Language Day.  I found out that Treehouse has a free
course [introducing Kotlin for Java developers](https://teamtreehouse.com/library/kotlin-for-java-developers).
Kotlin has been on my radar for a while but now that Google has made it an
officially supported language on Android knowing about it has gone up in
priority.  I installed the development version of Android Studio 3 which has
Kotlin support and watched some of the videos.  In the course a solitaire game
is built up.  I followed along but don't have my code on github yet.

Green Tea Press announced they are making their book "Think Perl 6" available as
a [free download](http://greenteapress.com/thinkperl6/thinkperl6.pdf).  I began reading through it.

Although "Let's Build a Compiler" is on hiatus for now, C is not being
neglected.  Well sort of. On day 62 I had mentioned writing a tiny interpreter
for a programming language called semicolonhash.  The reason it was so small
is that instead of linking with the C standard Library (libc) I was directly
calling the undelying Linux system calls via inline assembly.  Today on a
whim, I decided to make those syscall, um, callers, pure assembly. libc gives
you an extra layer over the raw system calls by giving you the error status in
the errno variable.  I wanted to do the same but ran into some difficulties and
had to ask on Stack Overflow.  I got it working in the end and the interpreter
is still only just over 1k in size.

Overall today was a good sign I've left the doldrums of the last few days.

**Links to work:**

* [;# interpreter](https://github.com/jaldhar/semicolonhash)

## Round 1, Day 70: May 31, 2017

**Today's Progress**: continued compiler tutorial 

**Thoughts**:

I've pinpointed where the bug is but I cannot for the life of me understand
why it is a problem.  I'm going to have to put this aside.  It's taking up
all my time and I'm not getting anywhere.

No android or react today.

**Links to work:**

[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 69: May 30, 2017

**Today's Progress**: continued compiler tutorial 

**Thoughts**:

My laptop froze for no reason and I had no choice to do a hard reboot destroying
a lot of todays work.  (In a fit of coding I had gone half an hour without
commiting to git.  Just as editors have autosave they should have autocommit.)
I redid it mostly but I'm too disheartened to continue today.  Plus there is
a bug in the compiler that is causing an incorrect error message.  That's why
I haven't finished all of part 4 yet.

No android or react today.

**Links to work:**

[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 68: May 29, 2017

**Today's Progress**: continued compiler tutorial 

**Thoughts**:

Today being Memorial Day I was too busy with my family to do much coding. So no
android or react today.

In the short time available I did part 3 of "Let's Build a Compiler" which 
finishes up expression parsing.

**Links to work:**

[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 67: May 28, 2017

**Today's Progress**: Continued XYZ Reader; continued compiler tutorial 

**Thoughts**:

I spent a lot of my time reading through the XYZ Reader source code to understand
what it does and how.  I tried to make some changes but they didn't seem to work.
I will have to investigate further tomorrow.

I did part 2 of "Let's Build a Compiler" which involved expression parsing. One
problem is that the machine code the compiler emits is for the M68K processor. I
will have to translate it to Intel if I actually want to see if it works which
means yet another thing to learn.

No react today either.

**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)
[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 66: May 27, 2017

**Today's Progress**: Started XYZ Reader project from Udacity Android Dev nanodegree

**Thoughts**:

I finished the rest of the "Make Your App Material" course on material design
and began the associated project; beautifying the XYZ Reader app.  I had 
problems with Android Studio which I only rectified after a lot of fiddling
around so no work got done apart from importing the project into my github.

No react or "Let's Build a Compiler" today.

**Links to work:**

[XYZ Reader](https://github.com/jaldhar/xyz-reader)

## Round 1, Day 65: May 26, 2017

**Today's Progress**: Restarted Udacity Android Dev nanodegree; Learned about React; Started compiler tutorial


**Thoughts**:

My mother had an operation to have a pacemaker involved and I accompanied her.
Plus as the Friday before the Memorial Day long weekend, there was not much
going on at work so I got a lot of coding done and, rarely for me, during the
daytime too.

I watched nearly all the material design videos from Udacity.

Day 3 of 30 Days of React.  Now we are getting to the good stuff: components.  
This was illustrated with a basic "Hello world" example.

I translated part 1 of "Let's Build a Compiler" into c++.  This is all the
support routines which will be needed for the compiler.

**Links to work:**

[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 64: May 25, 2017

**Today's Progress**: Restarted Udacity Android Dev nanodegree; Learned about React; Started compiler tutorial


**Thoughts**:

I (re)started the Udacity Android Dev nanodegree.  Nothing to show yet; I just watched some videos and updated Android Studio.

I read Day 1 (which was short and introductory) and Day 2 of 30 Days of React.  Again nothing to show yet; it's all theory and definitions so far.

I found an old tutorial in 16 parts by  Jack Crenshaw called "Let's Build a Compiler")
and thought that might be interesting to pursue.  His examples are written in
Pascal but I shall use C++.  So far my git repository only includes the articles.
I'll start work in earnest tomorrow.

**Links to work:**

[Let's Build a Compiler](https://github.com/jaldhar/Lets-Build-a-Compiler)

## Round 1, Day 63: May 24, 2017

**Today's Progress**: Got freeCodeCamp frontend cert

**Thoughts**:

I submitted the last two challenges, the Simon game and the Pomodoro clock and
claimed my certificate.  Altogether it has taken me approximately 200 hours over
9 weeks to finish.

So what next?  I want to take a break from webdev and (re)start the Udacity
Android dev nanodegree.  I expect that will take most of my free time.

I also would like to polish up my portfolio and projects and I want to do the
Roguelike Dungeon Crawler challenge from the next freeCodeCamp certificate
just because it's a roguelike.  That will involve learning react which is a
daunting proposition.  I have a book called ["30 Days of React"](https://www.fullstackreact.com/30-days-of-react/) whose subtitle is "An introduction to React
in 30 bite-size morsels" which sounds like it could work.

I should also do some algorithms practice by starting hackerrank or codefights
again.

I neglected to mention that I attended the New York Perlmongers tech meeting
this evening.  There were two talks both given by people who will be presenting
at this years Perl conference.  (Which sadly I will not be able to attend barring
a miracle.)  The second was about the inner workings of the Perl QA and release
processes.  Interesting in its own way but not nearly as much as the first talk
which was an overview of many of the most interesting modules which have been
uploaded to CPAN this year.  Although it is no longer in the limelight as much
these days, there is still a lot of life left in the Perl community so that's
another avenue I'd like to explore.

**Links to work:**

* [Pomodoro Clock](http://www.braincells.com/webdev/pomodoro/)
* [Simon](http://www.braincells.com/webdev/simon/)

## Round 1, Day 62: May 23, 2017

**Today's Progress**: Pomodoro clock finished at last!  Wrote interpreter in C

**Thoughts**:

Hooray got the radial progress bar  working. I made a few more cosmetic changes.
I used Comic Sans!  (Though as a respectable web designer I only used it as a
a fallback for Brush Script MT so don't drum me out of polite society just yet.)
I feel comfortable submitting this but I shall wait one more day to see if I 
can get some critique from freecodecampers.

As I was researching my radial progress problem, I came across [a stackexchange entry](https://codegolf.stackexchange.com/questions/121921/make-a-interpreter.)
about an esoteric programming language called ;# that only has two
instructions: ';' and of course '#'.  I had to try and make an interpreter for it.

I also wanted to see how small I could make the executable.  I did a lot of reading
about assembly language, and Linux syscalls, compiler flags and so on and I
eventually got it down to 1064 bytes.  I think it could get smaller than that 
though just how is beyond my current capabilities.

**Links to work:**

* [Pomodoro Clock](http://www.braincells.com/webdev/pomodoro/)
* [;# interpreter](https://github.com/jaldhar/semicolonhash)

## Round 1, Day 61: May 22, 2017

**Today's Progress**: Still not done with Pomodoro clock.

**Thoughts**:

Aargh this is so frustrating.  My radial progress effect is just not working
and I don't know why.  I'm going to sleep in the hopes that this problem will
magically resolve itself overnight.

**Links to work:**

* [Pomodoro Clock (WIP)](http://www.braincells.com/webdev/pomodoro/)

## Round 1, Day 60: May 21, 2017

**Today's Progress**: Continued Pomodoro clock.

**Thoughts**:

The Pomodoro clock is almost done.  It is functionally complete but I want
to add an effect where the border turns color according to the percentage of
time elapsed.  I think I know how it should work but I'm not quite there yet.

**Links to work:**

* [Pomodoro Clock (WIP)](http://www.braincells.com/webdev/pomodoro/)

## Round 1, Day 59: May 20, 2017

**Today's Progress**: Continued Pomodoro clock.

**Thoughts**:

Another short day where real life intruded on my coding time.  I did manage
to make some progress on the pomodoro clock though.  The main thing was some
architectural changes.  I was initially going to use the spinner from jQueryUI
but the HTML5 input type=number should be sufficient.  (I'm still going to use
jQuery itself for the logic.)  I was also going to hand code the CSS.  I'm now
using bootstrap instead.

**Links to work:**

* [Pomodoro Clock (WIP)](http://www.braincells.com/webdev/pomodoro/)

## Round 1, Day 58: May 19, 2017

**Today's Progress**: Began Pomodoro clock challenge

**Thoughts**:

I started the challenge.  There is not much to see at the moment but I have
a design in mind so I "merely" have to implement it.

I couldn't resist tinkering with the Simon game (which is still unsubmitted by
the way.)  I realize I am missing one feature namely a timeout if you don't
press a key fast enough.  Also I'd like different sounds for errors or if you
win.  I'll revisit these issues after I've worked more on the Pomodoro clock.


**Links to work:**

* [Pomodoro Clock (WIP)](http://www.braincells.com/webdev/pomodoro/)

## Round 1, Day 57: May 18, 2017

**Today's Progress**: Finished Simon game

**Thoughts**:

Finished at last.  I abandoned the web audio api and just kept the sounds as
audio elements in the HTML.  As it's already very late, I'm going to wait until 
tomorrow to submit this just to check for any latent bugs but I think it is
pretty solid.

**Links to work:**

* [Simon](http://www.braincells.com/webdev/simon/)

## Round 1, Day 56: May 17, 2017

**Today's Progress**: Continued Simon game

**Thoughts**:

The Simon game is now pretty much complete with one huge exception.  The sounds.
Playing a sound with the Web Audio API reliably locks up the browser. Browsers
I should say--this happens on Firefox for Linux and Chrome for windows and 
Linux so I'm pretty sure its a problem in my code and not a browser bug.  I also
need to review my use of timers.  I use them to make sure the color sequence
doesn't occur to rapidly but it sometimes goes faster and sometimes slower for
as yet unknown reasons.  It may even be related to the sound problem.

This has definitely been the toughest project to date.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 55: May 16, 2017

**Today's Progress**: Continued Simon game; Learned about Phaser framework.

**Thoughts**:

Work on the Simon game continues apace.

This evening I attended a presentation by [Playcrafting NYC](https://www.playcrafting.com/) introducing
the [Phaser](http://phaser.io/) JavaScript game framework.  We built a little
game which shows the basics of this powerful framework. One day I would like
to explore this further and make a real game.  But some other day.  For now it
is back to Simon.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)
* [An Introduction to Phaser](https://github.com/jaldhar/intro-to-phaser)

## Round 1, Day 54: May 15, 2017

**Today's Progress**: Continued Simon game 

**Thoughts**:

Today turned out to be more hectic than I had hoped so I have not finished the
game but steady progress has been made.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 53: May 14, 2017

**Today's Progress**: Continued Simon game 

**Thoughts**:

As today was Mothers Day as well as a normal domestic weekend day, not a lot of
coding got done.  I did manage to finish the rest of the Simon game UI.  Now
all I need to do is the JavaScript.  Let's see if I can put in some solid time
tomorrow.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 52: May 13, 2017

**Today's Progress**: Continued Simon game 

**Thoughts**:

With a little hint from a friendly freecodecamper, I solved my CSS problem but
it took a lot of the meager time that was available today.  I learned about
the web audio api which I'm going to need to create the beeps for the game.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 51: May 12, 2017

**Today's Progress**: Continued Simon game 

**Thoughts**:

I'm running into a problem with the CSS for the Simon game.  I need a circle
within a circle which seems like it should be easy enough to do but if you
look at what I have now, there are unsightly "peaks" at the top and bottom of
my inner circle.  (This is in chrome, it's worse on firefox.)  I don't
understand why.  I'm going to sleep on this for now but I can't figure it out
now, I will have to ask for help.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 50: May 11, 2017

**Today's Progress**: Continued Simon game 

**Thoughts**:

I am half way through the 100 days of code challenge.

I Did not have much time to code today.  I made a small change to the Orcs
and Elves game based on feedback and the minmax code works now making the
AI much more challenging.

The majority of my time was spent on the Simon game.  So far there is not much
to see but things are progressing behind the scenes.

**Links to work:**

* [Simon (WIP)](http://www.braincells.com/webdev/simon/)

## Round 1, Day 49: May 10, 2017

**Today's Progress**: Completed Tic-tac-toe (for now.) Began Simon game 

**Thoughts**:

My minmax is not working properly.  So I submitted this project with a much
weaker one which just randomly picks a square.  It looks like I will have to
investigate this in greater depth but for now, in order to keep up momentum,
I am setting it aside and moving on to the Simon game project.

**Links to work:**

* [Orcs & Elves (AKA Tic Tac Toe)](http://www.braincells.com/webdev/tic-tac-toe/)

## Round 1, Day 48: May 9, 2017

**Today's Progress**: Alas! Still on Tic-tac-toe project

**Thoughts**:

I thought I was almost done but got derailed at the last minute because 
apparently event handlers behave strangely with &lt;button&gt; tags.  Changing
it to &lt;input type="button"&gt; made everything work but I lost a lot of time
figuring it out.  On the bright side I was able to figure it out.

As I write this, I've noticed another bug where the game doesn't end properly
if both players are humans (i.e. not AI) and it is a draw.  I think I know why
but I'm too tired to deal with it now so it will have to wait until tomorrow.

I also attended the New York Android Developers meetup today.  One talk was
about RxJava which I haven't looked at yet and the other was about a library
called Conductor which replaces/supplements fragments which is something I
haven't needed to do yet.  Despite this, attending was still worthwhile IMO.

**Links to work:**

* [Orcs & Elves (AKA Tic Tac Toe) (WIP)](http://www.braincells.com/webdev/tic-tac-toe/)

## Round 1, Day 47: May 8, 2017

**Today's Progress**: Continued Tic-tac-toe project

**Thoughts**:

Once again I did not have a lot of time.  I decided that O's and X's are boring
so I've given the project a fun fantasy theme.  The AI works.  (In weak form not
minmax just yet.)  I need to complete the setup screen and then I'm done.

**Links to work:**

* [Orcs & Elves (AKA Tic Tac Toe) (WIP)](http://www.braincells.com/webdev/tic-tac-toe/)

## Round 1, Day 46: May 7, 2017

**Today's Progress**: Continued Tic-tac-toe project

**Thoughts**:

I spent some time learning about the minmax AI algorithm today.  I'm going to
need this for my games computer player mode.  I'm not a 100% there yet but I
think I am slowly getting it.  As the state machine approach worked well for
the calculator, I rewrote the tic-tac-toe prototype to use it.

This is all infrastructure stuff so there is not much to see yet but I think
I've got a good foundation set up.

**Links to work:**

* [Tic Tac Toe (WIP)](http://www.braincells.com/webdev/tic-tac-toe/)

## Round 1, Day 45: May 6, 2017

**Today's Progress**: Debugging Calculator project

**Thoughts**:

I was going to continue with the tic-tac-toe project today but I got reports
thats there were still a couple of bugs in the calculator which I decided to
fix.  Unfortunately that used up all my available time.

**Links to work:**

* [Calculator](http://www.braincells.com/webdev/calculator/)

## Round 1, Day 44: May 5, 2017

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

## Round 1, Day 43: May 4, 2017

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

## Round 1, Day 42: May 3, 2017

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

## Round 1, Day 41: May 2, 2017

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

## Round 1, Day 40: May 1, 2017

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

## Round 1, Day 39: April 30, 2017

**Today's Progress**: Continued work on Twitch.tv API project

**Thoughts**:

This log is very late because of an Internet outage which couldn't have come
at a worse time.  I was _this_ close to having the Twitch.tv project done and
shipped.  I still haven't figured out the radio button thing but that is just
cosmetic.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Round 1, Day 38: April 29, 2017

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

## Round 1, Day 37: April 28, 2017

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

## Round 1, Day 36: April 27, 2017

**Today's Progress**: Started work on Twitch.tv API project

**Thoughts**:

I started the next freeCodeCamp front-end certificate project.  Mainly, I did
a lot of reading to see how their API works so there is not much to see at the
moment.

**Links to work:**

* [Twitch.tv JSON API (WIP)](http://www.braincells.com/webdev/twitch-api/)

## Round 1, Day 35: April 26, 2017

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

## Round 1, Day 34: April 25, 2017

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

## Round 1, Day 33: April 24, 2017

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

## Round 1, Day 32: April 23, 2017

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

## Round 1, Day 31: April 22, 2017

**Today's Progress**: Still working on Wikipedia Viewer

**Thoughts**:

The good news is that I can now make the search box expand as it should.  The
bad news is I don't seem to be able to make it contract again and I don't
understand why.  Please take a look at the codepen linked below and let me
know what I'm doing wrong.

**Links to work:**

* [Codepen illustrating my problem](https://codepen.io/jaldhar/details/PmzdmY/)
* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Round 1, Day 30: April 21, 2017

**Today's Progress**: Continued Wikipedia Viewer; Learned CSS transitions and transformations

**Thoughts**:

I was hoping to finish the wikipedia viewer today but I got waylaid with
learning about CSS transitions and transformations.  I want to replicate the
way the search box expands like in the example project but I'm afraid I still
haven't got it right though I feel I am close.  So I am still resisting the
urge to peek at their code for now.

**Links to work:**

* [Wikipedia Viewer (WIP)](http://www.braincells.com/webdev/wikipedia-viewer/)

## Round 1, Day 29: April 20, 2017

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

## Round 1, Day 28: April 19, 2017

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

## Round 1, Day 27: April 18, 2017

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

## Round 1, Day 26: April 17, 2017

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

## Round 1, Day 25: April 16, 2017

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

## Round 1, Day 24: April 15, 2017

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

## Round 1, Day 23: April 14, 2017

**Today's Progress**: Continued Responsive Web Design course from The Gymnasium

**Thoughts**:

Feeling a bit better but not 100%.  I did a few more sections of the
Responsive Web Design course.  I learned a lot about media queries.  It's
really impressive how much work has to go into making a layout look good in
all possible dimensions. I really have to respect Bootstrap for hiding most of
that complexity.

**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)


## Round 1, Day 22: April 13, 2017

**Today's Progress**: Started Responsive Web Design course from The Gymnasium

**Thoughts**:

It's official; I'm sick.  Being dissatisfied with just the canned solutions
Bootstrap gives you, I took a detour from [freeCodeCamp](https://freecodecamp.com) and started a Responsive Web Design course from [The Gymnasium](https://thegymnasium.com) which is centered around
building a responsive portfolio site from scratch.  I only got through the
first two chapters in my weakened state but I'm happy I atleast did something.


**Links to work:**

* [Responsive Portfolio (WIP)](http://www.braincells.com/webdev/responsive-portfolio/)


## Round 1, Day 21: April 12, 2017

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


## Round 1, Day 20: April 11, 2017

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

## Round 1, Day 19: April 10, 2017

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

## Round 1, Day 18: April 9, 2017

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

## Round 1, Day 17: April 8, 2017

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

## Round 1, Day 16: April 7, 2017

**Today's Progress**: Finished building Random Quote Machine.

**Thoughts**:

Finished off converting the Random Quote machine to plain javascript.  It wasn't
that hard really though the DOM has some quirks that jQuery smooths over nicely.
Though doing without has been a very educational experience, I think I'll keep
using jQuery.  Ditto for Bootstrap.

I also learned about CSS filters though in the end I decided not to use them.


**Links to work:**

* [Random Quote Machine](http://www.braincells.com/webdev/random-quote-machine/)

## Round 1, Day 15: April 6, 2017

**Today's Progress**: Continued building Random Quote Machine.

**Thoughts**:

Another light day.  In the time I could spare, I fixed some bugs concerning
responsiveness in my flexbox-based layout.  I also converted a lot of jQuery
into plain javascript but the task is not complete.

**Links to work:**

* [Random Quote Machine (WIP)](http://www.braincells.com/webdev/random-quote-machine/)

## Round 1, Day 14: April 5, 2017

**Today's Progress**: Started building Random Quote Machine.

**Thoughts**:

Converted my existing Random Quote Machine design to use flexbox instead of 
Bootstraps' grid.  It basically works but there is more to be done to make it
responsive.  I also need to remove jQuery from the javascript code.

I didn't have time for anything else.

**Links to work:**

* [Random Quote Machine (WIP)](http://www.braincells.com/webdev/random-quote-machine/)

## Round 1, Day 13: April 4, 2017

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

## Round 1, Day 12: April 3, 2017

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

## Round 1, Day 11: April 2, 2017

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

## Round 1, Day 10: April 1, 2017

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

## Round 1, Day 9: March 31, 2017

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

## Round 1, Day 8: March 30, 2017

**Today's Progress**: More freeCodeCamp javascript exercises; Worked on Portfolio a bit more.

**Thoughts**:

Today I did even more of the freeCodeCamp javascript exercises.  I also did
more work on my portfolio including some interesting experiments in making it
responsive.  I didn't put up the current state publically yet but I think that
by tomorrow I'll be ready to mark this as done.  For now.

I should have done some codefights but got lazy.  I am suitably ashamed.

**Links to work:**

* [Portfolio (WIP but not for much longer!)](http://www.braincells.com/webdev/)

## Round 1, Day 7: March 29, 2017

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

## Round 1, Day 6: March 28, 2017

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

## Round 1, Day 5: March 27, 2017

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

## Round 1, Day 4: March 26, 2017

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

## Round 1, Day 3: March 25, 2017

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

## Round 1, Day 2: March 24, 2017

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

## Round 1, Day 1: March 23, 2017

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
