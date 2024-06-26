# The ultimate introduction to modern GUIs in Python [ with tkinter ]

[Video Link](https://www.youtube.com/watch?v=mop6g-c5HEY)

in this tutorial we will create a BMI app that can work with metric and imperial units an iOS theme calculator
that also has a light mode and a Photoshop inspired app that can change the brightness Vibrance rotation scale
and lots more of any image to make them I will use tkinter the
default user interface framework in Python and I will cover all of it before making the apps
I start with the basics things like buttons sliders and text then I go over how to create pretty much any kind of
layout including responsive and scrollable ones finally I cover styling which will include animations themes and
scaling images by the end of this video you should be able to create basically any kind of user interface in Python and
if you enjoyed this video check out my paid course where I cover 7 additional apps a responsive weather app an iOS
timer a map viewer a paint app a stock market tracker a snake game and a QR code generator
you can get the course for about 15 dollars and buying it helps me massively to create these larger videos and well
with that I hope you enjoyed this tutorial alright so let's get started with tkinter and already I want to start by
making one app that is going to be very simple but it is going to look something like this
in here we are converting miles to kilometers we have an entry field we can type any kind of number and if you
convert it you get the output in kilometers a very simple app but it is going to cover all of the basics of tkinter
although let's talk about these Basics first to make any kind of appendique Kinder you need three major components
the first one is called widgets if I show the app again a widget for example
could be a button it could be some text it could be an entry field all of these
are widgets tkinder has quite a few of them you're going to learn all of them although for now I'm only going to cover
three different ones text an entry field a button and another bit of text
besides that we have layout this one determines how the widgets are arranged
on the window for example in the app you can see here we have a top-down Arrangement where we have three
different rows and then inside of the middle one in here we have two different
columns one for the entry field and one for the button this would be a very simple layout obviously you can make
much more complex ones finally we have Style style for example determines the color
of the button the font of the text the size of this text and so on we could
also set the background color and lots of different things all of this is inside of the style if you understand
these three main components you are going to have a fairly easy time designing whatever kind of app you want
to create and Decanter that being said each of these parts can be quite extensive and I have lots of videos on
every single one of them and to understand them in detail it is going to take you some hours now to get started with this app here I
am going to skip over a lot of the details that I will cover in future videos so let me explain how you can
follow along for this video there are three ways you can approach this I would recommend you to follow along is
to download the code and then just play around with the code and follow along as I create this app from scratch that way
you're not going to get too lost and you can just play around and change some individual values and see what happens
besides that you can also follow from scratch and don't worry too much about the details because at this stage you
don't really need to understand every single bit you just need to have a very basic overview of how tikente works with
all of the individual bits finally you can also skip this video and go straight into the separate parts you
are not going to miss anything although I guess if you follow this video you have a tiny bit of a head start to see how the different parts
connect with each other but just to emphasize for this video you don't have to understand every single
bit of tkinter I am just going to cover the really Basics and over the next couple of videos we're going to flesh
out all of this in a lot of detail so just relax follow along and if you
understand even 10 you already have a really good start so let's jump in and let's create an app
here I have a completely empty python file and to get started I want to import tkinter and this is usually abbreviated
as TK besides that I also want from tkinder import ttk
inside of ttk we have all of the widgets that we actually want to use while TK
gives us the basic logic once we have that we can create a window or the main window we put everything
else on this we create with TK and then TK this we have to call is going to
return an object that I want to store inside of a window variable for this one you do want to be careful
here with what letters are uppercase and lowercase basically everything is lowercase besides the second t
with this we have a window although if I run the app now nothing is going to happen although we don't have a crash
that's usually a good start we actually see something we have to call what is called the main Loop let me
add another section here called run and I want to call the main Loop method
on the object we just created now if I run this we have a basic window
and on this window we can already make some changes for example I can get the window and set a title this is just a
string let me call it demo if everyone is now in the top left we have demo
besides that we can also set the size of this window this we do with window dot
geometry in here again we are going to need a string this string wants a width and a
height separated by an X for example in my case I want the app to be 300 pixels
wide and a 150 pixels high if it runs now we have a much smaller app
next up I want to create the first widget this let me add another section here called title and the widget I want
to create is called a label this label I want to store in a variable let me call it title label
label in tkinter is just a fancy word for text and this label we create with
ttk dot label in here we need a couple of arguments a
really important one is we need to set a master and the master is basically the
parent which in our case is going to be the window the way you want to think about it is
that this label needs to be in some kind of container and the only container we have right now is the main window
after that I want to create some text so the actual text this label is going to display
in my case I want to display myodes to kilometers and with that we have a label
widget although if I run the app now we cannot see any kind of text the reason for that is that we need
another kind of method to place this label on this window decanter has quite a few of those but
I'm going to use the simplest one it's called pack now if I run this again we can see miles
to kilometers although what I am quite unhappy about is the font size this one we can also
change by adding another font named argument and in here we need a string then we need the font and the font size
the font size in my case is 24 and the font I want to use is called calibri now
for once again we have a much larger piece of text what you can also do is add something
like bold in here that one would give me bold text next up I want to create the input field
if I run the app again the input field is going to be this area
here for this one I want to have an entry field next to a button
although what is really important here is that both of these widgets are inside of a larger container
so essentially if we have to create three different widgets here but let's go through it step by step
first of all I want to create what is called a let's call it input
brain this is going to be ttk and frame this like the label is going to need a
parent or a master which again is going to be the window which means I want to set the master to window besides that
the frame doesn't need anything else now I have a frame that I can put witches into and I want to put an entry
inside of this Frame and a button the entry we create with ttk and entry this
one now also needs a master but the master now is going to be this input frame
which means input frame in here Order button I want to have ttk and button and
once again the master is going to be the input frame although the button is going
to need a second argument and that is going to be the text let me call this one convert this will be the text the
button is going to display what we now have to do is take both of these widgets place them inside of the frame and then
place the frame itself inside of the window and that is going to happen the same way we have placed the label using the pack
method which means I want to get my entry widget and I want to pack it or
place it with the pack method this I also want to do with the button which means button dot pack
with that we have these two widgets inside of the input frame
finally I want to get the input frame and pack it on the main window
if I run this now we can see we have an entry field and a convert button
let me move this a bit to the side and the way you have to understand this
this input frame here is a frame around these two widgets and this we have
placed using the pack method and what pack does is it places widgets
below each other we first have the title label this is the first one here and then we have the frame this is the
second one here and inside of the frame we have these widgets here we have an entry widget and we have a convert
button since those are also placed with the pack method here they are on top of each
other I hope that makes sense once again if you don't understand this don't worry
too much about it I will explain all of this in a lot more detail although now I have a problem I want
this entry widget and this button next to each other for that we can add an argument inside of pack and this I want
to do for both the entry widget and the button the argument I want to add is called side and the side here is going
to be left if I run this now we have the widgets right next to each other
what you can also do in here is set some padding so pad X could be 10 pixels for
example and if I run this now we have a bit of a gap between the entry field and
the button this area here a similar thing I want to do to the input frame in
here I'm going to set padding for the y-axis this one could be let's say 10 pixels and now we have a bit more space
on the top and the bottom because of this pad white 10 pixels here we have a bit more space above and below
this Frame now finally we need one more widget and that is going to be the output in here I
want to have an output label this like the title label is going
to be ttk and label this one is going to be inside of the
window container which means the master is going to be the window
and for now I'm going to set some text let me call it
output this output label we now have to pack on
the window so we can see it and there we go we have output all the way at the bottom although for this one I don't
really like how small the font is as a consequence I'm going to steal the font from the title label and paste it in
here and remove the Bold part with that we have output that looks kind of similar to the title except a bit
less bold for this pack method I want to set a bit more vertical padding let's say five pixels and with that we have
our basic app now I can add a number in here and click on the button but nothing is going to happen
for that we have to add a bit of functionality the most important one is inside of this
button whenever a user is pressing the button I want something to happen and for that
we want to add the command argument this one wants to have a function let me call
it convert this is going to be a function and this function we have to create I want to Define convert it
doesn't need any arguments and then here we could for example print convert
if I now run this again and I click on convert we can see convert in the bottom
because of this print statement here what you really want to be careful here is that you only want to pass a function
in here you do not want to call this function the function is going to be called by the button itself so be
careful with that one next up whenever I'm pressing the button I want to get the content of this entry
field and there are two ways of getting this the first one the easier one is we
can get the entry widget itself and then run the get method if I run this again I can type some text
in here let's say 10 and now if I click on convert we get 10. that's a pretty good start but that's
not usually the method you want to use to get values from a widget it's not particularly efficient you will learn
later why instead what you want to do is create a separate variable that holds
the value of this entry widget and tkinder has specific objects for that
for example in my case I want to create an entry integer this accurate with TK
and int VAR and make sure to call this one
this is going to create a separate variable that can store and update values and this I want to connect to
this entry widget using the text variable which I want to set to entry integer
anything we're adding inside of this entry field will be stored inside of this entry integer also whenever we're
updating this entry integer we're going to update the content of this entry field although this isn't what we are
going to do for this video once you have that you can inside of the convert method instead of Entry I want
to get the entry integer although the get method still works just fine if I
run this again I can type a number in here I can click on convert and we're going to have the
same result so far this wasn't particularly useful but where this system becomes much more
powerful is labels can also have their own variable for example since I want to
change the output label to the result of this conversion I want to create another ticket variable
this I called the output string and this I create with TK and string VAR again
don't forget to call it now this variable is going to work kind of like the invariable except it is going to
store a string instead of an integer also I just realized I kind of messed up the naming
convention here this shouldn't be entry in like this this should be entry int like so
let me fix this right away I want to have entry in here and enter it all the way at the top
but back to the output label now we have a variable that can store the data for a
label this I want to connect to this output label once again for that we need a text
variable the text variable here is going to be the output string
and let me put all of this over multiple lines so it's a bit easier to see like
so now if I run this you will already see some difference and that is
let me scroll down a tiny bit when we created this output label we
have set a text but after assigning this text variable here we cannot see any
more text inside of the app the reason for that is that it takes variable overwrites whatever text is inside of
the label and this we can use to update the label dynamically
for example when I am pressing the button I want to get the output string
and I want to set a new value the new value could be let's say test for now if
I run this again and I click on the convert button we now have testing here
with that we are able to get data and update the widgets so now we can combine
all of that to actually make the app work first of all I want to get the mile
input this is what we're getting from the entry widget so this line here I can
just copy it in here like so with that we have the miles
this I want to convert to kilometers let me call it km output to turn miles into kilometers we need
the miles itself so mile input and multiply it with 1.61
one mile is always 1.61 kilometers and this kilometer we want to Output in
the label like so and now if I run this again I can type in a 10 in here convert this
and we get 16.1 I can do this multiple times let's say a 2 and we get 3.22
I can also add large numbers in here this is still going to work just fine let's try one more time and again this
is looking really good and with that we have some basic functionality
so with about 37 lines of code we have a functioning app that at the very least
does a basic thing although if I run this again this doesn't look very good right now the problem for tkinter is
that the default starting methods are very limited but to account for that tkhinter has external modules that you
can work with the one that I'm going to use I want to import with ttk and bootstrap this is
another module that you have to install and that is going to happen either in the terminal or on the Powershell for
example if you are on Windows you want to type pip install ttk bootstrap
and run this again in my case this isn't going to do anything because I already have this installed
and on Mac OS you would type pip3 install TDK bootstrap you would have the
same result with that we can use all of this and the way you will use this is you are
importing ttk bootstrap as ttk basically what's going to happen is that
ttk bootstrap takes all of the gtk widgets and adds more styling options which means I can simply comment out
this one here we can already see an update if I type A Tenon here we can convert and this entire thing already
looks much better that's a really good start what we can also do instead of setting the window
with tk.tk we can get ttk dot window run
this again and now we have to expand the window a tiny bit and we get the same kind of
styling although what we can do now is we can set a theme name
and in here we have a lot of different themes we could choose from for example the one you have seen
earlier is called Journal if I run this again and expand the app we're going to fix
this later now we have a different kind of app and while most of what you see is
a different button color but the rest still works just fine a dark color you could use here would be
called Darkly and this one is going to look something like this although this doesn't change any kind of
functionality there we go this is still looking pretty good and with that we have a basic tkinter
app we have covered styling we have covered widgets we have covered layouts and we
have covered functionality all of the basics of tkinder although over the next couple of videos I will flesh out all of
this in a lot of detail and we're going to start by talking about all of the widgets that you have available
I'll see you there let's get started by creating a basic window with some widgets that is going to look like so
in here we have one large text box where I can write some texts over multiple
lines I also have another widget and that is a single line entry so in here I have one
line of text besides that I have a button that if I press it it is going to
print something you can't see it right now but it definitely works finally there's one more element this
bit of text here is also what we are going to add although I jumped ahead a tiny bit
before I start coding I do want to cover a tiny bit of theory the most important part is that widgets
are the building blocks of T kinder which means anything you see like a text
a button a checkbox any kind of menu or any kind of frame is always going to be a widget the best way to think about it
is anything you see in a graphical user interface is going to be a widget
and understanding widgets is incredibly important to understanding any GUI framework
as a matter of fact any framework you are going to use in any language is going to work like that you always Place
widgets in such an arrangement that you get some kind of interface it doesn't really matter if you use tick
hinder react or something like flutter in the most basic sense they work in the same way although there are lots of
other differences but they all use widgets inside of tkin term we have two
sets of widgets one is called TK widgets and we have ttk widgets they do sound
fairly similar and they are but ttk widgets is what you actually want to use
the original TK widgets were made in the original part of tkinter they do work
and we are going to use some of them but most of the time they do look quite outdated all of them were made in the
90s and The Styling really doesn't look proper anymore ttk widgets however
haven't added much later and work in the same way but look much better and have some extra functionality which is why we
are going to use those primarily and that is all we need to get started so let's jump into the code and let's
have a look at all of this here I have a completely empty python file and the
very first thing that I do have to do is to import T kinder this is usually abbreviated as TK and
once we have that I already want to execute the code just to see if we're not getting an error and I don't which
is a good sign that means I have tkinter installed if you're getting an error you
probably want to check how to install the Kinder with that covered I want to create a window and this window we
create with TK and then uppercase t and lowercase k and this we have to call
what this is going to return is the actual window that we can place everything else in which means I want to
store this inside of another variable let me call it window when you look online you see quite a few different
names for this kind of variable a lot of people call it root or you see app quite
often I prefer to use window but it really doesn't matter choose whatever you think is best but once we have that
we do have a window that we could show however if I run the code now we can't
see anything the reason for that is that we need one more method and let me add another label
here and let's call it run what we have to do to actually see something is we
have to get the window the one we just created and call Main loop on it and
don't forget to call it as well now if I run it we can see a basic app
you can also resize it all of this works pretty well although it doesn't do very
much right now and let's talk very quickly about what main Loop is doing it does a couple of
things the main Loop has two major functionalities the first one is it
updates the GUI that way if you write some text or update any kind of widget you actually see the result besides that
the main Loop is also checking for events this means without the main Loop there wouldn't be any way to check for
button clicks Mouse movement closing the window or anything the user could potentially do all of this combined
means that our app couldn't run without the main Loop which is why we always have to call it but other than that it
is pretty straightforward although there is one thing that you do want to consider this main Loop here runs until
we are closing the application which means if I write something afterwards let's say print
hello and run the code again we can see the window but we can't see
this print hello only when I close the app we get hello
which means the code is stopped on this line here and only when we close the window then we get to the next line in
most instances this isn't going to be an issue but sometimes you do want to be aware of it alright with that we have a
basic window and there's already a couple of things that we can do for example we could add window dot title
and this is going to be method so we want to run it and in here we can add a string that changes the name of the app
in this case I'm going to call it window and widgets if I run this again and expand the app a
tiny bit we can see window and widgets all the way in the top left another thing that you can do is set the
geometry this is another method so window dot geometry
in here you can do a couple of things the most basic one is that the width and
the height of your app at least when it starts and this you do with a string again and
tkinder expects a string with the width then an X and then the height kind of a
weird format but it is what it is for example if you wanted to have an app that is 800 by 700 pixels you want 800 x
700. actually let me change this to a 500 so you can see it a little bit better
running this again now we're getting another app that is 800 pixels wide and
500 pixels tall the numbers we specified here and here later on we are going to
learn a few more methods to influence the window but for now I don't want to get into too much detail because it's a
tiny bit more advanced what is much more important is that we want to create widgets that is going to
be the actual lifeblood of our application and remember what I said earlier we have TK widgets and we have
ttk widgets and just to get started I want to create a TK widget one that we
are going to see fairly often is called TK dot text this is a multi-line text
input although when we are creating it we have to give it at least one argument
we have to tell it what its Master is in our case the master is going to be
the window the main application so Master is going to be the window
the way you want to think about it is that the master is basically the parent when we are creating this text box where
do we want to put it in my case I want to put it right on the window for now don't worry too much about it we are
always going to place widgets on the window but later on when I talk about layouts we're going to change this quite
a bit just don't worry too much about it this is all we need to create a basic text input box although if I run the
code now we can't see anything the reason for that is that this line
here only creates a widget and tells what the parent is we don't actually place it in a visual manner for that we
need one more method and tick enter has quite a few different ones the simplest one is called pack
if I run this and run the entire app now we can see a text box
and this one can work over multiple lines so in here I can write as much as I want this always works
when we get started we are creating One widget with this line here and this
widget has a master which is the window which means this TK text is going to be
a child of this main widget here and what pack is doing if I draw the entire
thing this one here is the main window the one we created here and we have
placed the widget in the middle of the top this is what pack is doing it takes
a widget and it places it in the middle on the top you can customize this quite a bit but for now I'm not going to worry
too much about it and with that you can create and place a basic widget although
in practice this is not exactly what you see what you see much more often is that people store this widget in separate
variable and then called pack on this variable separately which means I want
to create another variable let me call it text and this variable is going to contain the widget meaning I want to get
rid of this pack and on the next line I want to call text Dot pack
the result is going to be the same although now I do have access to this
widget with the text variable which I am not going to use for this part but in later tutorials this is
going to be really useful and this is what you see most of the time in tkinder when you are creating
and placing widgets and with the basic logic covered let's talk about ttk widgets those are the
widgets you actually want to use most of the time and to use those we first of all want to import them properly to use
them easily this happens with from tkinter import ttk ttk is just
another sub-module of tkinter so you can just import it from tikenter and that's all you need
after that you are using ttk widgets like you would use TK widgets for
example I want to create a label and this label I create with ttk DOT
label like we have done for the text we have to set the master
and this once again is going to be the window which essentially is going to be the parent
besides that for the label we need a text argument in my case I want to go with this is a
test with that we have a label and this label I want to pack on my window
if I run the code now we have a text widget this one doesn't do very much but
it will display some text and this is also a very good illustration of what the pack method does if this one here is
the window so we have a window like so what pack is doing is it takes a widget
and it packs it all the way on the top like a stack so text was our first
widget and then we had the label widget that we placed right below and since we
called pack on the text first number one here this one is on top and the label had number two so this one
is right below which means if I place those two around and create a label first like so we should have this widget
all the way on the top if I run this again they can see we now have the text on the top I hope it makes sense so far
I am not going to go into any further depth in terms of layouts until we get
into the proper layout section for now all you really have to understand is that we are using pack to place widgets
on the window so that is a label let me actually rename the comment here ttk
label and this I want to call TK text there are two more widgets that I do
want to cover in this section the first one is called ttk entry
this is a single line entry widget let me save it under entry and this we are
creating with ttk and entry in here once again as always we have to
set a master which is going to be the window and once we have that I want to get
entry dot pack now if I run this again
in the bottom we have another entry widget and in here we can write a single
line of text if I press enter nothing happens
but at the very least it is working and finally I want to create a ttk
button let me save it in a variable called button and this button I create with ttk
DOT button in here once again as always we need a master which is going to be
the window and besides that we need a text for the button this I get with text like for the label and let me call this
one a button this button we have to place on the window with the
pack method and if I run this we have a button that we can press so this one is
working pretty well although this button doesn't actually do anything right now to make it do something we have to add
another named argument in here and this named argument is called command
this one wants to have some kind of function for example this could be a button function
this button function is just a regular python function so all the way at the top I want to create the button function
I don't need any arguments and in here I just want to print
a button was pressed and now if I run this and I press on the
button we get a button was pressed which means every time we are pressing
this button we are executing this function the function we have created up
here and what is super important to understand here is that this is just a
function you do not want to call it that would cause an error
the reason why you don't want to call it is you only want to call this function when you are pressing the button so the
button itself calls this function so with that we have the basic widgets
these are the widgets you are probably going to use most of the time now with that what I want you guys to do
is an exercise and then we can finish this part what I want you guys to do is
add one more text label and a button with a function that prints hello the
label the one you are creating here should say my label let me put this one
in quotation marks like so and this label should be between the entry widget and the button
those two we have created here the label I want to be between those two and all of this should be fairly
straightforward so pause the video now and try to figure this one out
let's get started with the label that's the easier part the label I want to let me add the
exercise label here and I want to call this the exercise label this is once again just going to
be ttk dot label and in here we need a master which is going to be the window
besides that I want to have a text and the text should say my label the one I
specified in the exercise with that I have to widget and this widget so the exercise label I want to
pack on the window if I run this now you can see I have my
label all the way at the bottom the issue is this my label should be between
the button and the entry widget so we have to move it since we know that Pax respects the
order of our code what we want to do is to move this text label between the entry and the button like so that way
we are placing the first label all the way in the top below there we have the text then we have the entry then we have
the exercise label and then we have the button which means the exercise label is between the entry and the button
so let's run all of this again and there we go my label is between the entry widget and the button
which means all we have to do now is to create the exercise button
this I want to store in the variable I called exercise button and this is going
to be ttk dot button inside of it as always I need a master which is going to
be the window besides that I want to have some text the text here doesn't really matter let
me call this one the exercise button and just to see that this is working let me
place the exercise not the label but the button on the window
and if I run this now you can see all the way at the bottom we have the exercise button
that is a really good start now we just have to create a function that makes
this button print the word hello I want to create the exercise
button function doesn't need any arguments and what I want to do in here is to print the word
hello inside of the button I have to add the command argument and this is going to be
the exercise button function once again remember you do not want to call this you just want to pass the function in
here the button itself is going to call this function and now if I run this and I press on the
exercise button we get the word hello with that we have covered the absolute
basics of tkinter now there's one more really quick thing that I do want to cover and that is inside of the button
the function you pass in here doesn't necessarily have to be a function by itself it could also be a Lambda
function I'm going to duplicate this line here and comment out the original and I'm going to replace this exercise
button function with a Lambda function inside of this function all I really want to do is to print the word hello
the result is going to be the same meaning if I run the code now and I press on the exercise button we get the
word hello which means that these two lines here are identical although you probably want
to use the second one because this one is much easier to use since we only want to do something fairly simple a Lambda
function here would be perfectly fine also if you're not sure about Lambda function this is probably something you
want to look into for a tiny bit at least for any kind of GUI Lambda functions are pretty important
especially for buttons but well with that we have the absolute basics of the
kinder so far our app is pretty static so in this part I want to get widget
data and change widgets and for that we have to cover a couple of things the
first part is that there are two major ways to get data from a widget the first one is called tkinder variables this is
the one you want to use most of the time although this one is a tiny bit more advanced so I'm going to cover it in the
next few parts for now we're going to use the get method lots of widgets have fairly obvious data
that the user would want to get hence we have a dedicated method for it the best example here is the entry widget if we
run the get method on it it is going to return the text inside of that widget and that is the easiest way to get data
from a widget so let's play around with that and once we have that we can change the widget
with that data alright once again I have a completely empty python file and the
first thing I want to do is to import the Kinder SDK and since I do want to use the nicer widgets I also want from
tkinter import ttk and once we have that I want to create a
window this I want to store in a window variable and this we create with TK and TK
finally to see something I want to run the entire thing and this I do with
window.main Loop like so and if I run this thing now we
can see we have a basic window that we can work with on top of that I also want to change the
title which I do with window.title this I called getting and setting widgets
let me run this again and you can see we have a much better title
so with that I want to create some widgets that we can work with
I want to create a label I want to create an entry widget and I want to
create a button and this could already be a pretty good exercise for you see if
you can remember what was done in the last part and create the label an entry and a button and see if we can figure
this one out all right let's get started by creating
a label and this we get with ttk and label once again we need a master and
this is going to be the window for the content or the text of this widget I
want to set some text it doesn't really matter what it is just choose whatever you want in here finally I want label
dot pack this is going to be the label besides that we have the entry which we're
getting with ttk and entry in here we just need a master so I can
copy from the label and paste it in here and finally I want entry dot pack
for the button we need ttk dot button the master once again and we need a text
and this could be the button to show the button I want to pack that
button and with that we have the three widgets let me run the code and this is
looking pretty good I have some text I can write something in the entry and I
can press the button so this is working really well now what I want to do is when I'm
pressing the button I want to add a command and this is going to be the button function inside of this button
function whenever I press the button I want to get the content of the entry widget so let's create that function
for that all the way at the top I want to have a button function it doesn't need any arguments
and in here I want to get the content of the entry this entry here so how can I
get that and for that we have the get method all we really need is entry dot get this is
going to return the content of the entry widget so if I print it I can run the
entire thing again and now if I press the button nothing happens the reason
for that is that nothing is inside of this widget but if I write some text and
print and press on the button again we get if I write some text whatever I've just written this works with literally
any kind of text and now if I press the button without any content you can see
we have an empty line so this is working just fine this get
method here for a couple of widgets is the easiest way to get the information however you do have to be really careful
here because lots of widgets do not have a get method the label for example
doesn't have such a method so if I run label and press on the button we're getting an
error the error being that label object has no attribute get so this would not
work here I gotta change it back to entry because this is the only one that really works amongst all of the widgets
that we have right now so with that we can work on the next part and that is to
change widgets let's talk about that bit every single widget in tkinter has a
config method and this is what you're using to update the method at least in a very basic way
for example inside of the label we can use the config method to update the text this one should be fairly
straightforward and since this is so simple there's a shorthand in tkinter this one looks like that we're getting
the widget and then kind of like indexing we are passing in a named
argument in this case text the same text we have used up here and then we can assign whatever new
value we want to assign to it the same thing we have done up here
both of these methods are identical you can basically choose whatever you prefer so let's play around with them
back in the code whenever I'm pressing this button here I also want to update
this label for that let me add another comment here update the label
I want to get my label and I want to run the config method
inside of this I want to change the text of the label and this let's for now go
with some other text that is all we need let me run this entire thing and now if I press on the
button we get some other text so this is all we need here
now what you do see fairly often is that some people use config other people use configure
the result is going to be the same so if I press on the button again we get also some other text
right now both are working just fine but I think at some point config is going to
be removed so you probably want to use configure most of the time that being said this kind of thing here
is not really what you would want to use instead you would go with label
and then text and then you can assign the new value so in here I can set some
other text and comment out the line we've just created and run the entire
thing again and now if I press on the button we are getting the same result which means those two lines here are
equivalent they do the same thing and since this one here is a bit more concise I think this is what you would
want to use but once again it really doesn't matter whatever you prefer and now that we do have that we can connect
updating the label and getting the content of the entry widget so what I
want to do is I want to update the label to whatever text is inside of the entry
widget and for that I don't want to print the entry widget so let me get rid of the
print statement here instead I want to save the content let's call it entry
text as another variable and the value here is just going to be a
string and this string I want to use down here or my label
and this should be all I need if I run the entire thing again I can print a new
label and now if I press on the button we get a new label this also works
multiple times so some other text I press the button we're getting some
other text with that you can get information from a widget and you can update an existing
widget and that is basically all you have to know for the basics
although for now this is quite limited I guess what I could be covering is that
besides the text there are quite a few attributes that you could Target for example what you could do is you can
get the entry and there is the state the state determines if the widget is
enabled or disabled if I left it like this after I press the
button the entry widget would not work anymore let me actually try if I now write in here let's just call
it test and I press the button the entry widget is going to be disabled which means I even if I click on it
nothing is going to happen although we did update the label so it is still working but after we're
pressing the button it is disabled if you want to know all of the possible things you can do with a widget all you
have to do is call the widget you want to look at and then the config let's
call it configure method without any arguments this is going to return all of the options if you print that
you get what is being returned so let me press on the button and close and expand this a tiny bit in
here you can see all of the options you can work with for example I have used the text and I have also used this state
if I can find it really quick down here so text and State
and well there are quite a few more throughout this entire series I'm going to cover basically all of them for now
don't worry too much about them I'm going to comment out this part to not make it confusing and that was quite a
bit of information so let's do one more exercise and then we can finish this
part what I want you guys to do is to add another button that changes the text back to some text the one that we have
seen in the original on top of that after the button was pressed the entry widget should be
enabled again when we're pressing this button here the entry widget is disabled when we are pressing the other button
the one you are going to create it should be enabled again and pause the video now and try to add
this new button with the edit functionality and see if we can figure it out
let me start by adding the exercise button this is just going to be another ttk dot
button with a master being the window
or the text I just want to add let's call it the exercise button
finally we need a command and the command once again is going to
be a function I'm going to create it right here below the exercise let me call this one the reset function
it does need any arguments and in here I want to do a couple of things but
they're going to come in a bit so I'm going to add pass for now this function I want to call when I press the button so reset function and
also don't forget I want to pack the exercise button on the window if I run the entire thing now I have
never button that I can press but nothing happens that is the functionality we can work on
now there are two things we have to cover number one we have to change the text
back to some text let's work on that I want to get my label once again and in
here I want to change the text and the text I want is some text
that should already reset the label so let me run it and I can write some other
text and press the original button and there we go we have some other text
however now if I press the exercise button we go back to some text the
problem we have is that the entry widget still doesn't work that fortunately we can change quite easily I want to get
the entry widget in here I want to Target this state and this state I want
to set to enabled I can run the entire thing again I can
write whatever I want in here I can press the button and now the entry widget is disabled but if I press the
exercise button we have some text again and I can work with the entry widget again and write something else and now
once again if I press the button we go back to the enter widget disabled and we have updated the label and this I
can do as often as I want and with that we have added a fair bit of interactivity to our app it's not very
much but at the very least it's a start although in the next part we're going to make all of this significantly more
powerful in this part we are going to cover TK enter variables and this is
what you probably want to use most of the time to make widgets interact with each other
tkinder has a bunch of inbuilt variables and those are designed to work really
well with widgets what that means is that these can be automatically updated by a widget and they can also update the
contents of a widget but fundamentally we are still talking about basic data structures like string
integers or booleans for this part I am primarily focusing on a string just to
keep things simple but well so far this probably doesn't make too much sense so
let me give an example let's say we have a label and an entry and both of those should always have the
same text whatever I'm writing inside of the entry is also going to be the text of my label coincidentally that is
actually what we are going to make let me show you actually the project we are going to build is going to look something like this in here whatever I
write in the entry is going to be the text of the label
so those two widgets are very closely connected and this we couldn't do so far but we
can do it quite easily using a tkanta variable basically how it works is we are
creating a string variable so a ticket a variable that stores a string and this
variable automatically gets the value of the entry and it automatically sets the value of the label that way both of
those are always going to be connected it's not part of the slide but a stringvar also sets the value of the
entry so if you had two entry widgets they could also be connected using a
string variable I think all of this is going to be much easier to understand when we actually implement it so let's
have a look at this encode and let's see how far we get here is a nearly empty python file I have imported tkinter and
ttk with that covered I want to create a window and I want to run the window
this we have seen a couple of times by now I want to create a window variable and in here TK and TK
I guess while we're here I also want to set the title of this thing to tkinter variables
once we have that I want to run the main Loop and if I execute all of this we can
see a basic window it doesn't do very much right now but it's a start so with that I for now want to create
two different widgets I want to create a label and I want to create an entry
widget and once again if you want to practice create and pack them on the
window yourself but in my case both of those are going to be ttk
one is going to be a label the other is going to be an entry
although besides that both need the same Master which is going to be the window the label however needs some kind of
start text let me call it label for now it doesn't really matter we are going to change it
very soon anyway and once we have that I want to pack the label and I want to
pack the entry and let me add a tiny bit of white space run the entire thing and there we can
see we have a label and an entry field although they are not connected right now and for that we need a teak and a
variable this I want to create in a separate section in here I want to have a t cantare variable this you create
with TK and then you need the name of the variable you want to create the one
I want to create is going to be a string variable and this you have to call it's a
separate object this object I want to store inside of a separate variable I'm going to call this one a string VAR
and besides a stringvar you also have an INT VAR you have a double VAR and you
have a Boolean VAR depending on what value you need but
stringvar is what I'm going to use for this video for the next part when we talk about the buttons I'm going to use
other kinds of variables as well how this is going to work is that this string bar is going to contain some kind
of string and when we pass this into the label it is going to overwrite whatever the text is so for example if inside of
this string VAR we have a low then this hello would overwrite the text
on top of that we can also connect the string VAR to the entry and this would
mean that the entry widget overwrites this string bar which means this widget
and this widget have to be connected to this string VAR and for that we have
another named argument it is called text variable both a label and entry have the same one
so in here I want to pass in the string VAR and that is actually all we need if
I run the code now you can already see one change let me expand the window a tiny bit
we used to have a label here and it disappeared the reason why it disappeared is because the string VAR
doesn't have any value right now so the label does exist but it's empty so we can't see it however if I start typing
in here you can see the label text again
and the reason why this is working is that both the entry and the label share
the same data and this is a very powerful system what you can also do is let me create another
entry I can just copy this one and call this entry 2 and entry 2. and if I run
the code now again we have two entry Fields if I type in the first one
the second one is also updated and if I update the second one the first one is also being updated the reason for that
is that these three widgets all share the same string or string variable and
that way whatever sn1 is going to be in the other as well and that is a really
powerful way to connect different widgets it's super super useful what you can also do is set a start value for
this string VAR this you do by adding one argument that is called value in here we can set basically whatever
you want for example in my case I want to go with start a value now if I run
this again we have start value as the start value for all of the fields and for the label
although I can still change them to whatever I want in this case though I don't want to use
the start value but this is something you could do on top of that what you can also do if I
get rid of enter widget 2 and instead create another button this is going to be ttk button with Master being the
window and for the text let's go with button this button I have to pack
and if I run the entire thing now we can see we have a button it doesn't really do anything right now
for that I want to create another function let's call it button function
again we don't need a parameters and in here I want to print the content of this
string variable and this we can do quite easily because the string variable has a get method
which means all I have to do is add the command named argument for my button and
pass in the button function and now I can run the entire thing again and let me type and test it here the
label still updates and if I press on a button we also get test we can also write something else and if
I press the button again we get write something else finally there's one more thing that I do want to cover and that
is you can also set the value of any of these variables let's say after I press
a button I want to set the value of this string VAR to button pressed this I do
with stringvar and set and in here I just want to add the value I want to set
it to button pressed in my case if I now run this thing
and let me write just test test test and if I click on the button we get button
pressed and you can also see this is updated in the entry and in the label as well
because these two share the same data and with that we have taken the variable
although I think it might take you a couple of minutes to get your head around it but once you understand it
it's super useful and really powerful to connect different widgets and ultimately a much better system than using get
basically any widget in tkinter either has a text variable or just a variable
we're going to see quite a few more in the next section but before we get to that I want to do some exercises
specifically I want you guys to do this I want you guys to create two entry fields and one label that should all be
connected via a string variable also set the start value of test and
well that should be all you need and pause the video now and try to implement all of this
let's get started by creating another TK string VAR
this I want to assign to the variable let me call it exercise
VAR and in here we already want to set a start value now this you could do in two
different ways you could either get the exercise bar and set
it to the string test or you could set a start value so in
here the value is going to be test both of those are going to get you the
same results so let me stick with this one it's a bit more concise once we have that I want to create two entry fields
and one label and there should be one label
so let's say entry one and entry two
since they are both going to be identical I can just do this by copying the text I want to have ttk dot entry
then Master is going to be the window and the text variable is going to be the
exercise VAR and then I also want to pack both of them although this should be one and
this should be two finally I want to create a label and let me call this the
exercise label and I am very bad at spelling exercise
but for this one we need TDK and label Master is going to be window I'm going
to say that a lot we don't actually need a text here all I really care about is a text variable
and this is going to be the exercise of r finally I want to pack this label
and with that we should actually be good to go if I run the code now you can already see we have two entry widgets
and a text or a label widget and all of them have tests if I change the test in
either of the entry widgets we get something else once again this is working because they
all share the data which means if you update one you update all of them and with that we have string variables it's
super powerful Concept in the next part we will talk about buttons and then there this system is going to become
even more powerful so I'll see you there in this section we are going to create some buttons specifically we are going
to create this app here we have the normal button this one we have already seen then we have checkbox buttons and
we have radio buttons how they work in detail I'll explain while I make this section but these are the main buttons
we are going to work with so there are three major kinds of button we have a button a check button and a
radio button and a really important thing here is that to use them properly you are going to need teak into
variables there's stuff I have covered in the last section but well let's Jump Right In and let's have a look here I
have a new python file and I already have some imports and I'm creating the basic window the last thing I need is I
have to run the entire thing and this I do with window dot main Loop
which means if I run the entire thing now we can see we have a basic window I do want to make two minor changes first
of all I want to create a title and I call this one just buttons besides that
I also want to set the geometry of this app there's no particular reason for it
I just think it looks better I want to set the width to 600 and the height to 400. if I run this now we have a
slightly larger window which means now we can work with the buttons and let's start with the most basic button this
one we have already seen let me just create it again I want to have a button and this I get with ttk DOT button once
again we need a master and this is going to be the window now I have used this named argument here
quite a bit and you don't actually have to use that instead what you can do is just pass in window or whatever Master
you want to have for this widget as the first argument in here the first argument is always going to be the
master that way you don't have to write so much besides that for the button you need
some text for the name of the button let's say a simple button
finally we have to pack the button so we can see it and there we go we have a
simple button that we can click on although right now since the button doesn't have any function attached to it
it doesn't do anything that we can change quite easily and let me put the function right below the button so I
keep everything organized I want to create a function let's call it button function in here we don't have any
parameters and I just want to print e basic button
this I now have to attach to this button via the command
so in here I want to pass in the function if I run the entire thing now I can
click on the button and we can see a basic button besides that instead of using a proper function here you could
also use a Lambda function like so so Lambda and print and we have a basic
button running this again once again I can click on the button and we get the same result once again if you don't
understand Lambda functions definitely check out a dedicated video for it it's really important to understand for gui's
I am going to use it quite a bit you might be wondering what if you have a function let me return to button
function what if you have a function with parameters How Could You incorporate that because
when we are calling the function here we can't call this function so we couldn't pass in arguments
if you understand how functions work this should be quite easy I'm going to cover this in the next section in a bit
more detail for now just think about it and maybe you can figure it out already it's not that difficult but well this is
all we need for the basic button we have seen all of this already so there shouldn't be anything new so far
although there's one more thing that we can do and that is the button can also have a text variable
let me create one as a separate variable I once again want to have a TK and is string VAR don't forget to call it and I
want to assign it let's call it button string and this we can pass in
here for the button string if I run the entire thing now we have an
empty button the reason for that is that this button string is now overwriting
the text and since there's nothing inside of the string VAR we have a button without any text so it looks like
it's just a basic button that we can change by setting a basic value for the string
bar I'm going to call this one a button with string VAR and let me fix the typo there
we go if I run this now we have a button with stringvar and this is basically all
you need for a basic button it really doesn't do that much more later on when
we talk about layouts and styling there's going to be a bit more but for the basic button this is pretty much all
you are ever going to need so with that we can come to the next kind of button and that is a check
button this one let me create a basic check button I'm going to call it check this
one we create with ttk and check button in here as always we're going to need
the master which in my case is always the window then we have the text
like the normal button I want to call this one check box one
and that is all we need for now so let me pack this checkbox and see what we
get there we have checkbox one and in here I have a checkbox I can click and unclick
this also I click this quite fast away if I restart this by default we have
this other kind of value which is I guess neutral besides that we have on and off but once we click on it we can't
go back to the neutral position another argument you can pass in here is command and this works like in the
normal button meaning you could just add any kind of function you want in my case I'm going to go with Lambda and just
print check button this function is going to be run every
time we are pressing on this check button let me run this again and now anytime I am clicking on the checkbox we
get check button which is pretty useful and now you might
be wondering how could we get the value or in other words how do we know if this check button is on or off
we couldn't do something like check dot get if I run this and click on the checkbox
we get the check button object has no attribute get quite unfortunate so we couldn't use
that one let me undo all of this and I just want to print the word check button to store and check the value of
check we need a tkinter variable here I want to have a check VAR
the value here is actually quite open-ended we could for example use a TK string VAR
the one we have already seen and this we now have to connect to this checkbox and that we do I guess I could
put all of this over multiple lines so it's a bit easier to read like so
a checkbox doesn't have a text variable instead we have just a variable
and this is going to work the same so in here I want to add my check VAR the
reason why it's not called text variable is because this variable doesn't set the text of this checkbox
instead the check bar is going to store the value if this box is ticked or not
and that I can now check so whenever I'm clicking on this box I want to get my check bar and now I can use get
if I run the app now you can see we already have one difference and that difference is that this box right now is
not neutral anymore instead it is empty or unticked and if I click on it
we get one or we get zero and those values since we can only store
string vars is going to be a string I guess I can demonstrate this the value we get
returned I want to put inside of type and if I run this again click on the checkbox we're getting a string returned
it only looks like we get zeros and ones but we are storing them inside of a string variable so they are being
converted to a string although that doesn't have to be because we could instead of a string VAR use an INT VAR
the result is going to be the same if I run this thing now and click on checkbox we still get zeros and ones
however now if I use type on what we're getting returned once again
what we're storing now are integer values and that should illustrate quite well
that we are working with different data types we have an invar for the tkinter variable and we have a string bar
while those two are different the most basic thing you have to understand is that we're just storing basic data types
of python inside of slightly more complicated containers that's all that's happening here
you could also add in here a Boolean VAR and if I run this we have the same
result except now we're getting Boolean values and this might be the data type that makes the most sense here so if I run
the same thing again we're getting true or false depending if this thing is ticked or not and this is why it is
really important to understand taking their variables to work with buttons or the check button if you want to check
the value you basically always need a tkinter variable for Simplicity for this
one I want to keep on working with an integer variable this one let me run this again we are
always getting once or zero although we could change that because inside of this
we have what is called an on value and we have an off value
and those well I think they're quite self-explanatory on value is the value
that's being returned when this value is turned on or when the box is checked this in our case should be a number
because we are working with integer for the storage let's say the on value could be 10 and
the off value could be 5. if I now run the entire thing again I can click on the checkbox and we get 10
and 5 depending if it's on or off or checked or unchecked and if you want to change the start value you would have to
work inside of the intvar so in here if I set value to 10 and run it typing
again now the Box by default is checked cool so this is working quite well which
means now we can work on the Third Kind of button and that is going to be a radio button or rather radio buttons
because you basically always want to use multiple I want to start by creating Radio 1 and this we get with ttk DOT
radio button for this once again we need a master which is going to be the window and then
we need text and this I want to call radio button one since I do want to have two radio
buttons I'm going to duplicate this and change to 1 to a two both for the name and for the variable and now I just want
to pack Radio 1 and Radio 2 so we can actually see them like so and if I run
the entire thing now we have two radio buttons but now you can see something weird let me restart the entire thing so
I can explain what I'm doing right now both radio button 1 and radio button 2 are unchecked but if I click on
either of them all of a sudden both are being ticked so something weird is happening here this
super important thing you have to understand about radio buttons is that each of the widgets has to have a value
that is going to be just another named arguments so in here we have a value the
value here could be basically anything let's say for the first button I want to have a radio 1 and for the other button
I want to have the integer 2. now if I run this again I can click on each button and they don't trigger together
anymore if you don't set a value the default value is going to be zero and if
you have the same default value for every single radio button tikinder gets a bit confused you basically always have
to set a custom value here now other than that you can use this radio button like the buttons we have
seen already which means you could also add a command like so and this once
again could be just a function or a Lambda function let me go with Lambda because all I want to do is print
something and there's something I want to print is the value of this radio one and once
again I want to put all of this over multiple lines so things are a tiny bit easier to read like so
we once again have the problem that we couldn't use Radio 1 dot get if I run
this and click on radio button one we get that the radio button object has no attribute get instead what we have to do
is kind of the same thing we have done for the check variable we once again have to create another let
me call this one a radio VAR we have to create a t kinter variable and for this
one we have a bit of a problem because the value for this one is a string and the value for this one radio button 2 is
an integer the best way for that I find is to use a string VAR and this one is going to
convert any kind of integer into a string and that way you can work with it
and this you have to set as the variable or this radio one button so radio VAR
there we go and now you can use the radio VAR and get the value meaning if I
print the entire thing and I click on radio button one we get radio 1. that is the value we
specified in here for the value so far we basically have a check button
what makes radio buttons different is that the idea is you have this takened a
variable in multiple radio buttons let me add it for this button here radio
button two I want to have a variable as well and this is going to be the same radio variable
which means that this radio button and this radio button are both connected to this radio bar here
which by default isn't particularly useful if I run the entire thing again I can click on one and we always get radio
1. where this system becomes really useful is when I get the radiovar from
somewhere else let's say all the way in this button function I want to print
radio VAR and get the value if I now run the entire thing again
I can click on radio button 1 and click on the button we get radiovar again and
if I click on radio button 2 we get 2 or the value inside of radio button 2. and
the really important thing here is if I reorganize everything a tiny bit the basic idea of a radio button is that
only one button is ever activated meaning we could have multiple buttons and only one of them would ever be true
and then the value is going to be stored inside of this ticket variable and we
could get it for example with a button a checkbox is different to that because
inside of a checkbox you can have multiple values that are ticked or unticked whereas for a radio button only
one value is ever ticked I can actually demonstrate this as well
if I wanted to create a second checkbox let me create one right below I want to
have check two and let me be consistent with the naming here this check should be a one and a one here
check 2 is going to be another ttk check button
the master is going to be the window the text is going to be check box 2.
and let's say for the command I want to have another Lambda function that for now it's just going to print
test and all of this I also have to pack so check two dot pack
if I run this again now for the checkbox we can have multiple values and each of
those are essentially self-contained whereas for the radio button we only have one value ticked this is
quite different although that being said if you really wanted to you could connect those two
check buttons quite easily using the check bar for example if I click on check bar instead of printing something
I could also get check VAR and then set the value to the off value
let's say a 5. this would be 5 in this case I can now run this and right now checkbox one is ticked but if I click on
checkbox 2 checkbox one is not ticked anymore and I can retick it and click on
checkbox 2 checkbox one will always be false that way you can connect these two
buttons if you want to but by default they are not connected whereas for radio buttons they are always connected
although the connection here happens via the tkanta variable and then here sometimes you can get into minor
problems for example if I set the value to 1 for both of them and run the typing
again if I now click on one of them both are going to be ticked because they both have the same value
what basically happens is ticket that checks what is inside of the string variable right now this could be a one
and then it checks if this value is identical to the value inside of each widget if it is it's going to check this
radio button if it is not it is not going to check it so if these values aren't unique you are
going to have some slightly weird Behavior something you do want to keep in mind but other than that this is kind of all
you need for the radio buttons so with that we have radio buttons we have check buttons and we have the basic buttons
with that I want to do an exercise and then we are done and the exercise here
is going to be a tiny bit more extensive let me copy and paste it in it's going to look like so
I want you guys to create another check button and two radio buttons and they are going to be very connected for the
radio button each radio button should have the value A or B if you click on
either of the radio button you are printing the value of the check button the one you're going to create in a
second and also if you take either radio button you're also unchecking the radio button
so as soon as you click on the radio button you get the value of the checkbox and you uncheck the checkbox
and then for the check button if you tick the check button you print the currently selected value for the radio
value also you want to use a t Kanda Boolean value for the check button try
to implement all of this yourself and see how far you get
first of all I want to create the radius and let me call this exercise radius so it's a bit easier to read now
in here I want to have exercise Radio 1 and I want to have exercise radio 2.
both of those are going to be created in basically the same way I want to have ttk and radio button
the master as always is going to be the window then we have text and in here let
me call them radio and this is going to be radio a and Radio b
that way we have a bit of an indication if we're working with a or b to actually get that value we have to set well the
value and this one is going to be either a or it is going to be B to store this value
we need a tkinter variable let me call this the radio string
and this one is going to be TK string VAR I'm going to use stringvar because A and
B are both going to be strings if they were zero or true or false this would be
a different kind of teak inter variable Auto stringvar is the one you're probably going to use the most
besides that I want to create a function that we can work with and this let me
call it radio function in here no parameters and basically what I want to
do when I'm clicking on either of these I first of all want to set a command so
I'm connecting them with the radio function like so when I'm calling this function however I
want to get the current value of the check button and I also want to untick the current
check button the problem we have right now is we don't have a check button so we have to
create that one first I want to create an exercise check and
this is going to be ttk and check button in here we need a window the text is
going to be the exercise check and this one is also going to need a variable and
this one is going to need an on and an off value and we don't have to set an on on off
value because 0 and 1 is perfectly fine here and there's one thing I did forget because we are not placing anything on
the window right now which I can do with exercise Radio 1 dot pack then exercise
Radio 2 dot pack and then the exercise check dot pack
and that is some atrocious spelling before I'm running this I want to add
paths inside of the radio function so we're not cutting an error writing this now we can see we have a few more things
so something is definitely working we now just have to give it some proper functionality
and the first thing we are going to need now is to actually add ticket into variables so we can work with all of
this the exercise radio already has a string variable although I didn't connect it to it this we can do all the
way at the end we need a variable and a variable is going to be the radio string
the one we created here and let me put
the entire thing like so we have our data we have the widgets
and we have the layout I think that system makes the most sense
besides the radio string I also want to have a check and this is going to be a
Boolean value because remember in the exercise we want to use a t content variable for booleans
which means in here I want to have TK and Boolean VAR this Boolean VAR I now
want to place inside of my exercise check and here I need a variable and this is going to be the check
Boolean variable with that I can access the value inside of my radios and inside of my check buttons which means I can
finally work on the radio function in here I want to get the value of the
check button that is currently selected and I'm just going to print it so we're going to keep things simple
I want to get my check Bool and I want to get the value
and that is all I need for that part if I now run the entire thing again and I click i1 radio a on Radio b we are
getting false and that seems correct because the exercise check is not checked right now if I do check it and click on either
radio A or B we're getting true so this is looking pretty good next up I want to set the value of the
check button to false that way it's not going to be checked this I do with checkpool and set
and in here I want to pass in false if I run this again now I can click on
the exercise check and if I click either on radio A or B it is going to be unchecked
so that is going to cover the first part of the exercise for the next part we
have to work on the check button and we only really have one bit left and
that is that ticking the check button prints the value of the radio button value that is going to be so simple we can do
all of this inside of a Lambda function so in here I want to have Lambda and this is going to print the radio
string and I want to get the value the last thing I need is this should be
command and this is going to be very hard to read let me put all of this over
multiple lines like so I assume you have a much better monitor
than I do so you probably don't have to do this but in my case I want this to be visible
on even smaller monitors so I'm a bit more constrained
there we go this is a bit easier to read we have our exercise Radio 1 Radio 2 and
the check and the check now has a Lambda function that prints the current value of the radio buttons so I can run the
entire thing and now if I click on let's say radio a I have the exercise to check and I can
do this for B and we get B this is working pretty well and with that we have the different
kinds of button at least the basic ones that you can work with in tkinder on top
of that I think you have a pretty good understanding at this point about teak and their variables I am going to keep
on using them quite a bit so definitely make sure that you have at least a basic idea about how they work there's one
more topic I do want to cover and that's going to be a shorter one and that is functions with arguments inside of a
button and the keynote among you might have seen we have already fixed all of
this because when we called The Print function this one here we literally called a
function with an argument and this one was only executed when we are actually pressing the button which means with
this Lambda here we can call functions with arguments inside it's literally as
simple as that although alternatively you could also create a function that returns another
functions and have arguments via that so let's explore both of those
here I have a python file if I execute this you can see we have a basic tkinder
window it doesn't do anything right now but I want to add two widgets let me add
a comment here I want to have an entry this once again we get with ttk DOT
entry this one is going to need the window as the master
and I want to pack this entry widget besides that I need a button this I get
with ttk DOT button and here we need the window as the master and for the text I
just want to have button this button I also want to pack if I call this pack and execute it we
get an entry widget and a button and basically what I want to do is
this button should have a command that enables us to call some kind of function
let me call it the button function
and this button function needs to have an argument the argument is going to be the content
of this entry widget to get the content we could use get here
but I want to do this properly so I'm going to create an entry string and this
is going to be a TK string VAR variable and let's set a start value to test
this entry string I now want to pass into this button function when we are
calling this function although the function doesn't exist right now so let's create it all the way
at the top I want to create a button function this now does need to have a parameter
let's call it the entry string all I really want to do in here is to print a
button was pressed on top of that I also want to print entry string dot get with
that we have a basic setup and try to think ahead if I were to
execute all of this what would we get I suppose the best way to find out is to
actually run this program meaning if I execute the code we can see in the bottom left we already have a button was
pressed and test which is if I move this widget to the
side this is what we have gotten from this function the problem is we got it
without pressing the button on top of that if I press the button
as much as I want nothing is going to happen so let's talk about what the problem
here is the problem with this line right now is that python executes the code from the
top to the bottom like so that should be fairly obvious and when it comes to this
line here it sees a function and since we are calling this function with this
bit here python is executing all of this
which means we can see a button was pressed and we can see the value of this
string variable here the issue then however is that this
function is going to return none because we don't Define a return value as a consequence the value that this
command is going to get is a none which doesn't do anything
we don't get an error but when python tries to execute anything here it's getting command none and simply nothing
is going to happen as a consequence of all of this we can see these two values when we are starting the program and
afterwards nothing happens when we press the button and well there are two ways to fix this issue the easiest one the
one that you are probably going to use basically all the time is you just wrap this function inside of a Lambda
function this Lambda here tells python to only execute this code when we are
pressing the button the reason why this works is that this Lambda function by default is not being called and then the
Lambda function itself returns this function and then this is what the command value sees which means now if I
execute the code we can't see any value and if I type in here and press on the
button we can see a button was pressed and test and I just saw I made a mistake
because this entry widget needs to have the text variable
like so and this should be the entry string now let's try this again
now we can see test inside of the entry widget and if I press button we can see a button was pressed and test on top of
that if I change the value in here to something else and press the button again now we get a button was pressed
and something else meaning this is working quite well and if you understand return values and
functions this should be fairly straightforward although you could make it more explicit
so let's say that you really do not want to use a Lambda function and you insist
on using a function that you can call like this if you insisted on doing that you would
have to create two functions wrapped inside of each other let's start with the outer one let me call it outer
function and this one is going to have a parameter let's call it parameter inside
of this function we're going to Define another function and this one I'm going to call the inner function
this one doesn't have any parameters and this function is actually going to execute the code and here I want to
print a button was pressed and on top of that I want to print the
parameter which in this case is going to be this entry string which means we can
run the get method on it once we have that all I have to do is to
return the inner function and with that down here I can call the outer function
and this should still work meaning if I run the code now nothing happens that's a good start and
if I click on the button we can see a button was pressed and test and if I change the text to something else this
one is also going to work when we come to this line here python is
going to execute this function so we are executing all of this inside of this
function we are creating another function this one is going to get a simple string and print it that one's
quite easy and it also gets the value from the parameter which is the one we created down here the important part is
this return in a function because this is what's being returned to the command
argument so when we press the button this is what we actually get
once again if you understand functions and how they exchange values with return this should be fairly straightforward
so I hope that was helpful and most of the time you don't really have to think about it too much if you want to call a
function with an argument you just use Lambda and then the function you want to call with the argument in this case the
entry string that way all of this works perfectly fine let's talk about event binding
first of all what does that even mean and events can be lots of different things the most common one are keyboard
inputs although an event can also be a widget getting changed in which you're getting selected or unselected or a
mouse click motion or wheel all of these are different kinds of events and what
is super useful is that these can be observed and used for example you could run a function when the user is pressing
a button that is the main idea of an event and events are very easy to use
basically all you have to do is to bind an event to a widget this could for
example look like this we have a widget and then we use the bind method and then we have the event and the function the
event format is always going to be modifier type and detail for example if
I wanted to check alt and the a button I would go for ALT key press and a and
once we have that we can run whatever function we want to use so that's all we need let's have a look
at all of this here I have a tikenter file and I
already have a couple of things if I execute all of this you can see we have a text field we have an entry widget and
we have a button although there's no interactivity right now nothing is going to happen and what I want to add is a
couple of events there are quite a few I am just going to give some random examples
but let's get started slowly and let's do a basic example I want to get my
window so the main widget and on this I want to run the bind
method in here we need an event and we need a function for the function I'm going to keep it
simple and just use a Lambda function and this one is just going to print
n event for the event we have to get the proper
format and this is always going to be a string inside of that string
we need the modifier we need to type and then we need detail the example I gave
in the slides was if you want to check for the ALT key a key press
and then the a button there's just one more thing that we have to do and that is this thing needs to be
enclosed in a smaller than and greater than sign it's a bit weird I don't know
why it's necessary but you kind of need it every single time also this is key press with an uppercase
p with that I can run the entire thing and if I have the window selected and I
press alt and a we are getting an error and that is that Lambda takes zero
position arguments but one was given which means when we are calling this
function here tick enter automatically inserts one argument in there which we do have to
capture that we can do quite easily with Lambda we just have to add event here and now
this should be working again with the window selected I can press alt and a and now we get an event
yes I can do multiple times and with that we have keyboard input and just for detail let me print this
event to see what we get so I want to print the event if I run this entire thing now and I press alt a
we are getting an event that has a couple of attributes
for example it tells us what the current character is it tells us the position on the widget and that's kind of all we
really need this bit here is the only really important part if you understand this system here it is
pretty straightforward and there are quite a few different events that you could be working with
there's a very good website that accounts for all of them that one looks like this I'm going to add a link in a
second and in here if you scroll down you have a list with all of the events
you could possibly work with and well in here you have for example the F keys you
have the keypad and well you have lots of other things that you could be working with
that is basically all you need to understand the basics so with that in mind let's play around with this a tiny
bit more and let's create some more events although before that there's one important thing that this event right
now checks if we are anywhere on the window and pressing alt and a however I
could also change this to only work with the button and I just realized that I changed the naming Convention of the
button here a tiny bit let me fix that this should be button properly spelled
both is fine I just want to keep things consistent now we have an event that is connected
to the button so what does that mean and I think it's best to explain this when I
actually run the app here we have the app and if I now anywhere on this window press alt a nothing happens however if I
press on the button and now I press alt a we get the event back if I click
inside of Entry I press alt a nothing happens what you have to understand here is that
if we are clicking on the button tikenter selects that button and only if that is the case we are running events
on this widget and if we don't have the widget selected we are not running any kind of event on it so that's an
important thing to understand here a really good way to visualize all of this is to use window.bind and in here we can
check for one event that is called motion and now for this one I want to
create a separate function let me call this one get position once again remember you do not want to
call this function instead I want to create it get position
and this one needs to have one parameter it always needs the event
and what I want to do in here is to print an F string that is getting us the X position and
this we can get with event.x and besides that I also want to have y and this is
going to be event dot y let me use some semicolons in here
that way this is going to look a bit cleaner and now every time I am moving the mouse tikanta is going to tell me
the position of the mouse so let me run the entire thing and show my mouse now
you can see wherever I am on the window we have the position of the mouse if I go all the way to the top left we have 0
and 0 roughly here and all the way in the bottom right we have 599 and 499
which is basically the window Dimension -1
and with this you can get the mouse position wherever you are on the tkinder widget which can be super handy
however one important thing you do have to understand here is that right now we're doing all of this on the entire
window if I change this to only work with the text so the text field we
created up here and run the entire thing again if I keep my mouse on the bottom of the
window nothing is going to happen only if I start to hover over the text widget we can see the position and this stops
once I leave the text widget depending on what widget you bind the event to you
are going to get different results well obviously I guess the way you have to understand this is that TK enter only
checks the event on the currently selected widget although the window is always selected
another useful thing to consider is that you don't necessarily always need this
entire format sometimes for example you just want to check for any kind of key
press you don't really care about what specific key or what modifier you just want to check any kind of key press
if that is the case let's actually check for it I want to get my window I want to
bind an event and in here I just want to check for a key press
nothing else if that is the case you could just add key press and don't worry about the
modifiers so let me add Lambda event and I want to print
a button was pressed I can run this now and now if I press
any of the buttons we get a button was pressed and I'm still getting the input when I
move the mouse all of this is working just fine I suppose we could make this a bit more
elaborate by turning this into an F string and in here we can get event and
character if I run this now I can press any button and we can see what I have pressed that
way you can always capture anything on the keyboard let me move this key press right below
here so the entire thing is a tiny bit more organized finally there's one more thing that I do
want to cover let's say we want to check if the user has selected the entry field and then we
want to run some code this we can also do I want to check my entry widget and
in there I want to bind an event that is called focus in
and this once again is going to be a Lambda event and I just want to print entry field was selected
and before I run this let me comment out all of this so we can see a bit easier what's going on
so if I run it and now if I select the entry field we
are running this statement here which gets us an entry field was selected
I can do this multiple times so if I click on the button and return to the entry field we get the entry field was selected I
can still use it as normal but now every time I select it I get a function that I can use for whatever purpose
this also works the other way around with Focus out and then here I have an entry field was
unselected let's try this one now and now I have to field selected and I have the field
unselected pretty simple but very very powerful once again check out the website it
covers all the options that you could ever need so any kind of event is going to be covered in here and you just have
to look for what you need let me put the list actually all the way
on the top here so it's very easy to find you can also find it in the notes to this part
and alright there's one more thing that I want to do and that is going to be an
exercise and upon is going to be I want you guys to print Mouse wheel
when the user holds down shift and uses the mouse wheel while the text is selected the text being this text box
here and for that you will need the website so check it out and then try to
figure out this kind of event pause the video now and see if we can figure it out
obviously we have to start by getting our text widget in here I want to bind
an event for the event we need a smaller and greater than symbol and now we have to
figure out how to combine shift with the mouse wheel let's open the website for that
in here first of all we need a modifier the modifier is going to be shift so
that one is easy I'm going to start by adding shift in here then I need to Dash and now I have to
figure out the mouse wheel for that let me use a text search I want
to have a mouse wheel there we go this one is very easy to get
which means all we have to do now is add a mouse wheel here and then we are good
to go I can then add another Lambda function with event and all I want to do is to
print Mouse wheel like so and this should be all we need
if I run the code now and I use the mouse Wheel by itself nothing happens but if I hold down shift
and use the mouse wheel also nothing happens because my mouse isn't over the text field but if I'm
over the mouse field and I use the mouse wheel we get mouse wheel meaning this is working really well and
this is basically all you have to know about events it really isn't that complicated the main issue here I think
most of the time is figuring out the proper format for the event but if you play around with this for a bit it
should be fairly simple in this part we are going to learn about two new widgets they're called combobox
and spinbox and let me show you what we're going to make it's going to look like this this is the app for this part
and a combo box is basically a drop down menu in here I can select different items and then I can also get the item
and place it for example inside of a label is spinbox is this kind of selection
menu entry thing where I always have predefined values this could ever be a
number or it could be a letter or literally anything else so this is what we are going to create and it's not that
hard to make all you really need is a basic widget and you have to assign a list of values
to this widget and also you can connect a teak into a variable to select this widget and use it for basically anything
else that is all we need so let's jump into some code and let's have a look at this
here we are in the code and I already have a few lines of tkinder code if I
execute all of this we can see a basic window by now all of this should be
fairly familiar and I want to start by creating a combo box
this we do with ttk DOT combo box in here as always we are going to need a
master which in my case as always is going to be the window on top of that like any other widget I
want to assign the widget to a variable let me call it combo once we have that I can pack this combo
box fix my typo and run the code and there we can see a drop down menu
although right now it doesn't have any values to get the values we need some kind of
list let me create one let me call it items and this is just going to be a
list and I think for the demo I used ice cream I had
pizza and I had Rocco Lee you might notice I am recording all of this right
before lunch but this list I now want to assign to this combo box and this we do
well we can do it in a couple of different ways the one you probably want to use is by going with values and then
here assign the items if I run the code now and I select the
drop down menu we can see the different items in here this one is working pretty well
alternatively besides disk values you could also use either config or configure and then here
you can set the values to whatever the items are like so this line and this line do the
same thing which means I could comment out the first one run this again
and we have the same items in the drop down menu as always I would recommend this one here because it is more concise
but both options are perfectly valid besides that what you can do is to
create a ticket variable let me call it the food string and this one is going to be a TK
string VAR and this stringvar you can assign to this combo box with a text very bill I
want to assign the food string although if I run the entire thing by default nothing is going to happen
which means the box is empty when we start the app the reason for that is that we don't set a starting value for
this food string that is quite easily changed all you have to do is set a starting value and I want to get the
items and select let's say the first one that way on Startup the selected item
should be ice cream let's try and there we go we have ice cream in here and we
could select something else still this works just fine and for the basics of a combo box this
is basically all we need although there's one more really cool thing that you can do and that is events for a
combo box like we have seen in the last part you can get the combo box like any other
widget and bind an event to it and then run a function and the combo box has one special event
that is unique to it and this you call with a double smaller than and a double
greater than symbol and in here you have to type in combo box selected
what this does is it executes a function every time we are selecting any kind of item inside of it let me create a Lambda
function with an event in here and I just want to print test anytime we are selecting an item
inside of this combo box so if I run the code now and I select
Pizza we get test I select broccoli we get test this one is working just fine
I guess something slightly more useful here we could get the food string and
then get the value that way we are going to print whatever value is being selected so right now we have ice cream
then we have pizza and then we have broccoli that way you can extract the values from
this combo box quite easily as always using the TK enter variable with get is
the best way to get any kind of value and pass it around it's fairly simple and this you can now connect for example
to a label and this is going to be ttk and label
with the window as the master and this combo label I want to pack
on the window if I run this we can see that we can't see anything let me add
some text in here so we can see what's going on here we have a label so if I run this again we can see a label
this label I now want to change to whatever is selected inside of the combo
box for this one you could work with the tkinter variable the food string for
example what you could do is set the text variable and set this one to the food string if I run this now we already
have ice cream if I select Pizza we have pizza and if we have broccoli I have broccoli
that is one way to approach it although it's quite limited because we can't influence the string so I don't
actually want to do it instead what I want to do is what I'm clicking on combobox selected I want to get my combo
label and I want to run config on it in here I want to set the text
and the text is going to be an F string with selected
value is going to be the food
string and get now I can run this again by default we get a label but as soon as
we select anything we get selected value pizza or broccoli or ice cream and well
this is basically all we need so this is a combo box and this is pretty much all
you need the main things you have to understand is that all of this is just a widget the main difference compared to
other widgets is you have to create a list and assign this list to the values
other than that you can use it like any other widget with a teak into a variable and then with events although there's
one special event combobox selected so with that covered we can cover the
next kind of widget and that is called a spin box and I realized I have combo box with
lowercase C it should be an uppercase C that kind of annoyed me a spinbox works very very similar
compared to a combo box which is why I covered them in the same bit you are creating it with ttk DOT spin
box and in here you need a master which is going to be the window this I also want to assign to a variable
I'm going to call this one spin once we have that I can pack the entire thing and run the code we have another
widget that is an entry field with up and down arrows where we can select predefined values
and now like for the combobox to assign actual values you have to get spin then
the value and now we need some kind of list this could for example be one two
three four and five if I now run the entire thing we can select between one
two three four and five although since you very often work with numbers inside of a spin box there is an easier way to
get lots of numbers what you have to do is to define a from and really important
here you need an underscore and this is determining the start value let me set this one to a three
completely random values and then you need a two and this one doesn't have an underscore let's set this one to 20.
the underscore next to from here you always need and if you don't edit you're going to get an error there are some
predefined values that you cannot mess with don't forget that it's a very easy mistake to make but once we have defined
this from and to Value we can run the entire thing again and now if I click on
up we get the values from 3 all the way to 20. another thing that you could do in here
is to add an increment value this is essentially the step size for
example if I set this to a 3 run the entire thing again now we are starting with a free but then we move in
increments of three although here you do have to be a bit careful let me go all the way up and I
do reach the highest value of 20. and now if I go down we have 17 14 and
11. so the numbers here are not consistent it's a little bit annoying
basically what tikenter does it tries to go as high as it can get in terms of the two number but if it gets to 21 in our
case with the increment of three it limits the maximum number to a 20. so that way we actually change the number
and the increment doesn't really work anymore it's just something to be aware of it
can be kind of annoying but quite workable there are two more things that I do want to cover the first one is that
there is a command inside of a spin box in here for example we can use Lambda
without any parameters and just print a button was pressed or I guess arrow is
a bit clearer because if I run this again and I'm running this command every time I'm clicking on an arrow
if you want to have a bit more control so you only want to run a function if the user presses up or down you couldn't
use command but like the combo box a spinbox has special kinds of events too
actually we can use Spin and bind and event with a function and the event here is
once again we need a string and now two smaller than and two greater than operator signs inside of this we have
increment and we have
decrement increment is forget when we press the up Arrow decrement when we press the down
arrow and this we can connect to a Lambda event I just want to print
either up or I want to print down now I can run the entire thing again and
if I press on up we get up and an error was pressed and the same with down and arrow was pressed
depending on the level of control you want to have you can either use command or you can use an event both work
perfectly fine finally the last thing you want to be aware of is you can use spin along with
the tkinter variable for example I could create a spin integer
and this is going to be TK and VAR in here you could also as always Define
a start value let's go with 12. this spin integer I now have to connect
to the spin box and for that I want to separate all of this over multiple lines
that way you can see it a bit better in here I want to create a text variable
and this is going to be the spin integer and now we have 12 as the start value
and I can change it like so and this would also update the integer for example if I print the value instead
of an error was pressed I want to get spin integer and get
and now if I run this again and I press up or down we get the various numbers
very simple to work with most of this should be quite familiar at this point and with that there's only one more
thing that I do want to do for this video and that is an exercise I want you guys to create a spin box
that contains the letters a b c d and e on top of that what I forgot to copy in
is I want you guys to print a value whenever the value is decreased inside
of the spin box so pause the video now and try to implement this one
I am going to start by creating exercise
letters and this is going to be a list with a b
c e and e once we have that I want to create an
exercise string and this is going to be a TK string VAR and then here I do want
to have a start value like we have seen in the combo box with this part up here
I want to get my exercise letters and select the first item
once I've all of that I should probably create the exercise spin box
and this is going to be ttk dot spin box in here for the master as always we have
the parent and I want to have a text variable which is going to be the exercise string
let me put this exercise spin on the window widget with pack and now
we already have a start value the problem is let me run this again actually just to demonstrate what's
happening if I start the app we already have another spin box that says a that
happens because of this string VAR here however if I press up we're getting to
zero the reason for that is that we haven't assigned these letters as the values for
this spin box that we can do quite easily you could either get the exercise Spin and then
get the values and assign the exercise letters in here if I run this now I can
go up and down and we get the different letters although if you already know that you
want to have this list inside of this widget you can just when you create it assign the values with the exercise
letters and then I can get rid of this one here and we should have the same
result so now I have the same result that is pretty good
we are nearly done we have covered the first part now we have to work on the second one that I want to print a value
whenever the value is decreased and this we have covered up here I only want to
print a value when we are decrementing the value I want to get my exercise Spin and bind
an event the event I want to bind is going to be decrement
and inside of this I want to get my Lambda with an event and here
I want to print the exercise string and I just want to get the value
that should be all I need if I run the code now and I press up nothing happens but if I press down or I decrement we
get the different letters so with that we are done
and this is giving us two new widgets that are quite useful especially combobox I feel is a really commonly
used widget the next widget I want to cover is a canvas and a canvas is essentially a
widget that allows us to draw various shapes for example we could draw a square a circle lines text and quite a few more
elements in the most basic sense what we are doing is we are recreating paint inside
of tea Kinder or at the very least we have the basic tools to do so I already have prepared some code the
only difference compared to what we've seen in the past is I do not have ttk I only have TK because that's all I need
but if I run this code you can see we have a basic window I want to create a canvas which is one
specific kind of widget this I want to store in a variable that I'm also going to call canvas and in here we need TK
and can this like any other widget this is going to need a master which is going to be my
window once I have that I can pack this canvas and if I run the code now we can't see
anything however the widget does exist the problem is by default it's well
invisible we can change that the easiest way to do so is by giving it a background
in here you could choose basically any color for example I could use white in here if I run it now we can now see a
white background this would work with any other color red for example would look like this
there are quite a few more colors you could be using but I'm going to cover them later but now using basic names is
fine and I'm going to stick with white that's I think the easiest color to work with with that all we really have to do is go
through the different methods that the canvas object has for example one that I think is very simple is called create
rectangle this for the first argument is going to need a tuple and this Tuple is
going to determine the dimensions of the rectangle we are going to draw to make this work we need the left point the top
point the right point and the bottom point
let me actually use the values here for the left I'm going to go with 0 and for the top I also want to go with zero or
the right side I want to have 100 pixels and for the bottom I want to have 200 pixels
and now if I run this we can see we have a kind of rectangle
or at least the outline of one a better way to visualize this is changing these numbers to 50 and 20
that is a bit easier to see so what we have here is a rectangle or
the outline of a rectangle and this one is 50 pixels from the left this side
here and we have 20 pixels from the top that's this part here the right side this one here is this
line and then the bottom 200 is down here we are defining the four sides of
this rectangle and the Kinder uses that to create a rectangle another option we have to make this look
a bit better is a fill color and for this one again you could use basically any kind of color for example red would
be fine and now we have a red rectangle with a black outline
if you want to get rid of the outline you would set with to zero width here
refers to the Border width if I run this now we only have a red rectangle
and well basically now we have a ton of different options that we could be using the best website for that let me open it
this one here it's a little bit old but it still works perfectly fine on this side you have a canvas widget
and the canvas widget you can see has a ton of different options the one I have
looked at already or the one we're working with right now is create rectangles
you can already see in there we have canvas then create rectangle and then left top right and bottom and then the
different options the different options you can find here and you can see there
are a lot I could for example set the width to 10. this one gives us a very thick border
and besides that I can also specify a dash in here we did a tuple that
specifies what is called a dash pattern let me use some random numbers if I run this now we get a certain kind of Dash
what this Dash here means is the first number the one in my case tells me how
long each Dash should be and the second number two in this case is how big the
Gap is which in this case is going to be twice as wide as the actual pixel if I
change this to let's say four and two and run this again we now have a
slightly different look this is something you have to play around with quite a bit to really get the idea
you could even add more values in here let me add a one and a one run this again and now we get even weirder
results but mastering the dash pattern is well something that I'm not too concerned about so do this in your own
time if you are really interested another option we have is the outline
this determines the color of the Border in here once again we need just a color
and now we have a green outline I think at this point you get the idea with this thing it's not terribly complicated and
if you go through the list it's quite easy to work with which means I can work with another one
another very simple option is called canvas and create line
you might already guess what this one is doing it draws a line and then here we need
start X and start Y and then end X and
end Y and other than that we still have basically the same options we have seen for the rectangle let's say I want to go
from 0 and 0 to position 100 on X and
150 on y if I run this now you can see we have a
line oh and I forgot to mention right now I've just used numbers you could also
place all of this inside of a tuple you would get the same result the same applies to the rectangle you could just
have the numbers and everything would still work just fine I just think using a tuple here makes it a bit easier to
read and for the line we could for example use fill again let's fill this one with yellow what's a little bit hard
to see yeah it's going to be very hard to see let's go with blue that is much easier to see
besides that we also have canvas and create oval this one works quite similar compared to
the rectangle we are specifying the left the top the right and the bottom and
then TK enter is going to draw a circle or rather an oval inside of these limitations
although if you have a rectangle with these Dimensions so if I go 0 0 100 and
100 we are going to have a circle like this I want to fill this one let's say with
green there we go we have a circle right now but if I change this 100 to a 300
we have a oval I'm going to change this to 200 so we're not drawing too many
things on top of each other also I want to turn the coordinates into a tuple to keep things a bit more
consistent besides that we also have a create polygon for this polygon I'm going to do
all of this inside of a tuple we always need X and Y positions so we have X1 and
y1 then we have X2 and Y2 then we have X3 and Y3 and tick inter is going to
connect all of them so once again let me go with a point at
0 and 0. then I want to have another point at 100
and 200 and let's say a point at 350.
running this now we have a triangle because the point we have drawn consists of three points
so let me visualize this our first point is 0 and 0 that is the
point up here the next point is 100 and 200 which
means we're going 100 pixels to the right and we are going 200 pixels down
the final point is 350 so we are going 300 pixels to the right and 50 pixels
down and we're ending up on this point which you could see better if I remove the drawing this point here
and in here you could add as many points as you want you can also work with fill
let's say fill we haven't used white yet and for another point I want to have for
x 150 and you could also work with negative points let's say negative 50.
okay that um it works but it's very hard to see let's go with gray
there we go now we have a polygon on top of everything else there's one more basic method I do want
to cover but at this point this becomes fairly repetitive I want to create an arc for the arc we basically start like
we have started for the oval which means I want to put them like this
for these methods we are drawing always a rectangle and then we are filling the rectangle either with a rectangle itself
an oval or now an arc so a partial oval essentially to visualize this let me
actually copy this circle here or the coordinates for the circle and I also want to comment out the polygon so we
can see what's going on if I run the code now you can see something weird on the
circle the green bit here is the circle and on top of that we have this slice cut out
if I fill the arc this is going to be even more visible let's say fill with
red yeah I can see by default The Arc covers one quarter of the entire Square
these numbers you can specify for that you need a start point and this by
default is zero which means if I run this thing now nothing changes however if I change this to a 45 now the
thing looks like this the way you can understand this number is this line here
is angle zero and a whole circle around this well circle is 360 degrees
with this line here being 45 degrees what we have specified here for the
start point and by default The Arc goes counterclockwise by 90 degrees
this we can also change for that we need another argument here that is called extend by default this one is 90 so if I
run it nothing changes if I however I change it to 180 degrees it looks like this
we are starting here at 45 degrees and then we're going 180 degrees around the circle
so this point down here is degree 225. besides that there is one more
interesting argument in here and that is called Style in here we have to specify specific
tkinter options this could for example be TK and now on capital letters Pi slice and let me fix
the typo like so if I run this we cannot see any difference because this is the
default option however what we can do is change this to Arc and if I run this now you can't see
anything because the arc only draws the Border if however I change the outline which is
the Border color to let's go with yellow run this again now you can see very
faintly there's a yellow half circle again for this one I want to change the
width to 10 so we can see it easily there we go now it's a bit more visible
let me actually change the color to Red there we go now this is much more visible
also I want to put all of this over multiple lines
otherwise this is going to be quite hard to read there we go these are basically the main
options you can work with besides Arc and Pi slice you also have chord
running this gets us something like this um I am messing this up with the width let me change this to one
the difference compared to a pie slice right now is kind of hard to see because we are drawing half a circle let me
change this to a smaller number let's say 140 and I want to go with pi slice
running this now I get part of a slice the part that chord is going to change
is it's going to take away this bit here it's going to be easier if I actually
use it so instead of Pi slice I want to have the chord now we can see we are not drawing this bit here anymore that's the
only difference between the two and with that we have an arc and this covers another really important part
besides that you can also I want to comment out everything so you can see
things a bit easier besides all the shapes you can also draw a text
with canvas and create text or this one you have to start with a
position let me go with 0 and 0 and then a text argument this is some
text if I run this now we can see some parts of a text all the way in the top
left up here the problem we have with the coordinate right now is this point here 0 and 0 is
this point but we are placing the center of the text which means the actual bounding
rectangle of the text looks something like this
which is fine in general but right now it doesn't help us too much I'm going to change these numbers to 100
and 200 and there we go now we can see this is some text and once again you can also fill this
thing with different colors let's go with green now we have some green text
another option we could be using is with and this specifies the width of the text
if I change this to a 10. now the width of the text is 10 and tkanta tries to
fit everything inside of this width which means we have a ton of line breaks and once again if you go through the
list you can find a few more options but those are the main ones you could also change the font or if the text is
Justified or not there are quite a few different things you can do here the last important thing that you really
want to care about is you can also display widgets with a canvas which is a
super powerful feature let me use it we need canvas and this is called create window
for this first of all we need a position this is just X and Y let me go with 50
and 100. now we need a window argument and important here this window has nothing
to do with this window up here they just happen to be called the same the idea is
inside of this canvas we are creating a separate tkinder window and this we are using for drawing and drawing in widget
specifically and this window once a t can't have widget for example ttk dot
label and with this I realized I do actually in ttk so let me import it all
the way at the top from tkinter import ttk I should check my notes a bit better for
this one we now need a master which doesn't really matter but we still need it and then we need some text
or the text this is text in a canvas
this one we don't have to pack if I run this now we have this is text in a canvas and once again we are placing the
center of this widget which is 50 pixels from the left since the text itself is wider than that
we are going a bit outside of the bounding box which is totally fine to do just be aware of it and widgets for some
reason aren't being clipped off they are still visible I have no idea why it's just the way it works
I'm going to change this 50 to 150 and now this looks a bit better and this is
actually quite interactive for example besides the label we could also use a button
and this would still work you could even press on the button and execute functions all of this works perfectly
fine as a matter of fact or scrolling through a window you want to use this
method here for the more advanced parts we are going to see this quite a bit it's super useful
and with that we basically have all that we need for the basic canvas widget I'm
going to comment this one out as well and now I want to do an exercise that I think is going to be quite fun
I want you guys to use event binding along with the canvas to create a basic
paint app so wherever the mouse is I want to draw something so when you move the mouse around you can see a line
being drawn so pause the video now and try to figure this one out
for this one I as always want to get my canvas and I want to bind an event the
event I'm looking for is called motion which means I am checking for a movement
of my mouse and if that is the case I want to draw on canvas
this function doesn't exist right now so let's create it Define draw on canvas
in here remember for the parameter we are always going to need one for the event
from this event we can get an X and A Y position so X is going to be event dot X
and Y is going to be event dot y and these points we can use to draw on
the canvas although for that I want to have one more thing and that is the brush size
I'm going to use this in a bit again so I want to Define this as a global variable brush size and let's go with
four now that I have that I can get my canvas and create an oval
we need a left a top a right and a bottom let's say this point here is the
mouse cursor I'm going to call it m around this point I want to draw a
circle every time we are moving the mouse and this point is going to need four different Arguments for the left side I
want to go from the mouse position and then have the brush width which in our
case is going to be 4 over 2 or this number here divided by 2. that is going
to give us the left position the same thing I want to do for the top for this one I want to go up
by 4 over 2 and for the right side I also want to go by 4 over 2 that way the
entire width of the thing is 4 pixels which is our brush size I want to get x minus my brush size over
2. the same thing for y except now we need Y which is going to be the brush size
divided by 2 again or the right side I want to have X and then plus my brush
size over to and finally for the bottom I want to have y plus my brush size over two
that is all I need if I run the code now and I hover over the canvas widget we
have a very basic drawing app it doesn't look terribly good but at the very least it is working
one issue we have right now is that we are only redrawing the outline let me fill this thing with a black
color and now this is already looking a little bit better I think the brush size is
also a tiny bit large I can change this to a 2. and this is improving as well but well
this is a very basic drawing app and you can see here if I move the mouse really fast you can see the individual points
we are drawing besides that another cool thing that I realized you can do is I
also want to create a canvas method with bind and this one is going to be called
Mouse wheel if I'm using that I want to get a brush
size adjust function I'm going to create this here and this
is going to be brush size adjust as always this needs the event and for this one I want to update this
brush size which means I have to create a global variable that is called brush size
and when we are doing this let me print the event to see what we get if I now use my mouse wheel
we're getting a couple of different arguments the one I care about is called Delta if I move my mouse bit forwards
it's going to be plus 120 and if I move it towards me it's negative 120 or
backwards I guess for your mouse these numbers might be slightly different but the actual number doesn't matter I only
care that it's positive or negative which means I can use this inside of an if statement so if the event dot Delta
is greater than zero then I want to increase my brush size
let's say brush size plus equal four and else if it is negative then brush size
negative equal four with that if I run this again and let me
actually show my mouse that's going to make all of this a bit easier to see the drawing still works but now if I scroll
forward we have a much thicker Mouse and if I scroll towards me this becomes very
very small although he can see an issue I am scrolling just towards me and the number gets smaller and smaller let me
actually start this again so right now the line is very thin but now I'm scrolling towards me so the line
should get smaller I'm scrolling quite a bit towards me and more and more towards me and the line just gets thicker
the reason for that is when we're using the brush size here or
these numbers it doesn't really matter if the number is positive or negative the larger the number gets or rather the
larger the absolute number becomes the larger the circle is going to be which means as far as the brush is concerned
20 is the same size as negative 20 or almost the same they are slightly different but the larger the number
itself the larger the brush size this I don't like which means at the end of
this function I want to get my brush size and I want to limit it between two values
for that we can use minimum and this is going to pick the smaller numbers between two arguments
so in here I can have my brush size and the maximum number I want to have is
going to be 50. so let me run this again and now I'm scrolling forward and this
is the largest size that I can have for my brush kind of hard to see but it definitely
works this function I want to wrap inside of a Max function this one works
like minimum except this one selects the larger number and then here I want to have a zero that way our brush can never
go below zero if this number becomes negative the max always chooses the zero so now I can run
this again and I can increase the size and I can decrease it and at the minimum we get this line here
and that is a nice basic paint app you could play around with this quite a
bit more to add colors and we are going to do that later but for now I think this is a pretty good start with the
canvas app the next widget we are going to look at is called Tree View and if canvas is
paint Tree View is essentially Excel or rather we are going to create a table
this one is going to look like this in here we have a bunch of different entries that we can look at we could
also delete entries like so and you can also select multiple entries
and work with them it's a fairly straightforward table that
is quite easy to work with and well that's what we're going to create once again I have some code if I execute
the entire thing we have a basic window the one thing that is new are these two lists I'm going to use them to create
some random names in a bit for now just don't worry about them I want to create a widget and this is called Tree View
this we create with ttk.3 View
as always I want to store this in a separate variable and this I'm going to call table
in here we always need the master which is going to be the window and let me just pack the entire thing to
see what we get by default we're getting a plain white square although if I go to the top we
can already see we have some kind of top row that doesn't do anything right now
that we can change inside of this the idea is that you are defining some columns
for example what I want to do is I want to have a column called first then last
and finally email if I run this now you can see we have
three different columns although you can't see the title right now we have to add what is called headings
so I want to get table and then specify a heading and now I have to get the name of the
column and this is what we specified here the First Column is called first the
second one last and the last is called email which means for the First Column I want
to get my first column and the text in here is going to be first name and now if I
run this we can see we have first name right in the middle to get it to the left side we have to
add another argument inside of the original Tree View and this is called show and then here I want to add
headings now if I run this we get first name on the left side
by default tkinter is showing some elements on the left side or in the
first columns and with this option we are disabling that cool now besides that for the last
column I want to have let's call it surname and then for the email I want to
have the email and with that we have different columns
and then here you could add as many as you wanted and with that we can cover how to insert
values into a table this we're doing with table and the
insert method in here we need a couple of arguments the first one is called parent and this
is usually going to be an empty string what this means is you want this item to
be attached to this table and not have any intermediaries
later on we're going to learn you could also attach this new item to an existing item inside of the table and then you
will get the name of this item inside of the table as the parent but if you leave it empty
you're going to attach it to the main table besides that we need an index and we
need the actual values for the index for now let me go with zero and the values
is going to be a tuple and since we have three columns first last and email we
need three values in here let's call this John what is surname I
want do and for the email I want to have John Doe at
email.com or whatever you want to add in here if I run this now we have a first name a
last name and the email so this is going to create one entry but
I want to create a hundred entries so let me comment this out and instead I
want to create a for Loop so for I in range 100 and I want to use these values
here to create random names for that I'm going to need one more module and that is from random import
choice choice we can use to pick one item from a list
and this could actually be a really good exercise for you it's not going to be the main exercise for this video but try
to create from these names 100 entries and add them to the table and see if we
can figure this one out I want to create a first name a last name and an email the first name is
quite easy I want to have Choice and then first names the same for the last names I want to
choice and pick a random item from the last names for the email I want to create an F
string and for this one I want to have the first name
then I want to have the last name like so and then add email.com
this information we can now turn into a tuple let me call it data and here we are first we have last and we have email
finally I can actually get the table and insert the values
once again for the parent I want to have an empty string besides that for the index
well now I'm gonna go with zero and then for the values I want to have
data now I can run this and we can see we have a table with a ton of different
entries this is looking really good and there's one very quick layout thing
that I do want to do inside of pack I want to fill and add the option here for
both and then expand I want to set to true I'm going to explain those values later
but if I add them we're going to fill the entire widget with entries that looks much better
and obviously you could also change these values as much as you liked so for example in the demo app I don't use the
first name for the email I only use the first letter of the first name so index
0 here and now we have some slightly different email addresses now let's talk about index and the best
way to understand it is if I play around with the value for this one we need parent with an
empty string or the index by default this is going to be 0 and for the values I want to have
something that's easily visible let me go with XXXX then we have yyy and then
we have z z z if I run this now all the way at the top
we have the values that I just specified with this entry here if I change this index to a 1 we are
placing it on the first index So Below the first element
and this I can keep on doing three we have three items on top and so on
the question now is if you wanted to add an element at the end of this table how could you do it I guess in our case we
know there are 100 elements so I could add 101 in here and now all the way at
the bottom we have the entry I just created but
sometimes you don't know the end of the table and for that we can use TK and end
that way the new item is always going to be inserted at the end and I just
realized this needs to be or in uppercase letters like so and now this is working if I scroll all the way to
the bottom now we are always at the bottom and that is what index is doing
there are two more things that we have to understand we have events inside of a table and we have items and those work
really well together so let me start with events there's one special event at a table or a tree view has
we need two smaller than and two greater than signs and then here we have three view select
this is going to be triggered every time we are selecting an item inside of the table
for now let me just Lambda with event and I want to print the event that we
are getting so if I run this now and I click on one and we are not getting very much
as a matter of fact the event is always going to be the same no matter what we click on the event here you can basically ignore
what you rather want to do is get table and then what is called selection this
gives us the curly selected items so now if I click on something we get a random
number and I can click on multiple items the number is always going to be a bit random
so what does that actually mean if this one here is the table this table
is populated with lots of items this could be one item this could be another item this could be a third item
basically one item is one row of data this is the item we are going to talk
about in just a bit oh well we are talking about it right now
and each of those items has a specific ID this was what we have seen something like IO and then two numbers 45 for
example these numbers we can use to select items from this table and this I want to do in
a separate function so let me Define item select
this I want to run in here so item select in here I need one argument for the
event although since the event is basically pointless I'm going to add an underscore in here to indicate that I
don't care about this value in here once again I want to print my table and then
the selection so if I run this now I can click on
various items and we get some random ID this random ID I can now use the way you
use it is you want to get a table and then the item and in here you can add
the table dot selection if I comment this out there is going to be one
problem because if I click on this you can see we don't just have the ID we
have a tuple that has one element inside of them and that is the ID the reason
for that is we can select multiple items so if I select Thomson and hold shift we
have a bunch of different items the way you are going to work with this is inside of a for Loop that'd be an
easy way so for I in table dot selection
then I can use table and item and then here I want to look at the item
this I could for example print and let's see what we get if I now
click on let me show my mouse again if I click on Lisa Thompson we get
text nothing image nothing and then values Lisa Thompson LT Thompson and so
on those are the main items although there are a few more for this video I want to
keep it simple so in here I only want to show the values now if I should notice
again I can click on one item and I can select multiple by holding down shift and we always get all of the different
items or rather the actual values and with that we have also covered items
so let me get rid of the comment and this is covering the basics of a table
although there's one more thing that I do want to do I can find another event
for this one we only need one smaller and greater than symbol and in here I want to look for delete
if that is the case I want to delete items this delete here stands for the delete
key on the keyboard so in here I want to delete items and
create a function for the event again we don't care about it so an underscore and let me just print the lead so we can
see what's going on if I now run the entire thing and I have the table selected and I click on delete we get
delete and I want to use this to actually get rid of a value
and this I think could be a really good exercise for you try to figure out this function here
one method you need is called table dot Elite
in here you can pass an item and this is going to delete Whatever item you pass in here
and that is going to delete the selected row although you have to figure out how to
actually get all of the items so positively now and try to figure this one out
basically what we have to do is very similar compared to this in fact let me copy it and I again want to look at my
entire selection but now I don't want to print it instead I want to get my table and delete it and then here I want to
add I so now if I run this again and I can select a couple of entries
let's go with those two and if I click on delete they disappear this works with as many items as I can
select and they always just disappear that way we have quite a fancy table
that works really well and let me try to delete all of the values inside of this table
then you can see it very well that this is indeed working quite good cool so
with that we can delete items inside of this table or rather rows that usually makes a bit
more sense and with that we have the basics of a table now tables do get quite
complicated so there's a lot more stuff that you could cover but if you got so far and you have a documentation this
shouldn't be too hard let's create some sliders specifically we are going to
create this app here inside of there we have a couple of Sliders and a few
progress bars right now I'm dragging the top one and this one is connected to a progress bar on the bottom you can see
another progress bar and another slider and those are also connected meaning I can drag the slider and influence the
progress bar and also update the text besides that I can also write inside of
this box over multiple lines let me add quite a few
and on the right I can drag the text up and down
that is going to be the project for this part and let's cover some basics
in tkinter there are two main widgets to create sliders one is called the
progress bar and the other is a slider and both show progress in one dimension this could either be the horizontal or
the vertical axis you can Define this yourself in terms of differences the slider can
be moved by the user or it can be set independently meaning you can either use the mouse or you can use something like
a tkinder variable the progress bar Works a bit differently this one cannot be set by the user so
Mouse input is not activated basically always need some kind of tick in the variable or something external to set it
but other than that the two widgets work kind of in a similar way so let's have a
look I already have a few lines ready if I execute all of this we can see we have a
basic tkinder window nothing special so let's start by creating a slider
a slider is called ttk and scale this I want to store inside of a variable I'm
going to call it scale in here as always at the minimum we need the master which is going to be the
window and once I have that I can pack this widget now I can run this and we have a basic
slider I can move this around but right now it doesn't really do anything to get some interactivity we have to add
a few more arguments the one that is the most useful I feel is called command and
this one works like a button anytime we are clicking on the scale we are
activating this command meaning in here we need a function or a Lambda function I am going to go with a Lambda function
and I want to print let's say test I can now run this and if I click on the
widget we can see we are getting an error the error being that Lambda takes
zero positional arguments but one argument was given which means when we are calling this
Lambda function ttk dot scale enters one argument automatically this we have to
capture with a parameter which we can do quite easily I'm going to call it value and just to see what happens let's print
this value I can run the entire thing now and if I move the slider around we can see the
values that this slider has right now they start from zero and go all the way to one
these are the default values and those you can change quite easily we have seen the same thing from the
spin box you need from and underscore don't forget that in my case I want to set the start value to zero the end
value is going to be set with 2. I'm going to set this one to 25. with that I
can run the entire thing again drag this thing around and now we can see we have values from 0 to 25. works
pretty well before I continue I want to put all of the arguments on separate lines
otherwise this is going to be difficult to read another argument you might want to
consider is called length and this one sets the length of the scale so if I set
300 in here we get a much longer slider although in terms of functionality we
have the very same numbers finally we have what is called Orient and by default Orient is horizontal I
can run this now and we have the same outcome however you might already see where this is going I can set this to
vertical and now we have a vertical slider that still works in exactly the same way finally the last thing I do
want to cover for slider is you can set a variable and this variable is just
going to be a tkinter variable meaning before I create a slider I want to create I'm going to call it scale end
and this is going to be TK int VAR this
I can set as the value for the variable let me add scale in in here if I run
this now nothing is going to happen however what I can be doing is for
example set the start value of this decanter variable to let's go with 15.
if I now run this we can see that the start value is 0 the N value is 25 and
this value here is 15. which is already quite good at
demonstrating how these two numbers work together quite well or well not numbers
more like widgets you get the idea I guess there's one thing I should cover
and that is that this scale end Only Stores integer values that's why it's
called integer variable which means if I inside of the command Lambda function
get my scale end and get the value if I now run this again I am only getting
integer values in the original we had floating Point numbers so be aware that how you store
this data is quite important if you really wanted to store floating
Point numbers you would need a double VAR
this one stores floating Point numbers now I can run this again and now we have the same output as before
I guess I can stick with this one seems to work quite well although I do want to change the name here from scale
end to scale load cool and with that we have all of the
basics of a slider it really isn't that complicated which means next up we can work on a
progress bar this we get with ttk and progress bar
as always I want to store this inside of a variable I'm going to call this progress and window for the master and I
want to pack the progress bar widget if I run the code now
we're getting an error because this scale end should be scale float let's try it again in the bottom of the window
now you can see we have a progress bar problem is I can't click on it nothing
is going to happen the reason being here that there is no mouse input for a progress bar instead
what you want to do is to use taking the variables and connect them via variable to this widget for example I could use
scale float and now you already see we have some basic progress bar in here and if I drag this
thing down and up you can see the progress changes inside of the progress bar
although there's one thing that I forgot let me run the entire thing again by default we know that the slider
currently is set to 15. in this 15 we have down here as well
but we don't know how far this progress bar goes although we do know it starts
at zero if I drag the entire thing all the way to the top we get to zero that part should be fairly obvious
you might be tempted for this one to set it to argument like we've done for the
scale unfortunately this one works slightly different the value you want to specify here is called maximum if I set
this one to 25 I can now drag my slider all the way to the bottom and then we
have a full progress bar and this way we can connect these two widgets quite well and they work really really well
together these are the two arguments you basically always want to use with a progress bar although there are quite a
few more and to demonstrate them I'm going to set all of this over multiple lines that way I have a bit more space
the next one is called Orient and this one we have already seen in here for
example I can set this to vertical and we have a vertical progress bar although it works in exactly the same way
I don't want this to be vertical I'm going to set this to horizontal so now
we have the starting point again we can also set what is called the mode
in here we can either set determinate which is what we already have
no change or we can set this to indeterminate
if I run this you can see the difference between the two now we don't have a complete progress instead we just have a
small bar it's kind of hard to explain but you can see it pretty well besides
that we also have length this one like for the slider up here we can set the
length of the progress bar let's go with 400 and now we have a really long
progress bar that still works with the slider so no change there
with that we have all of the main arguments that you could use for Progress bar although there's one more
thing that is a little bit weird and that is that a progress bar has a couple
of special methods they're called start and stop for example if I said progress dot start
run the code you can see this thing starts by itself and since we are changing the number
let me move it to the side let me close it actually once I click on start the progress bar
is going to start some progress and this progress can also influence the
variables the one we have set here because of that we are also going to change this scale here
let me run the entire thing again actually you can see that when we start in the program the indicator for the slider
went down automatically and it can't go any further but if I move it now the two are kind of fighting
with each other so you have to be really careful when you're using start generally I wouldn't really recommend
using start there isn't usually a good reason for it when you're using a progress bar you want to have some
external data set that gives you the data for this progress like a download for example
using the start by itself probably is never really going to be useful although besides that we also have stop although
this one doesn't do very much because we are stopping this once we get started I suppose a better way of approaching
this is I want to stop this progress as soon as I click on this scale
this means instead of printing the value I now want to get the progress and stop
it let's try this one now and now if I click on the slider the progress bar
doesn't go weird anymore there's one thing I forgot and that is inside of the start method you can set a
step size or rather you can determine how often this start method is updating
the progress bar for example if I set 1000 in here this
is in milliseconds meaning 1 000 milliseconds are one second if everyone is now nothing happens but
after one second we get some minor progress so if that is your thing this is also
what you could be doing although in my case I don't want to use the start method so I'm going to comment it out
all right there's one more widget that I do want to cover and that is called scrolled text
let me fix the typo this scroll text we have to import because it's basically a
compound widget let me import it first and then you can see quite well how this is going to work
to import this we need from tkinder and we want to import scrolled
text all in lowercase letters once we have that just be aware that
this scroll text is not a widget in itself it works rather like ttk this one
contains other widgets which we can use down here I want to create another variable let's call it scroll text and
now I want to get my scroll text and then Dot and uppercase as
and scrolled text and this is now going to be a widget so this one needs a
master once I have that I can get the scrolled text pack the entire thing and
now if I run it we have a text field where I can type quite a bit
let me go all the way to the bottom and there you can see on the right we have a scroll bar
Works quite well this one is well quite straightforward what you really have to be aware of here
is that this is not one widget basically we have a normal text widget and then on
the right for the scroll bar we have a slider we could make this ourselves and
later on I'm gonna have one part where we do make this thing ourselves but for now if you just want to have
some simple text widgets this is how you would go on about it you can also set some custom parameters
here for example you can set the width to I don't know 200 let's see what we get possibly a bit much
let's say 100. there we go and you can also set the height of this
thing to 20 and that doesn't do very much let's go
with five so you can see it really well there we go now we have a very
short text field but other than that this scroll text you
would use like a text widget now I am not going to use this very much I just want to cover it so you have a
basic idea of what it is in case you see it in my case usually when you create a GUI
it is much more efficient to create your own scroll text which means this is not going to be terribly relevant
instead I want to do an exercise and then we can finish up this part
I want you guys to create a progress bar that is vertical start automatically and
also shows the progress as a number on top of that there should also be a scale slider that is affected by the
progress bar pretty much what we have done with these two widgets here
pause the video now and try to implement this yourself
let's get started by creating the progress bar that is vertical that starts automatically and that shows the
progress as a number since we do have to store some data here I want to create
let me call it the exercise and this could be an integer
this as always is going to be an INT VAR with no starting value once we have that
I want to create an exercise progress bar and this we get with ttk and progress
bar what a master we need the window then for the orientation to be vertical I
need to set Orient to vertical besides that I also have to declare the
variable for this widget which is going to be the exercise integer with that I can fix the typo and pack
this widget let's see what we get
that's looking pretty good although it doesn't do anything right now for that I want to get exercise progress
and start the entire thing running this again now we have an automatically
starting progress bar that covers most of the first bit so we
got so far this bit here next up we have to show the progress as a number
which means we are going to need a label with ttk and label the master is going
to be the window besides that we are going to need a text variable which is going to be the exercise
integer don't forget to pack this label
and let's see this is looking really good
cool I'm quite happy with this although here you can see one quite weird thing and that is that this number is well a
floating Point number we have point zero I don't actually know why tkinder is doing that but when you're using
an integer variable and set it as the text variable and the original number is
a floating Point number like what we get from a progress bar then tick interp
stores it as a floating Point number but rounds it down it's kind of weird but
this is basically never going to be an issue so not too much to worry about this covers the entire first part for
the next bit we have to create another slider that is affected by the progress bar
let's call this one exercise scale and we need ttk and scale the master is
going to be the window and in here I want to have a variable which is going to be the exercise integer
this exercise scale I now want to pack I can now run the entire thing and now
we can see we kind of have a problem that is the slider is always all the way
on the right the reason for that is that the default values for a slider are between 0 and 1.
to fix that all we have to do is set a from argument for the slider which I
want to set to zero and a two argument to let's go with 200 and let's see what
change that is going to make now we can see that the slider goes all
the way to the halfway point and if we change this to 100
we can see that all of this is working as intended there we go this is looking really good
and with that we have the basic sliders inside of tkinter the last change that I
do want to make is I want to set the orientation of the original scale widget to
horizontal that way this thing doesn't look as cramped anymore and this is what you have seen in the demo more or less in
this part we are going to cover something slightly more advanced and that is frames and parenting
frames are just another widget but you wouldn't really use them by themselves
instead use them to create better layouts and for the better layouts you
are going to need parenting let's talk about it so far for the parent we have always
used the window itself but that is very often not what you want
for example if we are going to create a menu you want to have every single menu item to have the actual menu as the
parent or if you have a tap entry you want to have every single widget inside of the
tab with the parent being the tab we're going to cover both of those cases in the next two parts so I'm going to go
into a bit more detail but for both you need more control over what the master is
what we're going to cover for this part is a complex layout or a slightly more
complex one because what you can do is you can create a container widget and
use that to organize your widgets and then you can place the container widget somewhere on the window
the container which it here is going to be the frame this one is called ttk frame and this is
an empty widget how you are going to use it is you are placing other widgets inside of it and
then you place the frame that way you are placing all of the widgets inside of it as well which is really powerful to
create more complicated layouts for now we're going to keep it fairly simple but
in the next major section we're going to cover layouts in a lot of detail so don't worry about too much for now what
you should take away from this part is how parenting Works once again here we
are in the code if I run all of this we have an empty window that has a custom size 600 by 400 pixels what I want to
start with is I want to create a frame this I want to store in a separate variable and this we create with ttk DOT
frame this one like any other widget is going to need a master which in this
case is going to be the window once we have that I can pack this thing
and if I run it we can see that we can't see anything the reason being that
frames are invisible that being said there's one way to visualize how a frame
is going to look like right now the window has this certain size this I want to comment out if I run the code now we
can see something like this we basically only have the top control buttons I can
extend it but by default we have this size here this happens because tkinter
or the window tries to have the size of the widgets inside which right now is an
empty widget with no size so we get something like this but for frame we can set the width let
me go with 10 and we can set the height in here I want to go with 20. if I run
this now we have a very small window I guess the numbers here are a bit small
let's go with 100 and 200 that is looking a bit better
we have a width of 100 pixels and we have a height of 200 pixels the numbers
we get here and here another way you could visualize a frame which I think is
even better is you could set a border with border with and this I'm going to
go with 10. although by default you're not going to see anything also there shouldn't be a typo in there border with
like so this is looking better now we have a border width but the Border has no color so it's invisible
for that we have to set a relief and for the relief we have a couple of
inbuilt options the one I'm going to use is called TK and Rich all in uppercase
letters if I now run this we get the frame we have seen earlier
except right now it has some kind of Border thingy the default for the relief
is flat with this one you don't see anything besides that we have raised and
we have sunken those look like this or like this
it basically starts to look like a button another option is called Groove like so
and this one I guess is even better let's stick with this one the relief option you're not going to
use too often because most of the Styles here look quite outdated and later on we're going to learn better ways to
style it now we can actually start the interesting bit and that is the
parenting or I guess a more appropriate name in tkinder would be Master setting
right now the master was always the window so the first argument we placed
into any widget was always the window which we created all the way at the top this does not necessarily have to be the
case what we could for example do is create another label or it could be any widget you create this always in the
same way ttk label in this case and now for the master I want to set the frame
other than that I want to have text and this I want to call label in frame you
also still need to pack this label and if I run this now we can see a
couple of things happened the first one is that we have the label inside of the
frame however besides that the width and the height of the frame have changed we
don't have something like this anymore instead we have well just this size here
so what happened well the issue you have to understand here is that ttk primarily
tries to set the size of a widget by its children in this case the frame only has one
child and that is the label and that overwrites the width and the height if you don't want that there is an
option to disable that you will get the frame again and the option is called pack and proper gate this is a method so
we have to call it and then here we can either set faults or we can set true if you set true
we are setting the size of the widget by its children if we set false we get the
original size meaning we are using the width and the height we have used for
this tkinter widget you can also set multiple children inside of one frame for example I could
create another button and this one is also going to have the frame as the master for the text I'm
gonna go with button in a frame I want to pack the button and there we go now
we have a button inside of it and you can't see we are cutting off the button a tiny bit meaning that TK enter
constrains the size of these widgets quite a bit let me increase the width of this widget
to 200 now this looks a bit better and that's kind of all you need to set the
master to something other than the window you have created right now this doesn't seem too useful
but let me demonstrate one instance where this could be powerful let's call
this example I want to create another label let's call it label 2. this label
is going to have the window as the parent and for the text I want to have label outside frame this label to I now
want to pack and now we can see that the label is outside of the frame which is giving us
quite a bit of space in here however now if I get the
original frame and only pack it after label 2.
if I run this now we can see we have the label on top and below that we have the
frame itself with the widgets inside of that frame let me move it to the side this label here is all the way on the
top and below that we have all of the other stuff this Frame here and all of
the children of the frame what is even more powerful and what we are going to learn more about later let me return
frame.pack to its original place so this thing is going to look like so again
you can also inside of Pack set aside by default this side is always the
string top but it doesn't have to be you could also set left for example let's see what this
gets us and now we have the frame on the left side with the label outside of the frame
being on the top this however we can also set to the left side and that gives
us two widgets right next to each other with this system you can create pretty
powerful setups and again we're going to learn much more about this later but for now this is all I want to cover for this
bit Let's do an exercise and then we are done what I want you guys to do is to
create another frame with a label a button and an entry widget and place it to the right of the other widgets pause
the video now and see if you can figure this one out
let's start by creating I'm going to call this the exercise frame
this is going to be ttk and frame this one has the parent of window I am not
going to pack it just yet instead I want to create a label a button and an entry
widget since those are not going to be doing anything right now I am not going to
store them inside of a variable I am just going to create ttk label
the parent is going to be the exercise frame and the text is going to be label
in frame 2. right after creating this I want to pack it as well I can copy this
one now instead of a label I want to have a button the other arguments can
stay identical and finally I want to have an entry widget this one doesn't
have a text argument once I have all of those I want to get
my exercise frame and pack it running this now we are getting a couple of other widgets
all the way on the top right Adobe I realized the text here this one
shouldn't be labeled this should be button in frame 2. let's run this again and this is looking pretty good
although the last thing that we do have to do is that when I'm packing the exercise frame I want to set aside and
decide should be left although this one has to be a string and now we have another widget to the
right of it this one doesn't have a border around it so it looks a bit different but it's basically the same
thing we have done in the original frame and this kind of system you can push quite a bit for example you could have
one widget inside of a frame which is inside of another frame which is inside
of the window but once again all of this we are going to cover in much more detail in just a few sections in this
section we are going to cover tabs let's have a look this is what we are going to create we have a basic set of widgets
inside of one tab then we have another tab with some other widgets the widgets in here work as expected
and you can just play around with them this is what we're going to create
and the widget we need is called ttk notebook the way this is going to work
is that we want to set a couple of children to this notebook this is almost
certainly going to be a frame and each frame is then going to become a tab
since you can add lots of widgets to a frame you can use that system to make widgets visible or invisible it's
honestly a fairly simple system here's the code if I execute all of this we have a basic window
and I want to create a tab widget or rather I want to create a notebook
let me call it notebook and the widget we need is ttk and node book
this one is going to have the window as the parent I can pack this notebook right away
although by default we can't see anything The Notebook by itself is going
to be invisible the only thing you are going to see are the tabs inside of it since we don't have any tabs right now
nothing is going to be visible which means I have to create a couple
let me call it tab 1 and this is going to be ttk and frame
what apparent I now want to set the notebook while we are here I want to
create a second tab I'm going to call it Tab 2 and this one also has the parent as The Notebook
with this I can run this again we still can't see anything what we now have to do is inside of the
notebook we have to add and this is going to be tab 1
and this wants to have a text this text is going to be the name of the tab I'm going to call this one tab 1 then I can
duplicate it and change this 1 to a two and now we should be seeing something there we go we now have two tabs
which means you can just Place widgets inside of either of the frame and then they are going to be visible inside of
the respective tab for example inside of tab 1 I'm going to add a tiny bit of white
space I'm going to call this tab one inside of tab 1 I want to create a label
with ttk and label this one is tab 1 for the master and for
text I want to have text in tab 1. don't
forget to pack this widget and with that we can see we now have some text in the
first tab although Tab 2 doesn't have anything right now but we certainly have
a good start in the demo inside of the first tab I also had a button let me call it button
one ttk and button with tab 1 as the parent and the text is going to be
button in tab 1. besides that I also have to pack this
button and now we have text and we have a button inside of tab number one
tab number two still doesn't have anything all of that is going to happen inside of
tab 2. in here I want to create Label 2 which is going to be ttk and label with
Tab 2 as the parent the text is going to be I guess text in
Tab 2 makes the most sense here this Label 2 I also want to pack
I have text and a button in the first Tab and in tab number two I have tab 2.
so this is working quite well there's also going to be an entry let me
call it entry 2 and this is going to be ttk and entry inside of Tab 2 and
there's nothing else in here and entry 2 and pack and now
we have the stuff you have seen in the demo honestly this wasn't very difficult
all of these watches work like anything else if you understand how to set the master this system should be really
really simple or at least I hope it is which means we can already do a
challenge what I want you guys to do is to add another tab with some buttons and text
inside let's say with two buttons and one label
to be a bit more specific possibly now and try to figure this one out
I want to start by creating another frame this I'm going to store inside of tab exercise and it's going to be a ttk
and frame with the parent being The Notebook inside of that I want to create button
exercise one with ttk and button
the parent being tab exercise and the text could be button one it doesn't
really matter what it is this button exercise one I also want to
pack and with that I can just copy the entire thing and add another button here
all I have to do now is change to one to a two the one in the name or the text should also be a two
that is going to give us the buttons besides that I want to copy this one more time I want to create a label
which I get with ttkn label this is going to be label
there we go now we are packing this one as well with this we have all of the widgets and the frame to put them inside
next up I want to get the notebook and add my
tab exercise like we have seen up here which means besides that I need a text
and this is going to be tab exercise let's try this one now and there we go
we have tab 1 we have Tab 2 and we have tab exercise with button one button 2
and the label that's pretty much it I hope you can see how this system is fairly
straightforward there shouldn't be too much that can go wrong I guess the one thing you want to be
aware of is that this Frame here or these frames here are not going to be
packed themselves for that we're using this add method for completion here you don't actually
have to set the notebook as the parent for example if I change this notebook to a window and run this again we get the
very same outcome although all of these other widgets do need the frame as the
parent I just think that in the notebook as the parent makes the most sense here but choose whatever you want in this
case it doesn't make too much of a difference let's talk about menus in tkinter you
are creating a menu with TK menu be aware here we are using TK not ttk
but other than that the widget is fairly straightforward however there's one thing you have to understand to create
more complex menus and that is that you are always using multiple TK menus and
you Nest them sometimes you can Nest quite a few of them at the same time and this can get a bit confusing and a bit
complex let me give you an example if you want to create a simple menu you will place a
TK menu inside of another TK menu and then this sticker menu becomes an option
now what does that mean let's say we have our normal application the entire window is the blue frame here inside of
there we have TK menu this is the main menu this would be just a normal top bar
like you've seen in basically any other application inside of that we are placing another
item and this would be the TK menu this would now be one of the entries inside
of this menu but other than that both of these are just TK menu widgets
the red menu though can now have a couple of extra options meaning here we actually have items we
can pick from I hope that makes sense you could make
all of this even more complex because you could place for a sub menu a menu
inside of a menu inside of another menu for this example I kept the colors
constant the main menu is the yellow one inside of there we have a red Sub menu
or one item inside of the main menu inside of that menu we have another menu
this would be one of the items in here inside of there we could have other
entries like so and we could even have other menus in
here this would still work the system overall can get quite complicated
but well once you understand the basic logic this really isn't too difficult as long as you understand the nesting
principle let me actually demonstrate what we are going to make it's going to look like
this we have a menu with a couple of entries and inside of one we have a sub
menu on top of that we also have a checkbox in here that we can check and uncheck finally there is a separate menu
button it's basically a button with a menu although it works like a menu
and that is all we need let's have a look at this in code once again I have a few lines of code
ready if I execute all of this we have a plane ticket window it doesn't do very
much in here I want to create a menu this we create with TK and menu like any
other widget this is going to need a parent which in my case is going to be the window on top of that this widget I want to
store inside of a variable that I'm going to call menu while this menu is just another widget
we are not using the pack method on it instead to turn it into the menu of the
window you would use window configure and then you would set the
menu to the menu if I run this now we can't see anything
the reason for that is that this menu by default is invisible we can only see the children inside of it
since we don't have any children right now we can't see anything but that we can change quite easily
let's start by creating one sub menu
I want to create TK menu again although now the parent is going to be
the menu the one we just created this one up here this I want to store as well in the
variable I'm going to call this one the file menu the name is basically arbitrary
with this we have an entry but if I run the code we still can't see anything the
reason for that is that we need one more line of code we need to get our menu and then the
method add Cascade for this one we need two arguments first
of all we need what is called the label this is the text you are going to see
I'm going to call this one file besides that we need a menu entry this
is the file menu we just created and now we should be seeing something there we
go in the top left we now have file although if I click on it we just see something empty that is doing some weird
stuff there are two reasons why this is happening the more important one is that
this file menu doesn't have any entries right now to give it some we have a
couple of different options the one you are going to use the most is the method add command
this one like at Cascade has a label let me call this one new and then we
have a command this one could be any function in my
case I'm going to set a Lambda function that is going to print
new file like so and now if I run this again I
can click on file and we have a new entry if I click on that we have a new
file printout that's pretty good although if I click again on file you can see we have this separator thing if
I click on that we are creating another window that is kind of weird although
the menu still works but this isn't the desired Behavior to fix that when we are creating the
file menu we have to add one more argument and that is called tear off
by default this one is true and that means you can tear away the menu and have it as a separate window I do not
want this Behavior so I'm going to set this to false running this again now inside a file we
only have the menu entry this is looking like a proper menu and let's go through the entire thing
again just to make sure all of this makes sense we have the entire main window up here
that is the entire window that one should be fairly obvious at this point inside of that thing we have a menu this
is the entire menu bar up here for that you need to menu widget itself
and on top of that you have to run window configure and set the menu as the menu
inside of that we have right now one menu or one sub menu that is called file
menu this is the file we have created here for that we need another TK menu and we
have to get the original menu and add Cascade then inside of this file menu let me
clean this up a bit inside of this file menu we can add different entries with for example add command there are a
couple more entries but at command is the one you probably want to use if you got this far the worst part about
understanding menus is basically over because now we could run this at command
a second time besides new let's say I also want to have open
which is going to print open file let's run all of this again inside of
the file menu I now have new and open let's still both do a command oh this is
working quite well and I guess besides at command there are a couple more methods you could use a
really simple one is called add separator don't forget to call it if you run this
one we now have a separator between the menus this one doesn't really do anything but it's a nice way to separate
the menu entries to get all of the entries this website here is pretty good because if you
scroll down you have a couple of basic options and below that you have all of
the methods you could use for example we have used add command and we have used ad separator
there's also a radio button a check button those are quite obvious I think and you can also delete and do quite a
few more things but I want to keep it simple if you want to go into more depth check
this out in your own time I want to create another Sub menu
this I want to store in a separate variable let me call it the help menu this again we create with TK menu once
again menu is going to be the parent and tear off I want to set to false
like the one we have created up here this submenu I now have to attach to the
main menu which means I want to get my main menu then I want to add Cascade
the label here is going to be help and then the menu is going to be the
help menu I can run this now and there we have a second menu item this one if I click on
it doesn't do anything because there are no entries but file still works just as before this one I want to have one item let's
copy the add command from the file menu except this one should be for the help
menu in here for example the label could be help entry and this one just prints help
it doesn't really matter what it is and this we have already seen a couple of times so if I run this we now have a
second menu besides file menu this one is pretty straightforward let's do something a bit more
interesting for this help menu I now want to add a check button
this is going to work basically like the normal check button that you have seen in the buttons a couple of sections ago
although first of all we need a label and this label I just called check
since we're working with a check button in here we can set an on value that I want to set to on and we have an off
value that I want to set to off these two values we have to store somewhere
for that I want to use a tkinter variable I'm going to call this one help check
string value the value here is going to be TK and a
string VAR this variable I now want to set for this check button so variable is going to be
the help check string that should be all we need let me run this and if I click on help now we have
to check entry I can click on it and now we have this entry checked I can click on it again and it
disappears cool once we have that we can always get the value from inside of this tkinder
variable for example inside of this add command instead of printing help I want to get help check string and get the
value let's try all of this inside of help I still have the check
entry I can click on it and it still works and now if I click on help entry we get either on or if I unselect the
check I get off so this is working pretty good with that we have created some basic
menus and once again the main difficulty here is the nesting that we always Place
one menu inside of another menu but they are the same widget besides that we can also create a menu
button this is a separate widget that is called ttk and menu button
this as always is going to need a master in my case this is going to be the window and we need a text like any other
button I'm going to call this one the menu button on top of that this needs to be stored
in a variable menu button is a good name here I think for this button we need the
normal pack method because this one functions well like a button menu button and pack
and now we have a menu button although if I click on it nothing happens right now because we don't have any entries
that being said once you get this far you can just add TK menus to it
let me create one TK menu [Music] in here the parent is going to be the
menu button and tear off is also going to be false
this I want to store let me call it button Sub menu
once we have that we basically want to do what we have done here we want to set the sub menu to the parent menu
via configure which means I want to get my menu button
I want to run configure and here I want to set the menu to my button Sub menu
let's try this one now and now if I click on the button we still can't see anything
the reason for that now is that this button Sub menu doesn't have any entries
although that we can change very easily all we need is the button Sub menu I
want to add a command for this we need a label with entry one
or whatever you want to add and we have a command that is going to be Lambda in
my case that is going to print test one if I now fix the typo and run this this
should be working now we have entry one I can click on it and we also get entry
one besides that we could also add a check button
for this one we can just leave it like so I guess I can call it check one
I can run this now and now we have a check button in here that I can click on
works like any other menu it's kind of similar compared to the menus you've seen before but not that
much the main difference is that now you have a menu button and for this one you have
to configure the menu to be the proper menu oh and what I forgot this configure you
could simplify a tiny bit this is what we have seen earlier besides this line you could get the menu button in here
you could get the menu and the value of this menu could be this button Sub menu the result would be the
same if I run it we still have the same outcome choose whichever you like more it's
really up to you both are equivalent we are nearly done although I want to do
an exercise this exercise I want to place before we are setting the menu to the window I
want you guys to add another menu item to the main menu like file menu and help menu you should
create another menu the one difficulty for this one is that this new menu
you're going to create should have one sub menu a menu inside of the menu you are going
to create for that you want to read this website the one I just talked about
I want to start by creating an exercise menu this is going to be TK and menu in
here that parent is going to be the main menu and tear off I want to set to false
just to make sure that we have one entry in here I want to get this exercise menu and add a command
for the label I just want to have exercise test one
this is actually all we need you don't have to specify a command if you don't want to or don't need to
finally to see this menu we have to get the main menu and we have to add Cascade
like we have done here and here we need a label this one I called exercise
the menu is going to be the exercise menu
with that I can run the entire thing and now we have the exercise menu with exercise test one and I can see I have a
typo this should be exercise like so with this we have covered the first part
of the exercise the next one is a bit more interesting I want to add a sub menu to this Sub menu
meaning we have a sub Sub menu this Sub menu I want to store another
variable I'm going to call it exercise Sub menu although this one once again is just
going to be another TK menu with menu being the parent and tier of
being false the way you have to think about it is that this exercise Sub menu we want to
add to the exercise menu like we've added the exercise menu to the main menu which we have done with ADD Cascade
which means I want to get my exercise menu and add Cascade
once again we need a label let's call it more stuff
besides that we also need a menu this is going to be the exercise Sub menu
now if I run this inside of exercise we have more stuff and this one doesn't do
anything right now because it has no entries but that we can change very easily
for this exercise Sub menu I want to add a command like I have done for the exercise menu
which means I can copy the exercise menu at command and change this to exercise Sub menu
with a new label some more stuff now I can run this and if I now click on
exercise more stuff we have a sub Sub menu this could then be literally anything
once again the nesting here is the complicated bit but all we have really done is we have the main menu all the
way on the top this is where everything else goes in inside of this menu we are
adding one exercise menu for that we are creating a TK menu widget and we are
using add Cascade on the parent menu to create this menu item
although this add Cascade we can do on any menu item for example on this exercise menu we
have added another Sub menu and I'm fully aware that this can be kind of
confusing definitely go through this slowly and make sure you understand every level of nesting although with
that we have finished the menus in this part I'm going to talk more
about how to change the window so far we only really changed the title
and the size of the window but we can do quite a bit more we can for example change the opacity
the position the full screen status and the title bar and quite a few more things
although all of this is really simple so let's Jump Right In and let's have a look
once again I have the basic setup that we have seen multiple times by now I can execute this and this is what we get
so far we always change the window title and the window geometry for the window geometry we always
specified the width and the height of the window which right now is 600 by 400. let me run the window again
600 by 400 specifies the width and the
height of the window although you can extend this a tiny bit
inside of this string you can also add the position of the window this you do by adding a plus then you give the left
position of the window another plus and then the top position if you add numbers in here you are going
to place the window or the top left of the window and then the rest is going to follow for example if I change these
numbers to 0 and 0 I now have a window starting in the top
left if I change the left number to 100 we now have a slight Gap to the left side
finally I can change the top number to 200 and now we have even more space to
the top you're probably not going to use this very much but in some circumstances it
can be really useful what you do want to use much more often however if I run this again by default
we always have this feather here or the logo of tkinter this you can also change
although for that you need a specific kind of file it's called an Ico or Ico file inside of the file folder here are
all of the Python files I have used so far besides that we also have a file called Python and this if I show you the
properties is an Ico file this is what you need for the title bar
once you have that all you have to do is get the window and I can bit map and now
you need to file name in my case this is python dot Ico now I can run this again and now on the
top left we have the python symbol instead of the tkinter symbol if you look online you can find lots of
websites that convert a PNG or JPEG file to an Ico file it's completely free and
very easy to do and it does make quite a difference in terms of how your app is going to look
so I would definitely recommend designing your own logo although well it can be something quite complex
besides that we have a few more let me call it window attributes
for this one for example we could set a window Min size
for this we need a weft and a height a tkinter can never be smaller than these
two numbers for the width let's say I want to have a minimum number of 200 or the height I
want to have a minimum height of 100. I can now run this thing again and if I
scale the window this is the smallest I can scale it too it never goes smaller than that
we also have a maximum size let's say for this one I want to have 800 by 700.
I can run this again and now I can only scale the window to this size
here let me move it a bit further to the top like so this is the maximum I can scale it to
there's one more entry that's useful here and that is called window and resizer Bill
for this one you can specify if the app can be resized either in the X Dimension or in the Y Dimension or horizontally or
vertically for example if I set X to true and Y to false we are only able to
scale the app in the horizontal Dimension let's try this one and now if I scale the app left and
right this one works as before however I cannot scale it up or down this one
simply doesn't work it's very hard to see but well try it yourself most of the time you are not going to
use this or the max size they are quite rare however the minimum size I would
always set because if you don't set it the user could minimize your app to size of 0 and 0 which would look very strange
besides that you can also get screen attributes so this green new app is
running on the two important aspects you want to know here are the width and the height of the screen your app is working
in this you would get with window and W info
underscore screen with don't forget to call it this
is a method this method is going to return the wift of your screen not the
app the actual display this I want to print and if I run this I
get 1536 this is the width of my monitor I can duplicate this the same thing is
going to work with the height linear can run this now and the height of my monitor is 864 pixels
this information very often can be surprisingly useful for example the exercise we are going to do in a couple
of minutes is going to be about starting the window in the center of the screen
and if you know geometry and this information this is quite easy to do
but let's first do some other things in here I want to set some window
attributes and I realized the naming here is not ideal this is actual window
attributes whereas this one was rather window let me rename this to window sizes
that's much more appropriate the reason for that is that a window has actual attributes
for example in here we could set the alpha value for this one you can set one additional
value and this value has to be between 0 and 1. with 1 being for transparency and
0 being the app being completely invisible let me set this to 0.5 run this again
and now we can see we have a transparent window works pretty well
if I set this to a 1 we have the proper window and if I set this to 0.1 we get a
barely visible app besides that we can also set top most
if you set this value to true you can run the entire thing again and let me change the transparency back to one if I
run this again you can't see any difference the app still works just as before however if I now bring in the
folder you have seen a second ago this folder is always behind the window even if I have it selected it's always
behind the window we just created and this happens because of this topmost
being true it sets the window we currently have on top of any other window besides that there are a few more
attributes but those can cause problems for that I want to add a security event
all I really want to do is add window dot bind and I want to check if I am
pressing the escape button if I am doing that I want to run a
Lambda function that quits the window which I can do with window.quit
so if I run this now I have a window open if I click on escape the window disappears
the reason why I want that is because some of the attributes can make it impossible to close the window
one example for that could be window attributes
and in here one option you can use and they always start with a dash I don't exactly know
why but you just have to add it you could disable the entire window
for this you have a Boolean value that is either true or false the default here is false but if you set
it to true the window is going to be disabled let me run it and now no matter where I click on the
window nothing is going to happen the only way I can close the window is by pressing on Escape because of this
line here but the window itself doesn't do anything finally another thing that you can do is
to set the window to full screen if you have set this one and you start the app
it is going to start in the full screen mode although if I run this right now we're going to get an error there we go
the reason being that this part here we cannot set the full
screen because we have a Max width and a Max height and this is smaller than my monitor
the problem is this one here let me disable it and on top of that I
also want to disable the disabling of the window and also I want to disable
topmost because we don't need them right now and I want to focus on the full screen now if I run this note here in
the top right we don't have any menu items or title bar so we can only close the window if we press on Escape
and this we can do because of this line if we didn't have it we would have to use the task manager to close it which
is kind of annoying but with that we have the basic window attributes there's
one more thing that I do want to cover and that is let's call it the title bar
also I want to comment out the full screen so we can see what's going on like so now for the naming what I want
to do now is this thing here is I think called a title bar this you can also
hide that you do with window and over write
read Direct I have no idea why it's called like that but if you said true in here you don't
see any title bar anymore which makes it kind of annoying to close the app so we have to close it via the
event but this is super useful to create nicer looking apps because if you don't have the title bar you have much more
options in terms of styling the problem is if you have something like this you also are not able to
resize the app which is well a problem for that tkinder has another widget that
you can use it is called ttk and size grip for this one I want to set the master to
the window and I want to store it inside of a variable that I call grip
this grip we could for example pack now but this is not what you would want to
do but if I do it we have this kind of app here and if I use it I can drag the
window again although right now I can only move it left or right or scaled in the
horizontal axis because of this resizable if I comment it out run this again now I can properly resize the app
and the position here is very awkward for this thing but we could change that
although for that we need a different kind of layout method we're going to cover those in much more detail in the
next major section but what you would use for this one is called place in here you can specify a relative X position
which is going to be 1.0 and a relative y position which is also going to be 1.0
finally you want to set an anchor and this is going to be south east or SE in
short if I run this now we have this size bar in the bottom right and this is much
better now we can resize this window the way let me place it like this the
way place is going to work is we have the entire window and we start at
position 0.0 and all the way on the right we have 1.0 and any point in the middle here we
can choose from this works either on the horizontal axis or on the vertical axis and those you
get with relative X or relative y if we get 1.0 for both we end up in the
point in the bottom right and this is where we are placing this
size grip the anchor is going to set which point you are placing the way you want to
think about it is that there's a rectangle around this widget and by default we are placing the top left or
the North West Point we however want to set the south east point so the bottom right point should
be in the bottom right corner I'm not going to go into too much detail
we're going to cover all of this in much more detail in just a bit but this is all you need to create a window without
a title bar which can be super powerful with this we have all the methods for a
basic window and this gives you a ton of control over how you want to style your app or it is going to give you much more
control later on in terms of what you want to do all right with that I want to do an
exercise and the exercise I am going to place right here below
the window creation because what I want you guys to do is to start the window in the middle of the screen
so pause the video now and see if you can figure this one out
first of all I want to declare some variables I want to get my window with
and this could be any number I'm going to go with 1400.
this by the way is going to overwrite this 600 here as a matter of fact I want to comment out this geometry here
entirely besides that I want to have a window height
this I want to set to let's go with 600. besides that I need to know my display
width and my display height both of those I am getting from this down here
so I can just copy them I want to get my window info
screen with and the window info screen height that is all the information we are going
to need once we have that we can declare a variable for the left point and for the top point of our
window and the way you want to think about it this one here is going to be the entire
window we are working with this one has this display width and this display height
inside of this display we want to add our app right in the middle the problem
is when we are placing this window we are placing this top left point and for this top left point we have to figure
out the left and the top position for that first of all I want to get the
center of my display roughly this point here this I get by dividing the window width by 2 and the window height by 2.
that way I get exactly to this point once I have that point I can simply
subtract half my window width and half my window height and then I get to this top left point
let's start with the left side I want to get my display with and divide
it by two from that I want to subtract my window
with and also divide this by two that is all we need the same thing for
the top except for this one I want to get my display height divided by 2 and
subtract my window height also divided by two
once we have all of that I can actually set window and the geometry
for this one I now want to create an F string in here we need the with x the height
the width is going to be the window with and the height is going to be the window
height after that we have to add a plus and now
we need the left point and another plus with the top point
those are the two points we have just created here and here which means now if I run all of this
we are getting an error the error you can see down here we have a bad geometry specifier but the numbers look kind of
okay the problem here is that tkinter is expecting integers but we got floating
Point numbers python always creates a floating Point number whenever you divide two numbers
this we can fix quite easily all we need is to wrap all of this inside of an integer function and then we're going to
convert the float into an integer so now if I run this there we go we have our
app right in the middle of the window and with that we have covered all of the
really basic parts you need to know about taking the widgets and the window so for the next major part we can work
on the layout layouts are one of the most important part of any GUI framework
they can also be one of the most annoying Parts because it's probably going to be a very common thing for you
that you want to place a widget in a very specific spot but somehow you just cannot place it there which is a very
frustrating thing to work with so let's talk about layouts and what you can do in tkinter
there are three major methods that you have to be aware of the most common one is called pack
this one takes a window and lets you stack widgets in a certain direction by
default you are going from the top to the bottom which means the first widget is all the
way on the top in the middle and then you place other widgets below it while you're doing that you can also
customize things quite a bit for example you can tell widgets to take up the
entire horizontal space or the entire vertical space or both as well that also
works besides that you can also stack widgets in different directions for example you
can go from left to right right to left or bottom to top other than that pack is fairly simple
and well that's kind of all you have to know about it we're going to do a lot of examples later on with this one the next
layout method is called grid this one works by creating a grid over the window and this grid you are then using to
place widgets in a certain position with a certain size this could for example look like this like this like this and
you can also Place widgets on top of each other with an overlap like so this system gives you a ton of
flexibility you could for example change the height of each row or the width of
each column grid is generally the system you want to use if you want to create really complex layouts again we're going
to do a ton of examples later on finally we have the place method this
one is kind of the simplest because you just take a window and you place widgets with a certain position
you can also change the size and this one is fairly straightforward you always have an X and A Y position
and you're using that to place the widget with that we have the three major
tools that you are going to use and what is super important that you have to understand is that you can combine these
layout methods very easily as a matter of fact this is what you have to do to create any kind of complex layout
for that though you do want to be aware of a couple of things the most important
part is that you are going to rely very heavily on parenting and frames
that way you can combine different layouts and keep them organized basically what you are going to do is
you are placing one layout inside of a frame and then you are placing that frame that way you keep everything much
more modular and much easier to maintain Let's do an example this is going to be our main window this
I want to separate into two parts for that I am going to use pack we have a frame on the left that is a
bit more narrow and a larger one on the right inside of the left one I want to
use the grid method like so to place a couple of other widgets like so
this could for example be a simple menu with a couple of vertical sliders
inside of the right frame I want to place a couple of widgets like so I can place them wherever I want since I
am using place with that I have created a fairly complex layout that is still quite
maintainable because each part Works inside of a frame and it makes it very easy to change things we never create a
layout that's too complicated what you can also do is mix different layouts inside of the same frame for
example you could place another widget on top of a grid that way you can basically create any
kind of layout so with that we have the basics that you need and let's do a couple of examples
although I really want to emphasize for this part I only want to have a couple of very basic examples over the next
couple of videos we are going to expand on all of this quite a lot as always we have a super basic window
if I run all of this we have a simple window it doesn't do anything right now inside of this one I want to create two
widgets let me call it widgets I want to have label one and I want to have label
two I'm creating both with ttk label the parent or the master is going to be the
window the text is going to be let's say label and this could be label
1 or label 2. on top of that there's one more thing that I do want to do when we are
creating the label we can style this very easily by giving it a background for this we can just choose plain name
colors like red or besides that we can also use blue
that makes it much easier to see what's going on these widgets I now want to place
somewhere on the window and for that we have the different layout methods the easiest one is pack
this one we always use by getting a widget let's say label one and packing
it in the simpler sense you don't need any arguments and I can just pack label 1
and label 2 if I run all of this we have label 1 and label 2. although in here you can specify a
couple of different things for example you could specify the site one could be left and this always has to
be a string or decide could be right if I run this now we have the label on
the left and on the right still in the middle though we could also use bottom here
also works just fine and if we have the left side for both
widgets we are stacking them on top or to the right of each other again
besides that you can also tell a widget to expand and this is either true or
false by default it is false if I set it to true however the widget is going to
take up the entire available space which means in our case the entire
available space on the x-axis is this space here although we have Label 2
which takes up this vertical space here which means the entire space to which it
can take up is this width and this height to make this even more visible we can
use the fill argument for this one we can either use x y or
both and this one tells the widget if it is going to fill the entire available space let me run this actually then you
see what I mean there we go now label one is going to fill the entire available space
whereas if I only set this to X we only filling the horizontal space if I set
this to Y we are only filling the vertical space you can do that with the other widget as
well if I expand this or I set expand to true now we are splitting the entire
window by two which means tick enter is quite smart about it if you have two widgets that
are expanding they are intelligently separating the space that is available
and let me set this to fill both and then we get something like this this
is one way to place widgets besides that we have the grid method
what a grid we have to start with some basic setup we have to get the window and then we need column configure and we
need I think you can already see where this is going we need row configure
or this one we are determining first of all the index of the row and then we
need a weight let's go with one for now with this we
have created one column I can create a second one by duplicating this line and setting this to a one
and let me add a third one with the index two and to wait for this one could be let's say two with that we have three
different columns although the final column is twice as wide as the other columns so if I draw the entire thing
we have one column here that has a width of one we get a second column also with
the width of one and then we have a final column and this is as wide as the other two columns combined
the same thing we can do for the row in here I want to have a first row of the index 0 and a weight could also be one
this information we can now use to get our label let me use label one and use
the grid method in here we have to specify a row let's start with zero and
a column this one I can set to 1. if I run this now we have the label in
some position it's kind of hard to tell what's going on although if I draw on this we have roughly one column here one column here
and then we have the wider column here with the width of two the reason why this is so hard to see
right now is because the label only takes up the minimal amount of space so the space it needs to display the text
but this we can change as well and the argument we need here is called sticky
this one tells it to which border the widget is going to stick and this one needs Compass directions
for example I could place it here just North that way the widget is always going to stick to the top part of the
cell I can also add another Direction solve that's why it sticks to the North and
the South and if I add all of the directions then it's going to stick to all four sides
and now you should see a bit better what's going on we have column 0 column 1 and then column two with column 2
being twice as wide as column one and two if I add Label 2 in here this is going
to be even more visible for this one I still want row 0 but now I want column 0
as well now I can run this one again and there we go now we have label one and label 2
and an empty column this I can make even more complex by adding another row and this one is going
to be Row one if I run this now we can see we have
split the entire thing in half what I can also do is Place Label 2
and make it take up this entire space for that I have to tell it to occupy
this column here and this column here this I do
with the column span method although first of all we have to change row to one column to one
and then we need column span I want to tell the widget to span two
columns and everyone is now we can see we have level 2 occupying two columns
once again I will go into much more detail later on but if you understand this system you understand ninety
percent of it it doesn't get that much more complicated the final layout method we have is
called place but this one again I want to have one widget and I want to place it
although this should be a Dodge we need an X position and we need a y
position for Simplicity let's start with X being 0
and Y being 0 as well if I place this now you can see we have
label one in the top left what you have to understand about this one is that when we are placing the
widget the actual position we are placing is the top left this position here
with the entire window being a coordinate system that goes like so and so
the one thing that can be kind of confusing here is that if you want to go downwards you have to increase y the
higher this number is the further down we go in computers basically any kind of
layout always works like that if you only know high school geometry this can be kind of confusing but you get used to
it quite fast if you do any kind of game development they use the same system although X is a bit easier if you want
to go further right you have to increase X this one should be quite straightforward
let's say I want to say x to 100 if I run this now this distance here is 100
pixels the same thing I can do for y if I set this to 200
we have 200 pixels from the top we know in our case the window has a
size of 600 by 400 which means if I set the Y position to something like 380 we
should have label one almost at the bottom and there we go this looks pretty good
you can actually also specify a few more things in here you have the whiffed I
could for example set this to 200 and you have the height this I could set to let's say 100 and
now for renders we can well only see part of the widget that's because it is so far down
if I set this to 200 now this is more visible we now have a widget that is 100 pixels
from the left this number here it is 200 pixels from the top
that is this number here and it has a width of 200 and a height
of 100. with that you can place a widget basically wherever you want and all of
these numbers are absolute so we always have pixel positions you can however if I am placing Label 2
with the place method again use relative numbers for this one you would use
relative X and relative y what you have to understand about this
one is that now we don't have pixel positions instead what we are doing for this one is this one here is the entire
window and we are declaring that the top left point is position 0 and 0 for x and
0 and 0 for y the bottom right position this one here is going to be
1.04 X and 1.0 for y
which means if we have relative x 0 and relative y being 0 as well we are going
to be in the top left position this point here
let's try this one let's try and there we go Label 2 is in the top left position
if I change this to 0.5 and 0.5
now label 2 is roughly in the middle or to be more specific we are placing a top
left point this one is right in the middle of the window I can actually demonstrate this by
reducing the size of this thing they can see this Label 2 is always in the middle even if we change the size of the window
this however doesn't apply to label one because for this one we only have pixel
positions generally when you're using place you want to use relative positions
you can also set the relative with let's say if this one is one now the
widget is taking up the entire space like so although keep in mind here we are
cutting off the widget a tiny bit this one here is the entire width of the
window and widget one is going to have the entire width as well however we
cannot see this part here because the widget is starting on this position so some bits are cut off
to change that we would have to change what is called the anchor this is the point you're actually placing
if this one here is the widget we are always placing this point
and then the rest of the widget is going to follow by default we always place the North West Point
but we could also place the South West Point or the South East Point
North East Point besides that we could also place the center
let's drive this one if I place in here this has to be a string I place the
center now we are placing the center of the widget and we are filling the entire
window width we could also change this to South East and there we go now we are
placing only the right point which means if I move this a bit to the side the point we are placing is the south
east meaning this point here is right in the middle of the window and then the entire weft is going to be something
like this which means once again we are cutting off some parts you can play around with this a lot and I would
recommend you to do so but this is all you have to know for the basics and well these are the three major ways
to place elements inside of a window over the next couple of videos I'm going to go into a lot of detail for this
video I'm not going to add an exercise instead I would recommend you to go over all of this and make sure you at least
have a very basic understanding of how this is going to work ideally create a few more labels and just place them
wherever and see if you can work with all of them at least reasonably okay
in this video we are going to cover the pack layout method in tkinter the project we are going to make by the end
of this video is going to look something like this it's nothing too complicated but definitely enough to understand the
basics of this layout method let's talk about it in the most basic
sense Pac works by stacking widgets in a certain order by default we are stacking
widgets from the top to the bottom which means the first widget is all the
way on the top and then with widgets always below that you can already tell here we have a
couple of ways to customize this for example we can tell the widget to take up all of the horizontal space or all of
the vertical space like so to create these kind of effects you have three different arguments that you have
to understand the most important one is the site this one determines which side the widget is added to the options here
are fairly straightforward we have left we have right we have top and we have
bottom with top being the default argument besides that we have expand that is true
of false this one determines the vertical or horizontal space in which it can occupy
can here is the key word because expand only determines how much space a widget
potentially has it doesn't tell you how much space it is actually going to use
fundamentally what you have to understand is that in tkinder we have a disconnect between the space in which it
can occupy for example this widget for here could theoretically occupy this
entire space but the widget itself might only occupy this area here we have to
specifically tell the widget to actually occupy all of this additional space here it doesn't do it automatically
for that we have one more argument and that is called fill this one determines how much space to
which it is actually going to occupy the arguments we can use here are X Y
both and none none being the default argument this one tells the widget to be as small as it possibly can however if
we specified X and here we would tell the widget to take up all of the horizontal space
which would make the widget look something like this if you understand these three arguments
you can use Pac really well although there are two more arguments that you do
need to understand both of those are for the padding those two are incredibly
easy and I'll cover them at the end don't worry too much about them so let's go into a bit more detail
for the site again we have left right top and bottom and this determines the direction of the widgets or rather how
we are stacking these different widgets the four options we have are top bottom left and right
I don't think I have to explain all of this too much it should be fairly straightforward
let's get started by playing around with this argument here I have some basic tkin Tech code I
am importing tkinter I have a basic window with a title and a geometry and
I'm running the main Loop that way if I run the entire thing you can see a basic window
on top of that I have created a couple of widgets most of them are labeled with
some basic text and a background that way it's easy to see what's going on
finally I have a button that doesn't do anything you cannot see any of these widgets
because I am not placing them on the main window but this I want to do by adding another section that I'm going to
call layout for this one I want to place all of the labels using the pack method
I have label 1 Label 2 Label 3 and the
button if I run this now you can see we have the basic pack order
we start all the way from the top and we are going downwards with each widget
taking up the minimum amount of space in this packing order we can customize
let me select all four of them and in here I want to specify a site
by default we have top if I run this one we cannot see any difference
however if I change this to let's say left now the widgets are being placed from the left and we're going further to
the right with the first widget being placed all the way on the left the next widget is to the right of it and then so
on the same is going to work with right
and finally we also have autumn there we go this should be quite
straightforward you can also combine different sides meaning not all of those have to have
the same side for example the first label could have decide right and if I
do that we get some slightly weird outcome I'll talk about this later for now just ignore it
with that we have the basics of the site next up we have the expand method this
can be either true or false this one determines how much space which it can occupy
again can is the really important word here also the widget only expands in One
Direction let's talk about this one once again we have a window and we are
placing One widget and then we are placing the second widget this is the one we have seen already what you might
assume here is that expand expands this widget all the way left and right but
that is not the case because the width of a widget is not set by expand if the side is top or bottom
instead we would only set the height of the fourth widget or in other words height is set by
expand but only vertically in this example and I'm pretty sure this is kind of confusing and for that I have made a
couple more slides the most important thing you have to understand in tkinter about layouts is that there are two
kinds of space this space in which it can occupy and the space which it will occupy
by default in which it will only be as big as the content it needs to cover for
example if we have a label the label widget is only as big as the text it needs to display but that being said
even by default the widget can occupy much more space than that
for example here we have another window and we have a couple of widgets inside
all of these widgets will only occupy the space that they need to display the content for example if all of these are
labeleds we would have a space to cover the space of some text this is the space
the widget is going to occupy this is actually what we have already seen if we return to the app and let me
change the bottom here to Top Again like so
when we place all of these widgets by default they are only taking up a tiny amount of space you can see this via the
background the widget essentially is always only as big as the text the exception here is
the button this one is a tiny bit wider but not that much so by default this is the size we get
for every single widget however all of these widgets can occupy
more space the amount of space that can occupy determines on the side right now
our site is top which means we are placing the widgets in a downward Direction so top is our current site
with that the witches could occupy the entire width of the container which in
this case right now is the window the same is going to be the case for the bottom side in either case widgets are
going to occupy the entire width of the container and expanse is going to tell
them to take up all of the available space in that direction for example if we add one more widget here
and set expand to true for this one then it's going to take up the entire rest of
the available space but only in the current direction that we are working in which is this downward Direction
meaning the widget is going to take all of the remaining vertical space and on top of that it is also capable of
occupying the entire horizontal space and just for completion sake here
when the site is top or bottom widgets can be as wide as the entire container
and the expand method determines the height of the widget if the site is left or right then the
widget can be as high as the container and expand determines the width I hope all of that makes sense this is
definitely something we have to play around with here we are back in the code and I want to add the expand method to
label one by default expand is simply false if I run it like this we're not going to see
any difference however if I said expand to true then the first label is going to occupy
basically the entire vertical space we are starting all the way at the top here
and we're going all the way to the bottom second here is fairly intelligent
it knows if there are other widgets and those need to occupy their space as well
but other than that we are occupying the entire height of the window we are
telling the first label to occupy as much space as possible and the other widgets take up the minimum amount of
space which is exactly the space they need to display the text although that being said as you can see in here all of
these widgets still are very small all we are telling them now for example for the first label that this widget can
take up all of this space but we are not telling it to actually
fill this entire space which means we have a ton of space around the first table but we're not filling that we're
going to cover that in just a bit on top of that we can also set multiple widgets to expand being true and tick
interp separates the space here intelligently although right now this is kind of hard to see
I think a better way to illustrate this is if I set the first and the last widget with expand being true
now you can see we have the first widget covering the entire
almost the first half and the bottom also gets the same amount of space
like so in between we have the other two widgets only covering the minimum amount of
space and this is also going to work with the other directions for example if I change top to left
then we can see if I expand this a tiny bit we now have the same issue again the
two middle widgets only occupied the minimum amount of space whereas the first table takes up as much space as it
can same with the button like so this however doesn't feel particularly
satisfying because we need one more argument to make all of this work properly for that we have the film method this
one can be X Y both or none and this determines if it which it will
occupy the available space by default this is going to be none which is telling the widget to only be
as large as it needs to be to cover the content if we set this to X we are telling the widget to cover the entire
horizontal space if we set this to Y we are covering the entire vertical space and when we set
this to both we are covering the entire space that is available let's have a look at this one once again we are in
the code I want to set this back to top so it's a tiny bit easier to see what's
going on for the first widget now I want to specify a film method the one you
probably want to use most of the time is called both and if I specify this one now my first label covers the entire
space it can potentially take up I could set this to X only then we are covering
the entire width and if I set this to Y then we are covering only the entire
height for this one I want to keep it at both the same we can do for the button let's
say for this one I want to fill this thing in the y direction there we go we have a button that covers
the entire available height and now I can also demonstrate that widgets by default cover the entire width even if
we don't use expand for example for Label 2 if I set fill to both
we can see that the label didn't grow in the vertical Direction but now covers the entire width of the window
which means if I only set this to Y we're not going to see any difference because the widget doesn't have any
available space it could take up although if I set this to X we can see the entire width is being occupied
so these are the three major arguments you have to understand site expand and
fill and I don't think they are particularly difficult although since this is really important
I want to add an exercise in here and I want you guys to recreate this kind of
layout pause the video now and see if you can copy this I guess let me move it a bit to the side
so we can see what we have already there we go now pause the video and try this one yourself
what we can see here is that the first label and the button at the end only occupied the minimum amount of space
meaning those don't have expand whereas Label 2 and the last of the
labels are occupying as much space as they can which means those two get
expand finally Label 2 doesn't have any fill because the widget itself is very small
whereas all of the other widgets do fill up the available space shouldn't be too hard to replicate
the site remains identical for all of them although for label 1 pack should
not be true so I'm just going to remove it although fill is going to be both if I run this again now we have the
first label all the way in the top and this is already a good starting point so first label is done
Label 2 however is going to need quite a bit of work this one is not supposed to
be filled but I do want to expand the entire thing I'm going to set it to true and there we
go now we have Label 2 with a ton of white space around it if I compare it to the goal this is looking pretty good
next up we have to work with label three in this one I also want to expand so
expand is going to be true and I want to fill this one as well both let me run this again now and we
are almost there this is starting to come together quite well the issue we have right now is that the
button is way too tall that happens because expand is true for
the button let's remove it let's try this again and we are nearly done the last thing we
have is that the button doesn't fill the entire width like we have done in the goal
the reason for that is that right now the button only fills the vertical space but I want it to fill the horizontal
space and now we can try this and there we go we have replicated the entire
window of the exercise if you could figure this thing out yourself you are understanding about 90
of the pack method the rest is going to be fairly simple the last two arguments inside of pack
are two kinds of padding the first argument is either pad X or pad y or
both I guess this one creates space around this widget which means we are essentially
creating a larger box around this widget and filling the box with empty white
space it is not going to be visible besides that we have iPad X or iPad y
this one creates padding inside of the widget which means that we are expanding
the widget itself or in practice we're not filling the entire space with white space instead we
are expanding the widget let's play around with this one as well
in the code I think that's going to explain all of this much better for label 1 I want to add pad y
if I set this to let's say 50 pixels now we have something that's very hard
to see to make this a bit more visible for Pack 2 I want to set fill to both that way we
can see where label one ends and label 2 begins let me run this again there we can see
what this pad y has done is I created padding around the top and the bottom of
the widget that way we have a bit of space and the larger number gets the more white space
we have the same thing you could also do for pad X if I set this let's say to a hundred
now we also have a ton of white space on the left and on the right of the widget all of this is padding
I think this one is fairly straightforward besides that we also have iPad Y and iPad X
although for now I only want to cover iPad y because conceptually this can be a tiny bit complicated to understand let
me run the code again now we can see that the widget is quite a bit larger we are covering this bit of
extra space this happens even though label 1 doesn't have any expand method the reason why it
occupies more vertical space is because of this iPad y we are essentially pushing the widget to be a bit larger by
the amount of padding we specify this is in contrast to pad X this one
creates white space around it I hope you get a difference here most of the time you are only really
going to use pad X because iPad y you don't really need to have much if you understand expand and fill they
basically fulfill the same task that is going to leave us only with one more thing to cover
and that is that you can combine different sides inside of the pack method although if you're doing that the
order of the pack holds really really matters on top of that usually you don't
want to combine different sides I'm going to cover this in the next video but using frames to organize a layout is
much much cleaner first of all to make this as easy as possible to see I want to remove the
padding and instead set expand to true
for all of them and also fill both for all of them this I also want to do for the button like so now if I run this we
have four identically sized widgets but let me change the top for the site
for the first widget to left if I run this now we can see that the
first label takes up a huge amount of space and why is that
let me put the widget to the side here the main thing you have to understand is
that the first time you're calling Peg with a certain kind of site this side is
going to get priority which means right now the first label is going to try to
occupy as much horizontal space as it possibly can then it sees these other widgets here
but all of them are set to top which means the horizontal space is
going to be ignored as a consequence they only get as much space as they need
to display their text you can see here the largest label is this one the last of the labels this one
occupies the most amount of space and this one determines the width of all of these widgets
that is the reason why this label gets this much horizontal space and since there's no other widget in the vertical
axis it occupies the entire height of the window after that the other widgets only get
this remaining amount of space and they will divide the space between
the three of them once again you can be really fancy with
this kind of system but most of the time you want to use frames to organize out of this and
that's going to be much cleaner again I'm going to cover this in the next video although this is something that you want
to practice which means we can do another exercise here is one window that is a tiny bit
more complex try to create this one yourself and see how far you get you probably
have to experiment quite a bit but it's certainly doable if you could follow along so far
first of all I want to set top to all of the sides if I run this again now all of
the widgets occupy the same amount of space next up for Label 2 I have set the site
to left what this one is doing is let me move this window a tiny bit to the side
sees that we have three widgets that occupy the top Direction and since the
first site that we are looking at is top it starts with that this means taken
that tries to get the entire height of the window and separate it into three different areas we have one we have two
and we have three they can already see this determines the height of our widgets
besides that teak inter sees that we have one widget that has left however
this one comes after the top which means tkinter tries to push this
first label as far as it can but I can only push it up to this first line here
because we have two other widgets with the top side this constrains the height of the first
label this also determines the height of label 2. this is the entire height
finally for the width like so thickener knows that there's no other widgets
inside of our sides that occupies any horizontal space so Label 2 tries to take up as much
space as it can the only constraint is last of the labels this one needs to
have the minimum amount of space to occupy last of the labels the bit of text here
which sets the maximum width of Label 2 to this point here and with that we have
the basic layout the last thing we have to do if I show it again we had some padding around the first label
this is quite easily done I want to have pad X for 10 and Pad y I've set this one
to 10 as well if I run this again now here's what I created in the exercise
and once again this kind of setup can work but most of the time it is much
easier to use frames to make all of this much easier and that's going to be the next video I'll see you there in this
video we are going to cover pack along with frames to create more complicated layouts in t Kinder what we are going to
create is going to look something like this we have a fairly complicated layout that has lots of individual elements
that come together quite well this is quite easy to do if you know how
to combine pack with frames although for all of this to work you should already know how pack works and
how frames work along with parenting check out the previous videos for more detail but I will assume you know at
least the basics just to reiterate using pack along with
frames is going to make it much easier to create more complicated layouts basically what you want to do is always
create single Direction layouts with the only exception that some of
these items are frames that contain their own layout for example we could have one window
like this and then here we have one frame a normal widget and another frame
note here that this entire widget only goes in a single direction there's nothing else in there
however inside of the first frame we have two widgets and inside of this
Frame we again only have a single Direction but if you combine the two we are
already creating a slightly more complicated layout this we can make even more complex by
adding another layout inside of the final frame and this one could be a normal widget and another frame and in
this final frame we could add a few more widgets as well with this system we are
able to create really complicated layouts without worrying about the pack sides too much and again if you don't know what pack
sites are or why that can be a problem check out the previous video that explains all of this in quite some
detail and just for comparison here is the widget we are going to make this one has
one frame all the way at the top then we have a widget here
and at the bottom we have one larger frame and this one consists out of two frames one that goes like this and the
second one that goes like so all of the layouts inside of this widget are single Direction layouts which makes
them much easier to handle that was quite a bit of talking let's have a look at all of this in code
alright here I have a really basic setup if I execute all of this we can see a
basic window although on top of that I do have quite a few widgets there are four labels and
two buttons all of which have the window as the parent right now or the master to be more specific this I already want to
change the first two labels should have one frame as their parent and the final three should have another frame as their
parent to keep all of this organized I want to have slightly more detailed comments
let's get started by creating a top frame for this I want to have a top frame and
this I create with ttk DOT frame this one is going to have the parent or the
master of the window but then label 1 and label 2 are going to have the master
as the top frame this is already giving us the first part that we need to make all of this work
this I can now use to create another section here I'm going to call this layout
actually let's be a bit more specific and I'm going to call this the top layout I want to get my label one and I want to
pack this without any other Arguments for now the same I want to do for Label 2 and now if I run this we can see that
we cannot see anything even though we have used pack the reason is that we
haven't packed this Frame or the top frame to be more specific which means we do have labels inside of
the top frame but the top frame itself isn't placed anywhere which is the reason why we can't see anything
to fix that we also have to get the top frame and pack this one now if I run
this we can see two labels this I can now use for example for label
1 and label 2 to fill the sides and I'm going to add both in here
if I now add this we can't see much of a difference the only difference that we
can see really is that Label 2 has become a bit wider it became the same size as the first
label the reason for that is that right now both of these labels are constrained by the frame width
and the frame is only as wide as the widest widget which is the first label in this case
that again we can fix by also adding fill and both for the top frame and now
let's have a look now it covers the entire width of the window by the same logic I could use expand
here and set this to true now we can't see anything
but that being said we know that this top frame here is going to occupy the
entire height of the window the reason why we can't see it is that we don't expand level 1 or label 2. if I
expand the two like so we can see we have both labels covering
up the entire window this is the first part next up I want to place label three
which again is just going to be now available with some text and a background color this is not going to have a parent so
window can remain although I'm going to add a comment here for the middle widget
tikenta doesn't care very much if you combine labels or frames or any other kind of widget which means I can also
add the middle layout here and simply get my label 3 and pack this thing if I
now run this we have another label all the way at the bottom this one since we didn't specify any
fill or expand argument it is only going to occupy the minimum amount of space it needs to display the label or the text
itself however if we set expand to true
now we get some slightly more interesting Behavior what tikenter is doing now is it says
that we have a top frame and label three those are the only two widgets inside of
the window this window here which we know because both of these have window S10 master
because of that tkinter is separating the entire vertical space into two parts this one here and this one here
I hope this already makes it quite easy to see why using parenting here is really useful because what we can do now
for example for label 1 and label 2 inside of the top frame we could for example set the site to left
and now we get this kind of layout which already is quite a bit more complicated and doing this kind of thing without
parenting would be kind of a nightmare next up I want to create the bottom
frame for this one I want to create a variable bottom frame which is going to
be ttk frame as well the parent here is going to be the window however for label
three button and button 2 the master is going to be the bottom frame once we
have that we can create the bottom layout for this one I first of all want to
place my button and for now I'm just going to use pack and nothing else the same thing I want to do with button
2 although between the two I want to have label 4. which I also need to pack
with this we have the three widgets finally we have to pack the bottom frame as well bottom frame dot pack like so
now if I run this we can see we have the other three widgets at the bottom
although if I compare this to the demo we have to get a slightly different layout here I first of I want to change
the side to left like so and now if I run this these
three labels are right next to each other the problem is they're not expanding for that actually let me show it again
right now we're telling tkinter to look at this top frame here and to take up as
much space as possible then to look at this widget here and to take up as much space as possible and then we have this
final frame here and this one doesn't get any expand so it's only as large as it needs to be
that I want to change which I do with expand and this I want to set it to true
if I now run this we have a slight Improvement inside of the window layout we have One
Direction and we are separating this into three parts because we have three widget this one here this one here and
this one here that compete for space because of that we have three equally
sized spaces this one this one and this one the problem in the bottom one frame is
that these widgets are not being told to expand so they only take a minimum amount of space
this we can also fix very easily I just want to add expand being true and now we
can't see any difference the reason for that if you check out the last video if you missed it
is that pack only works in One Direction right now our side is from left to the
right so we are going this way and expand only expands the widget in the current direction meaning it tells the
first button to take up as much space as possible same for the label and same for the final button
and then this one here is going to be the size of the frame to make it take up even more space we
once again need to fill argument and this I want to add to all of the widgets
and now if I run this this is looking much better now we're telling both the frame and all
the widgets inside the frame to occupy as much space as they can and fill the entire space as well
although what I also want to do if I compare this to the demo again we have a
bit of padding around this this area here I also want to add which if you use
frames is very easy to add all we have to do inside of the bottom frame I want to add pad X is 20 and Pad
Y is 20. if Iran is now we have a bit of padding around this
and with that we have a couple of basic ways to create more complicated layouts
it doesn't really get that much more complicated you essentially always create a single frame and then you pick
widgets in One Direction inside of this Frame and if you combine enough of these you end up with slightly more
complicated layouts and those are also much easier to understand and to implement
now you could replicate all of this by using the side very cleverly in tkinter
to get really complicated layouts the problem with that approach though is that this really often ends up with very
complicated layouts that are really hard to maintain which is why I would recommend to always stick with one
directional layouts and then add frames to create greater complexity that's basically all you need
all right and with that I want to do an exercise and then we're done with this part
what I want you guys to do I want you to create three more buttons and another frame the frame should be on the right
side inside of the bottom frame this bottom frame here and the buttons inside
of this extra frame should be stacked vertically inside of it the result of all of this should look
something like this the buttons should be here let me put it a bit to the side and
pause the video now and try to figure this one out yourself
we have to get started by creating a few more widgets this I want to do all the
way at the top I'm going to call those the exercise widgets
first of all in here we need an exercise frame this once again is just going to be
another ttk.frame with the parent being the bottom frame this is going to be the
only difference compared to what we have done here and here because for both of those the frame always at the window as
the master this Frame here has another frame as the master which is perfectly
fine to do after that I want to create button three and this is going to be ttk dot button
with the exercise frame as the master the text can just be button free
this should be a string though and I should also fix my typo I can copy this two times it should be
button four at button five both for the variable and for the name that is going to be all we need to
create the different widgets now we have to place them this I want to do all the way after the exercise comment
in here first of all I want to place the buttons I have button three
button 4 and button five all three of those should be packed
since the stacking order is going to be vertical I can just leave the default argument which is the top side
although I do want all of the buttons to occupy as much space as they can which means I only said expand to true and
fill to both sides once I have that I can place the actual
frame and this I called the exercise frame I want to pack this one as well and if I
run this let's just see what happens we are getting something
the problem we have right now is that this pack is very small it only occupies this area here
to fix that we have to do a couple of things first of all I only want single
Direction layouts which means the site here should be left like so
and let's see what we get now now it places this thing in the middle that's a good start besides that I also
want to set the fill and this could either be y there we go or it could be both
both work perfectly fine I tend to prefer both because it just works most of the time
but once again both here are perfectly valid finally what you could also do is set
expand to true and that's going to make these buttons a tiny bit wider
with this expand being true we are telling this Frame here to divide the
space into four equal parts we have number one number two number three and number four and all four of
those have the same width with that we have created quite a complicated layout
in the next video we are going to cover grids this one is going to be even more powerful so I'll see you there in this
video we are going to learn about the grid layout what we are going to make
is going to look like this I am fully aware this looks horrible but that's not
the point of this lesson what I want you guys to do is to understand how to create a grid and how to place elements
in here let's talk about how it works when we are using the grid method we are
creating a grid inside of this grid we can determine the number of rows and columns
on top of that you can also set the width and the height of each column or row you can see this one quite well for
example this cell here s is certain amount of width and a
certain amount of height this you can set yourself quite easily once you have that you can place widgets
in columns and rows and on top of that you can also specify how many cells in
which it is going to occupy for example this could look like this like this or
like this where you have one widget overlapping with another widget in the most basic sense this is a very
simple system however there's one limitation you need to be aware of
like with pack grid only determines how much space at which it can occupy but
not how much it will occupy and this difference is important inside of the pack method we had the
fill argument inside of a grid we are using sticky this one works like this this could be
one cell inside of our table and we can specify to which border the widget is
going to stick in here we have north east south and west and this we used to
place a widget inside of here by default a widget is always going to be right in
the middle however if we for example specify sticky North then the widget is
going to stick at the top this would look something like this
note here that the size of the widget hasn't changed however when we Define two arguments in here like North and
South in that case the widget is going to retain the width but is going to occupy the entire height of the cell
let me clean this up a tiny bit our widget is going to stick to the north and to the South which means the height
of the widget is going to occupy all of this however the width of the widget is going
to be determined by the content for example if we have a label with some
text then the width of the text is going to determine the width of the widget
although if we specify all four directions North South East and West let
me clean this up a bit if we have all four directions we are telling the widget to stick to all four
sides of this cell and that way we have one widget that is quite large or well
as large as the cell it's in that is quite a bit of stuff to cover so
let's Jump Right In and let's have a look at some examples here I have some very basic code if I execute all of this
we can see that we have an empty window that window we're getting from these lines here and we are running main loop
on the window we created besides that we have quite a few different widgets but right now we're not packing them so they
are not visible we have four different labels and each of them has a background color besides that we have two buttons
and we have an entry widget all of these I want to place using the grid method for that first of all I have
to define a grid for that you take the container and you run two methods the
first one is called column configure this is going to create one or multiple
columns for now I only want to create one at least on this line of code
this needs two arguments first of all is the index and the index here is going to be column 0.
then we need what is called the weight and this is going to determine how wide this column is for now I'm going to set
it to 1. once we have that I want to duplicate this thing and change the 0 to a one with that we have two columns
I want to duplicate this thing another time and change the column to a row the
index now being 0 and the weight being 1. with this what we created is is is
our window and we have two columns one and two this is what we're getting from
here besides that we have one row this is what we are getting here I want to place a widget
to place label one I have to get the widget label one and then use the grid
method I have to specify row and I have to specify a column for both of those we
have to use the index numbers we specified earlier meaning the column could either be 0 or
1. let me set it to zero for now the row right now always has to be zero because
we only have a single row with that we are placing label one let
me run the code and there we go we have one label the same thing we can do with label two
I'm going to copy this entire line change label one to label two
the row I'm not going to touch the column I'm going to change to 1. if I run this now we have label 1 and
label 2. and here we already have the first issue that being that the cells we
are specifying let me draw them on here we have column one and we have column two and the two are separated roughly
here besides that we have one row the issue we have right now is that there's a ton of white space both around label
one and label two and this comes back to the issue that is kind of annoying in tkinter and that is
that these cells only create a space for the widget but we're not telling the widget to occupy that entire space
as a consequence we are ending up with a huge amount of white space sometimes you
want that but most of the time you probably don't so let's get rid of it
to get rid of it we need the sticky argument in here we have to specify north south
east or west the order of the letters here really doesn't matter and let me just run it like this now this is
looking much better we are telling the widget to stick to all four sides
although I guess I jumped a bit ahead for now let's get started by just specifying North
if I run this now the widget sticks all the way to the top of the cell I can do this with the other sites as
well for example if I specify sticky to West for the first widget and then I
also add sticky with East then we can see we have each of the
widgets on the side of the window although I guess if I flip this around with east and west
now we can see where the borders of these cells are although that's not usually how you would use sticky instead
most of the time you specify two sides for example East and West tells the
widget to span the entire width of a cell you could also specify North in
here and then we are sticking the entire thing to the top you do have to play around with this a
tiny bit but eventually It's Gonna Come quite handy although most of the time you just specify north south east and
west you are occupying the entire cell and you are done that is basically the
fundamental thing you have to understand about grid layouts I guess what we can do is create a few more rows and columns
and then play around with this quite a bit more I want to have three columns in total 0
1 2 and 3. and already if I run this after creating more columns you can see the layout has
changed because now we have column 0 column 1 column two and column three so
the space we have for each column is going to be less what you can also do is change the
weight of each column for example if I change this to a 2 then we have even
less space let me add a higher number so you can see this a bit better we still
have 0 1 2 and 3 columns but the final
column is going to be much wider than the other columns I can demonstrate this quite well by placing label three this
one is going to be in row 0 but column three and I want this to go from east to
west there you can see we have a really wide label we can actually make it even easier
because these three lines are basically identical they all have the same weight
we just want to specify a different index for that we can also add a tuple
in here for the index and just call this 0 1 and 2. like we have done before and
this is going to give us the same thing which means I can get rid of this now we are creating three columns with the
index 0 1 and 2 all with a weight of one and then we have a final column with the
index free and this is much wider so if I run this we are getting the same thing
the majority of the time you are going to have columns or rows that have the same weight and then using tuples for
that is much easier to read for the rows I also want to have multiple
I have one two and three or well four rows in total but you get the idea and
like with the columns I can also change the weight let me change this one to a three now if I run this all of our stuff
is at the top because this is where the original row zero was this one here is row 0 and before we had
the other rows this was the only one but now we have a ton of stuff down here so
all the existing elements we had were pushed upwards but these cells I can now use quite
easily for example let's go with label two instead of row 0 I want to place this
one at row 1. if our one is now it is a bit further down and let me change sticky to north
south east and west then you can see this a little bit better there we go
this is looking pretty good this could also be column two
or it could be row 2. like so
the system here I hope is quite easy to understand it really doesn't get that complicated
so we can cover the next part and that is either column span or row span
let's start with roseban since I do have quite a few rows that I'm not using roseban is telling the widget how many
rows it should occupy by default this is one if I run this we are not seeing any
change however if I change this to A2 now we're occupying two rows and if I
change it to a three we are occupying all of the rows
let me draw this actually in this widget right now we have four different rows this one here is row zero
then we have roughly here Row one row two and the rest is Row three this one
is much taller than the other rows because we have given it a greater weight and this row span is telling the widget
to occupy this starting cell then another cell and then another cell
those numbers are 1 2 and 3 for the argument the same thing you can also do with the
columns let's use level three for that I want this thing to be in row one and
the column for now should be column zero also I want to have north south east and
west so if I run this now we have label three on the left side however I want to specify column span
this widget should span three columns if I run this now we have a much wider
widget that is overlapping with label 2. to make this even more visible we can
cover one additional concept that is two different kinds of padding if you have
watched a pack video this should be familiar we either have pad X or pad Y and this is going to expand the space
around the widget to give some space between the current widget and any neighboring widgets
meaning pet X or pad y create space around the widget besides that we have iPad X or iPad Y and this one is
expanding the border of the current widget it essentially makes it larger
back in the code to make this Label 3 here visible we want to add pad X let's
say 20 and Pad y let's go with 10. although before that I want to fix the
typo let's try it now there we go there is quite a bit of space in the X and the
y-axis although on the x-axis this side we have a large amount because pad X is
twice as large as pad y and if you changed pad y to iPad y
we can see well not much of a difference but let me add a much larger number in
here a hundred third virtual visible there we go basically what happened now
is that this used to be row 0 then we had Row 1 Row 2 and then down here Row 3
originally Label 3 occupied this height here
but because of iPad why we are pushing the widget up and down by quite a bit or
not really pushing we are rather expanding it quite a bit what you want to be careful about here
is that this is shrinking other cells label one in particular has become much smaller
so do be careful with this one I only want to use pad y with 10 pixels
like so this is much cleaner what can also be really useful let me Place label
4 with the grid method you can place elements in the corner for example this
label 4 I want to have in the bottom right corner for that I will need to roll that is the maximum which is Row 3
and I want to have the maximum column which is also number three running this now gets me label 4 but not
in the ideal position Instead This widget should be in the
bottom right here for that we can use sticky I want this to stick to the South
East if I run this now there we go the label is all the way in the bottom right even if we resize the window it will
always be in the bottom right I guess I didn't mention it but the grid always scales along with the window
which lets you make really cool stuff I think at this point this is becoming
quite repetitive ultimately using grid is quite simple it really doesn't get
that complicated that being said there's one thing that can be kind of annoying
grit has a tiny bit of a uniformity issue which means when you have cells
with content their width is not what you would expect let me do an example
let's say we have a grid like this and we want to place two widgets one and two
inside of this example we have 0 1 2 and 3 columns they all have a weighting of
one let me use a color like this they have one one one and one they are all
supposed to be equally wide the issue is if this cell here is empty and this cell
here is empty then tkinter is going to make the existing cells with content
wider than they are supposed to be there is a formula to calculate the exact numbers but most of the time you don't
need that because you don't want this Behavior at all because it's well inconsistent and kind of annoying but
let me demonstrate this issue first I want to comment out the third column
and I also want to comment out all of the other rows besides the first one
besides that I also want to comment out what we have done for Label 2 3 and 4.
that way I can focus on one specific thing I already have label one with a
grid and this one occupies the first row and the first column I am just going to copy this
and change column 0 to column 2. if I run this now
you can already see the issue quite well this column here and this column here
they have the same width but this one here in the middle is much less wide
I guess much less white is a bit of an exaggeration but it is less wide than the other two the reason for that is if
a column or a row has a widget in it he Canta is going to give it a bit more
space that being said though you can fix this one quite easily all you have to do is
add one more argument and that's called uniform in here you are supposed to add a string
and you can give different columns is similar uniformity in practice though you are hardly ever
going to use it most of the time I just had an a for every single row or column
like so and then every single row or column have a uniformity
I can run this now and now we have all the columns having the same size or a uniform size this is still going to work
with the weighting and that way you have much more expected Behavior
with that I can get rid of Label 2 and
uncomment everything else like so this stuff here I want to uncomment as
well like I have done this stuff here
all of those are going to get uniform also I want to change the weight of
column with index 3 to a two and now if I run this we got something that looks very much
like the example I had earlier that one looked like soap and we are
definitely getting there that is leaving us just with the exercise and then we are done with this
video what I want you guys to do is going to add the buttons and the entry field as a reminder
the demo app I had looked like this you have to add this button and this button
and the entry field try to figure out in which row and which
column they are and see if you can place them as well shouldn't be too difficult so pause the video now and try to sort
this we know that button one is very easy to
place because we have row 0 and we have column three
this button is in the top right it has to have these values or button two this
one here I know we have one row here and we have one row here
and besides that we have one column here another column here and that brings us
then to this cell which means this one is going to be column two and row 2.
let's start by placing those two and then we can work on the entry field I want to start by placing button one with
the grid method for this one I know that the row is
supposed to be 0 and the column needs to be three if I run this now we have the
button in the top right but the button doesn't fill the entire available space this we do by using sticky
and adding north south east and west which is what
I am always using but you could change the numbers here around as you want this could be north east south west it really
doesn't matter tikanta just cares about the numbers being present in there I can duplicate this slide now and
button two I want to place in Row 2 and column 2.
let's see this is looking pretty good finally we have to place let me open it
again we have to place the entry widget this one is a tiny bit more tricky
for example we know that this button here is on row 2.
which makes all of this row number three the issue is the entry is not perfectly
centered in here that would be roughly this line instead what I have done for the entry is I have taken up Row 2 and 3
and place the entry widget in the middle of that which places it roughly here which means we want to have column
number three but then for the row we want to start on two but occupy two rows
in total that should be fairly easy to implement I want to get my entry widget I want to
place it using grid the row is going to be 2 and the column is going to be 3.
like so if I run this now we have the entry widget right next to the button to push it down I want to add
a row span it should occupy two rows if I run this now there we go this entry
field is now in the position we had before you could make this a bit more explicit
by adding sticky to it although that would give us a really large entry field like so that's a bit weird because entry
only allows one line of input but it certainly works in this case though I don't want to add sticky in here I guess
we can add sticky or east and west like so that I think is a bit better
with that we have all of the basics of the grid method I hope it wasn't too bad
if you understand grid you understand the most common layout method in tkinter this one especially from a complex
layouts you are going to use all the time in this video we are going to cover the
place layout method what we are going to create is going to look something like
this once again not a particularly pretty app but it definitely teaches you
quite a bit on top of that this one is quite flexible and here you can see a
couple of different effects I'll explain them as we go along so let's talk about place
widgets are placed by specifying the left the top the width and the height of the widget this is a very flexible
system also I think a fairly simple one to understand although when you are
placing widgets you can do this in two ways you can either use absolute or relative values
let's start by talking about absolute values for this we once again have a window or any kind of container it
doesn't really matter and this container right now is 400 pixels wide and 800
pixels tall if we want to place a widget inside of this we would have to specify at least
two but ideally four values these four the values we absolutely have to specify
are these two values here those are crucial with these points we are placing
the left and the top of the widget which is this point here in this particular example the top left of the widget is
100 pixels from the left side and 200 pixels from the top besides that we can also specify the
width and the height of the widget these numbers are optional if you don't specify them the widget is going to have
the size of its content let's do another example we have a widget all the way at the
bottom for this one we once again would have to get the top left point
this one has zero pixels from the left and from the top we have something like
let's say 500 pixels the widget is about let's say 200 pixels
tall and it has the entire width of the window or the container which is 400.
and that's it I hope the system makes sense besides that we have a relative
values for this again we have a window or any kind of container but instead of
specifying a specific width or height instead we separate this thing into a
coordinate system that starts from zero and goes all the way to one and this we do both for x and for Y
which means that this point in the top left always has the coordinate 0.0 and
0.0 1 4 Y and the other for x
the bottom right point of the container then is 1.0 and one point for both axes
that way if you want to place a widget you would have to do it like this
instead of specifying a specific distance like we have done here we are telling the widget or the left side of
the widget to be 10 of the width of the widget or at 20 from the top of the
widget we can also do this with the width and the height for example we can tell the widget to have 40 percent or ten percent
of the width or height of the container other than that the system works in exactly the same way so if we do another
example for this widget the left position is still going to be zero let's put a zero here for the top
position this one is going to be a bit larger let's say this one would be 0.6
the height of the entire widget would be I don't know let's say 0.2
finally the width of this thing is going to be a one because I want this to cover
the entire width of the container once again that's basically it for the
basics of place it well is quite simple so let's have a look at all of this in
code I already have a few lines of code ready if I execute all of this all we can see
is a basic window the reason for that is that these widgets are not being placed on the
window let's create a layout then I am going to start with label 1 and
this I want to place using the place method for this one we at the very least need X
and Y coordinates and let me use some really simple numbers X being 0 and Y being zero if I
run this now we can see label 1 in the top left I guess I should talk about the widgets we have we have three labels
label one two and three they all say the same thing basically they just have
different background colors red blue and green besides that we have a button since we only have one button I guess I
can rename this just a button there we go now if I run this again we
can see label 1 in the top left the reason for that is that the entire
container the window in this case is going to be a coordinate system that goes something like this with the origin
point being up here or rather more specifically up here this point is 0 and 0 if you want to go
further to the right we have to increase X and if you want to go downwards we have to increase y so plus Y and plus X
if you are only familiar with high school math this might be a tiny bit confusing because in high school math if
you want to go up you have to increase Y which we are not doing in this case which can be a tiny bit confusing
you will get used to it quite fast and well all we have to do now is play
around with these values for example if I change X to 100 and Y to let's go with
200. if I run this now we can see a difference what we have is X being 100 meaning we
have a distance of 100 pixels between the left side of the container this side here and the left side of the widget
this distance is 100 pixels other than that we have y and this tells
us that from the top of the container to the top of the widget we have 200 pixels
of a difference what we can also do is set a width and a
height for example the width could be 200 actually let's go with 300 so we
have different numbers and for the height I want to go with 50. let's run this now and there we go the
widget is much wider and a tiny bit taller by default a widget is only going to
take up this space it needs to display the text which by default would be something like this
but if we specify numbers for width and height we are setting the width in this case to 50 and the height is going to be
300 that's very hard to read sorry about that we can play around with the numbers here
quite a bit for example X could be 300 y could be 100 and let's say for the width
we have 100 and for the height we have 200 and now we get a different kind of
witch that is all the way on the right to understand the numbers here we know that the entire widget is 400 pixels
wide this thing is 400 pixels and we are placing the left side 300
pixels from the left side of the window this distance here is 300 pixels
on top of that we are setting the width of the widget to 100 pixels meaning this distance here is going to be 100 as a
consequence the widget ends exactly on the right side of the container after that for y we have 100 meaning
this distance here is 100 and then we are setting the height to 200 so this
one here is 200. all of that I think should be reasonably
straightforward with that we have covered the absolute positioning besides that we can place
Label 2 and for this one I want to use relative positions this we do in a
similar way we still have to specify X and Y values except now they're called
relative X or Rel X and relative y or Rel y in here just to get started I can again
set 0 and 0. running this now we can see Label 2 all
the way in the top left although now I don't specify pixels instead if I set this to 0.5
and let's set y to 0.2
the top left position of the widget this point here is exactly in the middle of
the window meaning we have 0.5 to the left and 0.5 to the right 0.5 like so
and then from the top we have 20 but I think it's not too difficult to understand
if we use different numbers let's say 0.2 and 0.1 we should be a bit closer to
the top left we can also specify the width and height in a relative way this we do with
relative width or with relative height for this one let's say I want to have 40
of the width of the container and let's say 50 of the height
and difference now we have a much larger container I think the numbers here are fairly
straightforward I well I don't think the system is very difficult so it shouldn't be too hard to understand but drop a
comment if you think it's super complicated what we can do as an exercise to make this a bit more interesting is I want
you guys to place label three labor free should be positioned using absolute
numbers meaning we have x y we have the width and we have the height
and label three should be exactly in the same position as Label 2 meaning you
have to convert these numbers to X and Y positions possibly now and see if you can figure
this one out are to convert these numbers you have to
know the size of the container which in our case is the window for example for X we have to convert 400
by 0.2 which is going to be 80.
Y is 0.1 of 600 which is just 60.
the width is 40 of 400 which is 160
like so and height is 0.5 of 600 which is 300.
that should be all if I run this now we can see level 3 covering all of label 2.
that looks pretty good and well with that we can see that relative and absolute positioning works pretty well
together although that being said you do want to use relative positioning I can
demonstrate why quite easily here we have the app again right now this is looking really good but once I start to
move the window around we get some massive differences
the problem here is that Label 2 is relative let me move it to the side like
so the only widget that scales along with the window is label 2. this one here
it scales along with the widget because we are always using relative values
whereas label 1 and level 3 have absolute positioning so those two do not
move regardless of what the window is doing if you wanted to scale those you would have to update the value every
time you are changing the size of the window which would be kind of a pain in ninety percent of the cases you want to
use relative positioning because this one is much more flexible there's one more case that I do want to
cover I want to place this button and where I want to place it let me run the app again the button should be in the
bottom right corner of the window down here this I can't really do right now
although we can get started once again I want to get my button I want to use the place method and I want
to use relative positioning let's set relative X to 1 and relative y to 1 as
well if I run this now we cannot see the button the reason is that we are placing
the top left of the button in this corner here but then the rest of the widget goes in this direction and this
direction meaning the button is this yellow outline which is just outside of the window but
we just cannot see it this obviously is a problem so we have to learn about another argument that we
can control what is called the anchor when we're using the place method the anchor controls which point is placed by
default if this one is the widget we are setting the top left point but this you
can customize and here we have all the points you can use the default here is North West which is
telling tkinter to place the left and the top of the widget which is giving us
this point that's the default one that being said we could also tell tikenta to place the south east of the
widget and then we will place this point here besides that you could also tell
tikenter to place the center of the widget then you will place this point if you know the grid method this should
look fairly familiar let's play around with it for my button I want to set the anchor and that is atrocious spelling
that looks much better we need a string and I want to place the South East Point running this now now we
can see the button this one works as always it's a button to see a bit better what's Happening
Here I am going to place the center now we can see we can only see the top
left area of the button the reason for that is we are placing the center of the button in the bottom
right of the window or the container to be more specific that way we can only see the top left and the rest is cut off
I do want to cover one extra case and that is using the place method along with a frame I want to create a frame
with ttk and frame the master here is going to be the window after that I want
to create two widgets one is going to be a frame label which is going to be ttk
and label with the window as the master and the text could be frame label
on top of that I want to give this thing a background color which we can set to
Yellow that's the one we haven't used yet besides that I'm going to duplicate the entire line and change frame label to a
frame button this is going to be ttk and button enter button is not going to have a background
color also this should be frame button to be a bit more consistent what I now want to
do is to place this Frame using the place method and also add these two
frame labels inside of this Frame and for that I have already seen one problem
and that is that this label and this button need to have the master as the
frame because I want to place those two inside of the frame this I want to do in another section I'm
going to call this one layout frame layout looks good first of all I want to place the frame
itself which I do with the place method and this one I want to have the relative
X position of 0 and the relative y position of 0 as well
that way it's in the top left the width I want to have
0.3 and the relative height is going to be 1. that way if I run the entire thing
we can't really see it but the frame we have just created is going to cover an area roughly this size and I am very
very bad at drawing straight lines inside of this I want to place the frame label and the frame button
I will start with the frame label I'm going to use place again for
relative X I want to have 0 relative Y is also going to be 0 meaning this label
is in the top left and besides that I want to cover the entire width so relative width is 1 and
relative height is going to be 0.5 and there we go we have a frame label
that covers one third of the window what you really have to understand here
is that place always works relative to The Container which in this case is the
frame right now the width of the frame is this width here which means when we are
specifying relative width of one water frame label we are telling this Frame
label here to cover this entire width the width of the container if the frame
label had the master as the window then it would cover the entire width of the
window what you want to keep in mind here the parent or the master is incredibly important for layouts
but once we have that I also want to place the frame button
this one should take up the bottom half of this container relative X should still be zero but relative y should be
0.5 the other numbers I think can remain The Identical and that is looking pretty
good we have separated the space in half and I can even drag the window around
this is still working just fine cool I'm really happy with that on top
of that for this button here the one we created earlier I want to set the anchor to Southeast so all of this looks a bit
better ready with that we have covered all of the basics of the place method
all we have to do now is an exercise and then we are done what I want you guys to do
is this one here create a label and place it right in the center of the window the label should be
half as wide as the window and beat 200 pixels tall also give it a background color to make
it a bit nicer to look at which color you want to choose is entirely up to you
I am going to start by creating an exercise label this is going to be ttk
and label the parent here is going to be the window text is going to be the
exercise label finally I want to have a background color
let's go with orange this exercise label I now want to place
a position here has to be right in the center of the window which means I want
to have a relative X being 0.5 and relative y should also be 0.5
running this now we get the exercise label although it's not perfectly centered the point we have centered is
the top left of the widget what I want to do is to place the center of the widget right in the middle of the
window for that I have to set the anchor to Center and I am somehow unable to spell
anchor that's right now and there we go this is looking much better finally we have to set the width and the
height of the label it should be half as wide as the window and 200 pixels tall
which means the relative with is going to be 0.5 enter height is going to be 200. I can
run this now and this is looking pretty good on this line I realized I didn't mention
but you can combine these values quite easily so you could for example set the relative width and the height in pixels
they work together really really well the same could also be done with X and Y
for example I could set X to I know 200. and I think since the entire window is
400 pixels wide this is still putting us in the middle of the window you do want to be careful using this
though because if you now resize the window like so things start to get a
tiny bit weird so just keep that in mind there's one important issue that you
have to understand about tkinter layouts and that is the widget's sizes because
that can be a tiny bit tricky let's talk about it indicator every widget can have
a custom size however what you also have to understand is that this size will always be
overwritten by the layout methods you basically have two places where you can add a size of a widget but one is
prioritized for example if we have something like this we are creating a
label this label has some text but much more important we are giving this label a whiffed this specific width in this
example is going to be 50. really important here this is not pixels
TK enter uses a really weird measurement system where this 50 is the width of 50
characters it's kind of weird but don't worry too much about it
what is much more important for now is that we have two different kinds of width way after with I've just talked
about and then we have the width of the pack method because in here we're telling the widget to fill the entire
horizontal space as a consequence tkinder has to decide is it going to use this with here or
this width here and the default answer for tkinder is going to be this one here tikenter
always relies on the inbuilt layout methods as the main layout tool so if you have two different kinds of
width the actual width you are going to get is the one from the inbuilt layout method now this might seem quite simple
and most of the time it is but in some cases this can cause problems with the
layout which is why I want to talk about it I already have a couple of lines ready if I execute the entire thing we have an
app with two labels inside both labels have a background color I am importing tkinte at the top then
I'm creating a window after that we are creating two labels and after that we are placing both labels using the pack
method finally we are running main Loop to see the window all of this should be fairly simple and
now we can start working on the layout itself or more specifically I want to give Label 2 a custom width label 1 is
going to be a reference so I'm not going to change this which should make it a bit easier to see what's going on
both labels are right in the middle of the window if I now change the width of Label 2
with the with parameter I can give this a width of 50. if I run this now you can
see we have a much wider label too also what I really want to emphasize
here is that the entire width of the window is 400. this with here is 400 and
this is in pixels however this with here of the label is
this Dimension here and this very obviously is not 50. pixels
that is not the unit we are using instead what the Kinder is using is 50
whiffs of a character it's a very strange measurement you are not going to use it that much anyway so
I'm not going to go into much detail but just be aware we are not using pixels all right but with that we have a custom
width what we can also do inside of Label 2 when we are packing it we can set the
fill and this determines the actual size of the widget if I in here set this to X
and run this again we can now see that the second label covers the entire width of the window
which means that this for the X here covers the entire window while this width here is simply being ignored in
practice you could just remove it and this is what you probably want to do 99 of the time you simply want to use the
layout methods to create the size of a widget because that way the entire system is going to be responsive and
while using hard-coded numbers can be a problem for example if I remove this
fill here we can see our label has a certain width again but now if I resize the window
this doesn't change we always have the same width of the label which is going
to be a problem if the window gets too small or if the window gets really large this is a general thing you want to
understand for layouts you basically always want to have flexible layouts otherwise things can break very very
easily with that covered I want to do one more thing right now we looked at the pack
method but we also have to look at the grid layout for that one I want to give my window a
couple of columns and a couple of rows let me start with the column with column configure I'm going to create two
columns 0 and 1. both are going to have a weight of one and I'm going to set the
uniform to a this I can now duplicate and I want to have a row configure
I also want to have two rows with 0 and 1 with the same weight and same uniform argument that way we have four cells
with an identical size inside of this one I now want to place my label 1 and label 2 which means label 1 dot grid
this one I want to place in row 0. and column zero I can duplicate this entire
line change label 1 to Label 2 and this one should be in row 1. now if I run
this we can see we have two different sizes for the labels this once again
happens because of this width here however I can overwrite this quite
easily if I for example for Label 2 said sticky to north south east and west we now have
the label covering the entire cell so once again the inbuilt layout method
is overwriting the custom width we have set inside of the widget if you were using the place method the
same thing would happen this can be fairly confusing and frustrating at times so I hope this
helped another important part of the Kinder is the stacking order this one determines which widget is on top of
another widget so in here I can place different widgets on top of each other
especially when you use the Grid or the place layout method this can become quite important because for both of
those layout methods it's very easy to place the widgets on top of each other so you need to be able to control which
widget is on top of the other for that the most basic thing you have to understand is that widgets always
placed on top of other widgets when they are created really important here not
when they are placed for example we have two labels both are TDK label and
nothing else the arguments here really don't matter and then we are using the grid method to place them once again I
am ignoring the arguments here but just imagine they are on top of each other in this case Label 2 is going to be on top
but this is because we are creating Label 2 after we are creating label one
if we switch this around then label 1 would be on top of label 2. the grid
method itself doesn't have any influence on that it's kind of confusing to be honest but well it is what it is on top
of that you can also raise witches to the top of all of the widgets or on top of another widget
for this video I have something slightly more complex ready if I execute this I
have two labels label one and label two on top of that I have two buttons in the bottom right we have arrays label one
and race label two later on those are going to control which label is on top although right now they don't do
anything inside of the code I am importing tkinter I am creating a window
then I'm creating four different widgets I have two bits of text and two buttons
button one and button two after that I have a layout section in here I am placing the two labels using the place
method the arguments here are basically random the one important thing is that
those two labels are overlapping with each other that way I can show you which label is on top of the other
besides that we have the buttons and the only important thing here is that both buttons are in the bottom right that I
achieved with relative y being 1 and relative X being 1 or 0.8 that way both
buttons are in the bottom right with button one being a bit further to the left the anchor here is really important that
way we're placing the origin point of the widget in the bottom right of the widget with that covered we can start talking
about the actually important part and that is that right now we have label one
being below level 2. the reason for that is that we are
creating label one before label two I can demonstrate this by creating Label
2 before label one now if I run this we have label one in front of label 2.
however the layout method so place in this case has no impact on this whatsoever
if I place Label 2 before label 1 we get the same outcome and if I place Label 2
after label 1 we still get the same result in my case I want to start with label 1
and then create label 2. this means that Label 2 is on top of label one Now to
control the stacking order you have a couple of different approaches the easiest one is called lift for example
after I'm creating the widgets label 1 and label 2 remember here Label 2 is on
top right now so we have Label 2 on top but I could get my label one and then
run the lift method on it this elevates label 1 on top of all of the
other widgets alternatively I could get labeled 2 and then run the lower method
on it that way we are lowering Label 2 below all of the other widgets
so let me add both in here so you can see them in the code a bit easier we have lift and we have lower
besides that what we can also do let me comment out left and lower for now inside of the button let's say for label
one for now I want to add a command this command is going to be a Lambda
function because it will be very simple I want to get label 1 and what I could
do is simply run the lift method if I now run this again
note here label one right now is below Label 2 but if I click on raise label 1
we can see label 1 is on top of label 2 and what we can also do if I copy the command here now for race Label 2 I
could get Label 2 and lower it so now if I run this again and now if I
click on raise Label 2 we are lowering label 2. the naming here doesn't really
make sense but I'm going to change this anyway in a second so lift and lower you can use quite well
besides that you could also use TK rays and that does the same thing as lift let
me add it for both and now if I run this again we can raise label 1 or race label 2.
and that way we can control which widget is on top of the other you might be wondering now what is the
difference between lift and TK rays and quite honestly I have no idea they seem
to be doing the exact same thing so you can use whichever one you prefer it really doesn't make much of a difference
so with that let's do an exercise I want you guys to add a third label and
a third button meaning label three here and button number three
the command for button number three should raise the third label all the way to the top pause the video now and try
to implement this one yourself
this should be a fairly simple thing to implement because all we have to do is duplicate Label 2 change this one to
label three I also want to change the text to label 3 and for the color we can go with blue after that I want to create
button number three with button number three this one should be race label three and for this one I want to have
Labor 3 and then TK race with that covered I have to cover the
layout for both the label and the button for label three I once again want to use
the place method and here for the arguments I do want to have a different position so we can see this a bit easier
the numbers I went with X being 20 y being 80 the width is a hundred and
eighty and the height is simply 100. finally I want to place button number three for this I want to copy button 2
change it to button number three the only change I'm going to make here is
relative X should be 0.6 if I run your typing now we're getting
an error because I have some weird typo in here let me fix that like so and that
is looking much better now let's try this there we go now we have label three for this one if I click
on raise label one now we have label one all the way on the top the same thing we can do with label two and then we have
label three so one of this is working quite well and you can very easily control which label is on top this would
also work with literally any other widget I am simply using labels because they are the most easy to work with and I can
visualize easily what's going on now there's one more thing that I do want to cover and that is that both for TK rays
and lift we can add one argument and that is called Above This
by default TK race puts a widget all the way on top of all of the other widgets
but if you want to have a widget only on top of another widget you would use Above This for example for label 1 when
I'm clicking on TK race I want to only elevate it on top of label 2. so if
Label 3 is on top then label 1 would not be elevated all the way to the top it
would still be below the third label I hope that makes sense let me illustrate actually so now we have Label
3 all the way on the top if I click on raise Label 2 we have Label 2 all the way on the top
and now if I click on raise label 1 we have label 1 all the way on the top although more specifically label 1 is
now only going to be on top of label 2. if I raise Label 3 all the way again
and now erase label one again nothing is going to happen because label 1 already
is on top of label 2. I hope the logic makes sense here if you
think about it for a couple of seconds it should be fairly straightforward I supposed to illustrate this a bit
better if I raise Label 2 all the way to the top and now I raise Label 3 on top of it now if I click on Race table 1 the
green bit is going to be on top of the red bit but below the blue bit so Ray stable one there we go label 1 is on top
of label 2 but below level 3. the above this argument would also work with lift
I can run this again and we would have the very same outcome once again I don't really know what are
two different methods for the same thing but choose whatever you want it really is up to you
a really important aspect of tkinter is toggling widgets what that means in
practice is something like this we have a label and I want to talk that meaning I'm
switching it on or off or visible or invisible whatever you want to call it
this is actually quite simple if you know what you are doing in tkinder so let's talk about it inside of tikinta
you don't really hide or show widgets instead what you're doing is you are removing or adding widgets to the layout
chances are you already know how to add widgets this either happens with pack Grid or place but all of these methods
also have the opposite for example for the pack method we have pack for get and
this one does the opposite of the pack method it removes a widget all of this can also be done while the app is
running and if you know how to use it you can hide and show witches quite easily I already have a couple of lines
of code ready I am importing decanter I am creating a window and I'm running the entire thing
so this is what we're getting but now we have to cover a couple of
things for every single layout method we have to look at the actual layout method
and how to do the opposite and let's get started with the place method this one I think is the easiest one to understand
we first of all have to create a button let me call it ttk and button with the
window being the parent and the text is going to be toggle label
finally this one is going to get a command that I'm going to call toggle
label place we're going to create this one right away under the place method so all of
this is a bit easier to put together toggle Place method no need for parameters and for now I'm just going to
add paths in here finally I want to add the button and let's use the place method for that
since the button isn't going to do anything besides being clicked on the position here doesn't matter let's go
with X being 100 and Y being 50. so now if I run the entire thing in the
top left we have a button although I guess it's a bit too far down let's change this to 10 and 10. like so now we
have a button in the top left that I can click on but nothing's going to happen to make something happen we
need another widget I'm going to call this one label but it's going to work with any widget and in here I want to
create TDK label with the parent being the window and the text is going to be a
label and this label I want to place in the center of the window which means label
dot Place relative X is going to be 0.5 relative Y is going to be 0.5 and the
anchor is going to be the center let me fix my typo really quick and if I
run this now in the middle of the window we have a label what I now want to do is if I click on
toggle label this label should ever be hidden or shown I'm going to start by
simply making this label disappear this is going to happen inside of this function
to achieve that all we have to do is get the label and then Place forget
this is going to remove this label here and well then we can't see it anymore so
now if I click on toggle label the label disappears although the problem is if I
click on it again nothing is going to happen because well we can only really forget it once this doesn't work a
second time but the basic logic is in place here we have a widget that's
visible in the first place and then we make it invisible but to make this actually interesting we
want to have a proper toggle functionality and for that I want to create another variable I call this one
label visibility by default this one is simply a Boolean
value of true this I want to update inside of this function which means this needs to be a global variable so Global
label visibility I should probably rename this a tiny bit let's call it label Visa bill
that is making much more sense and essentially what I want to do if I'm clicking this button I'm going to check
if the label is visible or not which means if label visible if that is the
case I want to forget this label besides that I also want to get label
visible and set it to volts once I have that I can create an else
statement and now if I'm running this function here I know the label is not
visible because label visible is false if that is the case I want to set label
visible back to True finally all I have to do is run this method here again I am
reattaching the label to the window or to any kind of container this would also work with frames which means I can
simply copy this entire line here paste it in there and now if I run the entire
thing I can click on toggle label the label disappears and I can click on it multiple times and now we make it appear
or disappear and this is basically all you need to toggle a label or literally any kind of
widget so for example this label here could also be a button now we have a button
and this one would still work just fine although I'm going to keep it being a label
and this is the basic logic that you have to understand besides place we also
have grid so let's work with this one next I now want to work on the grid for
this one first of all we have to create a couple of rows and columns which means I want to get my window and run column
configure I want to have two rows zero and one that have the same weight let's
go with one and I also want to set Yoon form to a so they are the same size like
so besides that I am duplicating the entire line and change the column to a row although I only want to have a
single row so this isn't going to be a tuple it's just going to be a zero with that in place I want to create a label
and a button exactly the same thing I have done here
as a matter of fact I'm going to copy all of this and paste it in here and uncomment the entire thing
the button is going to be basically identical the only thing that's going to change is I'm not going to use place
instead I'm going to use grid the button is going to be in column 0
and row 0. for the label I still have label visible
being set to true I am creating a label but I'm not using the place method to
place it instead I'm going to use grid the label I'm going to place in column
being 1 and row being 0. if I run the entire thing now we are getting an error
that we are using a function that doesn't exist right now let me remove it and run the entire thing again there we
go we have toggle label right next to e-label although nothing is going to happen if I click on the button for that
we have to create the command once again this one is going to be toggle label
except now we're using grid the basic logic here is going to be the same as in place
but let's create the function itself Define I called this one toggle
label grid only for parameters and then here we are going to do the same thing
we have done up here but for good practice let's do it from scratch and if you want to practice
yourself try to do all of this yourself all you need here are grid and grid
forget but in my case I want to start by creating Global label visible that way
we can change this variable here from inside of the function if the label is
visible I want to get my label and I want to run
grid underscore forget besides that I want to set label visible
to true this we can already test if I run the entire thing now and I click on
toggle label the label disappears although if I click on it a second time nothing is going to happen that is the
functionality we have to work on right away so else I want to set label visible
back to true and then I have to run this grid method here one more time
so I can just copy it paste it in here and now this should be working let's try if I now click on toggle label the label
disappears if I click again nothing is going to happen so something went wrong I can already see the problem
this label visible here should be false now let's try it again if I click on
toggle it disappears if I click again it reappears this is looking really good
cool with that we have the grid method and this basically works in the same way
the displays method here is going to work and both of those are working really well because the layout isn't
really affected by other widgets so where we are placing the label isn't really affected by the placement of the
button each of those either have their unique positions like in place or their
own unique cells like in the grid this is going to be different for the final layout method and this is going to be
for pack for this one once again I want to copy the button and the label
place them in here and uncomment them and those I simply want to place using
the pack method also let me get rid of this command here so we're not going to take an error
if I run the typing now we get the two widgets right next to each other what is
really important to understand here is that the position of this label is influenced by this button the pack
method always places widgets on top of each other and this is kind of a problem
when we're using pack for get let me demonstrate and then you're going to see how this is going to work
although I want to make some changes this button I want to have all the way at the bottom of the window so I'm going
to pack it after the label and the label I am going to set to expand to cover the
entire window if I run the entire thing now the label is basically in the middle of the window and the button is all the way at the
bottom now we can work with this if I press on the button I want to run a
function which means I have to use command again and I want to toggle
label pack for this we have to create another function toggle label pack once
again no need for parameters and in here I can already demonstrate what the problem is going to be if I simply run
label and pack forget try to predict what is going to happen
but well let me run the entire thing and now if I click on toggle label the
button is going to be all the way at the top the reason being that originally the label covered all of this space and then
the button was placed at the bottom here but since we got rid of the label this
entire thing here disappeared and the button is now all the way at the top and this is going to be a problem that
we have to account for and accounting for that is going to be your exercise what I want you guys to do is to fix the
code so the button stays at the bottom pause the video now and try to figure this one out as a tip here try to use a
widget that is by default invisible
righty this solution here is if I run the entire thing again by default we
have two widgets we have a label and we have a button with the label taking up
this entire space here what I want to do is create a third widget and this one is going to cover
the same space as the label although it is not going to have any content
this could either be a frame or a label without any text both would be fine in
my case I'm going to work with a frame and this Frame is only going to be placed when the label is invisible
that way the button has something to be stacked below but let's Implement all of this step by step first of all I want to
create another widget this is going to be the frame this is simply going to be ttk and frame
and the parent here is going to be the window we're not going to place this one right away instead inside of the toggle label
pack function I want to once again set the label visible as a global variable
and now I can use the if statement again if the label is visible then I want to
pack forget the label I also have to set label visible to false
but now what I also want to do is to get the frame and pack this one
on top of that since the frame is supposed to take up the entire space that the label has taken I want to set
expand to true so expand is going to be true and now if I run this I can click on
toggle label and we have the same problem and the issue here right now is
when we are placing the widgets this label Here Comes as number one and then we are placing the button number two
so in the original widget we had the label something like this position and
then we add the button below this position here and the button moved all the way to the
top once removed this label here the problem now is that once we're
adding this frame with the pack method we are adding it below the button so the
label is going to be here which for our purposes is not going to be useful
we have to find some kind of method to place the frame on top of the button
and this we can do quite easily because the pack method has another useful feature
that is called B4 we can tell the frame method to pack a widget before a certain other widget
the widget we want to pack the frame before is the button
and now if I run this again I can click on toggle label and the button stays all the way at the bottom
the reason for it is that now we have created this Frame here and packed it
before the button so it is going to be in this position if you play around with this this should
become fairly obvious although most of the time when you're hiding or showing widgets you want to use either place or
a grid because this tends to get a tiny bit more complicated but let's finish it and then we can wrap
up this video I want to have else I first of all want to get the frame again and now run pack or get
this Frame should only be there when the label is not visible once the label is
visible it is going to take up the entire space of this Frame which means I also have to get the label
back which I'm doing with the pack method and this one needs expand being true and
also we have to use before again I want to have this labeled before the button
and finally label visible is going to be true let's run this one and now if I click on
toggle label this one is working really good so with that we can toggle widgets hope
that was helpful in this video we are going to combine the different layout methods in tkinter
what we are going to make is going to look something like this here we have a fairly complex UI that
also scales along with the window this is what we're going to create and
for that we're going to use Place pack and grid they all work together really well for all of this
later on when we can style things this is going to look actually good but we are definitely making progress
and before I jump in I do want to talk about the layout here it's quite important to understand
on the most fundamental level we are separating the UI into two parts which
is going to be two frames one is here and one is here both of those are placed with the place
method inside of the left container this one here we are mostly using the grid method
for example here's one row here's another row and here's a row at the end and then we have a couple of columns
they are three in total you can see this quite well with the sliders they are on the left and on the
right column although that being said in the bottom there is one frame that covers the
entire width of the column inside of that one we are using the pack method to place these two check boxes
finally the entry widget here at the bottom it's kind of hard to see this one is placed
using the place method that way it's always at the bottom in the middle after
that we have this entire area for this one I am using the pack method
to create these two areas with each area being one frame and
inside of the frame we are creating another directional layout that is just going to contain a label and a button
I already have a few lines of code and I realized the title I didn't change from
grid this should be combined layout but other than that we have a window
that's 600 by 600 pixels although there's one thing I already want to do and that is I want to get my
window and set a minimum size like so the minimum size should be 600
by 600 that way the window cannot be too small which would end up looking very strange
once we have that we can start by creating the main layout widgets I call
them for this one I have a menu frame and I
have a main frame both of those are going to be ttk and
frame with the parent being the window those two I now have to place and this I
do let me add another comment Main Place layout I'm going to use the place method
to place these two frames for example I want to have the menu frame I want to use place and now I have
to specify an X position a y position a width and a height since I want a menu frame always to be
on the left side x is going to be 0 and Y is also going to be 0. you could use
relative values here but since we are using 0 it really doesn't matter it's going to give you the same result
although for the width I do want to get the relative width this is going to be 0.3 in my case and
finally for the height I want to have a relative height that is going to be 1. if I run this now we can't see anything
because frames by themselves are invisible although we can make this visible by creating a ttk label with the
parent being the menu frame and this one is going to have a background of red
this I want to pack right away and in here I'm going to set expand to
true and fail to both if I run this now we can see the entire
area of the menu frame with that we can create the Mainframe and the Mainframe is going to take up
the entire remaining space which means for place I want to set e
relative X position and this one is going to be 0.3
I know I have to use 0.3 because the width of the menu is also 0.3 that way
those two start on the same point the Y position though is still going to be zero both of the widgets are supposed
to start on the top of the window after that I want to have a relative
width and this is going to be 0.7 the number here should be obvious with the
width and the height we have a total number of one so we are covering the entire rest of the window
finally I want to have a relative height and this one is going to be 1. to visualize this I want to copy the label
and change the background color to yellow and the master is going to be the
main brain let's try this one now and there we go we have covered the entire area of the
window I can also resize this and this is looking pretty good I guess if you make the window too large
the left side is going to become quite large but I'm not going to worry too
much about it let me comment out those two lines I'm going to reuse them in a bit for some
debugging just to see what we are doing next up I want to create the menu layout
widgets I guess we could just call this menu widgets for those I have to create quite a few
different widgets to save some time let me just copy them in we have to create all of these
widgets we have three buttons button one button two and button three then we have
two sliders slider one and slider two then we have a toggle frame and inside
of this toggle frame we have two toggles toggle one and toggle two both of the
toggles are just going to be check buttons I guess just to get started I can comment out the toggle frame so we only
have a couple of buttons and a couple of Sliders these I want to place now
now I want to create the menu layout since I want the menu to have the grid
layout I have to create the columns and the rows which I Do by getting my menu
frame and then creating column configure I want to have three columns which means
I'm going to create a tuple with 0 1 and 2. the weight I'm going to set to 1.
besides that I want to create a row configure and I want to have
three and four rows in total all of which have the weight of one once I have that I can
actually place things for example I can get menu button one and I want to use the grid method the
button here should be in row zero column 0 as well and let's just see what we get
we get an error because I have made a typo this should be column configure
let's try it now and there we go we can see button one in the top left the button doesn't cover the entire area for
that we are going to need the sticky argument and I want a button to stick to the
north south west and east of the container or the cell and now if I run this we have button one in the top left
finally I want this button one to be a tiny bit wider for that I'm going to set
the column span to two it's going to be very hard to see right now but this
button is now going to span two columns once I have that I can duplicate the
line and now I want to place button 2. this button is going to be on row 0 but
on column 2. it is only going to span one column though
and I want to stick the widget to all four sides of the cell let's run this one now and there we go
we have button one and button two with button one being much wider than button two
if I expand the window you can see this much better to really make these columns and rows
consistent I want to add the uniform argument uniform and I'm going to set the
argument here to a it doesn't really matter what it is as long as those two identical strings
now if I run this we can actually see that button one is twice as wide as button two that looks much better
after that I want to place menu button three this is again going to use the grid
method I want to set the row to 1 and the column to zero
column span is going to be free and sticky is going to be north south east
and west with that we are creating a button that spans the entire second row the result
is going to be three buttons in this kind of layout next up I want to place the sliders
these two sliders here both already have the orientation of vertical that's why
they're going up and down and just to demonstrate I want to have the sliders here and here which means I want to get
my menu slider 1 and I want to use the grid method again
the row should be number two here and column is going to be zero I want the
row span to be 2. and finally I want to set sticky to all
four sides so north south east and west running this now gives me one of the
sliders although I don't like how close this is to the buttons
to account for that I want to set pad y to let's say 20 pixels
and now we have a bit of a distance between the two which I think looks much better this I can now duplicate because I want
to place slider 2. or this one I want to have column two
and Row 2 can stay the same in fact all of the other arguments can also remain
identical if I run this now we have both of the sliders this is looking really good
with that we can place a slightly more complicated layout and that is the
toggle layout the one I have created here and commented out for now
this one is going to be one frame and the frame consists two toggle or two
check buttons to be more specific in terms of my layout though I can work with these separately for example I
first of all want to get my toggle frame and use the grid method to place it
I want this one to be in row number four and the column is going to be zero
although I want this frame to span the entire width of the
container so column span is going to be free what I also shouldn't forget is I
want to set this to Sticky with north south east and west just to be sure
and if I run this now we can't see anything the reason is again frames are
invisible we can use the ttk label again I created earlier I now want to set the toggle
frame as the master run this again and there we can see we are covering the
entire bottom bit so I want to comment this out again and now I want to use this area to place
these two toggle buttons for that I am going to use the pack method
I want to get my menu toggle one and pack the entire thing
since I want both of these toggles next to each other I want to set this side to
left and I want to set expand to Rue
this line I can now duplicate and change toggle 1 to toggle 2. and let's see what we get
that is looking really good we have both of the toggles right next
to each other I hope here you can see how it is really easy to combine different kinds of
layouts we have created the main layout using the place method then we have
created a grid inside of one of the frames and inside of this grid we have created another frame with the pack
method that way using containers gives you a ton of power
finally what I want to do is I want to place the entry let me call it entry
layout for this entry this entry doesn't exist right now
actually I want to create it when I'm importing all of the widgets here I want to create an entry widget and
this I do with ttk and entry the parent is going to be the menu frame
this entry I now want to place using the place method since I want this entry
widget to be in the middle at the bottom I want to use relative X being 0.5
then relative Y is going to be 0.95 and I want to set the relative
width to 0.9 if I run this now we get something
slightly weird or well if you understand place this should be familiar right now
we are placing the top left point and this one is right in the center of the
container right here the reason we get that is because we haven't update the anchor
for that we have the anchor argument and I want to place the center of this entry
widget let's try it now and this is looking much better this entry widget is now
always going to be all the way on the bottom of this container you could have also used another row
inside of row configure to place the entry widget using the grid method
although in my case I just want to demonstrate that you can combine different layout methods
although that has its limits you couldn't combine a grid and a pack
method for example if I wanted to comment out this one here and use entry
dot pack without any arguments run this we're getting an error the error message
we get is cannot use geometry manager with pack inside the reason is we
already have the grid method in here this though only applies to entry place is perfectly fine ready next up we
can create the main layout unfortunately for that we need a few
more widgets so let me add another section called main widgets and I'm
going to copy in the widgets I am going to need like so I have one more frame that I called
entry frame one inside of this Frame we have a label and a button alt label one
and button one both are super super simple the one notable feature here is that both of
them have the parent or the Masters entry frame one this one here this we're doing two times one time here
and one time here entry Frame 2 main level 2 and button two are basically identical to the first
one which means what I want to do if I run the entire thing again over this entire space here I want to
use the pack method to create two large areas one could look like this and one is going to look like this both of these
are going to be frames inside of each frame we are going to place the label and then we are going to
place the button which means we have to get started by placing entry
1 and entry 2. for that I want to get entry one and use
the pack method since I want both of these frames next to each other I want to set the side to
left other than that I want to set expand to true so we are covering the entire
horizontal space and I want to set fill to both this I can now duplicate and set
entry 1 to entry 2. all of the arguments though can stay identical
this if I run this again is not going to be visible because once again frames are invisible but I can once again use these
two labels to make all of this visible the master for the first one is going to be entry frame 1 and the master for the
second one is going to be entry frame 2. if I run this now this is looking pretty
good although I do want to have some padding between the two I want to create pad X
I went with 20 here and I want to create pad Y which I also set to 20. now if I
run this again we have a bit of padding around them ready with that finally I can get rid of
these two labels at the end and instead place all of these labels and buttons
I'm going to start with main label one the side is going to be the top since
that is the default argument I can just leave this empty although I do have to set expand to true and
Bill to both this line I can duplicate again because
now I want to place main button one this one up here this is also going to get expand true
and fill both let's try it actually there we can see we have the label and the button
what I don't like is that those two are right next to each other to account for that I'm going to give the button pad y
of 10 pixels now we have a tiny bit of space between the two with that all I have to do is copy all
of this duplicate it and I can just change main label one to two and Main button one to
two the result is going to look like this and with that we have a fairly
complicated layout that is well working quite well obviously we have no functionality but
in terms of layouts this is basically as complex as taking the widgets are going to be
now that being said all of this is still not particularly manageable because we
have a ton of different sections and this isn't Pleasant to work with
but all of this is going to be much easier managed when we are using classes and this is going to be the next video
but if you want to challenge yourself a really good exercise could be to convert
all of this to a class-based approach see if we can figure this one out although if you can't do it don't worry
too much about it I'm going to cover all of this in the next video I'll guess I'll see you there let's talk about
using classes in tkinter and what we are going to make is going to look something like this this is the same layout we
have seen on the last part except now we are using classes to organize all of this which is making the entire app
significantly more manageable let's talk about it and then we can Implement all of this
the most important thing that you have to understand is that we are basically always taking some kind of widget
usually a frame but it doesn't have to be and then we're adding widgets to this Frame and then in the end we are placing
this Frame somewhere on the window that way we can organize lots of widgets very very easily
if you understand basic tkinter this shouldn't be too difficult to implement although to make all of this work let me
show you my setup here I have two python files open on the left side we have classes dot Pi this is
what I'm going to work in on the right side we have the previous code from the last video this is the same layout or
the same app except that we are not using any classes so what we're going to do in this video
is convert all of this into class based approach that way I can switch between the two
and illustrate what's going on now first of all we have to import the basics this I can just copy straight
away I want to import tkin to SDK and I also want to have ttk now that we have that I want to create a class I'm going
to call this app but you can name this whatever you want this app is going to become the window
essentially this bit here is what we have to turn into a class
the really important thing here that might be a little bit complicated is that this app is going to inherit from
tk.tk which means that the app here is going to be the main window
let me implement it straight away this app is supposed to inherit from TK dot
TK in the function based approach this one here we have stored this object
inside of the window variable in the class-based approach we are storing the object itself
once we have that I want to call a Dunder init method for now this one just needs self and
nothing else in here there's one really important thing that we have to do before anything
else and that is to call Super and thunder in it this ensures that this TK functionality
works properly although besides that we don't have to add any arguments so this one can stay
as it is with these lines of code we basically have replicated this one line of code
here so far we have just become less efficient but what we can do now is get
self and for example set the title the title could be something like class
based app this would be the equivalent of this line here let me expand it a tiny bit
like so in the function based approach we got the object which we called window and
then we called the title method on it this we can simplify here a tiny bit because the object itself is well self
and we can still call the method on it because we inherited the entire object
and this is one method of it to illustrate how all of this is going to work let me go all the way down in
the functional approach and run window.main Loop in the class-based approach this would be self dot main
Loop without any arguments with that approach we can simply create
an instance of this object and run it and if I execute the entire code now we
can see we have a window that also has the same title class based approach
there you can see it better although right now our app is one class that is a lot easier to manage not for
now but it is going to be much easier so besides that I want to also duplicate
these two bits here which means inside of window I want to get self and I want
to set the geometry of this class or this app to duplicate this I want to have the
same Dimension 600 by 600. I can run this again and there we go we have a
larger window the same I can do if I duplicate this line I can set the minimum size here
for this one we just want two numbers with 600 and 600. that way if I run this
again I cannot make the app smaller than 600 by 600.
and with that we have copied all of this here to set up our window
although I do want to make some minor changes and that is I want to set the title and the geometry from the
arguments that we pass into the class when we create the instance of it which means inside of app I want to pass
in a title let me call it a class based app and then I want to add a tuple with the
with and the height which in my case is 600 by 600. which means I have to update all of this
a tiny bit to account for these arguments here which I think could be a fairly good exercise for you try to
update the code to account for these arguments most of you now and see if you can figure this one out
first of all we have to add two more parameters to a niche I want to have a title and I want to have let's call it
size the title is very easy to change because this one is just a string which means
inside of title I can pass in the title the geometry is going to be a tiny bit
more difficult although not very much we basically have to figure out how to turn this Tuple into a string in my case I am
using an F string which means I want to add an F in here and the first argument is going to be
size and zero the second one is then going to be size
and one and now we should be good to go I guess one more thing that we could be
doing is right now minimum size is static we can also update this one
although we would use the same numbers we have used with geometry so size 0 and
size 1. which means if I run this now we cannot see any difference although what I can
do is change these numbers let's say to 200 and 400 and now we get a different
kind of window although I don't actually want to do that and I think with that you can already see some advantages with
just one line of code we can call the entire window and pass arguments into it
so when we actually use the app this one is much easier to understand than these four lines here
and this is only going to become more advanced for the next bit I want to work
on the menu let me show this again here's the app what I want to work on is
the left side this bit here in the original code
I move this to the side we have a menu the menu is all of this bit here
a couple of widgets all of those are inside of a menu frame this menu frame
here or rather we are creating it here we are placing it here and then we're adding
widgets here on top of that further down there we are adding the layout of the widgets further
down here which all things combined is really annoying to manage we basically
have a huge amount of code that is really really disorganized this I can change very easily by
creating another class that I want to call menu this menu is going to inherit from ttk
and frame basically what we are going to start with is we are going to recreate this
Frame here except now we are not storing ttk frame inside of a variable instead we are
creating a whole new object inside of this like with the app we have
to create a Dunder init method this one is going to need itself and on
top of that we are also going to need a parent or a master because inside of the init method I want
to call the super Thunder init method and this one is going to need one argument and that is the master or the
parent the way you have to understand this is that this init method is basically the
same as calling the object by itself and for that we always have to pass in the
master which in this case is going to be the window with that we have basically created
another frame this we can now use inside of the app the way this is going to work
let me add a couple of comments here I want to create widgets and besides that
I have the main setup
all the way at the bottom I am running the app the widgets right now we only have self
dot menu which is going to be the menu although don't forget when we are calling this menu here we have to pass
in the parent and this could be an interesting exercise for you try to figure out what the parent is
the parent in this instance is self because the app is tk.tk what we called
window in the functional approach and in the functional approach we sort
all of this inside of the window variable and passed this inside of the frame in the class-based approach let me
move this a bit to the side app itself is the window so this app we are passing into the menu that way this
menu is going to have this app as the master although if I run all of this we can't
really see very much there are two reasons for it number one this menu right now is just a frame and frames are
invisible although even if they were visible we couldn't see them because we're not placing this Frame anywhere on
the app right now there's a parent or a master but we don't actually position the frame inside of the parent
which means there are two things we have to work on number one I want to create a label that
actually illustrates where the menu is for that I simply want to create a ttk
and label like so the parent here once
again has to be self I don't actually want to have text in there instead what I want is a
background this one can be read right now right after creating this label I want
to use the pack method and in here I want to set expand to true and fill to
both that way this label is going to fill the entire frame with a red color
and let me move this a bit further to the right so we can see the entire thing right with that we should be having a
menu that's at least visible although if I run this again we still can't see anything because we have to place the
frame itself and this can happen inside of this class as well
because all we have to do is get self and now we can run for example pack or we could run grid we could run whatever
we want to keep it simple for now I want to run the pack method if I run this now we can
see all the way in the top we have a tiny red bar this we can set to expand being true and
we can set fill to both and now if I run this this Frame is covering the entire
window although in the original if I expand this a tiny bit more when we are placing
the menu frame this happens here we are using the place method with all of these
arguments meaning I can just copy them move this a bit further to the site
again and now instead of Peg call the place method this one has X being 0 and
Y being zero so menu is always on the left side it covers 30 percent of the width of the window and it covers the
entire height I can run this again and there we go now we have the same position for the menu
why this approach is really useful is I can now minimize the menu and inside of
the app this is what I'm actually working with the entire menu is simply one entry I don't have to worry about
all of these different Snippets that are in different places the entire menu is
in one spot which makes it much easier to work with although right now the menu doesn't have
any content so we have to work a bit more on this and let me move this a bit further to the right there we go
inside of the menu I want to create all of these menu widgets these ones here
for that I'm going to create a separate method I'm going to call this one Define create
widgets this one itself and nothing else and in here I want to create all of
these widgets so let me copy them we have menu button one two and three we
have two sliders we have a toggle frame this one is a frame in itself and this one has two children menu toggle one and
two and finally we have a frame all of these I want to copy and paste
them in here and also fix the indentations there's one more change that we do have
to make and that is that all of these buttons and Sliders don't have a menu
frame as the parent instead I want to change all of the menu frame to self
because all of these buttons should have this many frame as the parent with the
exception of menu toggle 1 and menu toggle 2 because those two are supposed
to be a child of the toggle frame meaning those we don't actually have to change besides that the entry I forgot to
change this isn't many framed this should be self with that all I have to do is call this
method self dot create widgets and now I can run this and we can't see anything
again this happens because we're only creating widgets we're not placing them on this Frame
for that I want to create another method I guess we can call this one create
layout no custom parameters again and what I
want to do now is replicate basically this here
including this one as well as you can see in here we are using the
grid method to place all of these elements which means first of all what we have to do a bit further up we have
to create the grid for the menu this I have done here with these two
lines of code so let me start by copying those two
and once again I have to fix the indentation I move this thing a bit further to the side so we can see what's
going on I want to first of all create the grid
for this I can minimize the create widgets method I want to get this Frame here and I want
to set columns and rows on this which means instead of the menu frame I want
to get self although the rest can stay identical which means next up I can place the
widgets for this once again I can copy all the stuff I have done here all of
this and I can place it in here once again we
have to fix some indentations like so and now we can work with this
and now we have a tiny problem all of these widgets are only available inside
of create widgets they are in the local scope of this method inside of here
which means I couldn't access them inside of this create layout method
I guess there are two ways you could approach this problem number one you could change all of these variables to
attributes so for example you would turn this variable into an attribute using self and then down here you would use
self.entry.place that would be one approach although in my case I don't want to go with that one
so let me undo everything instead I'm going to be a tiny bit lazy here copy
all of this and then place it inside of create widgets
that way we are doing all of this inside of one method and we are staying within
the same scope not the cleanest approach and if you had a more complex app this would probably
be something you want to work on more but for this simple app this is totally fine at the very least let me add some
comments here I want to create the widgets then I want to create a grid and
then I want to place the widgets and with that I want to get rid of this
TDK label here because we don't need it anymore now I can run the entire thing and there we go
we have the entire menu still works just as before except now all of this is inside of one
class and this finishes the menu which means I can minimize this and now we can see
menu is simply one entry that is much easier to work with and if
we wanted to work with it we could simply open this and then change all of this and do whatever change we want to
make which makes maintaining all of this much easier so in comparison here's the
original we had just code for the menu here here here here here here
and this was very difficult to separate from the main widget for example
so with that we are making some good progress next up I want to create main if I run this again main is
this main area here this one is actually really simple because what we want to do again
is we have main.frame here just another frame this one we are putting on the
window using the place method again so this we can start on right away I want
to create another class and this one I called Main once again this has to inherit from ttk
dot frame and let me move this a tiny bit further to the side
in here like for the menu we are going to need a Dunder init method that gets
self and it gets apparent spelled correctly as well like so and
don't forget super underscore underscore init and pass in the parent in here
this is the same thing we have done for the menu so if I open the init method of the menu we had all of this
next up to actually see the main menu I want to run the place method again
although I can copy this from the original video we are calling this place method here
which means inside of the init method of main I want to call self and place
and then place the widget in this position to make sure that we can't see this I
want to once again create ttk label with self as the parent with background being
red and with the pack method setting expand to true and fill to both
with that I can simply create this main method inside of the app right below the menu itself let's call
it main is going to be Main with self as the parent and if I run
this now we can see the main frame let me minimize the menu and get rid of
TDK label here we definitely know this is going to work
which means with that let me show the app again we can start working on the actual entries these things here
this one once again is going to be one frame inside of the frame we have one label with a background and then we have
a button below or that I want to add a tiny bit more
code inside of main I first of all want to create a frame so I can just call it frame and this is
going to be ttk and frame the parent here is going to be self
inside of this Frame I want to have a label and a button so let me create a
label variable then I want to use ttk and label with the frame being the parent text is
going to be let's say test one and the background color is going to be red
after that I want to create a button and this is going to be ttk and button
with the frame as the parent text is going to be I call this one test one as well although let's call it button that
Pro makes a bit more sense these two buttons we now have to get inside of the frame and this Frame we
have to place inside of the Mainframe let's start with putting these two widgets inside of the frame
for that I'm going to use the pack method so label dot pack
expand should be true and fill should be both
yes I can now duplicate because the button is going to work in the same way with the only difference that the button
has padding y being 10 pixels finally I want to get the frame and pack
this one as well although for this one I want to set the site to left
actually I can copy all of this from the original in here we are placing all of
this if I find it really quick we are placing the main layout here we
have entry frame one and entry frame two all of this I want to copy like so
so let me move all of this to the site again and I want to use this pack method with all of these arguments
and with that this should be working let's try now and there we go we can see the entry inside of the main frame
we are making a lot of progress now this is starting to become a tiny
bit messy because this Frame here could be its very own class and this
incidentally is going to become your exercise I want you guys to get this
Frame here and turn it into a separate class along with all of its children so
it should be a frame class with a label and a button on top of that I want you guys to set
the color the label and the button via the arguments which means you should be
able to use the init method of this new class to set the text of the label the
text of the button and the background of the label and pause the video now and try to
figure this one out yourself let's get started first of all I want to
create a new class and this one I called entry as always we have to inherit from ttk
and frame inside of that we need the dunder init method in here we need self as always
then we need a parent then we need three more arguments we need the label text we
need the button text and we need to label background
these three arguments we need to cover the second part of the exercise with that inside of the init method
don't forget to call this super init method and then here you want to add the
parent this entry frame here is going to be this Frame which means inside of it
we can do all of this as a matter of fact let me cut out all of this and delete the frame
and instead I want to paste all of these things in here now we have a label a button we are
placing the label and the button and then we are packing the frame although for this to work we have to make some
changes first of all label and button have not the frame as the parent instead
self is the parent now or the layout this can stay exactly as
it was before although for the frame itself we don't want to pack the frame we want to pack
self because remember self is a frame that we can pack on the parent
with that we can already create a entry frame in here
the one argument we have to pass in here for now is the self although all the other arguments we are not using right
now so let me simply pass in one two and three it doesn't really matter right now
I can run this now and there we go we have the very same result and this is actually super useful
because now I can duplicate this entry widget run this again and now we have two entry fields or frames I can do this
multiple times and there we go we have lots of different fields in my case though I only want to have
two but I hope you understand the principle here although next up we have to actually
cover these three parameters and they are very easy to work with because all of them are going to be a string
the label text is going to be the text for the label this one here which means in there I want to pass in the label
text the same thing for the button I don't want to have a string button instead I
want to have the button text finally let me add the comma here for the background we don't want to have hard-coded red
instead we want to have the label background with that I now have to pass in proper
arguments in here let's say for entry 1 I want to have entry one
then for the button I want to have button one spelled correctly and for the
background I want to go with green let me duplicate all of these and paste them
into the second entry and let's call this entry two button to and for the color let's go
with blue let's try this again and there we go now we have widgets that work perfectly fine
and now I hope you can see the value of this approach because this makes it really easy to create lots of widgets
that are self-contained for example for the entry we are only having one entry here but this entry
contains a huge amount of stuff if I compare this to the original functional approach
we created the frame here we created some widgets here and then we could set the layout here and this was kind of
messy because in there we had the second frame and all of this was really hard to follow
whereas in this approach we simply have one frame that contains it all and we are placing it wherever we need it
and with that we have the entire app that is much more manageable because now
we have logical parts to it that we can work with whenever we need and this is what you want to use most of the time as
soon as you have any kind of complexity in your app this approach is vastly Superior in this part I want to talk
about a really important part of T Kinder and that is creating custom components
what that means is to use tickhinder or literally any GUI framework efficiently
you need to be able to create your own components for example when we use the
classes in the last bit we have created a couple of custom widgets one example
was the entry widget what we created looked like this and what is really important here is that
this entire thing was one frame that we customized so we gave it a label with a
background and a button and once we have that we could create this multiple times so we had another label and another
button besides that we also created this entire side panel as a separate widget I
suppose I should look at all of this in code straight away here's the code of what we just covered
before and all of this gives us this kind of app the really important thing you have to
understand here is that we are creating custom widgets this entry here inherits from frame and adds more stuff to it so
this Frame here this we can do multiple times we have one frame and we have another frame
this one here both of these were very easily created
we did all of that inside of Main in here we can simply create one entry and another entry I could duplicate this
again add entry free button free and for the color I could go with green if I run
this thing now we have a third entry widget with this kind of system we can
create more complex layouts fairly easily and also keep them more manageable which is why it is really
important that you understand how to use all of this I'm going to practice it in this video as well but definitely play around with
this in your own time although more importantly for this video what I also want to cover is that there are two ways
to create custom components the first one we have already seen is by using classes
inside of a class you inherit a widget and you add custom parts to it
this can create really complex layouts but the downside is if you end up with
too many small bits you might have a ton of classes which would be a bit annoying to manage to account for that we have
the second approach and that is a more functional approach all we are doing in here is we are creating a widget inside
of a function and then return the widget this is a bit more limited in terms of
what we can do but the upside is we can create lots of small components inside
of a class basically what you want to do for any more complex component you want to use a
class but inside of this more complex component you want to use the functional approach to create simpler bits all of
this is going to make much more sense when we actually make the app speaking of which what we're going to make is
going to look something like this in here we have a couple of custom components
the most important one is each of those rows is One widget and all of those are
made using classes inside of this we have three columns we have a label we
have a button and then we have this kind of thing with an entry and a button for
this final bit here I want to use the functional approach for the simple reason that this isn't
particularly complicated we simply have a frame with two widgets inside it wouldn't really Merit using a whole
class but I also don't want to create too much of a layout inside of the class
itself in the init method but well let's jump into the code and let's have a look at all of this once
again I already have a couple of lines of code ready if I execute the entire thing we have a basic window with a
title but not much else with that we have to figure out how to create this kind of thing what I want to
start with is that these rows are always one widget and this I want to create by
using a class which means I want to get started by creating a class and this I want to call
segment I guess is a good name this has to inherit from ttk dot brain
inside of this I want to create a Dunder init method this one itself we need a
parent on top of that we need a label text and we are going to need a button text
that way I can customize the entire thing quite a bit easier for reference once again
inside of each segment I have a label and I have a button once I have that I can actually create
the widget itself for that we first of all have to run this super init method
and set the master to the parent with that we basically have a frame and
essentially what I want to do inside of the global scope I want to create all of the widgets
the important Point here is I only want to call the segment and T Kinder almost
specifically the class itself should take care of everything else all I want to pass inside of the segment is the
parent which is the window that I want to have a label text let's go with label
and I want to have a button text button and that is it I don't want to do
anything else inside of the global scope the entire logic of this widget should be inside of this segment that way we
have one component that takes care of everything and we don't have to think about it too much
what this allows us to do is duplicate this a couple of times and we have different widgets that can do different
things for example in this case we would have different labels let's say button
and click or hello and test it doesn't really
matter what you place in here the important thing that you have to understand is that we are creating a
custom component that contains a huge amount of logic to get started in all of this inside of the segment class I want
to create a grid layout for that I want to get self and row configure
although for this one I want to have row 0 with a weight of one and that's
basically it although with that I can duplicate the entire thing change the row to a column instead of a zero I want
to have 0 1 and 2. I want to have three columns that all have the same weight on
top of that I also want to set uniform to a or it doesn't really matter what it
is but with this all of the columns are going to have the same size almost specifically the same width
inside of this I can now create a TDK label and I can create a ttk button
both are going to need fairly similar arguments the first one is the parent that is going to be self besides that we
also need text this text we already have because we have the label text and we have the
button text for the label I want to have the label text or the button I want to have the button text
after I have that I want to use the grid method to place both of the widgets
the label is going to be in row 0 and column 0 as well all of this I can copy
as well because the button is also going to be in row 0 but column is going to be one if I run the entire thing we can see
that we well cannot see anything the reason for that is that this segment is not being placed on the window which
means we have created a component but we are not placing it for that we need well
a placement method and this once again we can do inside of the component itself all I have to do inside of the init
method is self and then use one of the layout methods I'm going to go with pack
with that we can see the different layouts although right now all of this looks a tiny bit weird
so not ideal yet first of all I want to set this to expand being true and fill should be
both now if I run this this is starting to look a little bit better although I need
a few more widgets to make all of this look halfway decent that we can do very easily because to create more widgets
all I have to do is duplicate this segment and we get more widgets although I'm going to change the text here so we
can see a bit better what's going on I will just add random words in here it really doesn't matter what you add here
it's just for illustration anyway let's say exit and now we have five different
segments this still isn't terribly visible because there's so much white space in
here the reason for that is that both of the label and the button only take up
the minimum amount of space that they need to display the text that we can change by using this sticky argument and
I want to set sticky to north south east and west now if I run this all of this starts to come together much better
what you can also do is inside of this pack method set pad X to 10 pixels and Pat y should
also be 10 pixels if everyone is now we have a tiny bit of white space between the widgets and that
is basically it I don't want to repeat myself too much here but what we have done is we have created a custom
component called segment and inside of the segment we have a ton of logic that
way inside of the global scope this bit here we can simply create one component
and this component creates something much more complex in the app just imagine if we didn't have this kind of
setup we would have to create this code up here five different times and if we
wanted to update any individual bit let's say this hello here we would have
to go through a lot of code just to find this one part which would be really
annoying to work with but in our setup here all of this is very easily manageable
which is why you really have to understand this now this is one way to create this kind
of layout system there is another way though what we have done for now is we have
used a class based approach to organize our widgets but this we don't have to do
we could also use a functional approach let's have a look at this one by translating our class-based approach to
a functional one back in the app I want to all the way at the top create a function I'm going to call this one
create segment this one is going to need three different arguments
we need the parent we need a label text and we need a button text for the Keen
it among you those are the same parameters we have used here we don't
need self because we're not using a class inside of this function we are basically trying to recreate all of this
and then return the result basically what that means is I want to create a
frame which is just going to be ttk and frame at the end of the function I want
to return that frame which essentially means that we are taking this Frame here
except now we are keeping it by itself although first of all we have to set a
master for the frame which is going to be the parent we are passing into the function this parent here
next up we have to create the layout this grid layout here I suppose I could
just copy the entire thing paste it in here and fix the white space we don't
have self anymore instead we want to set the frame with rows and columns after
that I want to create some widgets I suppose I should be a bit better here
with the comments what we have done in the class based approach was also creating widgets that way all of this is
a bit easier to read in my case I want to copy all of this and paste it inside of the functional
approach now we have a ttk label and a ttk button although once again we don't have self
anymore instead I want to parent them to the frame the frame we created up here with that we have the same thing we
created inside of the segment here which means now that we are returning it we can simply use it
which means all of this here I want to comment out and if I run this we can't see any
widget anymore and let me minimize the class now you can see roughly the entire app
instead of using a segment I want to create segment
and for the arguments I have to get the parent the label text and the button text these three arguments if I run this
now we still can't see anything because what we have done inside of this function is create a widget but we are
not placing it this we could have done inside of the segment very easily because in here we could simply run
self.pack this unfortunately we cannot do inside of the frame because we are returning
the frame we couldn't place it right away although what we can do since this function here is returning a
widget we can on it run a layout method like Pac for example and this pack could
be expand true and fill both like so
another runders we can see we have one widget
although since we only have one all of this looks a bit weird but what I can do now is simply copy all of this
let me add some white space uncomment it and instead of a segment I want to use
my function create segment since we're using the same arguments all of this should still work also don't forget we
have to add the pack method to all of them like so and now if I run this we have
the same result although I did forget one thing and that is the padding for x and for y let me
copy it from the segment class and paste it inside all of them so we get exactly
the same result now if I run this we have exactly the same result
and we have done all of this by using either a function or a class both would
be fine in this instance because we are creating something fairly simple but once again I want to emphasize if you
want to create more complex layouts having either something like this or something like this let me uncomment it
is much easier to understand and to maintain than having a ton of widgets that you all create manually for future
videos I am going to rely a lot more on custom components so this is an important thing to understand
which means Let's do an exercise and I hope you can still keep up all we have to do is an exercise and then we are
done what I want you guys to do is create a smaller widget inside of the segment class using a function or a
method specifically inside of this segment class I want you guys to use a function
to create another widget like we have done up here instead now don't use a function use a method inside of this
class what you should be doing is create a container that has an entry field and a button stacked on top of each other
the button should be set via the parameters and all of this should be inside of the third column of this
segment as a reminder we are creating three columns and right
now we are only using column 0 and column 1. at the end of this out of this should
look something like this we have an entry field and we have a button for all of my buttons I use the text exercise
but this should be more customizable pause the video now and try to figure this one out yourself
alright let's get started I want to work inside of the segment again although
first of all what I should do is comment out all of these functions because I
only want to work with the segment class inside of this one I want to create a
method let me call it create exercise box for this one we need two arguments
we need self like for any method and then I want to have some text this is going to be the button text now inside
of this method we have to create a frame like we have done up here with create
segment we always start by creating a frame in this Frame we are returning at the end although this Frame while being
ttk and frame has a parent of self or a master to be a bit more specific at
the end of this method I want to return this Frame although before we are doing that I want to create a ttk entry this
one is going to have the parent of frame and besides that I want to have a ttk button this one has frame as the parent
but also text is going to be the text that we are getting from the parameters
this text up here we are passing in here once we have that we have to place both
of these widgets inside of the frame and this I want to do with the peg method
since both of the widgets are supposed to be on top of each other I don't need a side but I do want to set expand to
true and fail to both and that is all I need inside of this
method with that I can minimize it now inside of the widgets I can call Self
dot create exercise box and add the text in here for now let's
go with exercise if I run the entire thing now we still
can't see anything because once again I forgot that we have only created a widget we haven't placed it yet for that
we need the grid layout method so grid I want to have a row 0 and column should
be 2. on top of that I want to set sticky to north south east and west and that
should cover it all meaning if I run this now here we have a pretty good looking result we have an entry field
and we have an exercise button I hope you can see the value of this because
now inside of this class when we are creating the widgets we have all of this
in a fairly logical layout we are creating a label a button and then an exercise box now this exercise box could
be a separate class that would be perfectly fine but since it is so simple it's only four lines of code you don't
really have to do that it's kind of an Overkill which means in this case simply using a method to create something
slightly more complex is perfectly fine and much easier to maintain although there's one more thing I do want to do
and that is that right now we always use exercise for the text for the button but this I want to have a bit more
customizable so when I'm creating this segment I want to have another parameter
and that is going to be the exercise text this exercise text I'm going to pass
into this function like so and now when I'm creating all of these segments I
have to add one more argument let's go with test just to see if this is working and there we go now we have
test for all of these buttons I could change this the first one could be test the next one could be something
else then we have one two three we could also have an empty button or we could
have end it doesn't really matter but now we have different kinds of text in here and everything is still very easily
maintainable all of the customization happens in here and this is very easy to see and very easy to understand and if
you want to make changes you have all of this contained inside of one class that
is maintainable and very easy to work with a really important part of any app is
responsive layout what that means is let me run the app that we are going to create it is going to look like this
right now we have an app with a couple of items stacked on top of each other so
far nothing special however if I increase the size of this widget we are
at some point getting another kind of layout and if I go even further we have a different kind of layout
which means depending on the size of the window we get different kinds of layout
which is really important because I want the app to look good on basically any size and some layouts simply don't work on a
certain kind of size for example if I make this a bit smaller again this kind of layout here only really
works on very small windows while this one here would only really
work on a white window so I have to create different kinds of layouts now that being said implementing all of
this in tkinter isn't the easiest thing to do the reason for that is that tkinter
doesn't have inbuilt tools to create responsive layouts which basically means that we cannot update an existing layout
instead what we have to do is we have to create a separate layout for every Windows size or at least for the layouts
that we want to create so for this example I have created three different layouts let me actually show you I think
that's going to be useful here's the code that we are going to create over the course of this video all the
important stuff is inside of the app class basically what you have to understand is that we have three methods
one for create small layout create medium layout and create large layout inside of them we are simply creating a
frame we are adding widgets to this Frame along with the layout method and
then we are packing the frame also before that we are forgetting the previous frame that way if we go from
the small layout to the medium layout we are not creating extra widgets the
really important part of logic happens inside of another class this one is called size Notifier what this one is
doing is it checks the size of our window order with to be more specific and if we reach a certain threshold like
300 or 600 or 1200 then this class is
going to call the functions we are passing into it or the methods in this case which are going to be create small
layout create medium layout or create large layout all you really have to understand is
that we are creating three separate layouts and we are displaying each layout depending on the minimum size of
the window that's all that's happening here as a matter of fact let's talk about it really quick
what we are doing in the most basic sense we are setting different breaking points for the minimum width of a layout
so for example if the width of the windows 300 we want to have a small layout if the width is 600 we want to
have the medium layout and if the width is 1200 we want to have the large layout
and whenever the window resizes we are checking the width and if the window is crossing a new threshold if that is the
case we are building a new layout and for getting the previous layout that is literally the entire logic although to
implement it we do need a couple of things the major difficulty that we actually
have to face is in this step here by default we can use event binding to
check when the window is resizing the problem is this event is going to run on
every resizing of the window which is a problem for us because we only really want to check if the width crosses a
certain threshold so for example we want to check if the width of the app roses
300 we do not care if it goes from 350 to 400 that is completely irrelevant to
us we only care if we go from 299 to 300.
that is the major difficulty that we have to implement the rest is actually fairly simple but I guess let's jump
straight in and let's create all of this to get started all I have are the Imports for tkinder and ttk
the reason for that is that all of the app is going to be handled by classes the most important one is the app class
this one has to inherit from TK and TK inside of that I want to call the dunder
init method with self and I also want to have a parameter for the start size
should be fairly obvious what this one is doing inside of the init method I know what to
create is super thunder in it method although this one doesn't need any arguments next up I want to create a title for the
app which I called responsive layout after that I want to get the geometry of
the app this one is going to set the starting size the starting size we are getting from
the parameters this one is supposed to be a tuple with the width and the height this I have to convert into a string
which I'm doing with an F string I want to get start size and the index
number zero that is going to be the width then I want to do the same thing so start size except now I'm getting the
first Index this is going to be the height once I have that I want to run self dot
main Loop to actually run the app and this should be all we need to get started I can now create an instance of
this app so app is app or the starting size I went with 400 by
300. if it runs now we have a basic window what I now have to figure out is how to
get the size of this window when we are resizing it for that we need a certain kind of event before the main loop I
want to self dot bind and event and the event we're looking for don't forget the
smaller and greater sign what we're looking for is called configure this kind of event triggers
every time a widget resizes or changes the position just to illustrate what's
happening let me pass in a Lambda function don't forget the event all I want to do is print the event if I run
this now you can already see in the bottom we have an event that is called configure this event gives us the X and
the Y position of the window along with the width and the height so for example you can see right now we have a width
and a height of 400 by 300 the exact same thing we have passed into the app
on top of that if I am resizing the window you can see we get a different kind of width and height and if I change
the position of the window we get a different X and Y position but now we do have a tiny bit of a
problem or at least something to be aware of if I'm resizing the window again you can see for the width
we get lots of different numbers let me try to find a Breaking Point what you
can see in here we are running a new event on every change of the window and
I got a width of 977 988 999 1005.
and in just a bit I want to run a function to build a new layout when we
are passing a certain kind of threshold for example our threshold could be 1000 pixels which means if we go from 999 to
1005 we want to build a new layout but only at this point if we go from 977 to
988 I do not want to build a new layout which means we have to add some code
that we only Built a new layout if we are crossing a certain kind of threshold all of the logic I have put into a
separate class this class I called size node TEF fire
there's no need for inheritance and in here I want to have a Dunder init method
when itself as always then I want to have the window which is going to be the main window or in our case this app here
finally I want to have what I called a size dictionary for now don't worry
about it I'll explain in just a second first of all I want to get self.window
as an attribute which means self.window is going to be window next up I want to turn the size
dictionary into an attribute as well size dictionary itself is going to be size dictionary the basic idea is that
this size dictionary is going to have key value pairs like any dictionary the key is going to be the minimum size of
the layout and then the value is going to be the function that creates this kind of layout
let me implement it right away actually we're going to create an instance of this class inside of the app
we don't have to store it in a variable so we can just create it straight away I want to have a size Notifier the window
is going to be self and the size dictionary is going to be a dictionary I want to have for the key a
minimum size which I set to 300. the associated value is going to be a method
for example if our minimum width is 300 I want to create a small
layout this one doesn't exist right now so let me create it right away I want to create a small layout we need
self and nothing else for now so I don't get an error I'm going to add pass in here the code we are going to write
inside of size Notifier really is just going to check if we are crossing this
number and then we're going to call this function although to make this a bit more practical I want to have two
different layouts at least for now I want to create one at 300 the small one and then I want to have at 600
pixels a medium layout this one doesn't exist right now as well meaning I have
to create medium layout with self and pass that means inside of the size
Notifier if I am printing self dot size dictionary I am getting a dictionary I
don't need the window right now that has a key of 300 then a method and
another key of 600 and then another method this is a good start but I do
want to do one more thing and that is I want to order this dictionary right now it is already
ordered we are starting from a small number like 300 and going to a large number to 600. however what we could
have is a dictionary like this where we are starting with the larger
number this would be a massive problem later on so I want to order this dictionary right away this is actually
quite simple all I need is dictionary comprehension in here I want to create a new dictionary with key value pairs next
up I need 4 and key and Val u in now I
want to size dictionary and get the items with this we would essentially
copy the dictionary that we already have so if I run this we can't see any difference
to sort all of this I have to sort what is being returned from this items here this I can do very easily with this
sorted function now if I run this we have a dictionary that is sorted we can
get to the next part and that is going to be running this event here or binding
it to the window this I want to do inside of the size Notifier I want to cut it out and paste it in here although
for this to work I have to add self.window.bind because we want to check the size of the window
not the size of this size Notifier which wouldn't work because it's not a widget
and let me clean up the white space a tiny bit like so
the reason why I want to have this event binding inside of the size Notifier is because I want to connect it to a method
of this class the method I called check size or rather self dot check size
and this is going to be just another method important here we need self and we need
the event just to check if this is working I want to print the event this should already work if I run this
now we can already see we have one event printed out if I resize the window we
get lots of events so things are still working just fine Wicket already get started to create different kinds of
layout I guess for now what I could do is I could print small layout for the small layout and I
could print medium layout for the medium layout so we can see a bit better what's going on
these two methods I can already call quite easily for example when I'm checking the size I could get self dot
size dictionary with a key of 300 and then don't forget to call it
if I run this now I get small layout anytime I am changing the layout this
self.size by 300 is going to return this create small layout method the brackets
afterwards are calling this method importantly here when we are passing the
method into the other class we're not calling it we're just passing the method around which is totally fine to do what
we now have to figure out is when to call which method so when do we call the 300 method and when do we call this 600
method for that we need a couple of things first of all I want to get the window
width this one is really easy because all we need is event dot with next up I
want to have a variable that tracks which sizes I have already checked I call this check size by default the
value here is none also let me get rid of this function call here now the logic
that I want to implement is for minimum size in self dot size dictionary
I want to toggle through all of the minimum sizes inside of this size dictionary I can print right away what
we're getting minimum size if I run this now we get 300 and 600. the way I am
going to use this is I want to have the Delta size this is going to be the window with
minus the minimum size and let me print right away what we're getting
we get 100 and minus 200. what these numbers mean is by default this window
has a width of 400 and we have two breaking points one at 300 let's say
this is roughly here at 300 and we have another point at 600. let's say this one
is broadly here 600. this Delta is going to give us
either this distance here or this distance here
which is going to be 100 and minus 200. this information is
really useful because all I really have to know is what the smallest positive number is once a number goes negative I
know my window size this point here doesn't reach the next minimum size but
if the number is positive I am greater than the smaller minimum size so in this case we have two options 100
and negative 200. this negative 200 tells me that I haven't reached the next
minimum size but since this number here is positive I know I have exceeded this
minimum size which is this 300 here and since my window is 400 right now we're on this
point we know we have reached this minimum size but not the next one all I really want to check is if Delta is
greater or equal than zero if that is the case I want to get my checked size
and set it to the minimum size since Delta is becoming negative once we
don't reach the next minimum size this checked size here is going to give us the proper minimum size there's one
thing we still have to do and that is I want to check if the checked size is
different from self dot current minimum size
this is an attribute that doesn't exist right now but I do want to create it let me copy it and inside of the init method
I want to create a current minimum size by default this can be done it doesn't really matter what it is also this
should be size inside of this if statement I want to set self dot current Min size to the checked size
checked size like so this statement here is really important because this one actually tracks if we have a change in
our minimum size which means in here we can now run
self dot size dictionary and I can pass
in self dot current minimum size and this I want to run
now if I run this we get small layout and nothing happens if I just move it a tiny bit although if I moved a bit
further we get medium layout and if I go back to small layout this is working really well
however there's one problem already and that is if I go too far to the left we
get none the reason for that is if our window is smaller than 300 pixels we are
well trying to get the index on this dictionary of a number that doesn't exist as a consequence this one
here is going to throw an error the best way around that that I found is to set a
minimum size that is as large as the smallest size here so in our case I want to set the minimum size of the window to
300. that way we can never have a smaller layout than the smallest layout
that is quite easily added here I'm going to do this inside of the init method I want to get a minimum height
and I want to get a minimum width the minimum width is actually the easier
bit for the simple reason that I already have myself dot size dictionary and I
only want to get the first key from it for that I have to turn the entire dictionary into a list
on this list I want to get the first item that is literally all we need so
next up we have to work on the height for the height I simply want to copy what we are getting when we are creating
the app in my case that is going to be 300. one way to get that is first of all
I want to get the window or to be a bit more consistent self.window although in this case window and sales.window refer
to the same object it doesn't matter which one you choose this one has a method called W info underscore with
this is a method so don't forget to call it although let me print it right away
minimum height and well let's see what we get
we are getting one and that is going to be a bit weird
we know that the minimum height of the app when we are starting it is going to be 300. so why is this minimum height
going to give us one that is very strange the reason for that is that ticking that can be a tiny bit weird so
what it creates and when it places a layout there's a tiny bit of delay at
this point here when we are creating the size Notifier we have created the widgets but we haven't placed them
properly yet as a consequence the size of the app is going to be one
to account for that we have to call Self dot update this is going to put
everything in place and afterwards you can call the W info.wiff or hide and
then you get the proper numbers so if I run this now we are getting an error because size Notifier doesn't have an update method
instead what we need is self dot window dot update now if I run this we are
getting 400. and I just realized that is the width not the height I typed in with this
should be height like so now if I run this we get 300 that is much better ah
sorry about that with that I can get rid of the print statement here and once I
have these two numbers all I have to do is get self.window and set a minimum size the minimum size here is going to
be the minimum width and the minimum height let's try this one now
I have the app and I can move it to be wider and taller but this is the
smallest it's going to get all we have to do now is create different kinds of layouts we're already calling them so
inside of these two methods we have to create all of the layouts that we are going to use or while the two layouts
that we want to use for this small layout I want to have self dot frame which is
going to be ttk and frame the parent here or the master is going to be self
inside of that I want to create four labels and to save you watching me type
I'm going to copy paste things into here like so we have ttk labels four times they all
have cells dot frame as the parent then I'm setting the text to be label one
they all have a different kind of background and afterwards right away I'm calling the pack method
water pack Method All I'm really doing is I'm setting expand to True fill to both and then I'm giving them some
padding there's literally nothing complicated going on right now the last thing that we have to do in
here is self.frame and pack this entire frame for that I want to set expand to
true and I want to set fill to both and now if I run this
we can't see any kind of layout and this is a little bit weird because
we are creating a layout here and we're also placing it on the window so this should be working
now if I scroll down a tiny bit we are calling this method inside of this line
the problem is if I add a print statement in here let me call it test I run this again nothing happens
which means that this method here isn't being called and that's the problem right now the reason why it is not being
called is because of this self.window update if I comment this one out run this again now we can see our app
basically this self.window update causes this self.configure not to run
I'm not exactly sure about the reason why but we can overcome it quite easily by moving this configure
before the Windows update now if I run this there we go
this configure is run before the update as a consequence it runs when we are
starting the app and with that we can see our layout with that I can minimize size Notifier
and now we can start working on the other layout for the medium layout I do need quite a
few lines of code I think the best way for this is to Simply copy paste everything like so and then let me
explain it really quick we are once again creating a frame although this frame has a grid layout
which means we need a column configure and a row configure in this case we have two columns and two rows after that we
are packing the frame on the main layout so we can see it and after that I am
creating four different labels these labels have the same arguments that I used up here for the minimum
layout and here you can see a minor problem in tkinter and that is well we have to
create all of these widgets again there's no efficient way to copy widgets
from one master to another right now we have a very simple layout so this isn't too much of a problem but
if you had a more complex layout this would be quite a bit of work so well it's quite unfortunate but we have to
work with it other than that we are using the grid layout method four times to place each label inside of one cell
I'm also adding some padding but well that isn't very much and with that let's try the entire thing
I have the small layout and if I increase the size of the app we get something very strange
also a key error and well we have to cover a couple of things here the first one
let me close this and get rid of the error message the first problem we have is that once
we create the medium layout we are not discarding the small layout that is quite an easy thing to fix all I
want to do for that is create self.frame as an attribute in the init method this
is going to be tdk.frame as well with self as the master this self.frame I
want to pack right away self.frame dot pack we can set it to expand being true and fill being both as
well although this one doesn't matter very much because as soon as I create I have a small or medium layout I want
self.frame dot pack underscore forget this I want to do for both the small and
the medium layout essentially what is going to happen when we are starting the app we are creating
a frame by default this Frame is going to be empty however once we are creating this
small layout we are removing this Frame and then creating a new frame for the
same variable or while attribute this is important because if we now create a
medium layout we can use the same attribute to forget the current layout and then create a new one
that way if we go back to a small layout like this one here we can once again forget the layout and create a new one
with that we should be making some progress although still not ideal so now if I increase the size we get something
very briefly like so but we're getting a key error none
this problem happens down here in the size Notifier more specifically all the way down here
there's some kind of problem with self.current size let's print it actually I want to print
self.current minimum size now if I run this by default we get 300 that's a good start
but if I resize the app we get something really strange we
basically have an infinite Loop let me close all of this we had some kind of infinite Loop where
we kept on getting 300 and 600. and the issue here is
let me find it really quick this window.bind is being run whenever any
kind of widget changes size or position as a consequence this is also going to
be run when we are placing ttk.label also this is going to be run on
self.frame the reason why this is a problem is because all of these labels here all of these labels and this Frame
as well they also get the configure event and since they can change the size
we basically end up with the problem that this widgets here or more
specifically the grid layout method changes the size as a consequence of this change in size we are calling check
size which in turn once again calls this function here which once again calls the
grid method the result is we are creating an infinite Loop where nothing is going to work anymore and ticket gets
really confused fortunately this is really easy to fix inside of check size I want to add one
more if statement this if statement is going to be the event dot widget
should be self dot window I only care about this event and only if that is the
case I want to run all of this now if I run the code again I can resize
the window and now this is working perfectly fine and we can change between different
layouts this is looking good and with that we are done we have
different kinds of layout and well we can move between them although I would
really recommend you to go over this in your own time especially this kind of logic here can get a bit tricky
but well the exercise is going to be I want you guys to create a third layout
where all of the widgets are next to each other for that purpose I use grid but you could use whatever you want it
doesn't really matter and this layout should appear once the window is wider than 1 200 pixels pause the video now
and try to implement this yourself
alrighty first of all we are going to need another layout method
I'm going to call this one create large layout and we need itself as always
and here once again this is going to be quite a bit of typing so I'm going to just copy it for my notes it's going to
look like this and it's fairly similar compared to create the medium layout we are forgetting the previous frame then
we are creating a new frame with a column and a row although now we have four different columns and just one row
this Frame we're packing right away and after that we're creating four labels that all once again have the same
arguments after that we are using the grid layout method to place all of these labels
although now we're using column 0 1 2 and 3 and row is always going to be zero
now we have to figure out when to call this and for that I want to minimize all of these methods so things are a bit
easier to see when we are calling size Notifier we are passing in a dictionary
it's probably better to put this dictionary over multiple lines like so that way it's quite a bit easier
to read to this I want to add another entry 1200 that's the minimum width and I want to
create large layout and with that we are done I can now run
this I have a small layout I have a medium layout and I get a large layout
that's basically all we need I guess what you could do if you have your own app you could simply use the
size Notifier and use it for your own purposes this one is quite reusable and works really well
a really important part that I haven't covered yet is scrolling which is going to look like this we have
a canvas and on this one we have custom scroll bars that go up and down or left
and right now this really doesn't look too impressive but what we eventually can do
with this is something like this where we can create a frame that is scrollable
although for now we're going to keep it simple and let's start with some Theory
in teak and there are there are three widgets that can be scrolled we have canvas text and Tree View
the canvas is the most useful one since this one can display other widgets we
will cover that in the next part but for now let's get started with the basics I am importing tkinter I am setting up a
window and I'm running main Loop the result is going to look like this on this I want to start by creating a
canvas this I want to store in a variable that I call canvas and canvas we create with
TK dot canvas in here we need to parent or to master which is going to be window and just so
we can see it I want to set a background with a white color this canvas I want to pack right away so canvas dot pack I'm
going to set expand to through and fill to both now if I run this we can see the
entire background is white I guess for now I can change the background to red that is a bit easier to see we can
definitely tell the canvas covers the entire window but that's not actually what we want instead what I want is that
the canvas is larger than the window for that we need one more argument and that
is called scroll region this creates a larger canvas that we can use for
scrolling for this we need four arguments we need the left the top the right and the bottom the left and the
top are basically always zero and zero that makes it very easy to navigate for the right I want to set 2000 and for
the bottom I want to have 5 000. for comparison here the window itself is 600
by 400 pixels so the canvas now is going to be quite a bit larger although if I run the entire thing we can't see any
kind of difference first of all we only have a red color for the canvas right now which isn't
particularly helpful to actually see some scrolling we need content for the canvas in my case I want to the most
important one create a line this line is supposed to go from the top left all the
way to the bottom right which means when we are creating it I want this to start at 0 and 0 for the
left at the top the right is going to be 2000 and the bottom is going to be 5000.
with that we have the exact same numbers that we have used here although for a line the first two are the starting
position and the last two are the end position other than that I want to fill this one
with a color let's go with green and then I also want to set the width so it's a bit easier to see let's go with
10. now if I run this one we have a line although we can only see one part of the
line but that we can work on besides the line I also want to create a couple of
rectangles for that I'm going to use a for Loop let's say for I in range and I
want to create a hundred rectangles to create a rectangle I need canvas and
create underscore rectangle this one is going to work kind of like the line for
each rectangle we have to specify a left a top a right side and a bottom side
besides that I also want to have a fill which is supposed to be a color which means we have to create five different
variables we need a left side we need a top side we need a right side we need a
bottom and we need a color all of these numbers are actually fairly simple but since I do want to have
random numbers I need to import two things I want from random import rant int and
choice Rand int is going to give me the positions so left top right and bottom
basically all I want to do is run in from 0 to 2000 or from 0 all the way to
the right or the top I want to have Rand int with 0 and 5000 so all the way from
the top to the bottom for the right side I want to have the left side plus a
random amount let's say rant end with 10 and I think 500 is what I went with
finally for the bottom I want to have the top plus rant end 10 and 500. for
the color I want to use choice and choice needs a tuple with a couple of color arguments and here I want red I
want to have green I want to have blue I
also want to use yellow and let's go with orange with that I can run the entire thing and
now we can see at least parts of some rectangles and with that I can also change the
background of this canvas to White and we can still see things or at least
we can see the line for now we didn't get lucky to see any kind of rectangle but they are definitely there if I run
this again now we can see them with that we can cover the actually important part and that is a scroll bar
this grow body Kinder is just another widget we create this with ttk and
scroll bar this one is apparent let's go with window and I also want to store all of
this inside of a variable let's call it scroll bar for the scroll bar we need one argument
right away that you basically always want to pass in and that is Orient for this one you have horizontal or you have
vertical horizontal is the default one but I want this to be vertical
with that covered I want to place this thing right away and place was deliberate because I want to use the
place method this is basically what you always want to use for scroll bar because this allows you to set relative
X to 1 and relative y to zero with a relative height of 1 and an anchor of
North East that way this crowbar is always on the right side of the window so I can run
this now and on the right side we have a scroll bar although right now it doesn't do anything
now this scroll bar Works kind of like a slider what that means in practice is we
can give it one more argument that is called command this command wants to have a function you could pass a normal
function in here but most of the time you want to do one specific thing you want to get a scrollable widget like the
canvas and then get the Y view method this y view method is basically designed
to work with a scroll bar if I run this now you can't really see any difference on the scroll bar but if I move the
scroll bar we now have some scrolling which is a good start
to actually see the progress inside of the scroll bar we want to have the canvas and we want
to run configure the argument we need now is called y scroll
command this I want to set to scroll bar dot set now if I run this we can see the
scroll bar is working and we can use it to move around in the canvas this is
working really well and basically what you have to understand let me draw this actually we
have a canvas that is what we created here and then we have a scroll bar that
is what we created here those two are going to influence each
other the scroll bar is going to give us one size of the canvas and this we are
doing with this command and canvas.y view this picks one part of the scroll
region however we also have to go the other way that the canvas influences the scroll
bar and this happens down here with the scroll command is equal to scrollbar.set
this tells the scroll bar how tall the widget is and which section we currently
have you need both of these parts to make all of this work efficiently but once you have it you are basically done
so let me run this again and we basically have all we need for the basic scroll logic there's one more thing that
we can do and that is let me put it above the scroll bar Mouse wheel
scrolling for that I want to get my canvas again and I want to bind an event the event I
want to look for is called Mouse wheel be careful here the W has to be
uppercase once we're doing that I want to call a function and this could just be a Lambda
function don't forget the event here and for now let me just print the event itself
now if I'm over the canvas with my mouse and use the scroll wheel we get an event that we can work with on this event what
I care about is this Delta if I move my mouse with away from me
this is a positive number if I move it towards me this is a negative number I think it is always 120 but your results
May Vary depends on your mouse and your operating system I think but the number itself here isn't really that important the way
you are going to use it is by targeting the canvas and then calling the Y view
underscore scroll method this one tells the canvas to scroll in a
certain direction and for this we need two arguments we need the amount and we
need the units the units is kind of weird you basically need a string that is called units and you never use
anything else so just always pass units in there the amount is the much more important bit for example in here I
could simply add 20. although this might be a bit large if I now run this and I use my Mouse as a
scroll wheel we are scrolling quite a bit although this only works one way
in my case what I want to do I want to get the event I want to get the Delta and I want to divide this by 60.
remember here event Delta was either positive or negative 120. if I divide
this by 60 I am getting 2. which seems like a reasonable number but just play around with this whatever
feels good is fine here however now we need one more thing if I run this again and are you scrolling we
are getting an error and that is not actually the error I was expecting because I had a typo now let me try this
again if I now use the scroll wheel we get expected an integer but got a
floating Point number basically what you have to understand here is that tkinder for the scroll
always wants to have an integer so now if I run this again I can use
scrolling and now this works perfectly fine with my mouse wheel if you want to change the direction of
the scrolling you would just add a negative here depending on what operating system you
are used to you properly know different scrolling behaviors for some people if you scroll away from
you on the mouse wheel you want to go up other people want to go down I prefer that if I go towards myself I
am scrolling down and if I scroll away from me I'm going up but this is a choice you have to make but with that we
have all of the basics of using a scroll wheel to move along a widget it really
isn't that difficult so with that I want to add an exercise
I want you guys to create a horizontal scroll bar and this one should be at the bottom and
with that you are scrolling left and right on the canvas on top of that I want you guys to add
one more event that the user can scroll left and right by holding down control and the mouse wheel control or command
if you're on a Mac positively now and try to figure this one out yourself
first of all I have to create a new scroll bar let me call it the scroll bar
bottom this is going to be ttk and scroll bar
the parent is going to be the window and Orient for this one is going to be
horizontal although since this is the default argument you could just ignore it
entirely let me place this one right away I want to get this scroll bar and use the place method for this one I want
to have relative X being 0 and relative y being 1. on top of that I want to have
the relative with being one and the anchor should be the south west
let's run the entire thing and something definitely went wrong ah I see this shouldn't be scroll bar
this should be scroll bar Bottom now if I run this this is looking much better all the way to bottom now we have
another scroll bar there is a tiny overlap between the two scroll bars down here and for an actual
app you would want to take care of this but in my case I'm not worrying too much about it with that let's work on the
functionality we need a command argument and this command argument we have seen
here before we still want the canvas except now we don't want why view
instead we want to have x view I can already run the entire thing click
on the scroll bar you can't really see it at least on the scroll bar but in the canvas you can see we can go left and
right to make it visible in the scroll bar I want to have the canvas and I want to run configure now instead of Y scroll
command I want to have X scroll command and for this I want to have my scroll bar dot bottom and use the set method
with that I should basically be done now I can use the scroll bar on the horizontal axis
the vertical one still works perfectly fine and this is looking really good finally I want to cover the second part
of the exercise let me move it below because in here I want to have canvas dot bind
and I think the only difficult part was to figure out how to combine the control or command with the mouse wheel
on Windows this would be control and mouse wheel I believe on Mac OS it's actually the
same keyword but let me know if that's wrong and then I'll help you next up we have to call a Lambda function or well
some kind of function but Lambda is best here I guess I can just copy the entire thing I want to have a Lambda function
for this one we need an event and then we have to call canvas and not y view
but x view and scroll the other arguments though can stay identical with that we should be done
let's run this and now I can use my mouse wheel to go up and down and if I will control I'm
going left and right this is working quite well and this is going to cover all of the
basics of scroll bars at least for the canvas with that I want to comment out all of
this stuff because there are tumor widgets that I do want to cover the first one is the text widget
this we create let me start in a variable TK dot text the master is going
to be a window and I want to pack this right away text Dot pack with expand
being true and fill is going to be both if I run
this now we have a text box I can type in this but other than that we have no scroll bar
to make a scroll bar work I want to add some content to this text box
this I can do with a for Loop for I in range let's go from 1 to 200.
these numbers I want to use with text Dot insert and now I need two arguments I need a
position or rather a start index and then I need some text that I actually want to write the text is the easier bit
I just want to have an F string that says text with the current index so I
the index itself is going to be the starting position I already talked about it but basically in here tikenter
expects something like 1.0 with 1 being the starting line and 0 being the
character on that line since we do have the numbers from 1 to 200 we can simply turn this into an F
string and put this as I now if I run this we get a whole bunch of numbers that's a
good start although I do want to have some line breaks those we create with a slash and the
letter N now to run this this is looking much cleaner we can already scroll around here by
simply using the mouse wheel so this is the default Behavior although we don't have a scroll bar but this we can add
quite easily afterwards I want to have another scroll bar let me call it scroll text
and this is going to work basically identical compared to the canvas in fact I could simply copy all of the code here
and paste it here if I comment it out I want to rename
scroll bar in all of the places to scroll
bar text and let's go through it step by step first of all for the scroll bar we
are creating it we are setting it to the window we have an orientation and then we have the command right now the
command is for the canvas instead this one should be for the text other than that the text widget also has
a y view method so we can leave this one as it is next up we have to tell the scroll bar
that it is being set by the text widget for that I want to get rid of the canvas and replace it with text
for this one I want to have configured then the Y squirrel command and now I want to set scrollbar text Dot
set that's all we need here finally I have to place the scroll bar itself
and I want to have this one all the way on the right which is what I already have here so if I run the code now we
have a scroll bar if you understood this for the canvas this one should be fairly straightforward which means I can
comment out all of this and then cover the final one tree View
for this one I have quite a few lines already let me just paste them in and uncomment them
I am creating a table and this table has two headings we have one for the first
name and one for the last name then I have a bunch of random first names and a bunch of random last names then I'm
creating a for Loop that creates 100 items that I'm inserting into the table finally I am placing or packing the
entire table so if I run this we have a table I already covered treeview in quite a
bit of details so check that bit if you're confused about all of this it shouldn't be too difficult
once I have that I can simply once again copy the scroll bar from up here paste
it in here and remove the comment and let's go for this step by step I
guess first of all we have to create a scroll bar widget and this one I'm going
to call scroll bar table this week rate with ttk.scrollbar the
parent is the window and orientation should be vertical next up for the command I don't want to
have text.yview I want to have table dot y view that's the name of the widget we
just created or at least the variable we are storing it in next up we have to configure the scroll
bar itself for that I want to have the table and this one has to configure y
scroll command with scroll bar table and set
this is going to set the position of the scroll bar itself oh well to position and the size finally
I want to get scroll bar dot table and place it on the window for this I
already have all of the arguments here so if I run this now we have a scroll bar for this table as well
and that is it the really important part here is that you understand how to use scroll bars with the canvas because this
is the one you are actually going to use quite a bit but it's generally good idea to
understand all of them although I think if you understand one of them you understand them all another really important part for
layouts are scrollable widgets and this is what we're going to work on we have a
widget and we can scroll through it this is also quite flexible so if I extend it
like so at some point We Can't Screw anymore because the window itself is larger than the list
like with the responsive layouts decantera doesn't have an inbuilt tool for scrolling which is kind of a pain
but what we can do is have a scroll wheel on a canvas on top of that we can
also add widgets to a canvas if we combine those two we can create scrollable widgets but this isn't the
most straightforward process and well you have to be very specific in terms of what you are going to do for example in
the widget that we are going to create this one here you always use the pack method now you
can use any kind of layout but you always have to create some custom solution that is going to make much more
sense when you actually Implement everything once again I have a basic setup for the code and just as a reminder I want to
create a canvas and this canvas is going to hold a widget for that I want to create a canvas with TK dot canvas
the parent is going to be the window and let's say for the background color I want to go with white this canvas I want
to pack right away I want to set expand to true and fill to both running this
gets me a white background on this I now want to place a widget this I can do with canvas and create
window this one at the minimum needs two arguments we need a position and we need
a window a window is basically the name for the widget we want to place I want
to place the widget at a position 20 and 50 completely random numbers for the window tick enter does expect a
widget like ttk dot label for this one again we need a parent or a master I
usually set this to the canvas but it actually doesn't matter now we need a text and the text is going to be let's
say a label if it runs now we have a label the master here doesn't really
matter I can set this to window and it would still get the same result now this isn't a picture it's an actual widget I
can for example place a button and this button is here and I can even press it
it works like any other widget which is super useful because that way I can add
some scrolling mechanic and then I have a scrollable container although all of this does get a bit more complex so I'm
going to do all of this inside of a class let me get rid of the canvas and instead
create a new class I call this one a list frame it is going
to inherit from TDK dot frame and we need a thunder init method
this one itself it needs a parent then I want to have text Data finally I want to
have an item height basically how this one is going to work I'm going to create
a new variable to store it in list frame seems fine
this is going to be list frame this one needs three arguments the
parent is going to be the window or could be anything is really up to you then we need some Text data for that I
have a list of some random entries this one is literally just a list with a
couple of tuples inside and those are random strings this is going to be our Text data and
finally I need the item height this is going to determine if I run the entire thing again
the item height is going to be the height of one of those entries they are always going to span the entire
width of the container so this we don't have to set ourselves you can also see here we have for the first entry label
and button and this is this label and this button for the height I went with 100 but you can always choose whatever
looks best inside of the init method the first thing we always need is a super
Thunder init method for this one we need a master which is
going to be the parent right after that I also want to pack this list frame which I do with the pack
method this is going to be expand set as true and fill is going to be both
since we're just working with a frame any layout method is going to be fine here I'm just working with the simplest
one to not over complicate things once we have that I want to get my widget data this is going to tell me
some basic things that I need to make all of this work for that first of all I want to turn the text Data into an
attribute so self.text data is going to be text not text list but text Data
next up I want to know how many items I have this I called self dot item number
this item number we are getting from the text list this one down here I simply
want to know the length of this list I have one two and so on items which means
all I have to do is use the length function and then pass Text data in here
finally I want to have one more attribute and that is going to be the list height this is going to be the
height of the entire list this I get with self dot item number and multiply
it with the item height next up I can create the actual canvas that I want to
use for scrolling this is going to be self.canvas and then here PK dot canvas
the parent is going to be self and just so we can see something I want to set the background to red
this self.canvas I want to pack right away and I'm going to use the expand method this should be true and fill
should be both let me run it straight away and now we can see we have a canvas
that covers the entire window it's a pretty good start on this canvas we are now going to place
another frame I called this one the widget frame although a better name would be the
display frame essentially what is going to happen we are going to place all of our widgets
inside of this Frame and then this Frame we're going to draw on this canvas I
think that's going to be quite difficult to understand so let me explain what I'm implementing it
I want to have self.frame and this is going to be ttk dot frame the parent is going to be self and now I want to use
self dot canvas dot create underscore window
once again we need to position and we need a window the window is quite simple I want to use self.frame the position
actually is also very simple because I want to have 0 and 0 as a starting point so the top left of the canvas
that being said if I'm running all of this we can't see a difference however what I can do now is give this
self.frame a child let's work with ttk and label
the parent here is going to be self.frame and the text is going to be a
label I want to pack this right away without any arguments now if I run this we can see label all the way in the top
left not terribly visible right now but you get the idea at least it's working
one change we can already make is that we are placing the center of the widget right now
to make that a bit better I want to place the anchor and the anchor is going to be North West now if I run this we
can see a label in the top left that's much better although now things are getting a bit
weird we have this self.frame but we are never using a layout method to place
this Frame instead we are drawing it with the create window method and that
is creating some bits that are deviating from what you used to know about tkinter the most important one is that this
great canvas is now giving the space for the frame which means I could set the
width here to whatever number I want it wouldn't matter so the width of 200 is not going to make a difference
I could also set for the label fill to both we still couldn't see anything
the reason for that is let me remove them actually because they would be confusing
when we run create window great window tries to find Dimensions that are just
large enough to display the widgets inside which right now is just large
enough to display this label although you could customize this you can set a
rift let me go with 200 and you can set a height let's go with 400 in here so if
I run this now we can see a difference if I expand the window a bit the frame
with this label is 200 pixels wide and it is 400 pixels tall and this we
can already use because I know for example the hype is going to be the list height itself although I want to place
all of this over multiple lines so it's a bit easier to see like so
that is much better basically what you have to understand now is when we are creating this Frame I want the frame to
cover the entire canvas but since we can't use pack Grid or place we have to
do a bit of math here ourselves although the math is going to look as complex as this one it's really not hard the first
part we already have because the height of the list is going to be self dot list height
if I run this now we can see we have a longer widget here that goes up to this
point for the width I want to cover the entire width of the window so right now
this would be 500. let me change this to 500 and there we
go the label covers the entire window although if we resize the window this breaks but that we can work on
for now I'm going to leave this at 500 but later on we're going to make this flexible
what is much more important for now we have to make this canvas scrollable as well
right now the canvas is as large as the container so this TDK frame up here but
if you want to make this scrollable it has to be larger as a consequence we have to give this a scroll region
this one wants four arguments it wants the left the top the right and the bottom
the left and the top are going to be 0 and 0. those are really easy
for the right side I want to have the width of the list which right now is going to be 500. and the bottom is going
to be the height self and list height I should probably explain this in a bit of detail we have a list frame which is
just going to be a frame this is the parent of all of this inside of that we
have a canvas and this canvas is going to by default cover the entire frame
like so that being said I want this canvas to be larger which I'm doing with
this line here the width right now is hard coded so the width is always going
to be 500 but the height this part here can at least in theory be
larger than the window itself it might be something like this this entire canvas I want to fill with a
widget which is this create window this should fill the entire canvas and then
we are scrolling on it instead of creating a label I want this to be a bit more flexible
I want to cycle over this text Data here
which is going to be a for Loop for item in Text data
let's make this self.txt data on top of that if I run the entire app
again what we have is we have the index then
we have one bit of text and then we have a button the number here we are getting from the
for Loop for that I have used the enumerated method the numerate
with that we are returning an index and the item let me actually print what we get I want
to print the index and I want to print the item and I realized I made a fairly
significant typo this should be scroll region talking and typing is really not easy
there we go we are getting the index and the content of the text Data this is the information
we have gotten down here this I now want to turn into a proper
widget and then place it on this Frame since that is going to become a tiny bit
more complex I want to store all of this inside of a method I'm going to call it self dot create
item I want to paste in the index and the item
this I now want to create I want to Define create item we need itself we
need an index and we need the item I first of all want to create a new frame this is simply ttk and frame
the parent here is going to be self dot frame next up I'm going to create a grid
layout this is simply going to be frame and row
configure we have only one row so this is zero and weight is going to be one
then I can copy the entire thing and change this to column configure I want
that to be five columns so zero one two three and four all with the same weight
on top of that I want to have the uniform argument and set this to a
once I've that I can actually create the widgets this one is quite straightforward I wonder if ttk dot
label the master is going to be the frame text is going to be the index
I want to have a label for the index this is what we are creating right now then I want to have another label for
well label and then I want to have a button and this button covers a whole bunch of columns
to display the text here I simply am going to use an F string and pass the index in here
on top of that I want to use the hashtag symbol next up I want to place this widget using the
grid layout method the row is going to be 0 and the column is also going to be zero
this I now want to duplicate the text is not going to be the index instead I want to have the item and the
item has two parts because it is a tuple we have label and button in this case I
only care about the one with the index 0 which would be label or thing the first
item this I want to be in row 0 and column 1. finally I want to create one more widget
and that is going to be ttk and button the text here is going to be item and 1
and the column will be column two on top of that I want to have column span this
button is going to span three columns finally the button is going to be sticky
to north south east and west with that we have a frame and this Frame I want to
return this is going to give me a widget I can minimize this if I run this now we can't
see anything the reason for that is that this method returns a widget but we're not placing it on this Frame but that is
very easily done by using the pack method this should be expand being true
bill being both then I want to have a bit of padding for
why this is going to be 4 and 4 pad X this is going to be 10.
now if I run this we're getting an error because I forgot an equal sign
there we go now we can see actual widgets although I cannot scroll right
now and I move the mouse wheel and I don't have a scroll bar and if I resize this thing
you can see that we don't actually have scrolling we just displayed a whole bunch of items but it's at the very
least a starting point what I want to start with now is some actual scrolling and for that I'm going
to use the mouse wheel all I have to do for that is create another section here
for the events this is still inside of the init method
let me minimize the create window part to get mouse wheel scrolling I want to
get self dot canvas and then bind the
Mouse wheel although there's going to be one issue
that we have to be aware of let me just run a Lambda method with the event and print the event if I run the app now and
I have my mouse over the widgets and use the scroll wheel nothing is going to happen however if I extend the app and
use the scroll wheel over the red bits we can see scroll wheel the problem that we have right now is
that this canvas.bind is only working for the canvas but once we're adding
widget to the canvas with create window tkinter sees this as the mouse being active on this widget not on the canvas
itself which is why the event doesn't work this however you can fix quite easily with bind all this adds the event
to all of the children of the widget as well so now if I run this with a mouse on all of these widgets I
can use the scroll wheel wherever I am which means now I can create the actual Lambda function what we need here is
self dot canvas dot y view underscore scroll this one needs an amount and a
unit once again for the unit tkinder just wants to have a string that says units
for the amount you basically want to choose what works best with your computer
what I have used is negative integer and then event dot Delta divided by 60. now
if I run this I can use the scroll wheel and go up and down this is working really well although once again if I
make this thing larger well I guess it still works but if I
make it full screen we get some very strange Behavior although we are making progress for the
next part I want to make sure that the list covers the entire width of the canvas right now all of this is hard coded
when I'm creating the window it is 500 and when I'm creating the scroll region this is also 500. but we do know how to
get the width of a widget we need in this case self and W info underscore
either with or a height in this case with also don't forget to call it
if I now run this again we can see the same result because by default the window is 500 pixels
but this would still work even if we have different numbers this I also want to paste in for the with for the list or
Brava create window if you're honest again now although now if I run this well we can't
see anything the reason for that is that this W info dot with is one by default let me
actually print it if I print this you can see what I'm talking about I want to print self.w
info with don't forget to call it once again and if I run this we are getting one as a consequence the widget we are
creating is all the way on the left here and it is one pixel wide so not very helpful
to account for that I want to bind the configure part again so self dot bind
and in here I want to have configure
this is going to run every time we are updating the size or the position of this container this list frame here it
is also going to run when we are creating the widget for the first time meaning we can use this to update the
size of all of this and make this work again since we are going to use a couple of
lines of code here I want to create a separate method I got this one self dot update underscore size
let's create this right away I want to have update size remember here we need self and event
for the parameters we need self and event in here I want to get self.canvas again
and run create window one more time with essentially the same arguments all
of these here I want to pass into this one and now if we run this this is going
to work again because essentially what is happening now when we are creating this bit here
it changes the width to one so we can't see it but this configure is going to
call this update method once when we are creating the layout which is going to draw on top of this
create window and that way we can only see the updated canvas and this one has the proper size I'm not actually quite
sure why W info.wiff Works in here but not in here tkinder can be a bit weird
with that if you play around with this you will eventually understand this but it's more of an art than a science to be
honest what we can do is simply get rid of this thing here this is still going to work
now we also have scrolling and more importantly if I resize the window we are covering the entire wift because
every time that we are resizing the window we are
calling this method here with configure and configure is going to update the width of this create window
the weft is always going to be the full height of the container that way the
frame we are going to place this one here is going to cover the entire width
of the canvas also I want to get rid of the comments here because we have a ton of logic I want to
keep this a bit more organized although we are almost done we have the basic
widgets and they work very well the one problem we have right now is if I make
the container really large I can keep on scrolling and now this starts to look weird the basic problem we have if I
make the smaller again if the actual container is larger than the list this kind of logic starts to
break so we have to account for that that isn't terribly difficult and all of the logic happens inside of update size
let me minimize the init method so all of this is a bit easier to see the issue
here is the height we have a list frame and this would be
something like this it's just a frame nothing else inside of there we have a canvas and instead of the canvas we have
a frame this Frame could either be let's say this tall
or it could be this tall if the list is longer than the container this one is
perfectly fine we have enormous scroll logic and everything just works the problem is when we have a list that is
shorter than the container so the height here is what's causing the problem
what we have to do to fix that is if this list is smaller or well shorter than the entire container I want to
stretch the list to cover the entire height also I want to disable scrolling
because it shouldn't be possible if the list doesn't even cover the entire container all we have to do for that is
set a custom height right now we always set the height from the init method this
height here however if the list doesn't cover the entire height of the container
I want to have the height of the container as the height of this window which means if self dot list height
is greater or equal then self.w info not with but height if
that is the case I want height to be self dot list height this is basically what we already have
but this height I want to have in here although for now this isn't going to make a difference so the same problem is
going to come up again and here we're getting an error because if this condition is false
we are not accounting for it but that we're going to work on right away
if the container so w info dot height is taller than the list if that is the case
I want the list to stretch out over the entire height of the container which in practice means the height
should be self.w info and height with that I can run your typing again
and now if I maximize it the list now covers the entire container
although if I scroll up we still get some weird scrolling behavior all we have to do for this one I want to get
self dot canvas and then unbind all
the events for this one is going to be the
Mouse wheel this is going to be the opposite of bind all quite obvious I think so for the
canvas earlier we used canvas and bind all for the mouse wheel if the container is taller than the list
I want to unbind this so now if I run this this is looking still pretty good I
can maximize this and now if I scroll well I can't scroll anymore that way we
are simply covering the entire frame with a list and this looks quite responsive
the problem now is if I make this small again I still cannot scroll because
I remove the binding but that we can fix quite easily all you have to do is copy this entire line
and if the list is taller than the window height I want to bind this event again like so if you're doing this
multiple times tikkinder simply ignores The Binding chords so we can do this multiple times without a problem with
that we are pretty much done now I can scroll I can maximize the window and I
can't scroll anymore if I minimize this again I can scroll again this is working really well
with that let me minimize everything so things are a bit easier to see we are
pretty much done although I do want to do an exercise this is really important
what I want you guys to do is to add a scroll bar to all of this
first of all we have to create the widget for the scroll by itself this is going to happen inside of a niche in
here let's say before events I want to create a scroll bar
this should be an attribute so self Dodge let's call it scroll bar this we create with ttk and scroll bar
the parent is going to be self Orient should be vertical next up I want to
place the screw bar this I do with self dot scrollbar dot place the positions here are going to be Rel x
1 Rel y 0 meaning we are on the top right
and I want real height to be 1. with that we're covering the entire vertical
space finally we have to set the anchor to Northeast with that we should be having a scrolled
bar let's run the code and there we go on the right side we have a scroll bar although it doesn't do anything and on
top of that it's overlapping with the buttons so this isn't ideal
for this project I'm not going to worry too much about it but in an actual project you want to have a better system
here for example the entire container would be its own frame and then you
place a scroll bar to the right of it using the pack method that way it wouldn't be overlapping
with that we have a scroll bar now we have to connect it to the widget itself or more specifically to the canvas this
canvas here this requires us to add two more basic bits first of all when we are creating
the scroll bar it needs to have a command whenever we are clicking on it
and this command is going to execute self.canvas dot y View
that way the scroll bar is going to influence the canvas let's try now I can
click on the scroll bar and move the canvas this is working really well although we can't see it in a scroll by
itself for that we're going to need another line of code what we have to do
is to set self DOT cam this dot configure in here we need to command
y scroll command this is going to influence the scroll
bar depending on where we are on the canvas for that we need self.scrollbar dot set
and with that I can run the entire thing and now you can see the scroll bar only covers the appropriate amount and this
is working pretty well although you are going to notice here the cameras has one
slightly annoying thing if I move the scroll bar really fast you are going to see this you can see we get some graphical
glitches and that is because sometimes the canvas doesn't keep up with the drawing which unfortunately is not
something we can really deal with it's just a problem of tkinder although if you just use the mouse wheel this isn't
happening with that we have a scroll bar but there's one more thing that I do want to do that is if we maximize the window and
we can't scroll anymore the scroll bar should disappear because it's not needed
for that we don't need a net anymore instead I want to work inside of update
size in here the if statement is what really matters this if statement
triggers if we can scroll and this if statement triggers if we cannot scroll if we cannot scroll I want to hide the
scroll bar which we do with self.scrollbar DOT lace underscore forget
with that if I run the entire thing again and I expand the window at some
point the scroll bar will disappear this is looking good although if I make the window smaller again this robot doesn't
reappear which is what we have to work on next and this happens inside of this if statement here all we have to do is
place the scroll bar again this is what we have done inside of the init method this line here I can just copy it paste
it in here and now we should be good to go let me run the entire thing there we can
see the scroll bar again this is working pretty good now if I make the window larger let's full screen it actually now
the scrubby disappears and we can't scroll at all however if I make the window smaller again a scroll bar
reappears I can make the window even smaller and this is still working really good
I suppose there's one thing I should mention if you place or use any layout
method on a widget multiple times tkinder is going to override the previous layout method meaning if we
call place twice the last call is going to overwrite the previous one let's talk
about using multiple windows in tkinter what we're going to make for this bit is going to look something like this inside
of this app we have three buttons If I click on the top one open main window we are opening another window this is a
completely separate teak in the window and inside of this one we can create any kind of layout
although in my case I stuck with a simple one but this could be much more complex in this window you can also
close inside of the window itself like so or if I open it again I can also close it inside of the main window like
so besides that you can also create a more focused window for example sometimes you
only want to ask a user a yes or no question for that tick enter has a more dedicated option that looks something
like this in here you can click either yes or no let's click on no and then it disappears the input you can also
capture and then use for whatever purpose and tick enter has a couple of options for that we're going to explore
all of them but let's talk about it in a bit more detail first and then we can jump into the code
inside of the Kinder you have two options for extra windows the first one is called a message box and these are
more specialized windows for example if you want to create an alert or a yes or no dialog you would use a message box
besides that you have top level and this is going to create a whole new window
inside of that window you can create any kind of layout and use any widget you want I already have a couple of lines of
code ready if I execute all of this we have a window and we have a couple of buttons although none of the buttons do
anything right now we are importing tkinder up here we are creating a window here we are creating three buttons here
and then we are running the main Loop all of this at this point should be fairly straightforward
but now I want to actually make these buttons do something and I'm going to start with button number three this is
going to create a yes no window I want to trigger all of that inside of a function so let me add a command method
I call this one ask yes no this function we have to create and I
will do that all the way at the top Define ask yes no there's no need for parameters and in here just to test if
this is working let's print test if I run the entire thing now and I
click on create yes in the window we can say test that's a pretty good start
what I now have to figure out is how to create an actual message box in here
and for that we have to import something else from tkinder what we need all the
way at the top is from tkinter import what is called a message box all in
lowercase letters inside of this message box we have a couple of objects that we
could use for a well message box the option you have just seen is called
message box dot ask question inside of this one you have to add two
strings the first one is for the message box title let's call it title for now
besides that for the second argument we need a string for the body let me call this one body
like so and now if I run this and I click on create yes in the window we can
see we have another window with title body and then I can click yes or no let me click on yes and it disappears
and that is basically it although I suppose there's one more thing you have to understand and that is that all of
this here Returns the answer which means I can store what is being returned in a
separate variable and then print answer and now if I run this again I click on
create yes in the window and if I click on yes we can say yes in the bottom and if I click on no we can see no that way
you can use this one here to get the actual user input and that's kind of all you have to know
if you got this far all you really have to know is that there are different kind of methods you can use to create a
simple message box and there's a really good website to explain all of them let me open it right away it is looking like
this and then here you can see all of the options you can work with the one I've just used is called ask
question besides that I could ask okay cancel I could ask yes no I could ask
yes no cancel I could also show just an info or a warning or an error and well
these are all very simple Windows let's play around with a couple of them but this shouldn't be too difficult
yeah I'm back in the code and I want to comment out what I've just done so this
part here besides that I want to get my message box and show info
for this one I want to display some information and now if I run this click on the
button we have some information for the title but no actual text
this happened because we need two arguments in here one for the title and one for the body of the text like we
have done up here let's change this one right away I want to call this one the info title the
second argument is going to be here is some information now if I run this again and I click on
the button now we have here some information besides that we can get rid of show info
and show an error if I run this again we have an error message looks basically identical except
now we have an X here and with that we have basically all we
are ever going to need for these simple boxes let me add the link to the website here
so you can find it yourself it's super useful with that we have covered the simple Windows next up let's create some more
complex ones I am going to minimize the ask yes no function and create another one
this one I'm going to call create window doesn't need any parameters and in here
I want to create a whole new window that can do basically anything a normal t-kinder window can do
for that we need a new widget this is called TK top level
this is going to return an object that works kind of like the window in the
sense that you can just add other widgets to it and then they are going to be displayed let me store this in a
variable actually let's call it extra window and just to get started let's
actually run this function when we are pressing this button here which means on this button I want to have a command
that is creating the window if everyone is now and I click on open main window we have another window and
this one let me move it to the side doesn't really do anything right now the only thing we can really see is that
we have multiple windows as the title for both of them but this we can change so let me close all of this and what we
can do with this window is basically the same that we can do with this window down here for example we could get the
extra window and set the title to extra window and we could also get the geometry and
set this to let me use a larger number let's say 800 by 300.
if I run this now and I click on open main window there we go we have another larger window that we
can work with although let's use smaller numbers so this isn't getting too large what I used
in demo is 300x400 but these numbers are entirely up to you on top of that what
you can do is create other widgets and place them in here for example what I have done is I created ttk label and the
parent here has to be this extra window so extra window and then we can add some
text for example a label and this I want to
pack right away running this now I can click on open window and we have a label inside of
this extra window I could do this in another time except now I want to use a button let me run
this again and there we go we have a label and a button although with the wrong text in there let me change it
right away this should be a button and just to finish the demo here what I
have done what you've seen in the opener I have created another label and this is
going to be in never label and for this one pack I have set expand
being true now if I run this entire thing I can click on open window and there we go we have another window you
could also use a grid method or place method in here it works like any other widget in tkinder
finally what I want to cover is how to destroy this window and there's one very
easy way if I run this again I click on open main window and I can simply close this window by clicking on the X up here
and then it disappears but besides that I also want to be able to close the window by clicking on this close main
window which we can't do right now for that I want to create another
function close window no need for parameters once again and
this close window I want to call on the middle button which means this one is going to need a command like so
and all we really have to do now is somehow get this variable let me use it
right away extra window although this wouldn't work right now and I have to call the destroy method on
it the reason why this is not going to work right now is because in this extra
window only exists inside of the scope of this create window function
to fix that we can simply declare it as a global variable extra window and now
it is available everywhere which means this function here should already work I can open this window and move it to
the side and if I click on close main window it disappears with that you should know how to use
multiple windows it really doesn't get that much more complicated although there's one exercise I really want to do
and that is that this kind of approach is not really ideal because it gets kind
of messy you're creating a ton of local variables inside of a function and you
work with lots of widgets this doesn't really feel organized what you should rather do is create an extra class let
me call it extra right away and put all of this stuff inside of this extra class and that is
going to be your exercise so this extra class should be a top level widget and contain all of these
widgets and then you're creating this extra widget when you're calling the create window function pause the video
now and try to implement this one
first of all this extra has to inherit from TK Pop level with that we are
recreating this line here although for that to work properly we have to call an init method
that has self and nothing else inside of that we have to call this super Thunder
init method although it doesn't need any arguments now we have recreated this entire line
let me start by copying the title because all we have to know is called
self and then the title the same thing we have to do for geometry meaning I can copy this one as
well except for the class we have to run self and geometry
and with that we should already have a basic window which means I can comment out all of this stuff here and instead I
want to assign the extra class to the extra window that
way this one here is still going to work let me run the entire thing now and if I
click on open window we can see we have an extra window that's a pretty good start so next up we
have to create all of these widgets here which is going to be very simple I just have to copy them and remove the comment
and fix the indentation besides that now the parent isn't going
to be the extra window it is just going to be self that didn't go particularly well this is
looking much better now the label the button and the other label are all children of the extra
widget which means I can try all of this again I can click on open window and there we
go we have an extra window and what is even better now is that the entire extra window is inside of a
separated class that way when I'm calling the function all of this is very easy to work with
and if you had the entire app so all of this one here as well inside of a class you wouldn't even need Global you can
simply turn this extra window into an attribute and then work with this in any kind of method
the final part that you need to create good looking apps is styling for styling
tkinder has a couple of different options the first one is the inbuilt
styling tools for that we have the widget options and we have the style object widget options you should already
have seen for example when I'm giving a label a background that is a widget option
the next one is external themes this basically means your importing a set of
graphics and certain Styles and you apply them to all of your widgets finally we have external modules these
are literal external modules that people have made that build on top of tkinter and they are giving you a ton of extra
functionality and extra styling which are incredibly useful now unfortunately
there's one issue I really have to talk about and that is that the inboard
styling tools and the external themes just aren't very good there are a couple of reasons why they are quite bad
actually the most obvious one is that I just don't look particularly good but besides that they're also quite annoying
to work with and you don't have that many options I am going to go over them but I will not use them too much most of
what I'm going to use are the external modules because those are actually really good and significantly more
powerful so let's talk about external themes and tick interest in build styling tools for that I already have a
couple of lines of code ready I am importing tikkinder I am creating a window I am creating a label and a
button finally I'm running the window and that's literally it running all of this is giving me an app
like this it's probably a bit large let me make it smaller let's say 400 by 300
that is looking a bit nicer what you can already do is add a bit more styling
when you are creating either the label or the button for example what you have already seen
is a label can have a background and this is a background color for example
this could be white Adobe I suppose that's quite hard to see let's go with
red that's definitely visible in here you have a few more options for example
you could also update the foreground color let's make this one white if you spell this correctly this is also going
to work like so now we have a label with white text and a red background color
let me move all of this over multiple lines so it's a bit easier to read
another option you have for customization is called the font this one well it determines the font the
important thing here is this needs a tuple this Tuple should contain two parts we have the font and the font size
if font size is really easy this is just a number that determines the size of the font let's go with 20.
the font is the actual style of the text this one needs a string with the name of
a font style to get all of the fonts what you have to do is from the Kinder you want to import something else this
something else is called font once you have that you can print font dot families and
don't forget to call it if you run a code now you can see all of the fonts
that you could be using let me pick one at random let's go with
jokerman on your system you probably have different ones but just choose whatever
you want in here Joker man and there we have a font that's definitely visible if you install external font themes they
would also show up in the list so we can extend this quite easily for the text there are two more things that I do want
to cover the first one is called justify for this one we have the options
right left and Center what this one is doing I think is quite
obvious it justifies the text however if I run this right now the result would
not be visible but the simple reason that right now the text box is this wide
exactly as wide as the label because of that it wouldn't really matter if you put the label on the right on the left
or right in the middle since the label covers the entire area of the background
you are not going to see a difference either way however what we can do when we are specifying the text we can add a
line break in here with a dash and an n and then type on another line
if I run this now we have text that is centered if I change the center to left
we have left Center text and this would also be right there we go now we have right center
text although if you only have one line of text let's say only a label you wouldn't
really want to use justify instead you would rely on the layout methods those
make it much easier to place the label in a certain position although you can certainly combine different ways of
making all of this work it's entirely up to you with that we have a whole bunch
of style methods inside of the widget that's a pretty good start although if I
run this this still doesn't look terribly good I guess we have quite a few options but they are still Limited
but with that we are going to run into some problems for example I have a
button if I want to style the background of this button with background and red if I run this
now we would get an error we have unknown option background on top of that
let me comment out the print statement at the top this one's getting a bit annoying if I run this now we are just
getting in the error that button has no option background the same would apply to foreground
it's not available
which is very very annoying what is even worse if you look online
for example for this website here you might have Googled how to give a button
a background color and you found this you'll scroll down a tiny bit and you find a code snippet like this we can see
we have foreground and background so maybe the problem in my code was that I
used background but BG was the proper name let's try that one back in my code I want to use BG let's go with
yellow but if I run the code now we get unknown option BG
so what's the issue here you might have already seen what the difference is just check out this code
and then try to figure out what the difference is the difference is that this person is
only importing everything from tikhinter there are no ttk widgets and this is
something I talked about all the way in the beginning in tikenter we have t k
widgets and we have ttk widgets ttk widgets is what I have used most of the
time and those are the much more modern widgets TK widgets I have used sometimes
like text for example these TK widgets can use this kind of styling but they do
look much more outdated while the ttk widgets look more modern but have a
different kind of styling unfortunately a lot of websites online have written these tutorials a long long time ago so
this tutorial here probably wasn't updated in just about a decade possibly longer I would definitely not recommend
any of the courses be careful with that one so how can we
style a button for that we need a whole new concept that is called style what
that means is we have to create a style object let me save it inside of a variable right away we want to have ttk
and style don't forget to call it this is going to
give you a styling object that can apply styles to every single widget inside of tkinder I can actually use this right
away we can use style dot theme underscore use
body argument I want to use clam if I run this now we get an error on an option BG because
I didn't get rid of this background now let me try this again and there you can see the button is looking a tiny bit
different that is because of this clamp theme if you are on a Mac or Linux
system this might not work to figure out what themes are available on your system you want to print style and theme
underscore names don't forget to call it if I run this now on my system I have a
native clam alt default classic Whistler and XP native let's use classic for the
theme use and there we have a really old style button I think the theme they are
using is Windows 98. however all of these Styles aren't very good so I'm not going to use any of them
instead what I want to do is I want to have style and configure the style I'm
currently using in here we need first of all a string of the widget we want to update
and then we can set for example the background color choose something like let's say green
the name of each widget always starts with a T and then the name of the widget
for example a button would be a button t button would style all of the buttons in
your app meaning now if I run this we have a button with a green background
color it's kind of hard to see but it's definitely there I think if we change this to foreground this is much more
visible there we go now our button has a green text in here we can also set the font let me
copy it from the label I want to have jokerman and 20 like so now if I run
this we have a button with custom text what you can also do is add custom styles for every widget for that you
would have to add another kind of text whatever you want let's say new and then Dot and then t button this would create
a new style for a button but you could apply it specifically to a widget if I
run the code now the button would have the default style we would only get the styling back if I set a style for the
button and this would be new DOT t button
now for runders we have our styling back this style configure here is actually a
lot more powerful for example right now we only have the text of the button colored but what if I wanted the text
color to be different when I'm pressing the button or when I have pressed the button we can create a style dot map in
here first of all we have to Target a certain kind of element in my case this is going to be new DOT t button after
that we have to Target one kind of attribute this could for example be the foreground
but now we are assigning this a list this list is going to be full of tuples
inside of each Tuple we have the state and then the option for the color in
this case for example if the button is pressed I want a button to be red however if the
button is disabled then I want a button to be yellow
if everyone is now and I press the button you can see the button is red if
I inside of the button set this state to disabled
then the button color would be yellow and we can't click on the button because it's disabled inside of the map you can
then add more arguments let's say besides the foreground I also want to
have a background color and I am very bad at spelling background for this one
once again I want to have a list if the button is
pressed then I want to have a ring background color
another option here would be if the button is active I want it to be blue I
should add a comma and now if I run this you can see that we have a couple of
different background colors for the button they are quite hard to see because we are styling the background behind the button it's um well not ideal
once again this kind of styling is really annoying to work with and very soon we are going to find much much
better ways to work with all of this in fact let's do an exercise and then we are done with this bit
what I want you guys to do for the exercise I want you guys to add a frame
with a width and a height and give it a pink background color pause the video now and try to figure
this one out first of all we have to create a frame
this is going to be frame is equal to ttk dot frame the parent is going to be
the window on top of that I have to give this thing a height and a width I'm going to use
completely random numbers for width let's go with 100. finally I want to pack this entire thing
if I run the code now we can't see anything because frames by default have no color the frame now is kind of
similar to the button in the sense that we couldn't just add a background with
pink in here we would just get an error instead what we have to do I'm going to
cut this one out inside of the style we have to configure a new widget which means I have to use
style dot configure for the widget I used to have t button but now I need T
frame once I have that I can set the background let's go with pink if I run
this now we have a pink frame with that we have covered The inbuilt
Styling methods for tea Kinder this video is already getting a tiny bit longer so let's finish it here and for
the next video we are going to cover different kinds of themes another way to
style a tkinter app is to use themes basically what that means is tkinder has
lots of external themes that you can import and those themes are going to style every single element of your app
it sounds very simple and these themes are generally fairly easy to use
however you might remember a couple of videos ago I talked about that external
themes just aren't very good to illustrate why let me show you a list
of all the available Tech inter themes here is a list of all the teak inter
themes if you scroll down you can see preview colors and while some look okay
I guess this one here looks fine there are some more I guess this one is
passable but most of these themes look really old and outdated for example
using this one here would just seem like you're making a Windows 98 app same for
this one same for these down there most of these themes just don't look good at all
on top of that the styling here is very limited for example if you want to
change any of these options here for this theme you could maybe change some
minor things but most of these are hard set so you're kind of stuck with whatever you download which somewhat
defeats the point of styling because you want to have your own app I wouldn't recommend any of these but I do want to
cover if you've seen some other people's code what is broadly considered the best looking theme if I go all the way down
is called Azure if I search for it we have Azure and we have Azure dark this
we can get from GitHub let me open it really quick in here you can see we have a fairly good looking theme
it also tells you how to use it and this is quite a nice theme to work with to
use it you first of all have to download it which you can do up here you have to
click on code and then download zip this is going to download the entire
thing and this theme you have to unpack if I open my download folder here we
have Azure ttkv Main this I want to extract all to the
current folder and then we get this folder here Azure
ttk main theme and then there we have a couple of things although the only thing that we really
care about is this theme folder here because in there we have a dark a light theme and then some extra information
inside of for example light what we really have in here are a bunch
of images for example here we have the radio accent which is a blue dot same with 40
on accent this is just a button which is also telling you why this is quite
Limited in terms of customization but at the very least we have a good looking theme in my case what I have
done I went to the main folder and copied the entire thing after that I have another folder this
one has an app I'm going to open this in a second but I want to paste all of this
in here this is going to take a second there we go and rename it to let me just
call it azure inside of this Azure we now have the theme inside of the theme we have dark
and Light what I should have mentioned this Azure TCL is really important
also if you're using this for your own app you have to include a license I that's just good practice
let's open the app and let's Implement all of this the app I have just opened is what we created earlier this slightly
more complex layout although I do want to change the name this shouldn't be class based app
anymore let's call it theme based app using the theme is actually incredibly
simple all we have to do inside of the init method of the main window so
wherever you create tk.tk you want to do two more things before
you create any kind of widget you want to use the theme
for that you want to use self or whatever your main window is then TK and then call
inside of this you need two arguments the first one is called source this tells the kinder to import
something the next argument now is going to need a path the path that we want is inside of azure
and azure.tcl this is the file we want to import
which means the folder I want to go for is called azure in there I want to have Azure dot TCL
if I run this now we can't see anything but we're not getting an error message that's what I
was looking for to actually use this beam we have to use self again then dot TK and then call now
we need two arguments again the first one is called set beam after that we
have to decide between a light theme and a dark theme if I use the Dark theme now
we can see some major Improvement although it's not perfect yet let me expand it a tiny bit
you can see most things work okay but we have to change a few things the sliders
are the worst part right now but things are definitely getting better
the main issue we have right now is inside of I think all of this happened
inside of menu inside of there we have create widgets and further down there we
have the menu slider one and menu slider two both of those are ttk scales
the problem we have with this theme right now is that we are sticking them to all four sides this is causing a
problem the theme only really works if you stick the slider either on the horizontal or
on the vertical axis but not both now if I run this this fixes a slider
and that's looking much better sometimes when using external themes you have to be a tiny bit careful although
besides that instead of the Dark theme you could also use a light theme and there we go we have a different kind of
theme that probably looks a little bit better I know it's quite subjective I guess one more thing that we can do is
all of the buttons look quite close together they should have a tiny bit of padding
that is very easily done inside of create widgets we are placing all of the
buttons here all we have to do is give them a tiny bit of pad X let's go with 4 and Pad y
should also be four now if I run this again now we have a tiny bit of padding between the buttons
and if I increase the size of this window here we go this is looking much better
and that's kind of it for themes all of the themes work either in this way or in a very similar way and while this can
give you some decent results I really wouldn't recommend using it number one for this theme you either have a light
color or a dark color and that's all you can really do for customization on top of that since all of these elements are
simply images this also slows down performance you notice this in particular when you
try to resize the app let me show my mouse actually and let me try to resize
the app really fast you can see the thing really struggles and cannot keep
up at all and I think that's really bad user experience as a consequence while themes can be a
good way to get started I just wouldn't recommend using them at all they are much better ways to style your app
there's one important topic that I want to cover before I continue and that is colors
so far I always use the tkinter default colors those are for example red white
blue pink orange yellow I think they're about 10 in total which well is quite
limiting to create any color that you want you would use what is called
hexadecimal value system it sounds complicated but it really isn't that bad
hexadecimal numbers go from 0 to F that is going to sound confusing but the
numbers look like this we go from 0 all the way to 9 and then we continue with a
b c d e and f with zero being the lowest number and F being the highest number
basically just imagine that these letters here are numbers in this kind of numbering system
the reason for that is that with the system you can express a much greater range of values with fewer numbers you
see it quite often actually when you work with computers to turn this into color you have to combine three of these
numbers with the first value standing for red the second one for green and the
final one for blue this might look something like this we have 0 8 and F
this means that we have zero amount of red because zero is the lowest value and
in this case it means we have the absence of red next up we have d8 this one is roughly
in the middle of the system which means we have more or less 50 of green color
although this is not an exact number here finally we have F and this F stands
for blue and is the highest number in here which means we have one hundred
percent of the blue color finally to indicate that we are using hexadecimal
numbers you want to add the hashtag symbol in front of this if you add this into tkinder as a string
T Kinder is going to recognize this as a color let's have a look for the code I
am importing tkinder and ttk I am creating a window then I'm creating three labels and place them right away
using the pack method finally as always I'm running main Loop so we can see the app this is giving us an empty window
because none of the labels has any text although they don't need any kind of text because I only care about the
colors here to give it a color as always we need for example a background
for this so far we always use something like red with that we have a red
background color however now that we have learned about hexadecimal colors we can set the background to the color I
used was hashtag 0 8 and F if I run this now we are getting a very
bluish color this should make sense because we have no amount of red and we have a huge
amount of blue that way you would expect this color here to be quite blue
although since we do have a certain amount of green that's the eight this is
not going to be a complete blue I can actually demonstrate this if I copy all of this I could for example change the 8
to an f and the F to a zero what would we expect now for the color
well if I run this again we are getting a pure green because for this one we
have no red and we have no blue the only color that we have is green and we have
the full amount of green so with that system you could create basically any kind of color now it's
going to be really annoying to just experiment with each of these values and nobody actually does that instead what
people are doing is they use some kind of editor and they all have some kind of Color Picker in build
for example here I am in Photoshop if I click on the color
you can see down here we have a hexadecimal color system although this
one looks a tiny bit different compared to what I have just used instead of three colors we have six colors let's
talk about that one really quick hexadecimal color values are always either three or six digits long
the one we have just seen looked like this we have one digit for red one digit
for green and one digit for blue besides that we could also specify two
digits for each color two for red two for green and two for blue
this second system here is a lot more precise because we have twice as many
values for the red color for example as would have in this system which gives you well a whole lot more
options when you use basically any color editor online this is the system they are using they basically always have six
colors but you don't have to use it if you have a simple app this system here is perfectly fine
back in Photoshop you can see right now we have FF so we have a pure red color
and then 0 0 for green and zero zero for blue if I move around you can see these
colors change and you can create basically any kind of color value in total I think this gives you about 16
million options definitely enough for any kind of style that you want if you don't have Photoshop you don't
have to worry because Google has a Color Picker inbuilt as well in here you can simply move a color around and get
basically any kind of hex value that you want this is the value you're always looking for which means I could
literally just copy the value from this return to my code editor and paste the
color in here run the code and there we go we have the
same color we just created which makes all of this quite efficient because you can now pick literally any color that
you want Let's do an exercise on this one I want you guys to create a brownish
color using hexadecimal values you could use a Color Picker for that although
just to practice the system try to figure out the numbers without using an editor it should be fairly easily doable
but both approaches are going to be fine pause the video now and try to figure this one out
let me copy the final label here and place it below the exercise for this one
I want to work with just three digits let's start with f 0 and 0. this is
going to give us a pure red because we only have F and then 0 for green and zero for blue
which means we have a pure red this we now have to make darker to get some kind
of brown the best way of doing that is by increasing the amount of green instead of zero let's go with an a
if I run this now this is giving us a bit of an orangey color if I reduce the amount of green let's say 2 is 6.
this is definitely getting brownish although right now it's more of a dark orange if I put this to a green
we are definitely getting closer I guess if I increase this a tiny bit more to a five this gets close enough to at least
a light brown and if I reduce the amount of red from an F to let's say c
this is very much a brown color doing all of this inside of Google gives you much easier results you can just click
on a brownish color here something like this and you have a lot of different brown tones you could work with
before I move on there are two more things that I do want to cover and that is white and black
right now we always set a color but how can we get a white and a black color those two are really easily done I can
just copy this black is the absence of all colors which means 0 0 and 0.
running this gives us a black color and a white color is the opposite we have
every color 100 available which means f f and f with that we have white if you
have the same color value for every color you always get some shade of gray
let me duplicate this if I change 0 0 and 0 to 888
we're getting a grayish color with that we have covered all of the colors let's
talk about styling modules so far I mostly talked about stuff that you shouldn't do in teak hinder in terms of
styling this is going to change now because external modules are really good to add style and to use it easily
these external modules build on top of the Kinder and improve certain parts of it most of them are styling but they
also add a few more extra functionalities custom tkinter and ttk bootstrap are the really common options
I'm going to start with custom tkinter because this is what I think is the best option for tkinter in terms of styling
it's also the one I really like to use custom taken that works by using the
same widgets as ttk but it lets you customize all of them easily on top of
that there are also some additional widgets and every single widget has a dark and a light mode that way you can
basically create any kind of style that you want before I jump into the code there's one more thing I do want to
cover and that is that custom tikkinder has a really good documentation decide with all of the code is looking
something like this although if you scroll down you can already see some demos for the dark and the light mode
all of these elements are dynamically generated meaning you can customize a lot of different things here
on top of that if you go down a tiny bit further you have the documentation in here on the right side you have all
of the different widgets and all of the elements of custom tkinter if I for
example click on ctk label there we have an example of the code we
have all of the arguments and then we get a bit more information this is
literally all we need and here you can see for example we can set the text the width the height the
corner radios a foreground color a text color and a font and all of this is very
easily implemented I suppose the best example here would be ctk button on the
right this is just a simple Button as you can see here you can customize every
single element of this button quite easily if you contrast this with standard
tkinter well you have to create a style object and in there you have to create a map none of this is necessary here you
could simply set a foreground color a hover color a border color a text color a text disabled color
basically whatever you want there are lots of different options in here so let's actually create a basic custom
teakinter app although for that first of all we have to install custom t Kinder because it
doesn't come with python by default but that once again we either need the Powershell or The Terminal depending if
you are on Windows or on Mac OS in my case I'm using the Powershell so I need pip install custom tkinter
although in my case I already have this one installed so it's not doing anything if you were using Mac OS this would be
pip free install custom tkinter here we have a completely empty python
file the reason why I have nothing ready is because we are not going to use any
of the tkinter widgets we have used so far instead I want to import custom
tkinter this is going to be kind of annoying to write I usually abbreviate
this as ctk the best comparison here is that all of this is fairly similar to TDK in the
sense that inside of this ctk module we have a ton of widgets that we can use for example we can use this to create a
window this is going to be another window that I want to store in a variable and then here we need ctk and
then CT or upper score and then K and lower score don't forget to call this
once we have that we can run the entire thing with window.main Loop
if I execute the entire thing we already get a window that is looking significantly better a really important
thing that you do have to understand is that this ctk window inherits from the
tkinter window as a consequence we have all of the default arguments we could
use for the window for example we could set a window dot title let me call it a
custom tkinter app that is some terrible spelling that looks better if I run this
thing now and increase the size we have a custom tkinter app although I just
realized there's another typo in there that is looking better besides that we can also set window dot
geometry in here as always we need a string with a number let's go with 600
by 400. running this now we get a much larger window with that we have a window
next up we can create some widgets for example if we want to create a label
I want to store this in a variable all we need here is ctk and then ctk with
label just like with ttk we need the master which in my case is going to be
the window after we have that I can set some text this can be a ctk label
this is going to return a widget and this widget I have to place on the window with some kind of layout method
let's go with pack if I run this now we have a ctk label so
far we have some very basic functionality this ctk label gives us a
ton of options for customization just for reference here is the documentation
what we could set for example is the corner radius the foreground color and the text color I guess the foreground
color here isn't the perfect name this is essentially the background color for this one we can either use a tuple with
a light and a dark color or we can use a single color that is called transparent all the colors here we would either use
hexadecimal color or one of the inbuilt tkinter color names which means I can
set an F G color and set this to red if everyone is now we have a red
background color on top of that I can set a text color
let's go with white here with that we have a white label also I'm going to put all of this over
multiple lines that's going to make everything a bit easier to read another useful thing that custom ticket has that
ttk actually doesn't have is Corner radius this one determines the corner radius I
think that's quite obvious if I set this to a 10 we now have rounded corners for this label with that we have a label
next up let's create a button this we create with ctk and then ctk button what
you always have to be aware of you have C and T in capital letters and then the K is a lowercase letter
now this button like the label is first of all going to need a master which is going to be the window then we need some
text I'm going to call this one a ctk button this button I want to pack if I run this
now we have a ctk button we can click on it but nothing is going to happen
this button now is very easy to customize for example if we now set an
FG color or this one let's use an hexadecimal color we can use f f and 0
with that we get yellow on top of that we can set the text color and for this
one just to stick effects of decimal colors I want to have a black color so I'm going to go with 0 0 and 0.
now we have a yellow button although if I hover over it we get this
dark blue that we can also change although again I want to do all of this over multiple
lines so it's a bit easier to read to change the hover color we need well
have a color for this one I want to have a slightly darker yellow we started with
FF and 0 to get a darker yellow this should be let's go with a a and 0. if I
run this now I can hover over it and we get a darker yellow other than that the
button works like in TDK which means we can add a command this could for example
be a Lambda or literally any function but in this case I just want to print e button was pressed I forgot the
semicolon now this should be working and if I click on the button we get a button was
pressed now that we can execute a command we can work on something really
cool in custom t Kinder and that is to change the theme between light and dark mode by default custom TK enterp uses
the default theme of your system in my case if I run the entire thing again if
I show you the settings for Windows like this right now my system setting is dark
if I set this to light things will need a second to load but now you can see the
app automatically switched to a light mode if I go back to dark
Banks need a second again and there we go we have a dark Style app
again which is really cool for custom tkinter because it already knows if the user has a dark or a light mode and it
and it adjusts for that although you can customize this yourself if you want your app to run in light
mode or in my case I want the app to run in light mode once I press the button all you have to do is get ctk
set appearance underscore mode you can either set light or you can set dark
dark is the one we already have so I want to have light now if I run this and I click on the
button we have light mode although if I click on it again nothing is going to happen what is even better is that every single
color you can specify usually isn't one color but a tuple of colors let's say
for the label if we have a dark mode I want this to be red but if we have a
light mode I want this to be blue what you simply do in this way you have
a tuple the first argument is the light color the second argument is the dark color
which means if I run this again right now we have the dark mode so the color is red for the label but if I click on
cdk button now the label foreground color is blue because we have the light mode this
system works with every single color for example for the text color I can have white for the dark mode and I can have
let's go with black for the light mode if I now click on the button now we have
black text and a blue background color exactly what we specified in here if you
understand all of this so far you understand the basics of custom tkin term all you really have to do is look
at the documentation and then pick and choose whatever widget you want on the right side you have ctk widgets the one
I just used was ctk then we have ctk button and ctk label we also have a ctk
frame that works like a ttk frame although this one has a background color besides that we have a text box
we would have a switch although there's no image we would have a scroll bar also no image
let me find one with an image we have a slider this one also doesn't have an image okay some bad luck but let's play
around with a few more this system here doesn't really change if you found this series so far you already know how to
use all of this let's say for the next part I want to create a frame this one
is going to be ctk and frame although I forgot ctk dot ctk frame but
this one as always we need a master which is going to be the window if I
pack this Frame now you can see this already has a background color if you don't like it
you can simply set the FG color to transparent
that way it disappears this Frame is going to work like any other frame we have seen so far which means you can add
elements in here let's say I want to add a slider in there this we create with cdk and ctk
slider the parent now is going to be the frame and let's pack it right away slider.pack
there we go now we have a slide end here and this one works like any other slider
just to visualize that this is indeed inside of a frame let's remove the background color now we can see that
there's a slight background behind the slider if I'm adding some padding let's say pad X is 20 and Pad Y is also 20
now all of this is much more visible what you can also do is combine custom
tkinter with standard tkinter for that though I have to import
import tkinter SDK and I want from the counter import TDK it is totally fine to
combine ttk widgets with custom tkinter widgets although most of the time the
ttk widgets especially when you put them right next to the custom TK inter widgets they start to look really bad so
generally I wouldn't recommend doing it however what you might want to do is use
the T content variables those work perfectly fine with the custom taken that variables for example for the label
I can create a let's call it a string VAR which is going to be TK and string
VAR order value here we could set a custom string
this string VAR we can set as the text variable for the label so string VAR
exit in here and now we get a custom string for the label although strictly speaking custom
tkinter also has inbuilt TK inter variables we get those by simply using ctk and
then we can use stringvar invar and so on which means if I have ctk instead of
TK we're not going to see a difference right now the ctk and the TK variables
are identical although that might change in the future if you are using teak into variables and using custom tkinter use
the custom teak into variables with that we have all of the basics of custom
tkinter it really doesn't get that much more complicated which means we can do an exercise and then we are done
what I want you guys to do is going to look something like this all the way at the bottom we now have an exercise
switch this one looks absolutely horrible but if you can make it look this horrible and custom tkin term you
definitely know how to change a lot of different things which means you have to look at the documentation use the custom
tkin test switch and then make it look something like this pause the video now and try to implement
this one yourself we have to create a custom tkin test
switch although first of all let me add an exercise text in here I want to create a switch and this we create with
custom tkinter and then ctk switch this one first of all needs a master so
window is the default argument here next up I want to have some text this is
going to be the exercise switch to get started this is all we need which
means now I want to pack this switch I have made an error and you can already
see I made a typo the K here should be lowercase which means CT lowercase k now let's try
this and there we go now we have a basic switch that by default is looking pretty good we want to make this thing look
absolutely horrible so let's talk about how to customize this thing and to customize anything accustomed to
kinder the first step should always be look at the documentation here's the
documentation I still have the slider open but I want to look at ctk switch
this one here this one has a huge amount of arguments we could be working with I actually only
used a small amount of them you could make this look even worse I guess we can start with the colors I
want to have a FG color of red don't forget the comma Now if I run this
we get some bits of red to get the other color we need what is called progress
color this in my case I want to be pink now we have red or we have pink
I guess FG color sometimes he is a bit misleading it's basically the background color but you get the idea also if you
wanted to you could add a tuple in here with red for the dark mode and let's say
blue for the light mode if I run this now we have red as a default but if I
change this to the light mode now this is blue so once again a tuple always works here
to get the light mode color besides that if you want to change the color of the actual button you want the button color
I'm not sure if button is the proper name but you get the idea in my case I change this one to Green now we have a
green color for the button although if I hover over it it becomes white that I also want to change
and for that we have the button our
color I set this one to Yellow now if I run this again and I have over it it's
yellow you can already see we have a ton of customization here all of the colors can
be changed and this wouldn't really be doable if we used a theme because this
one relies much more heavily on images so those couldn't be easily changed what we can also do since all of this is
dynamically generated Wicket set is switch with if I set this to 10 you
should already be able to see what's going on now we have the width of the thing being much more narrow and if I
click on it nothing is going to happen although if I change this to let's say
60 now you can see we have a much wider switch
you can also set this switch underscore height to let's say 30
and now you have a huge switch thingy if you want to make this thing look
really horrible you can set the corner radius and this changes the corner
radius of the button if I set this to a 2 now we get a very thin slider
although it all still works perfectly fine I just made a mistake I just realized when we set the corner radius
we are setting the corner radius both of the button and the corner radius of the
background these Corners here at this corner as well so with that we have
custom decanter or at the very least the basics of custom tea Kinder if you know ttk already using custom decanter is
really easy basically all you have to do is replace ttk and then the widget with custom TK and then ctk and then the
widget name on 90 of the time this is all you have to do to understand custom
TK enter a little bit better I want to convert a ttk app to a custom tkinter
app the app I want to convert is the more complex layout app I created
earlier if I run this we get this app here I want to convert all of this to
the custom tkinder style this isn't going to be very difficult and it's not going to take very long
because of that I want this to be an exercise right away I want you guys to
convert the app to use custom tkinter it really shouldn't be too hard so pause
the video now so pause the video now and try to figure this one out
to make sure we are not using any default decantera functionality I am
going to comment out the import for tkinter and ttk instead I want
to import custom tkinter as ctk if I run
this now we are going to get a lot of error messages we have to go through this thing one by one and fix things
starting down here I want to change the title from class based app to
class-based app with ctk with that we have to look at the app
itself so the main app or this one I don't want to have tk.tk instead I want
to have ctk dot ctk that is actually all we need inside of the app because this
one doesn't actually do very much next up I want to work on the menu for this one we are inheriting from a frame this
I want to change to ctk and then ctk frame inside of the init method for this
one we just have basic stuff so this can stay as it is although inside of create widgets we
have to make a couple of changes first of all the buttons are very easy to update instead of ttk I want to have
ctk and then ctk button for the menu slider we cannot use scale anymore this
one doesn't exist in custom tkinter instead what we are using for this one is called a ctk slider which means I
want ctk and ctk slider after that we have toggle frame this is
going to be a frame so ctk dot ctk frame inside of there we have a menu toggle 1
and menu toggle 2. check button doesn't exist in custom tkinder but we do have a checkbox and
that's basically the same thing I want to get rid of those and use ctk and then ctk
check box and that should be all we need finally
we have an entry widget this one does exist in custom tkinder so I want to have ctk Dot ctk and entry the rest is
just layout all of this can stay as it is because it works with custom tkinder like it would work with TDK
I can minimize the menu we should be done with this one and that's the most amount of work inside of main we have
one frame this I want to change to ctk and then ctk frame the rest in here can
stay identical finally we have the entry in here as always I want to change the
TDK frame to ctk frame inside of this one we are using a label this we can
change very easily to ctk dot ctk label the same for the button this should be
ctk dot ctk button with that we should be nearly done
although if I run this now we get one error message and that is that Orient
inside of the menu doesn't exist the reason for that if I open the
documentation a ctk slider we don't have Orient instead we have orientation a
very easy thing to change instead of Orient we want to have orientation
let's try this now next up we have a typo There's No ctk
Label I once again made a typo let me minimize the menu the error message
happened inside of entry in here this should be ctk lowercase k
let's try this now there's one more error message and that is that custom decanter for label doesn't have
background although if I remove this one it should be working now there we go
although well it's not ideal yet we do have a couple of things that we
want to work on most importantly the sliders aren't great yet but that is
very easily fixable all we have to do if I minimize the app and to entry inside of the menu
when we are placing the sliders that happens down here I want to remove
the East and West now if I run this the sliders are looking much better
and let me increase the size a tiny bit here this is all coming together much better
although right now the sliders do look quite a bit thin if you want to make them a bit wider you can do that quite
easily all you have to do is go to the sliders and in here set a width let's go
with 15 possibly a bit too thin I guess 20 is better
yeah this one looks much nicer if I maximize the entire thing it still
works next up for the buttons I want to have a tiny bit of padding
which means when I'm placing the button using the grid method all I really have to do is to add pad X of 4 and Pad y of
4. with that we have a bit of padding and we are starting to run a bit out of
space but I hope you see the potential of custom tkinder because all of this is
starting to look much better than defaulty kinder most importantly it is really easy to change all of the
elements you see here can be customized and if you have a bit of experience you
can actually create pretty sophisticated guis with that that actually look modern another useful tool to customize tkinder
is called ttk bootstrap this one like custom tkinter is an external module
that you have to install ttk bootstrap is an external module that has really good theme support
what that means is well for custom tkinter we customized every widget individually or TDK bootstrap instead we
are creating one theme and applying this theme to every single widget while this means that we have a bit less control it
makes it much easier to style widgets although before we can use it we have to
install it as always this either happens in the Powershell if you're on Windows or in the terminal on Mac OS to install
it in my case on Windows I would need pip install TDK bootstrap if you're on the code now
we get a short message and then we have it installed if you're using Mac OS you
would use pip 3 install ttk bootstrap
and that would happen in the terminal the code I am going to start with is looking like this
we are doing the usual Imports in window creation the really important bit is this we have a label and then three
buttons finally we are running the entire app so nothing special if I run this code we can see we have a
basic app with three buttons and a label to style this we have to import ttk
bootstrap which means import ttk boot strap
and just by importing TDK bootstrap we are already applying a new theme to our
app meaning if I run the code now we can already see we have much nicer looking buttons
although to actually use ttk bootstrap what you usually see is that people import it as ttk the reason for that is
that tdga bootstrap basically works like ttk in the sense that all of the important widgets like label button and
so on exist inside of it and we are just accessing them except if we are using
ttk bootstrap they all look much nicer because of that we don't need the Kinder
ttk at all if I run the entire app now everything still works as before there's
only one change that you absolutely have to be aware of and that happens on this line here when we are using ttk
bootstrap we don't want to use tk.tk instead we want to use ttk Dot
window if I run this now we can see we have a different kind of title bar with
a custom icon but other than that not much has changed the reason why we need
this window is because with that we can add one more argument and that is called theme name this is where the actual
magic happens for ttk bootstrap because in here we can for example add Darkly
run the code now and they can see we have applied a custom theme to the
entire app another thing that we could be using is called Journal if I run this now we have
a completely different style if you want to know all of the available custom themes you have to look at the
website there's a full list let's have a look at that one actually the website is looking like this and in here you have
lots of explanations in terms of what you can do we can already see a couple of styles here
although to find all of the Styles at the top you have to go to themes in here you find one theme that is
called litera this is the default theme on the left side you can see light themes and dark themes let's have a look
at all the light themes and here we have Cosmo we have flatly we have journal litera and a few more quite a few more
actually besides that we also have the dark themes here we have solar Darkly Cyborg
and again a few more all of these themes you can use immediately on top of that if you want
to create your own theme you would have to go to ttk Creator and in here you
have an app that you can use to create your own custom theme I'm going to cover that in the next part
although before that there are a few more basic things we have to cover the most important part is if you look at
this app here you can see we have lots of different styles we have primary secondary success
and so on and all of these are different colors inside of a theme
but right now if I return to my code and run the entire thing all of the buttons
have the same color for example I might want to have the first Button as red then another button could be let's say a
warning the final button could be some kind of green button how could I get these colors to learn how to do that the
best way is to start with the documentation here we are again the important part you want to look at now
is called getting started the installation we have already covered next up there is a tutorial this covers
all you have to know about ttk bootstrap since the entire module isn't terribly difficult this is quite a short page
which means this could be a really good exercise read through this website and try to understand how to style
individual elements using ttk bootstrap so pause the video now and try to figure this one out
I guess a quick solution here would be using the boot style covers just about
everything this allows you to give certain widgets a certain kind of style for example One widget could have the
Style's success another widget could be info and well you have quite a few more
themes if you scroll down a bit more you can see all of the themes here
you have primary secondary success info warning danger light and dark all of
these can be passed into the boot style to get a certain kind of color how you pass it in there you can do in
two ways you can either import from ttkbootstraps.constance import
everything or if you go a bit further down you can use a string that looks
something like this the module is really flexible here so choose whatever you like
the recommended option you can see it down here is the dash this one here this
is the one I'm going to use as well in this one you always specified the color first and then if you want to have only
the outline or the full color I haven't covered this yet but you can see it up here quite well
we can either have a button with a solid color or a button only with the outline
the Sonic color is the default the outline you get if you add outline in
the style with that we have all we need although I guess one more thing that I do want to cover to actually get a
preview of how all of this is going to look you can look at themes and I'm looking Journal right now which is a
light theme in here we have Journal you can see we have the primary
secondary success info and all of the other colors that way you have an idea of how this is going to look in the end
so here I am back in the code and let's start by coloring in the first button I
need the boot style with a string let's call this one danger
now if I run this the first button has a different color now it's orange instead
of the default red if you only want to have the outline you would add a dash and then outline now if I run this we
only have an orangey label around it and if you hover over it like so then you
can see the full orange color for the warning you can add a boot style of warning
that is horrible spelling that looks better now the warning is more yellowy
finally for the green one I wonder if a boot style that is called success
running this one gives me a green button while I only use buttons these kind of
styles would work with literally any widget if I return to the documentation you can see we for example have a
checkbox we have a progress bar we have a slider we have a toggle down here we
even have a calendar we will learn about that later and we have scroll bars all
with these colors here every single aspect of the app will be styled
appropriately all you have to do is use the bootstrap ttk module and then use the normal widgets that way you already
get all the Styles you want I guess on top of that you have to set the boot style but that's a fairly small task
since all of that is fairly simple we can do one more thing here's the app we created earlier with
the more complex layout and I want you guys to style this entire thing using the TDK boot style module make sure to
use a couple of different colors and pause the video now and implement this one yourself
for this one I want to comment out from tikenter import TDK instead I want to
import ttk boot strap as ttk just by doing that the app
already looks quite a bit better although we can make a few more changes first of all inside of the app I don't
want to use tk.tk instead I want to use ttk dot window
doing that gives me a much smaller app but well we're getting a different title
bar although once we have that inside of this super dot init method we can now
set a theme name this theme name could for example be Darkly
Ebon I usually like quite a bit or to stick with what we have already seen we could use Journal
this one would look something like this other than that we don't really have to
make too many changes because we are still using ttk and the regular widgets
although I guess what we could be doing when we are creating the menu not the
init but in create the widgets for example for the buttons I could use different styles for example I could
have a boot style for menu button one that could be Danger that makes the first button orange I
could use boot style for the second button let's call this one success
now we have a green and an orange button for the third button I want to have
let's use dark and out line running this one we are getting a third
button although I don't really like the styling here but well you can see different kinds of styles
I think adding a tiny bit of padding here would make a lot of difference when I am using the grid method to place
all of the buttons I want to add pad X off for and Pad y of four
like so and this is a minor Improvement
I think this is looking a little bit better although the outline here doesn't work too well I'm just going to remove it
like so this is definitely looking better next up we can also change the menu
slider once again for that we need a boot style let's use one we haven't used yet
for example back in the app one that I haven't covered yet is called info
we also haven't covered secondary let's use those two the first slider should have the style
info the second one should have this style secondary
if I run this now we get two sliders one that is dark blue the other that is more
grayish after that we can style the check button I'm only going to cover one because this
is probably starting to get repetitive and here now we have one check button being blue the other still being red
I think you get the idea so I'm gonna stop this but I think the app already made quite a
bit of progress although there are a couple things you want to be aware of the most important one is that you still
have the basic ttk widgets which you see in particular here for the entries both
of those are just labels with a background and titigate bootstrap doesn't style those
if you wanted to have a better color here you would have to use a hexadecimal code to make a similar style compared to
these buttons here which certainly is doable a really cool part of ttk bootstrap is to create custom themes
this is very easily done because TDK bootstrap gives you this kind of app
where you can pick an existing theme let's say Journal I have already used
and simply change any part of it for example you could give it a different main color let's go with blue you could
give it a different background the default is white let's change it to a really horrible green
there we go you can literally change whatever you want this is also very easily imported into any app you're
using to get started there's only one thing you really have to do you start by
using either the Powershell or The Terminal the command you need you can find in the
documentation let me open it really quick here's the website for ttk bootstrap you want to go to themes and
in there is creator this one gives you a command python-m
ttk Creator this one opens this program here let me copy it
and return to the Powershell and simply paste the command in here if a run is now we can see we have the
app you have just seen a really important part do not close the Powershell or The Terminal this would
close this program here as well once you have it you can simply give your theme a
new name let me show my mouse folder of this actually in the top left you can set a name I'm going to call my theme
custom after that I can set a base theme let's go with simplex
it really doesn't matter what you're starting with with this one you can now basically very easily change whatever
colors you want let me use some colors that are very easily visible here we have a pink color
for primary and for the background I want to use a visible color let's go
with pure black that is going to be really annoying to see I guess we should make this a tiny
bit less black let's go with a darkish gray definitely an improvement but this is
absolutely something you have to play around with for a bit all I really care about for now is that
you can see how easy this thing is to use to use it all you have to do is click on Save and then you get the
message the theme custom has been created although nothing else fortunately that is because we don't
need anything else because with that you can use this custom theme like any other
theme in ttk bootstrap for example here is the app we styled in the last part
the theme name we got here inside of the app class we use Journal so far if I change this
to custom run the app again here we have the theme I just created
it's literally as easy as that to use the theme other than that what you can also do in the top left you can set
reset to get back to the starting point if you really don't like what you created
you can also Import and Export your theme all of that works really easily so with that we can create our own
themes there's one more thing that I want to cover for ttk bootstrap and that is some
extra widgets that come with this module the app we are going to create is going to look something like this in here we
have a couple of elements the top part is a scrollable widget this one comes by
default so you don't have to create it next up we can show a toast this one gives you a toast in the top right
after that we have a tooltip then we have a calendar where we can pick a date and get the date this one
only prints the date but you get the idea after that we have a better looking kind of progress bar
finally we have what is called a meter this one is looking really fancy all of
these switches we are going to create in this bit to get started I already have a couple
of imports at the top I am importing tikenter SDK and ttk bootstrap
note here I am importing TDK bootstrap sttk not tkinter after that we have the
window and we are running the entire thing finally we are using the Darkly theme
with that we can start creating some widgets the first one is called scroll
frame which creates a scroll level frame to understand this one in detail I would
recommend to read the documentation let's open it actually once again here I am on the website of ttk bootstrap and
you want to look at API in here we have a couple of extra parts that are really
useful the one I want to look at right now is called scrolled module and here
we have scrolled frame and scroll text scrolled frame is the one I really care about this one gives you no picture
that's very annoying but it gives you some code snippet on how to use it first of all you have to import a specific
subpart of ttk bootstrap although this one is basically just a frame so you can
create it like any other frame you can pack it on whatever container you want and then the important part is you want
to populate it with some kind of Widget the only thing you have to do is set the
parent or the master of these new widgets as the container widget you just created then these widgets are going to
show up inside of it back in the code the first thing that I have to do is from ttk bootstrap dot
scrolled I want to import scrolled
frame if you run a code now we cannot see an error that's a good sign that I didn't
make a typo now with that I want to create let me call it a scroll
frame this is going to be a scrolled frame as always this one is going to need a
parent which in my case is going to be the window I am going to pack this straight away using the pack method for
now let's set expand to true although if I run this all we can really see is a
scroll bar since we don't have any widgets yet this isn't going to do very much to account for that I want to create a
whole bunch of widgets this I do with a for Loop for I in range 100.
I want to create a ttk label and I want to create a ttk button both of those
have this grow frame as the parent which means scrolled frame is going to be the
master and after that I want to create a text that is going to be an F string
that shows us the number which is going to be I this I we're getting from the for Loop for the text I think I chose
label with I and then button with I
after that we have to make sure that we are packing these widgets and then they
are going to show up let's run this now and there we go now we have a scrollable
thing that we can work with I should have probably said fill to
both so this thing actually covers the entire window now if I run this here we
have scrolling that works for all of the elements although you can't see if I scroll
really fast the graphics here really aren't working too well so I would
generally recommend to create your own scrolling system I have covered this earlier on if you skipped it I suppose
what you can also do for the label and the button in the pack you can set fill to X that way they are covering the
entire horizontal space now the reason why I would recommend to create your own scrolling logic is
because all of this is quite Limited for example what if you wanted to have
if I'm drawing this if you want to have some kind of setup where you have one
widget covering this amount of height and then you have one widget on the left
for the label and then the button on the right this unfortunately you couldn't
easily do inside of this setup something you might want to try is create a separate frame with ttk and
frame and the scroll frame as the master the label and the button would then be
parented to this one which means here I want to have the frame and then I want to set this side to
left finally I want to pack the frame if I
run this now this is kind of working although you can see we're not filling
the entire space we could try to set fill to X or to both
although if I do that all we're doing is setting the frame on the left side
you might be thinking this is going to be fixed when we set expand to true but
it doesn't we still get the same result this happens because of the drawing logic here to get proper scrolling logic
you unfortunately have to create your own kind of widget but okay next up we get a much more
useful widget and that is called a toast a toast is a small notification for
example in the bottom right of the window you can get a message with some extra information this is what a toast
creates this one we once again have to import like the scrolled frame we do this with
ttk bootstrap dot toast import toast notification
I can already see there's a table here but other than that this is okay to use
this widget we first of all have to create it and store it inside of a variable let me call it toast and toast
notification this one doesn't have a master but we do need to set a title
let's call it this is a message title besides that we also need a message
itself I'm going to call one this is the actual message
finally I want to put all of this over multiple lines because we need one more argument in here that would be the
duration this tells you how long the toast is going to be on the window the number you
need to specify is going to be in milliseconds meaning if you want two seconds you would need two thousands one
second is one thousand milliseconds that is all you need to get started the
way you are using it is you get the variable that stores the widget and then run show underscore toast
if I run the app now you can see in the bottom right we have this is the message and it disappears after two seconds
although you can see that the entire app disappeared after we have used this
is a bug that happens if you use this show toast by itself if I remove it we
are back to the normal window essentially what you want to do is to run this toast only if the user presses
a button or does a certain kind of action only then you are calling it I want to add ttk and button
the window is the master for the text I want to have show toast finally the
command is the important bit here this is going to be toast and show underscore toast
I want to pack this widget straight away without any arguments because we don't need too many
now if I run this we have another button show toast if I click on it we now have the message and now the window doesn't
disappear anymore when the toast disappears this covers the basics I guess we can cover a few more arguments
in here but other than that this doesn't become any more complicated we can set a
boot style in here this could for example be dark let me run it now and
show the toast now this is dark we could also set this to warning
and now we get a yellow kind of button or well not button but a warning the one
thing you want to be careful about is that this boot style here doesn't support outline if I run this again
click on show toast we now get an error that this thing doesn't have an
attribute create outline frame Style you can only use the color there's no other style available
I'm going to stick with dark I think this one generally looks the best finally there's one more important thing
and that is you can set the position you have X petting y petting and then
the start position the start position is the really important one in here you can set
something like North East North West South East or Southwest these positions
would refer to the different corners of your screen for example Southwest would be the corner down here Southeast would
be down here we have Southeast South West then we have North East and we have
North West these are the different Corners you can start with and then you are using X
padding or white padding to get a bit of offset for example if you want to start with
the Northeast you would add an e in here and then you would use these numbers to get an offset
let's actually play around with that for X padding and Y padding I want to start with zero so we can focus on the corner
I want to start with North East if I run this again now I click on show toast now
the message is in the top right if I set this to North West run this again click
on show toast now it's in the top left I'm going to stick with Northeast and for the numbers I now want to have 50
and 100. this means if I show the toast we have a
hundred pixels from the top and 50 pixels from the right that covers everything there has to know about toast
if you want to read up on it you can look at the documentation you can find this here you want to look at the toast
module and this has a couple more arguments
as opposed to one I didn't cover is the alert this one plays a sound if you are playing it by default it is false and I
think that's a better way to go on about it but if you want your program to be annoying do play a sound
ready next up we can create a tool tip this is going
to be a very simple message that shows up once we hover over a certain element like a button for example in fact let's
create a button right away with ttk and button the master here is going to be
window for the text I want to have tool tip button to make this a bit more fancy
I want to set a boot style let's call it warning this button I want
to pack right away if I run the app now we have a yellowish orange-ish button I
think the entire thing starts to be a bit crammed so I'm going to add a bit of vertical padding
pad Y is going to be 10 for both of the buttons running this now this is looking a
little bit better this button I now want to have a tooltip once we hover over it for that we need
one more widget this we get from the top as before we need from ttk bootstrap
although now we need tool tip and we want to import dual tip
this is going to give us the widget also I'm going to minimize a couple of things here so the entire thing is a bit
easier to read all we have to do for the tool tip is we have to create an object from the class so call the class itself
in here we have to set a master and the master is going to be the element that we want to have the tooltip attached to
in my case that is this button here so the master is the button then we need
a certain kind of text it doesn't really matter what it is let's say this does something
if I run this now I can hover over the button and we get this does something
if I go away from it it disappears right now this doesn't look too great but we can style it using boot style for
example what you could be doing is use light in here now we have some other kind of color I think
using danger here might be a bit better let's try this one
yeah it kind of works now the boot style for tooltip has one specific thing and
that is called inverse if you attach that one and hover over it now you get the colors inverted if we didn't use
this we had red text and I think a black background with the inverse we get white text and a red background
inverse is the only styling you can use though you couldn't use outline this one doesn't exist if I use it we're getting
an error but I think inverse works really well here there are three more widgets that we have to cover the next
one is a calendar this is going to be another widget we have to import in a custom kind of way
like the ones we have used here although for this one we need from ttkbootstrap.widgets
from this one we want to import date entry this date entry I want to create and
store in a variable right away let's call the variable calendar the value is
going to be date entry this one doesn't need any arguments besides the master
after I have that I want to pack it right away with some vertical padding pad y let's
go with 10. if I run this we now have a calendar that shows the current date if I click
on the calendar I can even select other kinds of dates I can go further wherever I want and if
I click on the date we get to the current date if I select one we get the new date here and we can extract this one quite easily
as well to do that let me create a button I want
ttk dot button the window is going to be the parent
text is going to be get calendar date
the command is going to be some kind of command to print the current date this could be a function but in my case I'm
going to add all of this into a Lambda function what I want to do is I want to print the
calendar inside of this we have an entry widget this we have to Target and on
this one we can use the get method the calendar is basically a compound widget
the compound here is an entry widget and a frame with a bit of content all we really care about is the entry itself
once we have that I can simply pack the button run this entire thing and now if I
select a certain kind of date let's say the 1st of December 2022 I can get the
calendar date and we get the 1st of December 2022. I suppose one thing to be
aware of here the calendar has the date first then the month and then the year if you are American and you're doing the
calendar wrong just be aware of that the month is the middle part not the first bit that covers the calendar next up we
can create a progress bar although in TDK bootstrap this is called
a flat gauge once again we have to import this one this module lives inside
of the widgets besides the date entry I want to import the flood gauge
once I have that I can use it I want to store all of this inside of a variable that I call progress and here we need
ttk and blood gauge first of all we need a master which is going to be the window
besides that we can also set a text in here I will call this one progress so
that we have something after that I want to pack this progress with some vertical
padding there you can see we can see something but this doesn't look too great yet
what you want to be aware of for this flood gauge is that it needs a lot of horizontal space
in my case I want to fill the X and there we go now we can see this
progress properly although right now all we can see is a plain background to make
it actually work we need a tkinter variable let me create this one at the top I want to have I'm going to call
this a progress integer this is going to be a TK end
VAR with a default value of 50. this value we now have to attach to the
progress which we can do by setting a variable progress integer if I run this
now there you can see we have some proper progress bar if you update this
integer the value in here is also going to update for example what you could be
doing is to create another slider with ttk and scale the parent is going to be
window we want to go from 0 to 100 with the variable of progress
integer I want to pack this one right away if I run this now I can use this
slider to update the progress bar which is working pretty well
this flat gauge also accepts a few more arguments I will put all of the arguments over
multiple lines so this is a bit easier to read one obvious argument we can use here is boot style
this could for example be info now we get a different kind of color well not
that different we could also use danger now it's red other than that the really interesting
argument in here is called a mask this one is overwriting the text by
default let me call this one mask for now if I run this now we can see mask so
this isn't too useful however what you can do if you add curly braces in here
ttk bootstrap is going to add the variable number in here right away which
means if I run this now we get mask 50 and if I play around with the slider we
get numbers here updated right away which means I could for example add a
percentage sign afterwards and this makes it very easy to get a percentage as well as a visual
indicator in terms of where you are on the progress those are the main arguments obviously you can read up on
it on the documentation I haven't opened this one let's do it right away inside of the documentation you want to look at
the widgets module in here we have Floodgate if I open this one you can see a nice
preview and if you go a bit further down you can see all of the arguments you
could be using there are quite a few actually we are very nearly done there's only one
more widget that I really want to cover and that is the meter this one looks like this in here we have lots of different things
that we could be using all of these arguments
this is going to be your exercise what I want you guys to do is to figure this
widget out yourself in my case I have a meteor that's something like this it's a red color we have a full circle and we
can see the numbers straight away try to read through this page and see if you can implement this one yourself
back in the code the first thing that we have to do is to import the widget since it happens inside of the widgets
from here I want to import meter now that we can use it all the way at the
bottom I want to add a meter I'm going to store it inside of a meter variable and we create it with ttk and
meter since we are going to use quite a few arguments I'm going to start over multiple lines right away the first
argument as always is the master which is going to be the window but now this is all we need so I'm gonna
pick this thing run this and there we go we have a meter that right now doesn't
do anything to actually use it we have to first of all create an amount total
I want this to be a hundred this is the maximum value after that we want to have amount used this is the starting value
and the minimum is always zero let's say for this one amount used should be 10.
running this now we can see we already have a basic start that being said if I'm trying to click
on it nothing is going to happen to make something happen we have to set interactive to true
now I can click on it and move this thing around other than that you have lots of
different arguments you could be using for example we have the meter type this
could be either full that I believe is the default alternatively you can use semi with that
you get a semi-circle that otherwise still works the same you can also customize the text or add a subtext
let's go with some other text now we get some other text although the
functionality doesn't change you can also set the boot style this works with literally every widget I used danger for
this one this is giving us a red color these are the basic arguments I think you want to use most of the time
although there are quite a few more you could for example set the stripe thickness you could show the text or not
show the text you could set the media thickness and lots of other things you can work with you have a ton of options
in here and well with that we have covered quite a bit of stuff and this video is getting a bit long so let's
finish it here a really important part of good looking user interfaces are animated widgets so what we're going to
make is this app here inside of that I have a button if I click on it we have an
animated sidebar this has a button and it has a text field where I can write
over multiple lines if I write too many lines we get a scroll bar all of this is quite easily implemented
on top of that we can also do all of this in light mode we have the same sidebar although now it's looking a bit
brighter but with the same functionality so let's cover some Theory first
into Kinder you can create animated widgets but you do not have pre-built
components for it as a consequence you have to make your own systems for that you need two major Concepts the first
one is the after method this one allows you to call a function after a certain amount of time
this you combine either with the layout methods or with configure those can update the position the size the text
the color of any widget should go into a bit more detail widgets can be updated in real time
using either configure or the layout methods for example if you're calling a layout method
multiple times the current one overwrites the previous one if we are calling button Place once with X being
10 and Y being 50 and then call it again with 210 only the second one will be
displayed the previous one will simply be removed that way you can update the position and the size of a widget in
real time on top of that you can use configure to update the text the font the colors and all the stuff you can
update inside of configure I'm gonna play around with this in just a second but there's one more thing I do want to
talk about and that is when you're animating widgets you want to use place at least when it comes to the layouts
for the simple reason that only plays can give you pixel by pixel positions imagine using the grid method for
animations inside of the grid you can only specify the current cell we are working in you couldn't move a widget by
one pixel to the right only place can do that so we have to use it for animations that being said you
could totally use grid for animations it just wouldn't look good this gives us a couple of Concepts I want to practice
already I am using custom tikenter to make all of this look good but all of this would also work with the normal ttk
apps after that I'm creating a window and I have one button the one notable
thing about this button is that for the X position which we are placing with the place method we are storing the position
inside of a variable and this we're passing in here we're going to work with this position in just a second finally
we are calling window.main Loop to run the entire app which means if I'm doing that we have a window with one button
that doesn't do anything right now to influence it I need to run some kind of function which I'm doing when the button
is pressed let's call the function move button this function we have to create
move BTN there are no need for parameters and in here we we can use the
place method or the configure on the button to update the button itself let's
start with the place method itself because I want to move the button to the right every time we are pressing it since I want to use button X for that I
need to be able to influence this variable in my case I'm going to set it as a global variable using the global
keyword once I have that I want to Simply increase button X by let's say
0.05 every single time we're pressing the button to make sure that this is working let's print button X as soon as
we are pressing the button now if I'm pressing the button we get 0.05 0.06
some weird stuff with floating Point numbers but that isn't going to make a difference this number we can now use inside of the
place method let me actually copy it I want to place the button one more time with this button X
the difference now compared to the original is that button X becomes larger every single time
let's try it now if I click on toggle sidebar it always moves a tiny bit
further to the right the numbers are quite large and we only move when we are clicking but this is
the first step to understand animations besides relative X and relative y you
could also work with relative height let's say I guess we can use button X in here again
if I run this now every time I'm clicking the button gets a tiny bit larger I think I should set button X for the
starting height as well I wonder if real height is going to be
button X now if I run this we start with a much larger button and every time I click the button gets larger it moves to
the right you could also just use X and Y here that would be perfectly fine all of the
animations work either with absolute or with relative numbers that would cover the layout methods besides that we can
also use config or rubber configure for example what we could be doing is declare a couple of random colors let's
say red yellow pink and green every time
we are clicking on the button I want to give the widget a new color for that I need some Randomness which means from
random import choice every time I'm clicking the button I
want to get a color let's call it color and the value is going to be choice of colors that way let me print it really
quick I want to have my color and I click on the button we get one of
the colors okay we just got really unlucky in the beginning I'm going to add a few more colors in
here so we have a bit more variety like so now for runders we get much more
randomness that we can use to configure the button for example we could run button dot configure the argument in
here since we're using custom tkinter would be FG color to get the actual
button color and this I want to set to the color if I run this thing again and now if I click on the button and move
away from it we can see we get different colors after every single click
if you were using normal tkinter this FG color wouldn't work you would need to use the default styling options which
are quite limited which is why I'm using custom tkinter it makes all of this much easier but
well with that we can update a widget in real time what we now have to figure out
is how to make tikinta do all of the work for the animation for us for that we have to learn One More Concept that
concept is after and after can call a function after a certain amount of time
this one would look like this it always has to be part of the window we specify
two arguments the amount of time and then the function we want to call the amount of time here is in milliseconds
since 1 000 milliseconds are one second this number here would be one second what is really important is that this
can be circular a function that is called with after can contain after itself
in this case we could have a function like this after one second we are calling this
function here then we are printing test and then we are running the function again as a consequence this function
will run forever let's play around with this one actually I want to create another function I will call this one
infinite print it doesn't need any parameters in here I simply want to
print I suppose infinite is appropriate in here this I want to start whenever we are
pressing on the button meaning if I run this now the button only prints infinite but what we can do
now is run window after then we need the time and the
function we want to call let's say after one second so 1000 milliseconds I want
to run infinite print again if it runs now I can click on toggle
sidebar we get infinite once and after one second we get it again and again and again and again this is never going to
stop for animations one second is quite long but you could set this to even one
millisecond now if I click on it we get a whole bunch of infinites I suppose 100 milliseconds is a good
middle ground here while we are doing this infinitely right now you could also control this for example with an if
statement to keep on using button X we could check if button X is smaller than 10 and
only then run this to make that work we have to update button X for that I want to set button X
as a global variable again and then increase it by a certain amount button X Plus equal
let's say 0.5 only if the if statement now is the case I want to print infinite
and to make sure that we see what's going on I also want to print button X
let's run this one now if I click on the button we get infinite but only up to 9.5 then
the thing stops with that all we have to do is combine this function with this
function to get an animated button which is bringing us to one exercise already I
want you guys to animate a button so that it moves to the right side of the window after we are pressing it if you
combine this function and this function this should be fairly easy to do pause the video now and see if we can figure
this one out first of all I want to work inside of
this function here for that when I'm pressing the button I want to call the move button function on top of that I
don't want to change the height of the button meaning I'm just going to remove the relative height both inside of the function and when I'm creating the
button in the first place that way we're only focusing on one bit at a time with that we can actually
counter the animation inside of the move button for now I am declaring a global
button X I am increasing button exit and then I'm calling button.place so if I
run this we are moving the button a tiny bit to the side and we're also changing the color I guess we should remove this
one because that would be quite confusing the issue we have right now is after
we're clicking the button nothing happens but instead what we want to do is call this function one more time
or well not just one more time but until we are reaching the right side of the window for that I want to use the after
method I want to run window and then after I want to get an update every 100
milliseconds and I want to call move button with that I can run this thing
and we get some kind of Animation it's really choppy right now and it doesn't stop the choppiness we can fix very
easily all we have to do is reduce this number and this number I only want to
update the position by 0.01 units and I want to update this thing every 10 milliseconds if I run this now
this is a much smoother animation to control it a little bit better what we
can do is use an if statement that if button.x let's say is smaller than 0.9
only if that is the case I want to call the after method if I run this now
the button is going to move we have to wait a tiny bit at some point it should stop there we go now it's stopping on
the right side of the window this isn't perfect but I think for now it's good enough so that covers basic animations
obviously this doesn't look very good so let's make a good looking animated widget what I want to create is some
kind of slide panel I want to create something like this where we can click on a button and then we have a side
panel this doesn't have to be on the right it could also be on the left it's quite flexible this first of all has to
inherit from ctk and frame I forgot this cdk at the beginning that way we are
simply creating a frame when I'm calling the Thunder init method we now need a
couple of arguments the obvious one is self and we need a parent other than that we need a start position and an end
position the animation will then move between these two once we have that as
always we need the super init method and we have to set the master to the parent
I forgot the brackets here after that I want to create some general attributes
basically what that means I want to store the start position as the start position as an attribute the same I want
to do for the end position end position like so other than that I need the width of this thing self.wift the width I want
to generate automatically this is going to be the window I want the widget to
start here at position 0.0 for the simple reason that by
default the side panel should be on this side if however the user clicks the
button I want this thing to slide to left let's say to position 0.3 the demos you have seen was the
panel moving to the right but in this case I want to move to the left this thing is flexible though both would work
just fine with the same widget but first of all we need to generate the width and the width we get from this distance here
that number we get with the start position minus the end position and all
of this and needs to be absolute the reason why this needs to be absolute let
me print the with self.wift and create a widget this by
the way needs to happen before we create a button animated widget
I want to create an animated panel which is going to be the slide panel
for this one the master is going to be the window the start position is going to be zero and the end position is going
to be 0.3 although this one has to be negative running this now we get an
error because I am incapable of typing this should be an uppercase t now if we
run this we get 0.3 this is a proper width but if we didn't use absolute
numbers in here we would still get 0.3 but if we used other numbers this might
be a negative number for example if I want to start my widget on 0.7 so somewhere on the right side
and then move it to one then we will get a negative number since this would create a negative width
we would get some weird results as a consequence always use absolute values
in here also spell them correctly that tends to help with that we get positive numbers the
floating Point weirdness here you can just ignore it's not going to make a difference so with that we have a proper width
which means we can actually place the thing I'm going to use self.place let me
add a comment here as well I want to get relative X that would be self dot start
position relative y would be zero then we have
the relative width that would be self dot with and
finally I want to have relative height which for now would be one now if I run
this we have a sidebar all the way on the right it's kind of hard to see right now but
it is the brighter stuff here all of this to make sure that this is a bit more visible I want to set an F G color
to let's go with red now if I run this this is much more visible on top of that to move the panel to the left side I
want to change these numbers back to zero and negative 0.3 that way now the panel starts on the
left because the start position is zero so this self-estar position is zero with
that we need a few more things all of these numbers are for the animation itself so animation logic
first of all we have to track the position Itself by default this will be
the start position this will become important in just a bit besides that I want to toggle self dot in start
position by default this should be true this is going to be a switch and it is
going to track if our budget is in stock position or not in the start position if it is in a stock position we want to
move towards the end position if it is not in a stop position we want to move towards the start position
which basically means this thing is going to determine the direction we can use this right away actually
because I want to create another method that I call animate with itself and nothing else in here and
all I want to do is if self dot in start position then I want to self dot animate
or Ward if that is not the case meaning else I
want to run self Dot and made backwards these two methods are what
actually creates the animation so let's start with animate forward Define animate forward what I want to do
in here is first of all I need an if statement if self dot position is
greater than self dot end position I should probably draw while doing all
of this this one here would be our window a bit squashed a start position right now is this point zero
this would be our start position or rather this one here besides that we
have the end position the end position right now is somewhere here negative 0.3
that is a horrible three that's looking better finally we have a position this position
here at the start this is on the start position meaning it's here this position
I'm going to move a tiny bit further to the left every time we are calling animate forward
however I am only going to do that until we reach negative 0.3 for that we have
this if statement here we are only going to move the position to the left until we are reaching the end position
if that is the case though I want to update self.position and reduce it by
0.008 the number here is very subjective it basically determines the animation
speed just choose whatever you think looks good once we have that we can run self dot
place again let me copy the numbers actually from up here because we can reuse quite a bit
for the X position we now don't need start position we just want the position
relative y relative width and relative 5 can stay identical finally what we are going to need is
self dot after I want to run another function after 10
milliseconds the function I want to run is self dot animate forward with that we
should already have something let me run the entire thing again and now if I click on toggle sidebar
we are moving the button to the right and that is because the button still
gets the move button function this I want to change I want to get my animated panel in here I want to run a method the
method I want to run is this animate which means animated panel dot animate
now let's try this again if I now click on toggle sidebar this thing is moving to the left
although if I click on it again nothing is going to happen and to make it a bit easier to see what's going on let me update these
numbers here let's say to 0.3 and 0.1
now if I run this again this thing is much more in the middle and if I move it to the left now it only moves up to 0.1
I hope you can follow logic here I am going to stick with the original numbers like so and now we can keep on working
on this first of all once we are reaching this position which means an else statement
will be triggered I want to set self dot in start position
to false that way once we're clicking on the button again we would run animate
backwards this we now have to create Define animate backwards this one also doesn't
need any parameters besides self and now we have to do basically the same thing
we have done here as a consequence I can just copy the entire code and paste it in here and make some updates
first of all self dot position we only want to run if the number is smaller
than self.n position actually this should be this start position
the reason for that let me draw all of this actually again we have the window one more time and
again we have to start position at zero and the end position at negative 0.3
right now the position when we are calling this method here is going to be
on negative 0.3 and we want to move it a bit further to the right every time we
are calling the method however we only want to call it until we reach the starting position this line here
that is covered with this if statement if that is the case I want to increase
the start position by the same amount you could use a different number in here but you probably don't want to
after that you're calling Place although after now is animate backwards instead
of forwards finally if that is not the case anymore in start position should be true again
with that we should have a basic animation if I now run this I can toggle this and we have an animated sidebar
that's looking pretty good although right now it doesn't look very good let me run it again all we get is a
red frame that we can move but it doesn't have any content and well generally I want to make this thing look
a bit better first of all I want to have a gap between the frame itself and between the
surrounding this I do with relative Y and relative height for example I could set the relative height to 0.5
0.05 and then the relative height is going to be 0.9 running this now we get a gap
between the top and the bottom while the frame itself is still in the middle besides that for the start position we
can increase this by a tiny amount let's say 0.1 now if I run this again we have
that's quite a large gap let's go with 0.05 it's looking a bit better
the toggling itself still works although we have to make a few more updates here the problem if I run this again once I
click on toggle sidebar we are covering the entire height so this we can change
already I want to copy all of these numbers here and now when I'm calling place in here and in here so animate
forward animate backwards I want to have these updated numbers that way it's looking a bit better
although there's a small jump in the beginning and that is because of this we
are setting the position to zero because we're in start position from the parameters but not from the updated
value here we can fix that by setting self.start position and now this is much smoother
that being said I think this is a tiny bit large let's go 0.04 that's looking a
bit better once again you can play around with these numbers it's entirely up to you they're quite subjective what
is much more important though I don't want to have a red background color instead I want to minimize the side
panel and work with the animated panel what is really important to understand now is that this side panel is simply a
frame which means we can place any other widget inside of it and it would still work the same for example I could create
a ctk and ctk label with the parent being the animated panel
after that I can set some text let's call it label one
like so and this I want to pack right away although any other layout method would
also work just fine I want to set expand to True fill to
both and on top of that I want to add a bit of pad X
let's go with 2 and Pad y with 10.
if I run this now we have label 1 covering the entire frame the rest still
works just fine I can do this again and change it to label 2.
run this again and now we have two labels in here the same thing would also work with another widget let's say with
a button I simply call this one button if I run this now we have a button all the way at
the bottom although the padding here looks a bit weird especially X padding
doesn't work particularly well in here but why padding I think still works just fine yeah that looks okay
on top of that for this button I want to remove the corner radius so I'm going to
set it to zero now this is looking much better finally One widget that we can
use that I don't think I have used yet is called ctk and then ctk text box
this is a text box with the parent being the animated panel and this I want to
pack as well with expand being true and fill being both
now if I run this we have a text box that we can type in although the
background color here doesn't really fit to update that we have to set inside of
the widget the FG color the colors here should cover both the
light mode and the dark mode the colors we need are this now if I run
this we have no more background color so this is looking much better
although this might be very hard to see and it's a tiny detail but in the bottom
left we have a sharp corner like this whereas in the top left we have a round
corner this happens because now this text box has sharp corners and is
overshadowing the frame unfortunately we cannot cut this off but what we can do is set vertical padding
so pad Y and set it to 10. now we have a rounded Corner because the text box
widget only reaches to this point here we have a text box that works over
multiple lines it's looking pretty good we can still use it just fine
we're making a lot of progress on top of that since we have two different colors we could also update the theme so what I
could be doing is ctk and then set appearance mode to light
and I can run it again and we still have the same outcome with colors that look consistent
the animation once again still works just fine although I do prefer the dark mode but choose whatever you like
with that we are nearly done yes one more thing that we have to do and that
is to make this slide panel a tiny bit more flexible so if I run this again I can click on
the button and all of this works just fine however I want a system to work a tiny
bit different what I want to have is that by default this panel here is all
the way on the right and not visible to the user only once we click toggle sidebar then it should be on the right
side like so this by the way if I run the demo again
this is what I want to have at the End by default I can't see anything on the right only if I click on toggle sidebar
we get the cipher window and then I can remove it again so by default it shouldn't be visible
for that we have to make a few updates although none are too difficult as a consequence we can add a second
exercise what I want you guys to do is to update
the panel so it moves in from the right
you would have to figure out a couple of things but pause the video now and see if we can figure this one out
first of all I want to update the positions my start position should be
1.0 so the app is invisible and the end position should be 0.7 if I run the app
now we can't see anything because the actual frame now is roughly here
what is even better if I click on the button this still works just fine which is a really nice start which means
now we can work a bit more inside of the button to fix some minor things
first of all when I'm running this thing you can see on the right side we are
losing the Gap this one is very very narrow to account for that for the end position
I also want to add let's say 0.04 now if I run this again we have the Gap
back although again it's a bit large let's make this smaller say 0.03
that I think looks better once again these numbers are fairly subjective just choose whatever you like
we have a pretty good app this is working just fine I guess the one thing
you want to be aware of here is that the starting position always has to be to
the right of the end position because in our case animate forward
reduces the amount and animate backwards increases the amount which means forward
in our case is always left and backwards is always going to the right although
this video is already getting quite long so this you can Implement yourself it shouldn't be too hard another really
important part for good looking user interfaces are images in tick interim you can add images to
some widgets labels buttons and canvas is what you're going to use most of the time
that being said for images that scale properly you will need to create a logic yourself so the scaling logic doesn't
come with tkinder that is something you have to make yourself on that note what I have mentioned yet what we're going to
create is going to be this one here we have two buttons one with TDK and one
with custom tkinter and then we have a raccoon and this raccoon we can't scale and it's always going to cover the
appropriate area this kind of logic you have to make yourself it doesn't work by default now
before we can do all of this we have to do one more thing and that is we always need a pillow library to use images
pillow is the default python image Library this one you have to install on your own
first of all this you do either of the Powershell or The Terminal in my case this is the Powershell what you have to
type is PIP install hello this is going to install quite a few
things obviously if you're on a Mac and using terminal this would be pip free install hello
once you have that we can start working on some code for the starting setup I am importing tkinter and ttk on top of that
I am importing custom tkinter we are going to use both because they have slightly different setups for importing
images after that we're creating the basic tkinter window and then we are running the main Loop the end result is going to
be a basic window before we can start properly we have to do one more thing and that is we want from p-i-l import
image and image TK pil is the pillow we
just installed for some reason the input here is a different name compared to the import in
the Powershell or The Terminal pil stands for python image library and some
are for a PQ to call it pillow I don't understand it either it's quite weird but this is how you would import it
inside of pillow you have one really important object and that is called image you basically always use that one
and image has a custom teak and a variant that is called image TK on that note I have made a really long tutorial
on pillow itself it's on YouTube you can watch it for free you can use pillow for all sorts of
things like scaling images changing colors adding text and well lots of other things so check it out if you are
interested although for this video I just want to import an image
to make that work first of all I need to cover our folder structure right now I have one folder and this
folder contains the code the code file here is called images in this folder I have three more images I have python
dark hyphen Lite and raccoon those are the images I want to import for the import first of all we need to
import the image itself so image let's call it origin nil
this we get with image dot o pen and now we need to file path
since I want to import let's start with the raccoon I want to import raccoon and
the file ending here is jpeg with that we have an image so I can run the code we're not getting an error that's
looking pretty good now I have to figure out how to get this image on a widget
for that first of all we need a widget to get started I just want to create a
label and this can be ttk label the parent is going to be window
the text could be let's go with raccoon and let's pack the label
there we go we have raccoon a label can also take an image
although what we cannot do is simply pass in the original image in there we will get an error that the image
specification must contain an odd number of elements I don't know what that specifically means but basically what
tkinder wants is a image TK not an image we can account for that quite easily I
want to store this in another variable I'll call it image TK this image Decay we create with image TK dot photo image
you only need one argument that is the image original with that we can pass an
image Decay into the image and it should be working there we go the problem we have right
now is that the image is way way too large for reference the raccoon has a size of
six thousand by four thousand while our window is only 600 by 400 so we can only
see a very small part of this window right now but we can resize the image
this we do when we are importing the image this image here is returning an image object this image object has a
couple of methods the one we care about right now is called resize resize wants
a tuple with a new size and a new width let's say for now I want to cover the entire window with the image
this will be 600 by 400. with that we have the raccoon covering the entire
image although if I resize the window this breaks quite fast
but at the very least we do have a start unfortunately though you basically never
want to use an image inside of a label for the simple reason that you cannot resize the image if the window changes
you always have the same image size depending on what you get from here to change that you need quite a bit more
logic so I am going to cover that later on let me get rid of the resize and comment out the label
running this again we have a plain window but we do have an imported image before I expand the logic on how to use
images I want to cover buttons because buttons are very easily usable with images
let's say I want to create a button this is going to be ttk dot button the parent
here is going to be the window and for text we can go with a button
this button I want to pack right away now we have a button
this button can also accept an image I could add imhdk now we have the raccoon
again but remember the raccoon is way too large but the raccoon is not what I want to add to this button instead I
want to import a different image that image is going to be python dark which
we get with image dot open the name of the file is called python underscore
dark dot PNG important here we have a different file ending because python dark has Alpha
values so we need a PNG this once again we have to convert let me call it python
dark TK for that we need all of this I can
simply copy it like so and paste in Python dark this
python dark TK I now want to use for the button like so and this is still way too large although
I guess a little bit better since the button isn't going to change size for this one it is fine to Simply resize the
button here and then you don't have to worry about it anymore in my case I want to resize the button to a size of let's
go with 30 by 30. now we have a button with a python logo to see the text again
we need a compound argument if I for example set right here we now have a
button and then the logo to the right this can also be left
and then we have the image to the left of the button for a bit more spacing you could do a tiny bit of a hack here and
simply add some spaces for the button and now we get a bit more spacing between the two however if I duplicate
all of this and change the button to let me call it a button ctk because I want
to create ctk dot ctk button for that one we are getting an error that photo
image object has no attribute create scaled photo image once again I'm not quite sure what that means but the
concept you have to understand is that you couldn't use an image TK this one here inside of a ctk widget instead what
you would need to do is create a separate ctk image if you get with ctk and ctk image
this is what you have to pass into is ctk widget if you want to have images I'm going to store this one in an image
ctke variable the reason why this is different is because for custom tick
enter we always need a light image and we need a dark image
those we have to import separately but other than that we are using it the same way
how you usually want to do this let me put it over multiple lines actually what you can do with the input here is simply
use image open as the argument for example I could paste image open
python dark in here and then for the Dark theme I want to have python light
this might look confusing here basically you want a dark image for the light
theme and the light image for the Dark theme for the simple reason that light image has a light background so you want
to have a dark image and then the other way around it's going to work the same with that we have an image cdk and this
is what you want to pass into this image now I can run this and there we go we have a python logo for a button that is
bright right now if you were using custom tikkinder and had a light and a dark theme this would also cover the
Dark theme although since I am using tkinter by itself this isn't really applicable but it would definitely work
with that we can actually cover how to use tkinter with images the major problem that you have in tkin
type of images is that images do not scale by default we could have as large
or a small of a window or any kind of container the image unless you add some custom code is not going to update which
would break any kind of layout really fast to account for that we have to add an image to a canvas and then use the
canvas Dimension to update the size of the image that we can do in real time although we have to figure out a few
Mappy things in here it's not going to be too bad although once we have that we can add an image to a container and
always make the image scale to that container and before I start I want to create a different kind of layout I want
to have a grid where those two buttons are on the left and then on the right we have the actual image
for that I'm going to put it up here I want to create a grid layout I want to
get window dot column configure
in here I want to have 0 1 2 3 in total four columns that all have a weight of
one and I want them to be uniform like so so uniform is equal to a besides
that I only want to have one row so row is just going to be zero uniform we can
just ignore for that the image Imports can stay the same although for the buttons we have to update them because
we're using pack but now we have a grid as a consequence I want to put both buttons inside of a frame
I'm going to call this button frame and this is ttk dot frame
with the window as the parent both of the buttons are going to be
mastered to this button frame finally I want to place the button frame using the
grid method I want column to be zero
I want the row to be 0 and then I want to have sticky with north south east and
west if I run this again now there we go we have the two buttons all the way in the top left I think to make this look a
tiny bit nicer we can give both a bit of vertical padding let's say 10 pixels now there's a bit of space between the two
with that I can create the canvas for the image
this is simply going to be a canvas so TK dot canvas
the parent is going to be the window and for now this is all we are going to need
this canvas I want to place right away canvas dot grid this is going to be column one
column span is going to be free we are covering all of the remaining columns finally row
is going to be zero also I want this to be sticky to all four sites if I run
this now we can't see anything because we don't have a background color which I can change quite easily background let's
set it to red and there we go now we can see the canvas itself however the canvas
doesn't cover everything perfectly for example at the bottom here we have this very thin line
same on the right side and we would have the same on this side and this side as well this we have because of the border
of the canvas we can get rid of it though all we have to do is set BD to
zero then we need High light thickness
and set this to zero as well finally the relief should be rich with these numbers
the canvas is now going to cover the entire area and we have no border also let me set this to Black so it looks a
bit better there we go on this canvas we can now add an image this we do with canvas dot create image for the
arguments here we need an X and the Y position I'm going to set it to 0 and 0 which is the top left and then we need
an image this needs to be a TK image which in my case for the raccoon I have
image TK image Decay now if I run this we can see one eye of the raccoon
what we could also do in here is set the anchor by default we are placing the center anchor like this but I want to
place the North West now we can see a top part of the image again but it doesn't do very much the way you have to
think about it is that the entire image starts here and then goes really really
wide to the right and to the bottom I believe the numbers were six by four
thousand so much larger than our window to account for that we have to
dynamically resize the image I don't want to create the image right away instead I want to do all of this
inside of a function this function I'm going to trigger every time we are changing the size of the window this we
get with canvas dot bind in here we need
on figure this is going to trigger every time the size of the canvas changes if that
changes I want to run a function this simplest for the image is stretch image
you're going to see in a second what this one is going to do but let me create it first of all all the way at the top
I want to create stretch image in here since we are working with an
event we need one default argument and that is the event what we are going to do in here is we are going to get the
size of the canvas and then we are going to scale the image to that size finally
then we can actually place the image for that though first of all we need to get the windows size or more specifically
let me call it size we want to get the width and we want to get the height
the width is going to be event dot with and the height is going to be event dot
height if I print both of those numbers we have with and we have height
now if I run this we are calling this function and if I resize the image we get updated numbers so this is working
quite well just to make sure now the thing is really narrow and very very small but now it's much larger so the
numbers seem to be pretty accurate these numbers we can now use to create
an image although what is really important you already want to have one
image imported and you only resize it when you resize the entire window you do not want to re-import the image every
single time you are resizing the window that would be really inefficient in my case though I already have one
image imported this is what I want to work with I want to store all of this inside of a new variable I'm going to call this
resized image we need the image original and
then resize it since resize wants to have a tuple with a width and a height this is quite easy because we already
have width and height although this is still just an image but we need an image
TK we need another variable that we call it resized TK this is going to be image
PK dot photo image the same thing I have done down here except now the one
argument is going to be the resized image finally this we can place on the canvas
for that all we need is canvas dot create image the start position here is
going to be 0 and 0 the image I want to place is resized EK finally the anchor
is going to be North West now if I run this we only get a black background color so
something didn't go well the problem is that the image TK this line here always has to be in the same
scope as the main Loop or wherever you call it in our case an easy fix here would be to
set resize TK as a global variable resized TK and now we can see the
raccoon so just to reiterate we have our window in the global scope and we're also
calling window.main Loop in the global scope because of that the image Decay needs to be in the global scope as well
they always have to be in the same and once again I have no idea why but with that we have the image of a raccoon and
if I resize the window the raccoon resizes with it because we are updating the size of the window every single time
we're updating the canvas which is working but you can see a limitation here we are stretching the
raccoon quite a bit to account for that I want to create a second function I'm going to call this
one fill image this one is not going to resize the image instead we are going to fill the
entire image and we're going to cut off parts of the image that don't fit what we are going to do for this one let me
explain it first before I create a function let's say this one here is the canvas and the image might be as large
as this bit here inside of this function if the image is
larger than the canvas we're going to cut off this bit and this bit
that way the raccoon is going to keep the same aspect ratio later on we will create a third function that will keep
the raccoon always inside of the canvas but for now let's fill the entire canvas for that once again the one parameter I
need is the event I want to have Global resized PK
now in here we first of all need to get the current ratio of the event
or off the canvas the same thing this we get I want to store it in a variable canvas
ratio all we need here is event dot with divided by event dot height this number
is really important and we need it both for the canvas and we need it for the image we have imported this image here
this we can also get quite easily I want to store it in a variable let me call it image ratio to get the width and the
height we need image original dot size this is returning a tuple with the width
and the height which means the width is going to be zero and this I want to divide
by the height so size 1. if I print all of this
image ratio this one we get 1.5 that number we get if I open
the folder again the raccoon has a size of 6000 by 4000 pixels
dividing six thousand by four thousand gets us 1.5 this number is really
important because it tells us how we are going to scale the image itself for some context
here let me do all of this actually on a separate surface imagine we have a perfect square where all sides are one
if that was the case and we would divide the width by the height we would get one
this is telling us that we have a perfect square if we have some kind of rectangle with a width of Two and a
height of one in that case we would divide two by one which would give us
two which tells us that the larger that this number gets the wider the entire thing
is by the same logic if we have a really narrow container something like this
where we have a height of 1 and a width of 0.5
that is a horrible five 0.5 then we would do 0.5 divided by 1 which would be
0.5 which means the smaller this ratio becomes the more narrow our container is
going to be this applies both to the canvas and to the image itself this information we can use so in our
case we know the ratio of the image and of the canvas what we want to do imagine this one here
is the canvas or C in short this we want to compare with the image itself or the
aspect ratio of the image let's say this could be something like this this would be I for image if the canvas has an
aspect ratio of let's say 1.8 with the image having aspect ratio
of 1.5 we know that the canvas is wider than the image if that is the case I
want to scale the width of the image to the width of the canvas
which right now would simply stretch out the image so this wouldn't be
particularly useful however since I know the aspect ratio of the image I can simply use the weft and
then combine it with the aspect ratio to get a new height of this image even if I
resize the entire canvas I would fill the entire width and then the top and
the bottom part of the raccoon so the parts that are outside of the image are simply going to be cut off
I hope all of this makes sense the math here isn't particularly difficult but you have to get your head around it I
think if I Implement all of this this is going to make a bit more sense what I really want to figure out is I want to
get the coordinates of my image which means ultimately I want to get a
whiff for the image and I want to get the height of the image although for these images first of all I want to know
if the canvas ratio is greater than the image ratio
if that is the case we know that the canvas is wider than the image
if that is the case I want the width of the image to be the event with that way
we are filling the entire width of the canvas there's one thing that t can do is a bit
fussy here and that is that we always need to have integers a very easy thing to account for once we
have that width let's say for some imaginary numbers the width of the canvas could be 800. on top of that we
know that the image ratio is 1.5 these two numbers we can now use to
calculate the new height of the image all we have to do for that is rearrange this formula here initially we got the
canvas ratio but now we want to have the height this height here this we get by
getting event dot with or the width of the image itself this width here and
then divided by the image ratio this also needs to be
an integer let me remove the white space this information we can now use because with
that we can create a resized image which is going to be the image original and
then I want to resize it with the with and the height after that
we can create a resized TK which is just going to be image TK dot photo image
with the resized image finally there's one more thing we have to cover we still want to get canvas and create image
although now for the X and the Y position we want to place the image
right in the middle of the canvas all we really have to do is get event dot width
that is the width of the canvas and divide it by two decanter or the canvas more specifically wants to have an
integer this we can do again for the Y position I simply want to divide the height of
the canvas by two finally besides that I'm going to set an anchor the anchor is
going to be the center once we have all of that ideally over multiple lines so it's easier to read we can place the
image itself the image is going to be resized TK
now if I run this we can see the raccoon and the raccoon scales with the canvas
because I forgot to actually call fill image whenever we are resizing all of
this now if I run off this again we are getting an error because by
default this if statement here is not true to account for that
let me change it to else with with being one and height being one as well so we
get at least something with that we can't see anything however if I make this less tall there we go we
can now see the raccoon at least on a certain aspect ratios but if I make this smaller at some point it disappears that
happens because this if condition doesn't apply anymore because in the
else statement the canvas is narrower than the image
this is what we have to account for as well for that let me copy the width and the height now I need these numbers here
for this one we now want to have the image covered the entire height of the canvas which means the height is simply
going to be the event dot height for the weft I want to get the
height once again and multiply this with the image ratio this should be multiply
not plus with that all of this should be working now we can see the raccoon and the raccoon works just fine we're never
scaling this one we are simply cutting off parts that are outside of the canvas
this is looking pretty good border math year if you really want to understand this I would recommend to go
over this a couple of times basically you always want to imagine that you are scaling a canvas and then you are
fitting an image inside of it when you're hearing this the first time it can be quite confusing so definitely go
over this in your own time the math really isn't hard it's just some logic that you have to grasp
with that we are nearly done there's one more thing that I want to do in this case the raccoon is always going to be
fully visible and we are scaling it in such a way that we never cut off
anything but the aspect ratio itself stays identical this is going to be reasonably similar
compared to what we have done here with fill image which means it's going to be your exercise
I want you guys to create a third scaling Behavior to always show the full image without cutting off parts
the video now and try to figure this one out you can reuse a lot of this
since I am going to reuse quite a bit I am simply going to copy the entire function paste it in here and rename it
to show full image this function I want to call right
away down here inside of configure I want to show the full image inside of the function Global can stay
the same the current ratio we also need and all of the stuff down here is also going to stay identical which means the
only part we have to change is this bit here specifically we have to get new numbers
for the width and the height for all aspect ratios the way you have to think about this one
we once again check if the canvas ratio is larger than the image ratio which
means that the canvas is wider than the image for example if this one here is the canvas the image would be something
like this what we have done before is we have scaled the width of the image to
here and then use that number to calculate the new height of the image this I want to change now instead what I
want to do to show the entire image I want to scale the height to only be as tall as the canvas itself
this number I am then going to use to calculate the width of the image which means for this one I want to have a new
height the height is simply going to be event Dot height with the with simply being the
height multiplied by the image ratio we can try this one right away
if it's like this we have the entire image but now if I go even further now we have a black background
and we can see the entire raccoon which only leaves us the last bit here
or this one I want to start with the width because now the canvas is narrower
than the image in this case the width is going to be the event dot width order height I want
to get the width and divided by the image ratio that should be all we need
with that we have the entire raccoon and we can always see the entire raccoon
regardless of aspect ratio and well the raccoon updates automatically this image
in all of its forms so these three functions work slightly differently but
once you have them you can place the canvas in any kind of container and the size would always scale that way you can
use the image wherever you want which is what makes it actually useful let's talk about image animations what
we are going to make will look something like this I can click on a button and we have a
star if I click on the button again the start disappears the important part is that we have animation for this star
to create something like this you already know most of the steps if you can import images and animate widgets
you know the basics although there are some problems let me go through them number one for these kind of animations
you have to import a lot of images so far we may have imported one or two images for this one they are going to be
a lot more that very neatly brings me to the folder structure this one looks like this we have one python file this one
contains the program we are going to make other than that we have four folders and all of them contain images
for example inside of yellow we have a whole bunch of stars what we're going to
do is we're going to play one star after another and if we do that fast enough we
have an animation in case you're wondering here the first image is only white because Windows is
weird the image here is actually empty going through the images is actually not that hard we just have to configure a
button what is much more important is how can we import all of this I guess you could write 30 import
statements but that would be kind of a pain because we also have other folders We have the black folder here we have a
black star then we have a dark folder and here we have another kind of animation and then we have the light
folder here's one more animation if you were to import every single file manually you would have to write a lot
of code which means I want to find some smarter way of doing that for part number two we have to organize State
Management this is going to toggle if the button has been pressed and goes forward with the animation or if the
button was already pressed and we have to run free animation backwards while doing that we also have to make sure we
are preventing interruptions so what happens when the user is pressing a button while the animation is playing in
my case I'm going to prevent any kind of button click other than that it's just basic animation logic so let's have a
look in my case I am relying on casted T Kinder because this one is slightly more complicated but all of the logic would
also work for ttk the reason why I'm using custom tkinder is because well it looks much nicer but
and if you can use this with custom tkinter you can also use it with normal T Kinder other than that I'm importing from pil
image so we can have images then we are creating a basic window and we are running main Loop
the result is going to look like this a basic window to stay consistent one thing I forgot is the comment to say run
before the main Loop now for the button I want to have a dedicated class class
let's call it animated button for this one I'm going to inherit from
ctk button I forgot this cdk first of all
this is the button we want to work with so far I only really inherited from
frames but you could inherit from any widget and add specific bits to it in here we want to create a Constructor so
done there in it method this one needs four arguments in total or while parameters self as always definitely the
parent after that we need a light path and we need a dark path those are for
the light images and the dark images because remember in custom tkinter when we are creating images we have to
account for a light and a dark theme which means you always need two kinds of images
I guess if you want to be lazy you could have the same image for the dark and the light image but that wouldn't look as good what we have to do in here first of
all is run this super Dunder init method the master is going to be the parent
besides that we want to have some text what you put in here really doesn't matter let's say a button
or rather a animated button once we have that we can place the
entire thing using the pack method or while any kind of layout method here is fine I'm going to use pack because it's
easy with expanding true the button is going to be right in the middle with that I can create the animated button I
can add in the window as the parent then I need two paths although for now I'm just going to add none and none
because we have nothing for the paths if everyone is now we have an animated button although this one doesn't do
anything right now that is bringing us to the first part that we really have to care about we
want to write a method that Imports a whole folder or rather folders because
what I want to do in here is I want to add self then I want to have the light path and the dark path
the argument I'm expecting here is a path to a folder so if I reopen the
folder again we have the python file here and what I'm expecting is for example yellow or black or dark or light
any of these folder names is what I'm expecting just to be explicit here I want to have
for the light theme I call this one black for the Dark theme so the second
argument I want to have yellow once we have the actual images we can play around with the colors here but
they all work in the same way in here we have to figure out how to work with that first of all though I want to Loop over
both of these paths which is very easily done for path in then a tuple with the
light path and the dark path if I print the result path
while also making sure that I'm running this method in the init method self dot
import folders with the light path and the dark path this method needs to be run before the
Super method that is really important you will see later on why although if I run this now we get black
and yellow now we have to figure out how to get the folder contents from this
path for that we are going to need another module that module is called OS
however I don't just want to import OS instead I want from OS import walk
what walk is doing is if you give it a folder name it gives you the content of
a folder for example what I could be doing instead of printing the path I can print walk and then the path if I run
this now we get a generator object that didn't go as planned but if you convert
this thing to a list then you can see what's going on this is looking much better let me extend this a tiny bit
we are getting two lists this list here for a light path and this list here for
the dark path you can actually see for the first argument we are getting black and we are getting yellow those are the
folder names for each list there are actually only three arguments the first one is the
folder name this one we don't care about because we already have that next up we
have an empty folder for both of them if there were any subfolders inside of these folders the names of these folders
would be in this list since we don't have any subfolders we can entirely ignore this one as well
it's simply not relevant for us however afterwards we have a long list
with all of the files inside of this folder this is what we actually care about
on top of that you want to be aware of the order here in my case I'm starting with zero zero zero zero zero zero one
then two three and so on on some operating systems I think in
particular for Mac OS this order might be messed up I'm going to show you later how to account for that but it's
definitely something you want to be aware of it can mess with your animations quite a bit although another really important thing to mention is
that what we are getting in here are just file names all of these are strings
they are not files they're not images we just get a string of a file name we
still have to do the actual import but that comes later first of all though I want to add
another for Loop or let's call it data in walk path
the result is going to be if I print the data we have the stuff I've just shown
you although we can be a bit more elegant here since this walk path is
returning three things we can unpack them right away inside of the for Loop we get the folder name we get sub
folders and then we get the let's call it image data
all we care about is image data this is what I want to print so if I run this we
get all of the image names to indicate that I don't care about the folder name I will replace this one with
an underscore a subfolder I also don't care about so this one is going to be a double underscore next up the image data
if I print this again we absolutely have to make sure that this data is sorted it
always says to start with zero zero zero zero and end with zero zero zero and two nine
with the numbers going from the lowest to the highest you might get this by default you might
not and you really want to make sure for that I want to create a new variable
I'm going to call it sorted data in here we want to use sorted
what I want to sort is the image data but to be a bit more specific here I
want to set a key because if we just passed in the image data let me show one entry I want to
print image data and then the one with the index one also let me comment out this bit here so we're not getting an
error if I just print one we get this bit here and this is a string
if we use this with sorted python wouldn't really know what to do with it because if you compare different strings
it's not really clear which one is smaller and which one is larger instead what I want to do is only get
the last five digits if I then turn this into a number python
can sort it from the lowest to the highest and obviously if you have different file names the logic here would be different
it very much depends on what kind of system you have in my case I created these with After
Effects and this is the default name so I can't really change that let's first of all only get the number here with
this one item we first of all have to get rid of the dot PNG
that we can do using the split method and I want to split this wherever we have it dot
like so if I run this now we're getting a list with two items returned I only care about the first one
which means I can use indexing here to only get the first one with that we get
image and light zero zero zero one since we can do indexing on strings we can use
indexing here once more I want to go from negative five all the
way to the end if everyone is now we are just getting the number itself
although if I print the type of what we are getting
we are still getting a string which means we have to convert all of this to an integer and now we are just getting a
number you can see we're getting a number because python removes all of the zeros
which means this logic here is what we actually want to use let me uncomment sort it put this over
multiple lines now for the key I have to use a Lambda function the Lambda
function will always get one let's call it item this item is now going to be my image
data which means I can copy all of this paste it in here and replace image data
with item then I can comment all of this out fix the white space here on top of that we
have to remove this one here we only use that to get one item from the image data this we don't need
anymore now if I run this we're not getting an error that's a pretty good sign but just
to be sure let me print sorted data the result is still going to go from 0
all the way to 29 although now I think if you are on a Mac the result here
should now be a properly sorted list with that I can get rid of the print statements this one and this one and we
have sorted data this is still not enough because now we need the full path
you might be wondering now don't we already have that from this image data the answer is not quite
let me print it actually again if I print sort it data what we get is a file
name but this is not a path what we have to do instead is first of all for the
full path we need the folder name then Plus
then a slash and then we need the image name fortunately we have everything we need
the image names we are getting from this list here the folder name is I have a light path or dark path
which we are getting from the path although since we have quite a few of them I want to store all of this inside
of a list let me change full path to full path data and now we are going to use list
comprehension I first of all want to get the path this is either light path or dark path in our
case this would be black or yellow after that I want to add a slash and then I
want to add one of these file names I guess we can use item again so I want
for item in sorted data with that if I print the full path data we are now
getting actual paths we go into the black folder and in there we have image zero zero zero then black image001 and
so on this is what we actually need although we have to get all of this out
of this for Loop so we can use it a bit more efficiently for that I want to have another variable
I'm going to call this one image paths this for now is going to be an
empty list and once I have full path data I'm going to append that image
paths dot append bold path data with that after we are finishing the for Loop
let me minimize it actually I want to print image paths
this is not going to give us two long lists full of image paths
the first one is all of this and the second one is all of this
this is a good start but I want to modify this a tiny bit ideally I'm going to have a list
let me draw it here inside of this list I want to have lots of two builds each Tuple should contain one dark image path
and one light image path so one in here and one in here then I
want to have another Tuple with two more of those so that would be this image here or this image path and then this
image path here I want to assign a new value to my image path the value I want
to assign is zip and then I want to unpack
the image paths let me print actually what we get this might be a bit complicated
image paths what we now get is a zip object that's not particularly helpful but we can turn this into a list and now
we can see what's going on what we're getting now is one long list
and this list is full of tuples one Tuple contains the first image for the
dark image so black image000 and then the light image so yellow image 0 0 and
0. then we have another Tuple here and this continues forever we keep on having more
and more two builds this makes it very easy to work with this data which is exactly what I wanted
also in case you're wondering here zip is a function that zips together two
lists in a way that you take the first item from the first list and the first item from the second list and then you
combine those two into one Tuple zip is expecting two arguments which should be two lists which we get by unpacking
image paths because this one contains two lists with that we have all the data that we need so now we can turn all of
this into actual ctk image objects those I also want to store in a list so
we're going to continue by creating ctk images which is going to be another empty list we are almost done actually
this is the much easier part what I want to do now is for image path in image
paths let me print what we get image path we are simply getting
a tuple with the light images and the dark images or however you want to call them the naming here doesn't matter
terribly much what I want to do with that is I want to create a ctk image this I do with cdk
and ctk image this is what we need in custom tkinder to store image data
inside of this we need a light image and we need a dark image
since in my case the first item inside of the image path Tuple is the light image this is what I'm going to assign
here which means we can now use image dot open
and pass the path in here which would be image path 0. I should probably put all
of this over multiple lines otherwise this will be difficult to read we are using image open on the first
item now we are doing this on the second item as well or the one with the index one once we have that all we have to do is
get ctk images and append the ctk image
with that we are going to have one long list with all of the cdk images
this is what I want to return so return ctk images then we can close this method
and never worry about it again and this was by far the most difficult part of this tutorial if you got so far the
worst part is definitely over once we have the imported folders I want
to store the return value inside let's call it self dot frames just to make sure this is working let me print self
dot frames and we are getting a list of objects this doesn't tell us very much
right now but at the very least we are getting something I guess you can tell here we are getting
ctk images so that's a pretty good sign once we have that we need actually to
create a bit more stuff in here so let me create a proper section that I call
animation logic setup besides the frames we also need what I call a frame index
this by default is going to be zero later on I'm going to explain the animation logic but for now this is what
we're going to use to pick one item from the frames that we want to display we can actually already use this when
I'm setting up the button instead of the init method I can also add an image
this image is going to be self dot frames and since this is a list I can use
indexing I want to get self dot frame index in here and once again this should be over
multiple lines otherwise I'm cutting off some text if I now run this there should be an
image you can see there's an empty space but nothing more the reason for that is that
the first image is completely empty this is why you can't see it however what we can do now if I change the frame index
from 0 to let's say 20 . now we can see one star if I increase
the number to 21 we get a slightly larger star if I go to 26
okay it is going to be very hard to see but if I go to let's say four we get a
very small star the differences between these images is so small it's really hard to see if you see them by
themselves for now just trust me this is definitely working next up we need self dot animation
length this is going to be the length of self
dot frames although from that I want to subtract 1.
the reason for that is imagine if we had a list right now with three items the
list would be 0 1 and 2. this would be three items
however if I want to use indexing it would always be the length minus one the
final item would be the length of the list so three minus one this is going to be really important for this animation
length because I only want to go up to this final item but then I want to stop so I
have to know what is going to be the final index of the list which I'm going to call length it's not exactly accurate
but I think I get the idea there's one more thing that we need and that is self dot animation status
this is going to be a tkinter variable almost specifically is ctk string VAR
this one is going to have the value of start by default now why do I want the animation status
to be a string VAR well the reason here is because with that I can use tracing
so self dot animation status and I can use trace and anytime I'm updating the
value so I'm writing in it I want to run a certain kind of method this method is
going to be animate let's create this one right away I want
to have nmate what is important here besides self we also need unpacking and arcs because
every time we are using trays we got some default arguments although in our case we don't really care about them
for now I'm going to add pass in here because there's one more function that I want to create that is going to happen
inside of this super init method because I only want to start the
animation when I'm clicking on the button which means this one needs a command the command function is going to be self
and I called this one trigger animation I'm going to create this one above
animate so trigger animation with self and nothing else
in here we are going to the State Management which means we are updating animation status
for example if self.animationstatus dot get which would
right now get us start if that is the case so if this is equal to start then I
want to set self dot frame index to zero so we are starting on the first frame of
all of the images on top of that I want to set self dot animation status
with the set method 2 for Ward which basically means that we want to
start at 0 and move the animation forward besides that I also want to check if
self.animationstatus dot get is equal to end if that is the case
I want to get self.frame index and set this to self dot animation length other
than that I want to set self dot animation status with the set method to
backward since with this we are updating the tkinder variable with forward or
backwards this animate is going to be triggered now we can check for different things
for example what I could be checking for is if self dot animation status dot get
is equal to forward if that is the case I want to play the
animation which in this case means I want to get self dot frame index frame
index like so and increase the value by 1. which means that this number here
self.frame index when we use it first time gets the first image which we are
using down here with the image this I want to increase to 1 2 3 4 all
the way until the end of the animation frames if I go through them fast enough we are going to have an animation
which means I can use this now with self.configure I want to update the
image the image is going to be self taught frames in here self dot frame
index let me run this actually if I now click on the button
we get a very small star this is because we are only calling this
animate once so we only go from frame 0 to frame 1. we will need self dot after
after 20 milliseconds I want to run self.animate again with
that if I click on this now we have an animation and then we are crashing since we are running this method here
forever at some point we are going to run out of frames or more specifically we have a larger index than the length
of the list which is giving us the error or more specifically we get list index out of range
to account for this we need an if statement if self dot frame index
is smaller than self dot animation length only then do I want to update all
of this if I try this now and click on the button we have an animation that's
looking pretty good if that is not the case so else I want to set self dot animation status using
set to end that is telling us once we get to the end of all of this I want to have a new
status because I know the animation has finished if we're done pressing again this is stepping here with run and we
would set the animation status to backwards by now this wouldn't do anything because
inside of animate we only have this bit of code here meaning we're only running any kind of
Animation if the status is forward to account for that we need a second one
that checks self dot animationstatus dot get is equal to end
if that is the case I want to do very similar things compared to what I've done here although not exactly let me
start by copying it and now I want to set self.frame index and reduce it by one every time we are
calling this configure still works just fine although for this if statement I
only want to do all of this if self.frame index is greater than zero
this part is still fine although in the else statement if we are finishing the animation I want to set the status back
to start if I'm running all of this now I can click on an animated button and now we
are almost done the animation works but we always go to the end and then back to the start
the reason for that is that we only want to do this if the status is backward
now if I run this this goes forward and now nothing happens but if I click on it again we're
now going backwards yes I can do multiple times still works just fine
on top of that when I'm creating all of this I can get ctk set
appearance mode and switch all of this to light mode
we are now getting a different kind of Animation or while the same kind of Animation just different colors if I
open the folder again we are importing yellow this is the dark images this one
is all yellow and then black has the same animation just in completely black
although besides that we also have dark this one has a hard animation either for white or for the dark path
which means if I add in here light and dark we importing those folders and now
we get a heart that we can also animate although I think there should be the
other way around dark and Light that is definitely looking better
if I remove the appearance mode I guess it kind of works
let me stick to yellow and black
I think those look a bit better although I had this the other way around earlier this was black and yellow
there we go now we have the yellow animation again cool with that we have made a lot of
progress although there's one challenge I have for you I want you guys to create another
animation and this one should run forever that means we go from frame 0 all the way to the end once we reach
that point we're going back to the start and then once again we go from zero to the end that way the animation will keep on
starting over and over again try to implement this one
I want to keep all of the logic contained inside of a method I will call this one infinite animate no need for
custom parameters this I also want to trigger when we are pressing the button
to check if this is working let's print infinite if I now click on the button we
get infinite that's a good start
now we have to figure out the logic for that self.frame index and increase it by one
once I have that I want to use configure again I want to update the image
the value is going to be self dot frames with the index of self dot frame index
finally I have to run self dot after I want to update this after 20
milliseconds and call Self dot infinite animate again if I run this one now
we get the first animation but then we are crashing because we are running out of list indexes again
to account for that we need one more line of code basically what I want to do I want to update self.frame index and I
want to set it to zero if self dot frame index is greater or equal than self
dot animation length however if that is not the case else I
want to keep self.frame index as self.frame index the way you want to think about it is if
we have a list with 0 1 2 3 and 4 items
self.frame index is going to start here and it's going to jump to this one then to this one then to this one then to
this one and if we get to this point here this if statement is going to trigger and it is going to put
self.frame index back to the start that way the animation will go on forever let's try this one now if I click on the
button we get a continuous loop
although I think because of the equal sign here we are skipping the last frame let's remove it and play this again
there we go you can't really see a difference but well there's one more frame in the animation now
and with that we have animations obviously you can make all of this a lot
more fancy but this should be a really good start in this tutorial we are going to work a bit more with colors we
already know how to color in the background of any app especially if you use custom TK enter this should be
fairly easy however what we don't know is how to color in the title bar this one so far
always had one color it was either white or black and unfortunately there's no
easy way of changing it we actually have to use Python to Target windows and then tell it to give it a custom color and
this is only going to work on Windows so we also have to make sure that if we're running the code on Mac OS or Linux
we're not crashing the entire app and that is giving us quite a few things to work with so let's Jump Right In
here we are in a code editor and first of all we have to import tkinter now in
this case I'm going to work with custom tkinter but this would also work with the normal decanter what I want to do is
import custom tkinter as ctk after that I want to create an app this we get with
ctk and ctk I guess while we are here we can also give this a geometry of let's
say 300 by 200 the number here doesn't really matter and after we have that I
can run main Loop to start the app with that I'm getting a small window that
isn't looking too terrible and I do have some control over the colors most importantly to set the background color
when I'm creating the app with ctk and ctk I can set an FG color this could for
example be red if a run is now we have a red background color
you could also use hexadecimal values for that you need a hashtag and then let's say ff00 and FF and that would
give you a pink color just as a reminder FF stands for the red color 0 0 is for
the green color and the final FF is for the blue color which means in our case we have a full amount of red and a full
amount of blue and combine these two colors and there's no green whatsoever and the result of that would be pink
however now we have one important thing that we can't do and that is to change
the title bar color how can we do that to get started we have to import a
couple of things I want from C types import win dll then by ref
then size off and finally C underscore int all of those modules are quite specific
the one we really care about is wind dll because this is giving us access to some
system level functionality of Windows and that we can use to color in the title bar and for that we will need a
couple of steps first of all we have to Target the current window because right now what we're doing is we are talking
to Windows directly and what we want to do first of all is to get our current window this you usually store in a
variable called hwnd which is standing for the window handle and that window
handle you get with win dll then user32 get parent or get parent make sure you
spell this right the G and P should be uppercase this is a method so we have to call it
we have to add one argument and that is app W info underscore ID and this is
also a method basically what is going to happen this app W info ID is giving us
the current ID of the window we have open the app we just created and this ID we are using to get the
current window handle this is what Windows as an operating system sees so this is what we are now storing in the
variable with that we have access to the window which means next up we can actually
change the title bar color and this we do with win dll and WM API and then
uppercase the WM set window attribute
this method wants four arguments the first one is going to be the window handle this we just got so HW and D next
up we will need one argument that tells us what attribute we want to address because this set window attribute can
Target quite a few things to give this a bit more context here is the windows documentation for this method we have
dwm set window attribute and in there we can Target quite a few different
attributes for example in there we could Target the Border color the caption color the text
color and well quite a few more things most of those we are basically just
going to ignore I'm going to add a link to this website but it's not going to be too important back in the code all we really have to
do is add a 35 in there this is the attribute for the title bar color
next up we will need the actual color and you might be tempted to Simply add something like red unfortunately that
would not work instead we need a very specific kind of
color and this is called hexadecimal color let me store it in a separate variable actually
I will call this one the title bar color and this is going to be a weird format
we start with 0 then an X then 0 0 and then we can add a color that looks
something like this except it's inverted which means we are adding two digits for
the blue color then two digits for the green color and then two digits for the red color
for example if we want to have pure red this would be 0 0 then 0 0 again and for
the red color f f once again we are using hexadecimal values which means zero is the absence
of the color and F is the full amount of the color you might be wondering now what kind of value is this even because
we have a bunch of numbers but in a couple of strings so is this a string or a number the answer is this is an
integer if I simply print the type of the title bar color and comment out the
dwm set window attribute and run all of this we're getting a class integer what
we're creating with this one is a special kind of integer although we don't have to worry too much about it
this color we now want to use but we have to convert it and for that we have pyrav and C underscore int to use them
we first of all have to use buy ref and this one wants the argument with C underscore end and this one wants the
actual color title bar color and let me put all of this over multiple lines that's why it's a bit easier to
read there's one more argument we need to make all of this work and this one is fairly Technical and it's always going
to be the same what you need is size off and this one wants the argument C underscore int
at this stage don't worry too much about it just always add it and then you're good to go but now if I run the app we
get a red title bar color that is because in the title bar color string we
have the full amount of red we have no green and we have no blue if we change
this to an FF for blue and 0 0 for red run out of this again we get a blue
title bar color what you can also do let me copy all of this and paste it right
below if you target attribute number 36 then you target the color of the title
bar text which means if I run this now we can't see the text anymore the bit up here is gone oh well it's not
really gone it's just the same color as the background however if I give this another kind of color let's say the
title text color this would have to be the same format
that we have used up here let me copy it actually and let's say for the color I want to
have no amount of blue I want to have the full amount of green and just a bit
of red so let's go with Nine and Nine and this color I want to use for the text color and if I run this again we
get some greenish looking color that is because we have the full amount of green and some red with that you can change
the title bar color and you can change the text of the title bar color it's not terribly elegant but it certainly Works
however there's one major issue that we have to address all of this code is only going to work
on Windows and let me get rid of the white space if you try to run this code on Mac OS
you would get a crash because python couldn't import win dll this one is
exclusive to Windows as a consequence we want to add a tiny bit more code that if we are running all
of this on another operating system that would cause an error we are simply skipping this part of the code
which means we want to add a try and an accept statement and this I have covered earlier in the python introduction we
basically need two important keywords they are called try and accept
I hope you remember those two in fact this is going to be your
exercise I want you guys to make sure that this code would run on any operating system which in effect means that if you're
running this on anything other than Windows we are simply skipping this line and all of these lines
pause the video now and try to figure this one out you might have to go back to the python introduction but see how
far you get first of all we have to wrap all of this
import into a try statement which means I want to try to import this like so
and when I'm using try I also have to use accept in this case I simply want to add pass
to all of this I am telling python to try to import all of this stuff
if we are on Windows this is going to work so python is going to be happy and run this line however if we are on Mac
OS this is not going to work and as a consequence we're going to end up with the accept statement and in there we
simply have a pass so this is not going to do anything that is going to be the first part we do
however need a second part if we'll have the code like this we would skip this
line so the code would work up to that point this bit here would also work however
now python would try to run this code on any operating system and since we don't
have windll we would get an error as a consequence all of this also needs
to be wrapped in a try accept statement let me indent it and I will need Rye
at the end of all of this since we're using try once again I will need accept and once again I want to accept pass we
are telling python to try this entire block of code and check if it is working
or not if it is working everything is good and simply continue however if it is not working simply don't do anything
which we're doing with accept pass I can run the entire thing again we are getting our current APP however now if
you run out of this on Mac OS although it would have the standard colors so at
the very least we have something and with that we have covered another really important part about styling
hello in this part we are going to create a BMI calculator for this one you
can change the weight and the height and then you get your body mass index it's a
fairly straightforward app I guess the one extra thing I added here was you can change this to Imperial units and then
use ounces and inches it really isn't anything complicated in here I am just
using custom tkinter with some basic sliders and buttons and then the formula for BMI is also really simple
and before I jump in really quick here is the folder I'm going to work with
let me make it a bit larger we have BMI and there we're going to write a code right now it's entirely empty besides
that we have settings.pi this is going to cover the colors and the font sizes and stuff like that finally we have
mt.ico and this is to hide the icon of the app that is all we need so with that let's
jump into some code here's my code editor ifbmi dot Pi open and I have settings.pi inside of settings.pi we
have a couple of basic information about the text sizes and then some colors finally we have the title hex color this
one is also a color but it works slightly differently so what we're going to start doing is
create a basic window using custom tkinter and color it all with one shade of green this shade of green here in
particular for that first of all I want to import custom tkinter as ctk and after that I
want to create a class I got this one the app and for this one I want to have ctk and ctk
this class app is going to need a thunder in it method with self and nothing else the first we want to do in
here is some kind of window setup yes as always means to call the super
Thunder image method we can call straight away an F G color which is
going to be green that is going to be this green color here although right now
I don't have my settings available for that inside of pmi.pi I want from
settings import everything just to make sure this is working I am
going to call Self dot main Loop inside of the app after that I'm going to
create an instance of the app with that if I execute the code we can
see we have a small window that has a greenish background what I want to do now is to write the title and
the icon this I do with self dot title and set a title to an empty string with
that I don't have a title anymore next up to hide the icon I want to use I can
bit map and for that we are going to use Mt dot Ico that is the blank file we have
inside of the folder I am importing this one with this line and now if I run the code
we don't have anything at the top left anymore meaning this error here is completely
empty although right now when I'm starting the window the window is quite small for that I want to use
self.geometry and give my window a start size of let's say 400 by 400. if
everyone is now this is looking much better on top of that since this isn't a flexible layout I want to self dot
resizable I do not want to allow resizing the window which means in here
I want to add faults and false this means the window cannot be resized
so if I try to click on the corners nothing's going to happen the main reason why I don't like resizable for these small apps is simply
because there isn't that much to fill the content if we are something this simple and we resize it all of the
elements just become really small relative to the Windows size although I guess if you wanted to add more elements
you could fill the space a bit more efficiently but if you don't do it it's just starting to look a bit silly but
right we are very nearly done the last thing we have to do and this I want to do in a separate method I want to change
title bar color this is going to be a method
so I have to create the method here and this one is self and nothing else what I want to do in here let me add pass for
now I want to change the color of the title bar
and since I covered this earlier this could be a really good exercise
although there's one additional thing I do want to add this will only work on
Windows but I do want you guys to make sure it does not crash on Mac OS
pause the video now and try to implement this one it shouldn't be too difficult
first of all we have to import a couple of things all of those we are getting from C types
specifically I want to import win dll by ref
size off and finally C underscore int when dll however only exists on Windows
meaning if we tried this line here on Mac OS we would be getting an error for
that I want to use try spreading it correctly would also help try like this meaning we are trying to
run this code however if we are getting an error then we are using accept
and if that is the case I simply want to run pass meaning we're not doing anything once we have that I can work
inside of the method and once again in here I also want to run try
because if we couldn't import this line up here then we definitely cannot run this line here so both need to have try
and here I want to get H and WD and this I get with win dll dot user32 dot get
parent this one needs one argument which is self.w info underscore ID and do not
forget to call this one next up we have to get what is called a dwmw a underscore attribute and this is
simply 35. next up we need a color and the color we
already have this we have inside of settings this color here it does look very strange but I added a
comment here the hex order is 0 then x 0 0 this you can entirely ignore after
that we have the blue colors the green colors and the red colors so the green
color that I want is this one here which is the same that I have up here for the background color
although in my case all I have to do is copy title hex color paste it in here and then I'm good to go
finally I have to get win dll then bwm API dot now comes the long name
uppercase d w m then set window
attribute inside of this one we now need HW and D then we need
dwma attribute finally we need buy ref C underscore int
of the color for the last element we want to have size off and then here C
underscore int the last argument is quite technical so you don't have to worry about it but
basically what we're doing in here just to recap when dll dwm API and then set
attribute sets one specific attribute of a window inside of this one we're
getting the current window then we have to Target one specific attribute and the
one we are targeting is the number 35. this targets the color of the title bar
and then we are giving it a color with this line here the way this is working is a bit more cryptic but that's just
how it works but well with that we are done so let me run the entire thing and
I am getting an error that after this try statement I am not adding an except
that is very easily fixed except and pass if I now run this we don't see a
difference so something went wrong most likely in this line here because this one's really long and I can see the
error this should be a lowercase C now if I run this there we go now we
have a completely green window with that I can get rid of the exercise
text and minimize the app for now although there's one more thing that I want to do
this app here should be wrapped inside of an if statement and that if statement
is going to be if done their name is equal to the string Thunder Main
only if that is the case I want to create an instance of this app if I run the code now we're not going to
see a difference but if you have multiple files this is generally what you should do that way we
don't accidentally run some code in some other file like in settings for example although in this case there's no real
code to run here we're just storing some data but it's got practice so I am going to
include it in this part we're going to create the four widgets that are visible inside of the app meaning we're going to
create the title for the BMI text then we have the weight buttons after that we
have the slider for the height and finally in the top right we have the metric Imperial button for now they are
not going to do anything but at the very least we are going to have a pretty good start I want to keep on working inside of my
class app in here before we can create any kind of widget we have to create a
layout in my case I have used a grid layout although we only have a single column
which means I can run column configure I have a column with 0 and the weight is
going to be 1. the rows are going to be much more important in my case I have four rows 0 1 2 and 3
all with a weight of one on top of that I have set uniform to a the way the app
is going to work if this is the entire window we have four rows one two three
and four the BMI text is going to cover the top two buttons the white buttons
are going to be in this one here and finally the height slider is in the bottom one
all the way at the end the Imperial metric button is going to be in the top right and this one we are placing with
place not with the grid layout since you can combine them this isn't a
problem we have the layout meaning I can minimize the class app and now create
all of the widgets each of them is going to get their separate class first of all I want to have class let's call this one
the result text since this one is only going to be a label I want to inherit
from ctk label although this one like any other class we're going to create is
going to need an init class in here we need self and for now we need a parent we have to call the super Dunder init
method to initialize the parent the most important argument in here is the master which is going to be the
parent to get something in here for now I want to give this some text let's go with
22.5 once we have that I want to place this result text right away using the grid
method we are in column 0 and row 0 as
well since I do want this widget to span two rows I need a row span of two
finally sticky is going to be north south east and west this should be all
we needed to get started with this text meaning now I can add another section in
here let's call this one the widgets I want to create my result text
I need the parent in here which is going to be self other than that there are no arguments
needed let me run the code now and there we can see 22.5 right in the middle
that's a decent start but well it is very very small for that though we can make a few
updates inside of settings we have a font and a main text size
I want to use those two to create a font and then this font should Define how large the text is I suppose for this one
to keep things a bit more organized I can create a font inside of this result text this I have to do before the Super
init method in here I want to create a font this I create with ctk and then ctk
font this font is going to need a family and a size
both of those we're getting from the settings the family is going to be the font
this one here next up we need the main text size for the size let me copy it the size is going to be the main text
size all we have to do now is send the font of the text to the font we just
created and now if I run this again this is looking much better there's one more
thing that I do want to do inside of the font I want to set a weight the weight
should be bold and now if I run this again this is looking significantly better
with that we have to resolve text and next widget is going to be the weight
input this one is going to inherit from CT k for aim
as always we need a Dunder init method this one itself enter parent first of
all in here I want to call the super Dunder init method
the master needs to be the parent and I guess while we're here I can also set an
FG color which is going to be white this white we are getting from the settings I'm using this right here
after that I want to place this widget as well with the grid I want to use column 0 and the row is
going to be 2. also sticky should be north south east and west
with that we should be seeing something after creating an instance of this class
which means I want to create the weight input itself as the one argument for the
parent run this entire thing again and there we go this isn't looking terrible although it needs a bit of refinement
most importantly when I'm using the grid method I want to add a bit of padding
for the horizontal and the vertical I want to use 10 pixels each
and now this is looking a bit cleaner and what I'm looking at is I can see I
forgot one thing it's probably very hard to see on your computer but the color of the text is slightly darker than the
color of this box this is because when I created the text
I did not set a color that we do with text color and this one
should be white as well now if I run this both the text and the Box have the
same color inside of the weight input we now have to create a layout for all of the buttons as a reminder here is the
final app what I want to create for the layout is once again I'm going to use
grid we have one row and then we have a bunch of columns we have column 0 column
one column two column three and column four the easy part in here I want to use
row configure the index is zero the weight is going to
be one and uniform let's set this one to be simply because
I have used a up here also I don't need the class app right now I just want to work inside of the
weight input next up I have to work with the column configure
I have to create five columns so let me duplicate this a couple of times so that
we have 0 1 2 3 and 4 5 columns in total
the middle column should be the widest one so this one is going to get a weight of three
column one and three are for the small buttons I like to keep them at one
however column 0 and column four need a weight of two so they are twice as wide
as the columns one and three once again to illustrate what this means column 0
and 4 are these large buttons here they get a weight of two each
next up we have one and three these are the smaller buttons so they only get a
weight of one finally the text in the middle is going to be column two this
one needs to be the widest which means this one's going to get a weight of three and I am incapable of
drawing a free this is giving us the layout so now we have to create the widgets or the buttons whatever you want
to call it I guess it's not all buttons so let me just call it widgets the most important
widget in here is going to be the label this one will be a ctk and ctk label
self is going to be the parent for the text for now let me just write
in 70 kilogram this label I want to place right away so
label dot grid row is going to be 0 column is going to
be 2 and with that if I run the entire thing we can see something very very faint but
there is a very faint 70. it's tiny and basically white so we have to change the
styling here first of all the text color should be I
think I call this black if I go to settings we have black here so now let's run this and this is
definitely more visible on top of that I also want to create a font like I have done before this is
going to be ctk and ctk font we need a family and a size both we already have
inside of the settings the font size I want for this one is the input font size
for the family I simply want to use my font now once I have that I want to set the
font to the font I just created and this is looking much more visible
let me change this once again a better comment here would be the text because now we can add the buttons
there are four buttons that we need let me start with one I want the minus button this is going to be ctk and ctk
button the parent is going to be self and the text for this one is simply going to be
a minus this one is also going to need a font and for the font here we can simply
reuse the font we created earlier which means font is going to be font where we are here we can also set the text color
to Black let's add this minus button to the layout right away using the grid method
this one should be all the way on the left meaning the row is still going to be 0 and the column is also going to be
zero if I run this now we are getting an error that this black is not defined this should be an all uppercase letters
black now if I run this this is feeling a bit better but I guess I can already
see some problems we first of all have the completely wrong colors and if I hover over this the hover color is also
wrong also this button is a bit too wide first of all I want this button to cover
the entire height of the container for that I need sticky and the argument I
want in here is north and south now if I run this again the button is going to cover the entire area
although that's also not exactly what I want instead what I want to do is give this a
padding of 8 both vertically and horizontally so pad X is 8 and Pad Y is
8. and this is looking much better although the colors still don't work
for that inside of the button I need to add a few more arguments first of all I have to set an FG color
this FG color I termed light gray this once again we get from the settings
light grain here now if I run this again this is looking significantly better however if I hover
over this we're getting a really ugly color so the last thing we have to do is we
have to set a hover color the hover color is simply going to be Gray
this is the gray we're getting here is slightly darker shade of gray so now if
I run this again we have a hover color that works and well this is looking really good although that being said
there's one more thing that I did add and that is a corner radius I have set this one to six
although this one is going to be very difficult to see but I think it definitely makes the entire thing look a
bit nicer although this corner radius here I should add to the settings
which means inside of the settings let me edit here I want to have button Corner radius and
it should be six this I now want to copy and replace the 6 with the button Corner radius
the result is going to be the same but now we can change the styling from inside of the settings
so with that we have the minus button once I have that I can simply duplicate
these lines and create the plus button the only difference here really is that
the minus should be a plus for the text and when I'm placing this button using the grid method the column is going to
be 4. now if I run this one we have a plus and a minus button that both look pretty
solid meaning now I can copy this entire thing one more time because now I want to have
let's use the plus button again I want to have a small plus button
this one is still going to show a plus sign however since we're placing it on column three it is going to be smaller
meaning now if I run this we have a smaller plus button this is almost working but this covers
the same height as the bigger plus button to account for that I simply remove this
sticky argument run this again and there we go now this plus button is much more
square-ish which is looking better on top of that I want to change the
padding from 8 to 4. and with that we
have a much nicer looking button there's just one more button that we need so I'm going to duplicate all of this one more
time because now we have the small minus button the only two changes that
we have to make is change the plus to a minus and the column shouldn't be free it should be one
and now if I run this again we have all four buttons meaning now I can hide the
weight input and work on my next class this is going to be the height input
this one once again is going to inherit from ctk frame and then here I want to have an init
method that takes self parent and that's all
that we need for now and here as always I want to have the super init method I want to set the
master to the parent and the FG color to white
after that this is getting a bit repetitive I want to use the grid method row is going to be free and column is
going to be zero also we need sticky north south east and west and Pad X
should be 10 and Pad y should be 10. this should be giving us a container
although I do have to create an instance of this class meaning inside of the app below the height input I want to have
the height input with self now if I run this we have the final container
that's looking pretty good we now just have to fill the swing since this layout is pretty simple we
can stick with the pack method so I can jump straight to creating the widgets I want to create two widgets in
here I first of all want to have a slider this I create with ctk and ctk
slider the parent here is going to be self as usual and that is actually all I want
for now once I have that I want to pack this slider the most important argument in here is
the side because I want to place this on the left side I also want to fill the entire
horizontal space and I want to set expand to Rue also for a bit of padding
I want to set pad y to 10 and Pad X to 10. if I run the app now this isn't looking
terribly bad although we definitely have to work on the styling inside of the slider I want to set a few more things
and I am going to work over multiple lines because there are quite a few in there
also I want to use named arguments so let me set the master to self and then
we can work on the rest first of all I have to change the button color and this one should be green
the green here should be in all uppercase letters now if I run this the button that we can drag on the slider
let me show my mouse the button that we can show is going to be green although if we hover over it it defaults to this
ugly bluish color to get rid of that one we have to set a button hover
color the button have a color I set is gray and now I have a green button by default
and if I have over it it becomes a lightish gray next up I want to set the
progress color and this one should be green as well what this one is doing is
it colors the left side of the slider so this side here is now green
the last thing that we have to do is to change the f g color and this one I have
set to light gray this one updates the right side of the slider so this side
here it's now light gray that is giving us the slider although I also want to have some text let me name
this the output text this is simply going to be a ctk and ctk
label although I can already see my typo there should be uppercase t in here once
again the master is going to be self and for now the text is let's go with 1.80
this output text I want to pack right away I want to set the site to left as well
and Pad X I want to have 20 pixels of padding now if I run this one
we can once again we have the same issue we have to text earlier the text here does exist but it's really hard to see
and it's also very small but that we can work on first of all I
want to set a text color to Black and now with that this is much more
visible also I realized there should be a meter at the end like so
and now we get 1.8 meters besides that I have to create a font and so far I
always created a separate variable but we don't actually have to do that I can do it straight in here so I can simply
create c t k and font with the family being the font
and the size is going to be I call this one the input font size
enough around this we have a much larger font that covers the height input so
there's only one more thing to do I call this one the class unit Switcher
what this one is going to do let me run Define lab again this one is going to be the text all the way in the top right
here by default it's going to say metric and it's going to be a bold text with the
same font but a smaller font size what is really important about this one is that it's not placed using the grid
method but rather the place method this is really important to know because
this final widget is going to be your exercise I want you guys to create that text in
the top right the only important things that you have to know for this one is that inside of
settings we are using the same font so calibri but now we have a switch font
size for the text color go with dark green that is all you have to know so pause
the video now and try to figure this one out yourself
first of all we have to figure out the inheritance for this one I'm going to
use a ctk label simply because the entire widget is just
going to be some text inside of the init method in the class way after yourself and then get a parent
this parent we can use in this super in Niche method because in here we have to set a master which is the parent
on top of that just to see something for now I'm going to set the text to metric
now we have to figure out how to place this kind of widget and importantly here
we cannot use the grid method or well we could use it but it wouldn't give us the right result instead I want to use the
place method for this one I want to use relative values which means I want to set
relative X relative Y and then I also have to create an anchor
the way you want to think about it is that this one here is the entire app the
position I want for the widget is going to be roughly somewhere here so I have to figure out how to get this widget in
the top right with a tiny bit of padding also remember the sizing here for
relative numbers so relative X for example would go from 0 all the way to
1.0 and for relative y we're also going from 0 to 1.0 these numbers we can use
quite easily to create padding ourselves because the place method doesn't have padding
the way I approach this is I said relative X to 0.98
and relative y to 0.01 finally I have set the anchor
to North East and this should be a string
basically I have set the anchor to North East which is this point here then
relative y 0.1 gives me almost a top so almost this line here except a tiny bit
of difference this would be 0.01 that's why we get a tiny bit of padding
at the top a similar thing I have done for productive X I am going almost to
the right side but not quite so if this line here is zero I'm going
almost to the end but not quite 0.98 leaves this tiny bit of space
and now with that I simply have to create an instance of this app let me call it in here unit switcher
with self and now in the top right we have our metric text
that is a really good start although we have to work on styling a tiny bit more
first of all I want to update the text color and this one I believe I called it dark green
inside of settings this dark green that's looking good let's try this one and there we go we have a dark green
text besides that I have to create a font which is going to be ctk and ctk bond
the family is still going to be the font on uppercase letters
this size is going to be inside of settings I have a switch font size I
want to use that one and the weight for this one is going to be bold
now if I run it again there we go in the top right we have the metric text and with that we have all of the widgets
now this video is getting a tiny bit longer but I did want to cover all of this in one go so now we can work on
actual functionality for this part we're going to start implementing the logic for well the entire app which means if I
now press on any of the buttons or use the slider we are updating the BMI
number for now I'm only going to use metric numbers in the next video I'm going to cover how to use Imperial
numbers or rather how to make the user think they are using Imperial numbers but let's focus on the basic logic for
now once again here we are in the app and now I have to start thinking about how to implement the entirety of the
logic for that first of all inside of the app we have to add another section before
the widgets because to make any kind of logic work here we have to account for
the data so I want to store some data in here I want to create three different
variables the first one is going to be the height and this is going to be an integer this accurate with ctk and int
bar don't forget to call it and then here I want to set a start value of let's say
170. also I just realized this should just be invar without the ctk in front
now if I run this this is working again besides the height end we also need a weight although this is going to be a
float which we are creating with ctk and then double VAR
for a start value here I want to go with 65 kilograms finally I want to have
self.bmi string this is going to be ctk and is string VAR this one does not have
a starting value but what we can do now is run a method that I call Self dot
update BMI this we have to create let me do it on top of change title bar color I
call this one update BMI for now I will not need any custom parameters and what
I want to do in here is first of all I need to get the height in meter oh and I
should mention the formula for BMI is the weight
divided by the height squared and by default in all of this
the units you would be using are kilogram and meter the 65 here is totally fine
for the weight however for the height we have 170 right now this would be
1.7 meter for any American viewer watching this I hope you understand the units just drop
me a comment if this is too confusing and I'll explain more basically the way you want to think about it if you never
encountered metric units is one meter is a hundred centimeter and the unit we're
using in the height in so far is centimeter on top of that one kilogram
is going to be 1 000 Ram although this one we don't
really need because kilogram is much easier to use how these numbers relate to inches and
pounds I will cover in the next video for now don't worry too much about it the most important thing for now is we
have to get our height in meter this is super easy to get all I want is self dot
my height integer and importantly here I want to get right now this would get me
the value of 170. which would be centimeters to convert
this to meter I simply have to divide it by 100 and then I'm done next up I want
to get my weight in kilogram this I get with self dot weight float
and get since we are already using kilogram this one is totally fine by itself
finally we can calculate the BMI result for this I want to have my weight in
kilogram and divide it by my height in meter although this one needs to be
squared and as soon as I have that number I can simply update my BMI string
using set and pass in the BMI result
this will give me the proper value inside of this BMI result however there's one problem we have right now
this BMI string is not connected to this result text we could update it as much as we want it
wouldn't be visible to account for that when I'm creating my result text in this line here I want to
pass in self dot Emi string and now inside of the result text
we need another parameter which is going to be the BMI string
and this BMI string I have two instead of the super init method set as the text
very Bill like so in here I want to have my PMI string and
now at the very least we should see some kind of different starting text let me
run the entire thing well we can certainly see a change the problem is that this number here has way too many
decimal points to fix that I simply have to round this result this I can do using
the round function the second argument here would be how many decimal points we have I think two are totally fine here
now for run this this is looking much better now we get a proper result
now the issue is I can use the slider and the buttons they don't do anything right now to fix that we have to connect
the height integer to the height input and the weight load should be connected
to the weight input let's get started with the height integer this I want to do inside of the
height input I want to also pass in self dot height integer
now once we have that inside of the height input we need another parameter
let's call it the height int this height integer I now want to set inside of the
slider as the variable so in here height integer if I execute
the code now you can see that by default the slider is all the way on the right
the reason for that is that by default this slider goes from 0 to 100 which
isn't ideal to account for that I want to add a from and to parameter
I want to go from let's say 100 centimeters so one meter
should be the minimum if you are below that the formula doesn't help anyway two let's go with 250. this is 250
centimeters I I think that's a bit taller than eight feet so very few
people are going to be larger and if they are a BMI formula would not apply to them anyway
so now if I run this we can see the slider is slightly to the left so this would be 170 this would be 100 and this
would be 250. we have the basic slider with a height integer now the problem
with that if I run the entire thing again I can move the slider as much as I want it is not going to influence
anything for that let me minimize the height input again because what we can
do inside or rather after the starter I can add what I called Racing for the
basic logic here essentially all we have to do is whenever this height or the weight
changes then we want to call this method here and this would update the text the
functionality for that is inbuilt into tkinter we are getting this with for example for the height integer using the
trace method there are two arguments we need in here do we want to run a function or a method whenever we are
reading the value or when we are writing on the value in my case whenever we change the value so when we are writing
on this variable I want to run a method which is going to be self dot update BMI
there's one more thing you have to be aware of and that is if you run a method
using this Trace method tick enter automatically adds a couple of arguments into it as the second
argument those usually capture with star arcs and then you just completely ignore
them meaning no if I run this again I can update the height and we are updating
the value for our BMI so next up we can do the same thing for
the buttons which means for this one as the second argument I want to pass in self dot
weight load so now I can minimize the app to have a
bit more space and I want to work inside of my weight input I have to get the weight load in here as
a parameter so the entire thing doesn't crash and we have the weight float available inside of the class
that's a good start however now we have a problem each of these buttons does something
slightly different we have to figure out some kind of system how to make every button change
this weight float slightly differently for example if I click on the minus button I want to reduce the weight by
one kilogram however if I click on the small minus button I only want to reduce
the weight by 0.1 kilogram for the plus and the small plus button
the same thing just in a positive direction since this is going to be a bit of extra
logic I'm going to create a separate method let's call this one the update weight
method besides self I also want to have let's call it the information by default this
is going to be none for now all I want to do is to print the information now how this is going to
work is each of those buttons is going to get one method this method here
and then we're using that to pass information in for example for the minus
button I want to add a command and this command is going to be a Lambda function
although this Lambda function is simply going to call Self dot update weight
the reason why I'm using lambdar is because this allows me to add an argument when I'm calling this method
what I want to pass in here is a tuple with two values the first one is going to be minus the second one will be large
the reason is this is a minus button so we have minus and this is a larger button so we have large
that's literally all of this then I can copy this entire line paste it in here
because now we have the plus button meaning this minus should be a plus next up we have the small plus button so
I can paste this in again this should be a plus button and it is a small button
finally for the small minus button I want to pass in the command line again
this should be minus and small way of that let me run the app and now
if I click on the large button we get plus large plus small minus small and
minus large that way within one method we have all of our buttons
inside of this method I first of all want to get an amount so by how much do
I want to update this value this will be one if info 1 is going to
be large this large only exists inside of the minus enter plus button these two
buttons here they have large and large if I have either of them I want to
change by one kilogram however if I don't so else then the
amount should be 0.1 this would cover these two buttons here
once I have that I can simply check if info 0
is equal to let's start with Plus then I want to self and set the value
what the new value is going to be is self dot weight load dot get
Plus the amount however if that is not the case so else I can simply duplicate this
line and the plus should be a minus I hope these lines here make sense
basically all we are doing is we're getting the current amount of the weight and then we are either adding or
subtracting the amount we have specified here although I think I've realized this
attribute self.weight float does not exist right now all we have is this parameter but we're never turning it
into an attribute let's do this right at the top so self dot weight float is weight
float now this should be working if I click on any of the buttons nothing is happening
although if I print
self.weight float dot get let's see what's happening if I now click on the small Plus
we can see at the very least this is working and yeah we do have the proper values
here and don't worry too much about all the floating Point numbers here they are not going to make a difference they just
look weird but to a computer they're totally fine all of this here is working
totally fine meaning we can minimize it but when I am opening the app again or
the class app nothing is going to happen so why is that and well we're looking at
it right now we haven't set a tracing for the weight meaning I want to duplicate this line
when I'm updating the weight load using Trace as soon as the value updates
I want to call the update BMI method so now if I run this and I click on Plus
we are once again updating the BMI value it's looking really good also the slider
still works just fine now this video is getting a bit longer and I can't think of a good exercise I guess what you
should be doing is definitely understand how this tracing method here works and why it is important it's a really
important thing to understand because this one allows us to work inside of these widgets by simply passing in any
of these variables and as soon as we are making any kind of change all of that will be captured by
these two tracing methods that keeps all of this much more organized so definitely have a look and see how this
works at this point we have a reasonably working app which means I can click on
the buttons to get a higher weight and I can also move the slider to get a different kind of height on top of that
we get an updated BMI number all of that is working just fine however what we don't have is the weight and the height
being updated which makes the app feel a bit weird and this is what I want to work on now for now I'm just going to
work with metric units but later on we will also add the switch the one up here to switch to Imperial units as always
I'm starting in bmi.pi and we have to work Ivan side weight input or height
input depending on what we want to start with let's say I want to start with the height input
the order here really does not matter what we have to do inside of this one we have to update this output text here for
that I have created another text variable I called it self dot output
string this is going to be a ctk and string VAR without any starting value
although inside of the output text I want to set this as the text variable
meaning text variable is going to be self and output string if I run the thing now we can see that we can't see
the text anymore so this text here is gone to make it reappear I want to create another method I call this one
update text besides self we are also going to need an amount so what amount
do we want to set for the height for now let me simply print the amount
the way we are going to use this is inside of this slider I'm going to add a command let me do it all the way at the
top the command is going to be a function which is going to be self and update text
since the command for the slider automatically inserts one argument which is the amount on the slider we get the
amount here right away if I run this now and move the slider I'm getting the current height that's
looking really good once again we are getting a huge amount of floating Point numbers so all of this but well we can
simply ignore it it doesn't matter for our purposes this number I now have to convert to meters for example if I get
182 centimeters this is what I would be getting from a slider not centimeters
but just 182 and that I want to convert to 1.82 and meters all of this needs to
be one string for that first of all I have to convert the amount to a string let's call it text string
and all I'm going to do is turn the amount into a string also while we're
here I want to turn the amount itself into an integer that way we get rid of the floating Point numbers they are
going to be a bit annoying once we have that I want to have the meter and the centimeter and the
conversion here is really simple because for example if we have once again 182
this would be the string right now I simply want to get the first digit
this works reliably because my slider only goes from 100 to 250 meaning we go
from 1 meter to 2.5 meters it is literally not possible to be below 1 meter or greater than 10 meters
which means this first digit is always going to be the meter to get this one I want to get the text string and simply
get the first element which isn't going to be 1 but a zero
next up for the centimeters I want to get my text string again and now I'm going to go from the first element all
the way to the end with that I have my meter in centimeter so now I simply have to update self dot output string using
the set method and then here I have to add an F string the F string needs the
meters meter in here then I want to have a DOT after that I want to have the
centimeters and finally I want to add the units so meter at the end with that I can run the entire thing
again by default we can't see anything I will fix that in just a second but if I move the slider we can see the meters
being properly updated that's looking really good to see the text right when the app is starting we simply have to
call this method somewhere after we have created this output string
let me do it right after self dot update text and really
important in here we have to add the amount if we are calling update text inside of a slider this amount is added
automatically but if we don't do it and just call it by itself we have to edit manually this fortunately is quite easy
to do because we know the current height we're getting this from the height int let me copy it paste it in here and all
I have to do is get and then we should be good to go now if I run this we can see 1.7 meter by default and I can
update this this is working just fine with that we have finished the height
input now we can work on the weight input for this one we have to follow is
somewhat similar logic compared to what we have done in the height input which means this
label here is going to get a text variable once we have that we can use update weight we already have a method
for that to update the number as well since this should be reasonably
straightforward it's going to be an exercise I want you guys to update the text to display the current weight pause
the video now and try to figure this one out
first of all I once again am going to need another output string
which is going to be ctk dot stringvar this we now have to connect to the label
which we can do very easily I want to have a text variable which is going to be self dot output string with this
output string we don't actually need to text anymore I can simply get rid of it
I should also do the same thing for the height input just to keep things a bit cleaner this text 1.8 meter we don't
need any more back to the weight input now that we have this output string and we have
connected it to the label if I run the app we shouldn't see any text anymore and we don't that's working just fine
next up we have to work inside of update weight to actually update the text label
and for that I want to call this method right when the app is started which
means after I've created this output string I want to call self.update White
if I run this we are going to get an error this error happens down here
because right now info is going to be none and we are trying to get the index
on none which doesn't work to fix that error I have to put all of this stuff here inside of an if
statement that if info exists only then do I want to do all of this
and with that I can run this again we still can see the text but at the very least the app isn't crashing anymore
however what I can do now after the if statement set the output
string what I want to have in here is some kind of string that looks like
let's say 80.1 kilogram the weight I already have because I have
the weight float which means I can get rid of this string here replace it with an F string
I want to get myself dot weight underscore float and let's just see what
happens we are getting the name of the ticket variable because I forgot the get
method if I run this now and click on the button this one is working just fine
for full kilograms however if I click on the small buttons this seems working up there we go
now we have way too many numbers after the decimal point although this we can fix fairly easily
all we have to do is round the weight let's say with one decimal point now if
I run this the kilogram buttons so the larger buttons still work perfectly fine
and on top of that the small buttons should also be working totally fine now and this is looking really good
although there's one thing I have to add and that is the kilogram afterwards now
if I run this we have kilograms although the rest of the buttons still work just
fine all right and with that I can minimize
or before I want to get rid of the exercise text and let me add a comment here for output
logic now I can minimize the weight input fix the white space and we have
covered another important part to finish the app I want to activate the button up
here so we can switch between metric and imperial units for now we only work with
metric ones so meter and kilogram but obviously for Americans and British
people this isn't going to work the logic fault of this one isn't complicated I just have to talk about a
couple of formulas to convert kilogram to pounds and ounces and meters to inches and feet shouldn't be too
difficult let's Jump Right In back at my code there's one thing I want to do inside of the app to get started and
that is I want to add one more variable to my data I guess we can do it right at
the top I want to create self dot metric and this is a Boolean
which I create with ctk and Boolean VAR the default value here should be true
this metric Boolean we're going to pass into the white input and the height input to change the units and into the
unit switcher to control it let's get started with the unit switcher and here I want to pass in the metric Boolean
with that I can minimize the app for now and work on the unit switcher because in here we are going to have some important
logic we have to start by adding a second parameter I got this one the metric pool
this we have to turn into a parameter right away self dot metric pool is going to be
metric pool what we now have to figure out is how to turn this unit switcher into a button
which actually is quite simple all we have to do is use bind so we have to use
events the one event I care about is called button this is simply a mouse button click if
that is the case I want to run a method that I called change units
this one doesn't exist right now let's create it right away change units and
here we need self and we need the event although the event we are going to ignore entirely in here we have to do
two things number one we have to change the metric rule
meaning if it is currently true then we want to set it to false and vice versa
this is very easily achieved all we have to do is get self dot metric boole and
then set it with a new value since we only have true or false we are working with Boolean values the new
value is simply going to be not self dot metric Bool dot get if this value is
true right now the not is going to turn it into false and if this value will be false then not
would make it a true value that way we can have the entire logic in a single line of code which is quite
handy next up we have to update the text that is also
going to be fairly simple I want to check if self dot metricpool dot get if
this is true then I know I am using metric units which I can use with the configure
method to update the text to metric however if that is not the case
else I want to configure the text as well let me just copy it except now the
units are going to be Imperial with that we should already have a basic start let me run the app and now if I
click on Metric we get Imperial if I click on Imperial we get metric we essentially created our own button with
that I can minimize the unit switcher and not worry about it again although the white space here does annoy me
back in the app I now have to work either on the weight
input or on the height input let's get started with the height input in here I have to pass in the metric boole
and for that let me minimize the app again and work on the height input we
are now going to need another parameter metric rule this one absolutely has to
be an attribute let's do that right at the top self dot metric pool is going to be the metric
Boolean although we are not going to use it anymore inside of the init method we are only going to care about it inside
of update text because in here I only want to do all of this if metric pool is
true so if self.metric pool dot get if that is the case I know I am using
metric values but if that is not the case so else then I'm using imperial
units for that I have to figure out feed and inches right now we have the
centimeters inside of our amount for example the value we start with is a hundred and seventy and this would be
centimeters these 170 centimeters I now want to convert to inches the formula to
get an inch from centimeters would be one
centimeter divided by 2.54
that's literally it it's not terribly difficult next up to get two feet
we have to get one inch and divide it by 12.
these are all the units that we are going to need all of this can actually be done in a single line of code
how I approach this first of all I want to get the amount and divide it by 2.54
this would simply give me the inches but what I can do now is to use diff mod and
then add a second argument which is going to be a 12. for example right now we are starting
with 170 and 170 divided by
2.54 would be almost 67. what div mode
is then doing is divide this entire thing by 12. so divided by 12 which
would be giving us a 5 and then point let's say almost 0.7
both of these numbers we are getting separately which is literally all we need to
convert centimeters to feet and inches as a matter of fact to make sure this is working let me
print feed and inches now if I run this again
I have to click on metric to get imperial units and now if I move the slider
we are getting some units the text doesn't update anymore but at the very least in the bottom you can see that
this seems to be working just fine to actually make it visible I want to duplicate this line here because I want
to set the output string but this isn't going to be meters and centimeters anymore
instead I want to have my feet the short end units for this is a single quotation
mark which is going to confuse python so we have to add the Escape character this one here ensures that we can only
see the quotation mark or the single quotation mark after we have that I want to add the
inches and for this we need a double quotation mark and just to make sure that this isn't
confusing to python I want to add the Escape character as well way of that we should be seeing
something if I now go to metric and update all of this we can see that
well we get a whole bunch of numbers the issue once again is we have a huge
amount of numbers after the decimal point to account for that I want to wrap both of those into an INT function
and now let's try this again I have to click on Metric
to get Imperial and now I get the feet and inches
this is going to give us the basic logic so we have a good start however you
might have already noticed there's one problem I can update the meters individually and if I now click on
Metric I get Imperial however the meteors right now are still visible only
once I update the slider do I get to the feet and inches so the issue is only when I'm moving the
slider do I run this method here you get the different kind of units if I simply click on the unit switcher
nothing is going to happen let's work on this one next this is going to happen once again inside of the
app in here I want to use tracing one more time
I want to get my metric Boolean and once again I want to trace and check if the
value is changing if that is the case I want to call a method I called change
units this one doesn't exist right now let's create it right away
change units in here we need self and we need the arcs
although once again I'm going to ignore them entirely inside of this method I want to run a
method on the height input which isn't possible right now because I didn't turn this instance of the class into an
attribute although that I can change quite easily I want to have this as the height
underscore input now I can access this self dot hide
input the method I want to use is called update
text I believe I called it let's check inside of height input I have this update text method this is
what I want to use this one wants one argument and that is
the current height which we do have available inside of this height integer
let me copy it and simply pass it in here with the get method with that this
should be working now I can still update the height but if I click on Metric I
now immediately get the imperial units I can still update them just fine and if I return to metric I am back to meters
with that we have finished the height input so next up we can work on the weight input
for this one like for the hive we first of all need another parameter which is going to be the metric Boolean
this we have to pass into it when we create the instance so in here self dot
metric pool and let me minimize the class app so I
have a bit more space first of all I want to turn the metric pool into an attribute self dot metric
pool will be the metric Boolean after that I don't need the dunder init
method anymore because the entirety of the logic is going to happen inside of update weight
in here I still want to check if the info exists however now the amount I
want to have a bit more flexibly what that means is I want to check if
self dot metric bull is true
and only if that is the case I want to increase the amount by one or by 0.1
it also be the sensible units for kilogram however if that is not the case
I want to use Imperial units once again the units for this one would be pounds and ounces
for that once again we have to talk about units I am once again starting with one kilogram or 0.1 kilogram
and I'm not really going to convert them instead what I'm going to do is I'm going to increase the pounds by one
pound one pound is
0.453592 kilogram a g at the end to get two ounces we simply let me write
ounce in here all we have to do is get one pound and divide it by 16.
since the units are actually fairly simple all I really have to do in here is get my amount and by default this is
going to be one pound which would be 0.453592 kilogram this I only want to
get if info 1 is equal to large which
should be a string if that is not the case so else I want to get this same number and divide it by 16. with that
I'm either getting one pound or one ounce except I'm expressing them in
terms of kilograms and grams that is actually the entire trick for how this logic is going to work I am
always working in metric units like kilograms or meters and centimeters except for the front end I'm converting
these numbers either to metric units or to Imperial units because of that this logic here can stay exactly identical we
simply change the amount that we are working with however at the bottom we have to make a
few more updates because right now we are only working with metric units to update this one
I want you guys to do an exercise I want you guys to do some research and
get the proper output for both metric and imperial units meaning we either want to have kilogram
this we already get and if we're using imperial units I want to display the pounds and the ounces
parts of you now and try to figure this one out
the first step that we have to do is we have to check if we are using metric or
imperial units which we get with self dot metric Bool dot get
if that is the case I know I'm using metric units so this line here can stay identical
if that is not the case and I forgot the if statement here if that is not the case so else then I want
to use imperial units which means what we now have to figure out is how to get the pounds and the
ounces the function we can use here is divmod once again
however for that we will need just the ounces which we don't have right now
because this is what we are trying to get although once we have the answers we simply have to divide them by 16 and
then the remainder will be the ounces that are left now how can we get the answers first of
all well for that I want to add another variable let me call it the raw ounces
for that first of all I want to get the current weight so self dot weight
load and get this would get me the kilogram to turn this into pounds I want
to multiply this with 2.20462 and just in case you're confused if we
have one kilogram this would be
0.45 pounds this is what we have done here however what we do down here is the
reverse so we have one pound and that is going to be
2.2 kilogram also I forgot the G here that needs to be there
with this we would have the pounds to get to the ounces we have to multiply this by 16 because remember they are 16
ounces inside of one pound with that we have all the ounces that we need and this is what I want to use div
mod with once I have that I can simply get my output string and set a new value
for this one we need an F string we first of all want to have the pounds
with lb afterwards then a white space and then we get the ounces
the short end for that is Oz now let's try this
if I now click on Imperial we can still see the kilogram but if I click on a button we now get something else
once again the issue is that the rounding here creates way too many numbers to fix that
I want to turn both of these numbers into integers and now let's try this again I click on Imperial and now if I
click on a button this is looking much better so I can change the answers and
the kilogram with that I can get rid of the exercise text we don't need it anymore in fact I
can minimize update weight entirely the last thing that I have to do inside of the app when I am calling change
units I also want to update the weight input for that I first of all have to
create an attribute self dot weight input is going to be one instance of the class
now that I have that inside of change units I want to get self dot weight input
the method I want to call if I scroll down a tiny bit is simply update weight
this works because inside of here we are only updating the units if we have information but by default this is none
so if we call it the method by itself without any arguments it is simply going to run this bit down here which is all
we need meaning in here update wait with that we
should be done I can now click on plus and minus 40 kilogram I can update the
height in meters and now if I click on Imperial we get pounds and ounces and we
get feet and inches all of those we can update quite easily this seems to be
working just fine and we also get the PMI updated so with
that we have finished another app let's get started by working on the calculator you can see the result already it is
very much inspired by the iOS calculator although for the most part let me show my mouse I can simply add any kind of
calculation in here and I would get a result I can also clear the entire thing and on top of that I have the plus and
minus button from the iOS calculator and the percentage sign other than that it's well a calculator there are two major
changes compared to the original calculator the first one is on the top we now have the formula that we have
typed in which I think is really annoying that this doesn't exist in the original calculator this is quite easy
to add the other change I made is that besides the dark mode we also have a light mode
it works in exactly the same way but if your system settings are light then you're going to get a much brighter
calculator which fits much better into the system overall all of this will be covered in this section and there really
isn't terribly much that is complicated to work on the one slight complication is that we have to create a lot of
buttons and most of these buttons have some slight difference in functionality for that we're going to work quite a bit
with inheritance but I'll talk about that more when we get to it for now I
want to set up a basic window but before we get to that I want to talk about the folder we have because this one is
slightly more elaborate before that I'll be starting with is going to look something like this in here we have calculated.pi and
settings.pi in terms of python settings.pi is going to contain already quite a bit but all of these are just
settings so what the calculator will look like and where the buttons are going to be I'll shake it up on in just
a second the entirety of the logic though is going to be inside of calculated.pi right now this one is
completely empty besides that we have empty.ico I'm using this one to hide the icon that's literally all it does
finally we have one folder called images if I open this one in here we have four
Images one for division and one for the inversion I think this is we always have
one for dark mode and one for light mode the reason why we need those four buttons is because the character doesn't
exist in the normal alphabet as a consequence when I'm creating these buttons I would have an image and then
use this image for the button that covers the setup let's have a look at all of this in code here you can see
calculated.pi it is completely empty besides that I have settings let me scroll to the top and here we do have
quite a bit more I start with some basic sizing information this is giving us the
app size and how many rows and columns I have after that we have some text information so the font and the font
size then I have a tiny bit on styling and all of that is fairly simple the
really important bit here are these three dictionaries because they contain the position and some additional
information about the buttons for example this entry here is for the button number two this button should be
in column 1 Row 5 and span one cell or this entry here for example this is for
the multiplication button this one is in column three Row 3 it shows the character X for multiplication but the
operation is going to be multiplication that's this sign here I'll explain all of that later finally all the way at the
bottom we have a huge amount of colors this part should be fairly straightforward
now inside settings.pi we are not going to add any logic all of that is going to
be inside of the calculator speaking of let's create a basic window this I want to do with custom tkinder
which means I want to import cast term T Kinder s c d k once I have that I want
to create a class that I called Chi Q later you could call it whatever you
want but I guess calculator makes sense here this one needs to inherit from ctk and c t k
first of all in here we have to create a dender in it method with self but no other parameters finally the first
argument we always need is the super Dunder init method to initiate the parent with that we have a basic object but to
see the actual window we have to add one more line this would be self and Main Loop don't forget to call it with that
we're going to have a window that we can at the very least see all we have to do is create an instance of this calculator
with that we have a basic window this one looks pretty good although I do want
to customize this quite a bit while I'm doing this I also want to be conscious of light and dark modes meaning for now
if the system settings are light then I want to have a white-ish background if the system settings are dark then I want
to have a black background for that first of all we have to detect if the user is using a light mode or a dark
mode for that we have to import dark the detect we can use this one let me put it
above the calculator I want to print dark detect and then the method is dark
don't forget to call it now if I run the code I get true because in my case I'm using the dark mode however
if I go to my system settings and I switch from dark mode to light mode and
return to my code I can run this thing again and now this is going to be false which means I now am aware if the user
is using dark mode or a light mode in my case I'm going to stick to dark mode but I will switch around quite a
bit back in here I want to go back to dark mode to account for all of this inside of the
app I want to add a second parameter that I called is dark with that I can
simply pass all of this into the calculator and then I know if the user
is using dark mode and light mode and I can account for that inside of this class although before that I want to add one
more if statement this if statement is going to check if the name is equal to
Dunder Main only then do I want to create an instance of the calculator the result is
going to be the same but that way we prevent any kind of code not inside of this file to cause some accidental
errors once we have that we can actually come to customizing the calculator itself let me put all of this inside of
a setup section and in here we have to add quite a few more things number one I want to set the
appearance to dark or light depending on is dark if this is dark is true then I
want to call the dark mode if it is false then I want to call the light mode besides that number two I want to set
the f g color and set this to white or black depending on the light mode or the
dark mode these two colors you can get from the settings because all the way at the bottom we have black and white black
is pure black white is not perfect White if you understand the hexadecimal colors
here you can see that this is almost perfect white but not exactly these two colors you should be using
number three get the start window size from the settings and disable window
resizing to start window size you can get also from settings in here finally number
four hide the title and the icon I want you guys let me resize this a
tiny bit this stuff here should disappear these four things should be fairly
straightforward as a consequence this is going to be an exercise pause the video
now and try to implement this one yourself
number one for this one I need ctk and then set underscore
appearance underscore moat this one is expecting either dark or light which
means if I run it like this we get light mode if I run it with dark we get the dark mode
this entry I want to make dependent on is Stark which I do with an F string I
want to have dark if is dark is true if that is not the
case else then I want to have light let's try this one and it's looking pretty good
next up I want to update the FG color this has to happen inside of the super
internet method in here I need an FG color since we have a color for the
light and the dark mode we need a tuple in here the first argument is going to
be for the light mode the second for the dark mode which means with a tuple white and black I can run this again
and we're getting an error because white is not defined that is happening because we're not importing settings that we can
change quite easily I want from settings import everything if I fix my typo this should be working
there we go now you can see the background color is completely black before this was a dark gray number three
I want to set the start window size and also disable window resizing to set the start size I want to use self
dot geometry this one wants a string something like 400 times 600. however inside of the
settings we have a tuple with the app size let me copy this one right away actually
to get this one I want to replace the 400 with curly brackets in here I want app size and the
entry zero then I can copy all of this and replace the 600 with app size and
one now if I run this we have a much larger window besides that I want to disable
window resizing this I get with self dot resizer bill
the arguments here are false and false those cover the horizontal and the
vertical axis now if I run this let me show my mouse I can try to resize the window it simply
doesn't work for the final part I want to write the title and the icon the title is the
easier bit for this I need self.title and an empty string running this again
now on the top left we don't have a title anymore to hide the icon we need self and I can
bid map this is going to import an icon that we're going to set as the icon for the
app for this one I have empty dot Ico if I run this one now there we go in the
top left we have nothing anymore which looks significantly cleaner this also covers the exercise let me get rid of
all of the comments because they are getting a bit tedious that is much better for the final part
if I run the app again I want to color the title bar because right now this bit
up here looks a bit weird it doesn't fit at all with the rest of the app which
means I want to create another method that I called
title bar color for the parameters we need self and I want to pass is dark in
here in here we can now run some code to color the title bar however for that we
have to import a few more things also since this is only going to work on Windows I want to wrap all of this
inside of a try statement that way on a Mac we at least don't get an error I
want from C types import Wind dll by ref
size off and finally C underscore int however if we're getting an error so
accept then I want to run pass so nothing at all with that inside of title bar color the
method I want to create another try statement because in here I can now run
the code to color the title bar for that first of all I want to create a
variable that iOS call hwnd this we get with win dll user 32
and then get parent to get the parent we need the ID of the
current app which we get with W info underscore ID do not forget to call this
one next up we need to dwm dwa underscore attribute which is simply going to be
35. the one important difference here in the earlier tutorials I always add a single
color well we still have a single variable but this variable now is either going to
have the hex color for let me open inside of settings we have either the dark color or the light color
which means we have to add an if statement in there I want to copy the title bar hex colors
I want to get dark but only if is Stark is true if that is not the case else
then I want to get title bar hex colors with the light color
well I think that's what I called it yeah light color that gives us all we need which means
finally I have to call win dll dwm API now we get to the long one
capital d w m set window attribute
for this one we want to Target the window which is awnd then I want to get the dwma attribute
after that I have to add the color except I have to convert it a tiny bit for that we have five ref then C
underscore end and this one is getting the color
for the last argument we need size off and then C underscore int
that should be all we need for this one although the last bit is we have to add
an accept statement which is not going to do anything with that all I have to do now is called
self title bar color and pass is dark in here
if it runs now we're getting an error that is because I forgot the if
statement in here now if I run this again this is looking much better
on top of that what I can do I can set this is Stark to false to check the
light mode so if I run this now we have the light mode although I want to keep on working with
the dark mode which still is working just fine with that I can minimize everything
because this covers the first part we have our window now that we have a
basic window we can start working on the elements that are actually visible there are going to be quite a few what I want
to start with let me type a tiny bit in here actually let's say something like this what I
want to start with I want to have this text here and this text here although for now they are not
going to do anything I just want to have the basic widget later on they will become Interactive
back in my code I want to keep on working inside of the calculator the first thing I have to do in here is
I have to create a layout because without that we can't add any widgets I
want to use a grid layout in fact let me talk about how this is
going to work the grid layout is going to be well a grid
for this app I want to have seven rows and I want to have four columns
The Columns should be fairly straightforward we have column 0 column one column two and column three
for the rows this part here is also quite easy to understand this would be row number six five four
three and two after that and those columns you can't
really see we have these columns here one is looking something like this for
the main output this would be row number one and finally we have all the way the top row number
zero those numbers I'm actually getting from the settings if I scroll up here we have
main rows and Main columns those I want to use to create all of these columns
and rows dynamically although for that first of all I have to start with self and row
configure what I ultimately want to get in here is zero one two three four five and six all
with the same weight of one also I want to have uniform and set this to a
the thing that I have to create dynamically is this list here for that I'm going to use the range
function and pass my main rows in here
I think that's what I called it main rows I'm using this variable here this by itself is not going to work
because row configure is expecting a tuple or a list whereas this range is going to give us a range object but this
we can convert to a list or a tuple and then we have the proper outcome with that I can duplicate the line
because besides a row I also want to have a column the only difference now is going to be
that I'm not going to use main rows instead I will be using main columns
or at least that's what I think I called it yeah main columns I can now run the app and well we can't
really see a result but now we have a grid that we can work with to organize the text I want to create a separate
class which means I want to minimize the calculator and create a class that I
called output label since this is just going to be a label
I'm going to inherit from ctk label other than that we need a dender init
method and this one for now is just going to be self and parent after that as always we need this super
in Niche method first of all I want to set the master to whatever the parent is
after that I want to set the text so we can see something let's say I'm just
going to type one two three in here next up we have to place this output label
since we're using the grid layout this has to be a grid in here we have a
column which is always going to be zero after that I want to set the column span which
is going to be 4. after that we have to specify the row and the row has to be more flexible
because this output label we are going to use twice once for the formula and
then for the actual output as a consequence we cannot hard code the row this we have to get from the parameters
which means I want to add the row in here and pass it to the grid method once we have that inside of the calculator
I can start creating some basic widgets
although later on we're going to create a huge amount of widgets as a consequence I want to have a separate
method to create the widgets I'll call it create widgets
so I need a method called create widgets with self and nothing else in here for
now I'm going to create the labels or to be a bit more specific the output
labels for this one I want to create an output label
with for now I will need a parent and a row the parent is always going to be
self the first label is going to be in row 0. after that I want to have the
exact same output label except this one should be in row 1. with that if I run the app we can see we
have one two three twice although the positioning here is not ideal if I draw
this one in we have one cell here and we have a second cell here just imagine
that I'm able to draw straight lines the first minute I want to do is I want to move this one two three here the
first one to the bottom right it should be somewhere here
the other one two three this one here should only be moved all the way to the
right which means it should at the end be somewhere here
that way later on once we have larger font sizes they are properly filling the entire available space in a proper way
also to achieve this kind of thing this is going to be your exercise I want you
guys to update this class so you can control on what corner the label is going to be
I suppose I should be adding this in text the exercise is going to be update
the class so you can control which corner the label is attached to pause the video now and try to figure
this one out the argument that we need inside of
self.grid is called sticky this one tells the label which side to stick to
in here for example we can set this to e and then our text is going to stick all
the way to the right however since I want each label to stick to a different site I want to set this
via the parameter let's call this one the anchor
this I want to pass through to the Anchor now for both of these we need one
more argument in here for the first output label let me actually add a comment here this is
going to be for the formula this one should stick to the south east
or the bottom right whereas the result
should only stick to the east side now if I run this again you still can
see much of a difference but well we will be getting there we make this a tiny bit more visual the
first cell would be something like this well the second cell would be looking
roughly like this before I'm continuing I'm going to get rid of this text here we don't need it
anymore on top of that I want to set some horizontal padding of 10 pixels that way the text isn't completely
attached to the right side anymore what we have to do now is add a font so a text here looks significantly better
unfortunately we couldn't just create a font inside of the output label
for one because these two labels need a different font because they're different text sizes on top of that later on I
want to reuse the font for the formula for the buttons as well as a consequence I want to create my
fonts inside of the create widget method that way I can pass them into the output labels and later on into the buttons
the first bond is going to be I call this one the main font because this is
what I'm going to use the most we are creating this one with ctk and ctk bond in here we need a family and we
need a size the family we're getting both from settings the family is always going to be the font I
can pass this one in here next up for this size I want to use the normal font size
this in here and then we're good to go this main font I'm going to use for the formula and for all of the buttons
besides that I want to have a result Bond or this one I can simply duplicate this
line here because most of it stays the same the one difference is that I now want to use
the output font size instead of the normal font size that is giving me two fonts and those I
want to pass into the formula which is going to get the main font the output
label for the result is going to get the result font once we have that inside of the output
label we now need one more parameter that I called the font
this font we now have to pass into the Super init method in here font is equal
to font now if I run this again that is time to come together much nicer
the last thing that I want to do is that right now both the output labels are simply displaying text one two three
this has to become a tiny bit more interactive although for now we're not going to use it
for that inside of the initi method before I'm creating the widgets I want
to add another section that I called Data in here I'm going to create two string
variables first of all I want to create self dot result string this is a string so ctk
string VAR the default value for this one should be a string of zero this is what we should
be seeing by default after that I can duplicate this because next up I want to have another string
VAR or the formula although this one for the default value
has simply nothing basically later on when we have actual functionality the results string is
going to get the result we see from any kind of calculation and the formula is going to well give us the formula
these two string vars I now want to pass into these output labels and set them as
the text variable for each of the label which means for the output label for the
formula the final argument is going to be self Dot formula string
whereas for the result label we need self dot result
string because of that we will need one more parameter let's call it the string
VAR this string bar I want to set as the text variable which is going to be the
string VAR with that if I run all of this again we can see 0 for the result
and nothing for the formula to make sure this is working let me add test for the
formula and we have test so this is definitely working also because of the text variable this
text is now redundant meaning we can get rid of it entirely to make all of this a bit cleaner with that we have finished
the output label which means I can minimize everything because this covers a really important
part next up we can start working on the buttons this is going to be a larger
section now that we have the labels we can start working on the buttons for that we need quite a bit for the
simple reason that we have a lot of different buttons just to go for them really quick we are
going to have these number buttons here those are going to give us the numbers from 0 to 9 and the DOT besides that we
have the math buttons those are divide multiply minus and plus and the result
button I also added in here at the end we have these are called the operator buttons those are clear invert and
percentage sign all of these work in slightly different ways so we have to account for that
on top of that what is also quite important is that for the division button and the invert button we have
images instead of text this we also have to account for as a consequence I will create quite a
few different classes for the buttons and then work with that should be a really good practice for
inheritance but let's Jump Right In and let's have a look at all of this back in calculated.pi I first of all want to get
rid of this white space because it annoyed me now since we're going to create quite a few different buttons I'm going to store
the logic in a separate python file meaning I want to with control and N create a new file and save this one with
Ctrl and S this file I'm going to call buttons dot Pi we are still going to use
custom tkinter but we only need one class which means I want from Custom
tkinter import ctk button this is the only part of custom
decanter I am going to need although besides that I am also needing from settings import everything to get
started in here I want to create a class that I called button it should also
start with a capital letter this one since we are simply going to create a button I want to inherit from ctk and
button importantly here you do not have to add ctk at the beginning because now
we are importing a ctk button straight away for this one first of all I want to have
a thunder init method this one itself we need a parent
we need some text then we need a column and a row separated by a comma
and that is all I'm going to use for now I should also specify for now I am going
to create this AC button and the percentage sign those are going to be
basically the simplest buttons that we are going to have to create those inside
of this thunder in the method for the button I have to call Super and thunder init as
always in here I will need quite a few different arguments so let me use named
ones I want to have the master which is going to be the parent
next up text is going to be text that is all we need for this super init
method to place the button I want to call Self dot grid this one is going to get column with
call and row is going to be the row we are simply passing these two
parameters in here and here besides that I also want to make sure that the button
sticks to all of the sides which means I want to use sticky and north south east and west
this is going to give us an incredibly simple button that we can use which means back in calculated.pi
I want all the way at the top below custom decanter from buttons I want to
import for now only the button if I run the code now this is not
crashing so at the very least we know that this is kind of working which means now inside of the calculator
I can minimize the init method and the title bar color we also don't need
instead I want to create the AC button which is going to be the clear button
let me type it like this that's a bit clearer this is going to be simply a
button which is the button we just created for this button we're going to need a
bunch of arguments to cover all of these parameters let me copy them actually and
paste them in here we definitely want to use named arguments because later on they're going to be a lot more arguments
in here first of all the parent is easy this is going to be self
for the text for now I simply want to have AC the column for this one is going to be
zero the row is going to be 2. with that if I run the code
we are getting an error because I stopped using the keywords this should be column
this should be row not a stratus and there we go we have the first button it
doesn't do anything right now but at the very least we have something although there's already one thing I do
have to change because the text the column and the row I want
to get from the settings this is really important I want to work with this
operator dictionary in here we have the clear button and this has the column the row the text and
if we add an image it would also have an image path the clear button doesn't have one but the invert one does have one
this kind of setup is really important because I want to make sure for The Styling and the layout of my button all
of this is organized separately that way I can make any kind of change in here and it would be reflected inside of the
calculator or anything more complicated you do want to separate the logic and the layout
makes it much easier to work with a more complex program all right I want to get the operators
use the operators inside of my button as a matter of fact let me put all of this
over multiple lines so it's going to be easier to read first of all I want to get the operators
in here the button I'm working on is clear this one here this is going to give me
another dictionary inside of this dictionary I have the keys column row and text
I want to have the text then I can copy all of this for the
column instead of text this should be call finally for the row the text should be
row if I run this now we cannot see a difference because we have used the same
data but now inside of settings I could make an update here and it would be reflected in the app
just to test this let me rename AC to something
run the calculator again and now we get something meaning all of this is at the very least
working but now obviously if I run this again this button doesn't look very good we
have to make a few more changes here inside of the button we have to do a couple of things
a very easy thing to work on is to set a corner radius
this corner radius we're getting from the settings in here we have styling
I want to get my styling this is another dictionary inside of
this styling we have Corner radius with that if I run this again now we
have no more Corner radii another important thing is I want to add a font
this font we already have which means I can set this to font and get my font via
the parameters this I can do because inside of the calculator we have created two fonts all the way up here I want to
use the main font for this button as well which means I can copy it
for this button I want to set a font to my main font now if I run this we have a
much better looking text what we now have to work on is the color for that I want to have another
parameter and let me explain how the colors are going to work inside of settings at the
bottom there are a whole bunch of colors the color we will use for now is dark
gray this is the color I generally want to use for the operator buttons we have
a foreground color we have a hover color and we have a text color
these colors are always going to be two birds for example for the FG color we have this Tuple here one is for the
light mode the other is for the dark mode this applies to all of the colors we always have a tuple with two
different colors which means when I'm assigning the color here I can simply pass in a default
argument with dark gray although this by itself isn't going to do anything I can run the code again we
cannot see this color do account for that when we are running the super init method we have to add
quite a bit more for example if I want to get the FG color
I want to get from my settings I want to have the colors paste this in here this
colors is a dictionary all of this stuff here I now want to get one entry in here
which is going to be dark gray this dark gray I am getting via my color this one
up here so all I have to do is pass this into this dictionary with the color
with that I am inside of another dictionary in here I want to get the FG
which is the foreground color which means another dictionary with FG
and now I can run the calculator again and there we go this is looking much better if I hover over it we still get a
bad color but at the very least we're making progress on top of that if I now switch to the light mode
meaning if I set a stark to false we also get an updated color although we
do have to work on a text color let me revert this and now we can keep on working inside of buttons and make a
few more changes besides the FG color I also want to set the hover color and the text color
which is fairly easy to do I want to have the hover color which is going to be the same thing we
have done before all of this except now we don't want to use FG instead I'm
going to use hover hover in here without any white space and now if I run this again show my
mouse the basic color still works if I have over it basically the same thing just a tiny bit brighter but it
certainly works finally I want to have the text color
which once again is going to be basically identical I want to copy this
one and now this shouldn't be hover this should be text or at least I think that's what I called it yeah and here we
have text now if I run this this is still looking good
other should also work this is looking nice you can mostly see this when I switch to
the light mode meaning this one should be false again now this button is much more visible
I still want to use the dark mode and with that we have one of the buttons at
least to an extent the problem we have right now is that this button doesn't do anything which is not ideal for a button
to account for that to get started inside of the button I want to have let
me put it right beside text I want to pass in a function
which the button is then going to call to connect this one to the button we have to give this button a command which
is going to be the function with that we just going to need a function we can pass into this button
since this is going to be the clear button I want to create one method inside of the calculator
which are called clear this will not get any parameters and for now I simply want
to print Lear once we have that inside of this button I want to add another named argument the
function is going to be self.clear really important here do not call this
function we just pass in the function around we're not calling it yet this is only going to happen once we click on
the button in fact let's try this one now if I click on the AC button we can see clear
inside of the code editor so this is working quite well this is
going to give us one button there is a second button we can create right away
I call this button the percentage button if I run the entire thing again the
button I want to create now is this one here since this should be reasonably easy
this is going to be your exercise I want you guys to create the percentage button
and you have all you need pause the video now and try to figure this one out
for the percentage button we are going to use the same button class meaning I
can just copy all of this and paste it in here we just have to make some updates
the most important one or the most visible ones are the text the column and the row
this information if I look inside of settings we can get from the operator dictionary because in here we have
percent to access all of that all we have to do inside of the button I want to replace
this clear with percent if I run this now we have the percentage
button also works with the hover so this was really easy to add the main font we are also going to use
the only other change that we have to make is this function because well this
button is not going to clear the calculator it is going to let's call it the percent
which needs cell for now and in here we're going to print percent once again this button isn't
going to do anything for now we are just working on the UI I have to replace clear with percent and
then test all of this I have the AC button this one still says clear and the percentage button says percent alrighty
with that we have two buttons definitely some progress
at this point we have two buttons this one and this one both of those are using
text next up I want to create this invert button here and this one is
different because it uses an image instead of text for that I'm going to create a separate class
although for the most part it is going to be quite similar compared to the other buttons let's Jump Right In and
let's have a look at this one back inside of calculated.pi let me run this again we have two buttons not a bad
start but we need a bit more inside of buttons.pi
I want to create another class which I called image button
this one once again has to inherit from ctk button we need it under image method
with self we need a parent and then well we are going to need a lot
of the stuff up here as a matter of fact let me just copy it all in terms of changes this one does
not need a font but we do need an image this image we're going to create inside
of the calculator which means we don't have to create it in here once we have all of that
I have to create a super Dunder init method
with the usual stuff as a matter of fact I can copy all of
the stuff I created up here and simply paste it down here
with that I can get rid of the font but I do have to replace it with an image
which is going to be the image we're getting from the parameters also let me put it up here so if the
styling all together once we have that I want to place this button using the grid method which once
again is going to be very similar compared to this grid method so I can simply copy the entire thing
and we don't have to change very much while I'm here I did realize I forgot
one thing and that is inside of settings if I go up a bit we have a gap this Gap
I haven't used right now but I do want to use it which I can do by adding pad X is going
to be styling and this one I called Gap at least I think I did yeah Gap
this is going to be pad X and will also be pad y
which I want to do both for the image button and for the normal button this
one up here they both got this kind of padding it's not going to be visible for now but later on it is going to be this
tiny black line between the buttons with that I can minimize the button and
now for the image button we are basically good to go what we have to do now is actually use
this button which is going to happen inside of the calculator.pi file in here first of all I have to import this
button which means image button with that we can use it if I run this we can
certainly import it the program doesn't crash now inside of the calculator I don't
need the init method instead I want to work inside of my create widgets in here
I want to create the invert button this button is going to be an image
button but before we can create that we have to create the invert image
which is going to be is ctk and ctk image importing this is actually going
to be your exercise I want you guys let me type it import the image and create
the image button there are way too many typos in here
image and see this is looking much better I want you guys to import the
image and then create an image button in the appropriate Place pause the video now and try to figure this one out
yourself ready first of all we have to import the
invert image for that inside of ctk image we need two things we need the
light image and we need the dark image both of those we are getting by using
image dot open although this image we don't have available right now we're
getting that all the way from the top let me put it below here I want from pil
import image that way I can import images
with that image.open the file path I am getting from this
settings the one we are looking for right now is this one here inside of the operators I
want to get invert this is going to give me another dictionary this dictionary has image path
I want to get my operators I want to get the invert dictionary
inside of this dictionary I have the image path meaning now we are in here which in fact
is going to be another dictionary which has light and dark
for the light image this is going to sound a bit counterintuitive I want to have the dark image
on top of that for the dark image
I want to have if I copy all of this I want to have the light image
the way you want to think about it is that light image is the image for the light mode since we have a white
background for this one we want to have a dark image whereas for the dark image so the image for the dark mode we have
lots of black so for the actual image we want to have the light image now we have to figure out the image
button for that we need all of these parameters the color can stay dark gray this one is
totally fine for the parent I want to have self
text we can simply leave MD like so for the function for now this should be
over multiple lines we want to create another method I call this one invert once again no
need for any parameters and for now I just want to print invert
the function is going to be self dot invert
next up we have to column the row and the image the image is the really easy bit because this is what we just created
invert image column and row we are getting from the settings in here I want to get operators
invert this one has column and row although this I can simply copy from the
other buttons I have operators they shouldn't be percent this should be invert
the same I can do for the row this should be in Verge
and row with that we should be having something working let's try with that we
have a button I can click on it we get invert and we also get the hover effect on top of that we check the light mode I
want to set this dark detect to false once again run this again and there we
go this also works in light mode meaning I can go back to dark mode and this is looking really good
there's one more change that I do want to make and that is that this text right now is not really necessary however if I
go to the buttons and don't set a text here run this again we get ctk Button as the
default text which is well not ideal we do need this text in here however what
we can do we can set a default argument for the text but for that to work we
have to put the text all the way at the end and now we can set a default empty string
this text needs to be at the end because we have a default value whereas for these we don't
once we have that we have a default value so inside of this image button I can get rid of the text which is looking
a tiny bit cleaner the result is still going to be the same with that I can get
rid of the exercise and we have our image button you might be wondering now
if I look at the buttons the normal button and the image button look really
similar they are roughly 80 identical so why didn't I use the button as the
parent for the image button and that is a really good question what I've could have done for example is
combine these two classes where the button gets an image argument which by
default is going to be none and after the init method I can check if
an image exists and if that is the case I want to run self.configure and set the
image to the image we get that way we could have skipped this entire bit however this didn't work in custom t
Kinder whenever I tried this I get some weird Behavior around the images which might be fixed in the future but
right now this is some behavior that is there that's why I'm creating two separate classes for the next button
though we are going to inherit from this button to create the number buttons but
that's going to be the next bit I'll see you there at this stage we have three buttons which is a start but
didn't get us very far so for this bit we are going to create all of these
number buttons that is a terrible square but we're going to create these buttons here
for that we are going to use the base buttons we have created and then use inheritance to create the other buttons
that way we don't have to start entirely from scratch also it's a really good way to practice
inheritance let's have a look at this one here I am back in my code I want to
work inside of the buttons and let me minimize everything I want to create another class
I have caught this one a num button really important here this num button is
going to inherit from the button the one we created a tiny bit earlier this one
here in fact let me open both then I can explain a bit better what's going on
as always we are going to need the dunder init method in here
this one needs a couple of parameters now self is the usual one after that I need
a lot of the parameters that we created up here in fact let me just copy all of them we have parent text function column
row font and color there's one change that I already want to make that is inside of color these
buttons shouldn't be dark gray instead they should be inside of settings I have
the colors they should be light gray let me copy this color here
I can paste it in there and now we have a light gray color already this covers
the entirety of the color inside of the init method we need Super Thunder init
what is really important to understand now is that this thunder in it is going
to call this init method as a consequence we have to get all of these
parameters and find a value for them we're going to put all of this over multiple lines
for the parent we want to use the parent or the text we want to use the text or
the function for now we just want to use the function column is going to be the
column row is going to be the row bond is going to be the font and color
is going to be the color in this case since we simply duplicated
all of these parameters this might seem quite mundane but what this is already
giving us is all of this styling here basically what is happening when we are
calling this init method we are taking all of these parameters we're going to create them in just a bit
and then we are going to this init method inside of this one we are adding
Arguments for all of these parameters after that we are going to create the
actual button which means for example this color here
light gray would now be this color here so instead of dark gray we get light gray because of that these three colors
here are now going to give us a light gray instead of a dark gray color I hope all of that makes sense
inheritance can be a tiny bit tricky especially at the start let's actually create the buttons and
then this should make a bit more sense first of all I have to import the num button
I think that's what I called it yeah this num button here inside of the calculator not in the init
method but inside of create widgets I now want to create all of the number
buttons for that I want to look at settings in here we have num positions
for each num position we have a value and then a dictionary the dictionary contains a column a row
and a span most of the buttons only span a single column with the exception of
the zero button this one spans two we cannot account for this just yet but we
will cover that in just a bit for now I just want to go over this dictionary and use the column and the
row to place all of the buttons for that inside of the calculator I am
going to need a for Loop for the number and the data in num
positions this is the dictionary here on this I want to get the key and the
value which I'm getting with items the key I am storing a num the value
inside of data meaning the data is going to be this dictionary here
once I have that I can create a num button
the number now is going to need all of the parameters I have set up here color
has a default value so we can just ignore this one but for all the other values we need
parent text function call row and font font is the easiest one let's start with
this one I simply want to use the main font
parent is also going to be really easy this should be self for the text I simply want to use the
num because num is 0 to 9 or a DOT
the function we don't have just yet for now let me add a Lambda function in
here that is going to print the text so at the very least we have something
for the column if I look at the dictionary inside of data we have column
and row which means I can get data and column I
can do the same thing for the row which is going to be data and row
with that we have a number button if I now run the code we can see we have a
whole lot more buttons this is getting much more efficient however we do have quite an obvious
problem there is a big gap in here this exists because the zero button should
cover two columns like so which we can't account for just yet to achieve that
inside of buttons we have to update this num button so it is accepting another
parameter which I'm going to call Span in this span we have to use inside of this grid
method here which means we have to figure out how to get this span into this init method and
then from this ended method we want to go into this grid here on top of that we have to make sure that
when we are creating the normal button which we've done earlier for The Operators we are not getting an error we
know that all of the operator buttons don't care about span they always have one we really have to make sure that we're
not breaking these buttons all of this is going to be your exercise I want you
guys to get the zero button to span two columns on top of that make sure that
you don't break existing buttons also let me fix that typo that looks much better pause the video now and try to
figure this one out you will need inheritance
let's work backwards for this one first of all inside of grid we have to add one
more argument let me put it right after the column we need a column span
for most buttons in fact all buttons except the zero this is going to be one however for the zero it should be 2. as
a consequence this can't be hard coded this needs to be span this span I'm going to get from the
parameters I will put this one all the way at the end we want to have a span
value once we have this parameter inside of num buttons we already have the spam
button here so we can add span and span in here with that this is going
to be passed into this span argument and then this span argument is going to span
two columns however now if I run the calculator we
are getting an error that non-default argument follows default argument this we can fix quite easily I can move
span in front of the color although we are going to get another
error that button in it is missing one required position argument Span in this
error we are getting up here this button and this button as well the
button for percentage and clear they now both want an argument for this span which we don't have
to fix this you can approach this in two ways you could either add a span
of one in here when you're creating the button however since they both have one this
wouldn't be ideal instead what I would recommend is simply add a default value here of one
with that these buttons should still work but now we're getting another error that when we're creating these num
buttons we're not giving them a span argument which we can do quite easily because inside of settings we have a
span value which means span is going to be data and span now if I run this here we go all of
this is working perfectly fine now also I haven't clicked on any of the buttons yet we are getting an error here
so we do have to work on that as well the text here shouldn't be text it should be num now if I run this we get
well we always get nine something definitely went wrong here
which doesn't matter so much because we have to create a custom function here anyway since I want to capture the input
I want to create a method I call this one num press this one
itself and it needs a value for now once again I simply want to
print the value this nump press I now want to use as the function here although this should be
self Dot numpress this however is going to give us an
error if I run the code now we are getting calculated.numpress that's the method we
just passed into the number button is missing one required position argument value
which means we are passing in the function which right now is numpress the
one I just created this one the problem is that numpress is expecting one value this value however
we are not getting inside of this function to fix that we can use Lambda I want to
get Lambda and then my function with that I can pass n parameters
just to test this let me add test in here if I now run the code I can click on off
the buttons and I'm always getting test that's looking pretty good what I can also do is pass the text in
here the text for now we simply used for the button text but we can also pass it into the function and now
I am getting the proper output for all of the buttons that is looking significantly better
when we are passing in the numpress function we are passing it in here and
from this function we are creating a Lambda function meaning we are wrapping the function
inside of a Lambda function that way we can add parameters in this case the text
all of this is going to create a new function which we are then passing into the command of the actual button
that way we can create a function with parameters that is only going to be called when we are pressing the button
or rather when the user is pressing the button so with that we have another major part
which means I can minimize the calculator and finish up this section
to finish up the layout I want to create the orange buttons they are mostly going to work like the
number buttons which means we have to pass in a function and this function gets one argument
which is going to be the Plus for the plus button the minus for the minus button equal for the equal button and so
on the one difficulty is that these four buttons here are simple buttons whereas
the division button has to be an image button but other than that there isn't going to
be anything new so let's Jump Right In and let's see how far we get back in the code let's go to settings
and let's see what we have what I now want to create are all of these math
buttons the information for that is inside of the dictionary math positions we have a
dictionary with the key being the operator so divide multiply minus equal
and plus the value attached is a dictionary that has a column a row a character an
operator and an image path although the only image we have is for
the division button from that inside of buttons.pi below the number buttons I
want to create the math button this one has to inherit from but turn as
well because primarily this math button is going to work kind of like the number
button the only difference that for the number button inside of the function we
are passing in the text which means the text for the button is going to be the same as the text for the
function for the math buttons this is not going to work because if I look at settings what the button is supposed to
say is going to be inside of the character x minus equal or plus distributed text
for the button however what we actually pass into the function is going to be inside of the operator
as a consequence we can kind of copy this but we have to make some updates
since this should be quite doable we can do an exercise right away I want you guys to create the math
buttons the only important thing here is that you have to separate the character
and the operator once you have that also all the buttons with a four Loop inside
of calculator dot pi in calculator and create widgets
there should be another for Loop somewhere here for the math buttons
try to figure this one out also for now don't worry about the image I will cover that after the exercise
first of all I need a Dunder init method as a matter of fact I will need most of
this so I can simply just copy it all and then we can work on it the first
minute I want to do is to update the color because I know that all of these
buttons should be orange also they don't have a span value
because they're all simply occupy a single cell meaning I can get rid of span entirely
that is looking better the final change that we have to make I'm going to put this right next to text besides the text
for the button I also want to have an operator this operator I'm going to pass into the
function which means now we have a separation between a text so what the button looks like and the operator so
what the button actually does other than that we are good to go for the math button there really wasn't that
much to do in here so now inside of the calculator first of all all the way at the top I have to
import the math button once I have that class
I want another for Loop for let's call it operator and data once again in the
dictionary I have called math positions don't forget to call items on this one
that way we get the key value pairs I want to create a math button
this math button is now going to need all of these arguments let me copy them
and paste them in here first of all the font is super easy it
is going to be the main font we have done this a couple of times by now parent is also going to be easy tap on
is going to be self after that we need text operator function column and row
most of these are fairly easy if I open settings inside of the
dictionary which is data in our for Loop we have column row character and
operator also I realized in this one that I have duplicated data a tiny bit
these operators here and the keys for the dictionary are
identical meaning we could use either one it really doesn't matter I suppose what I could be doing is
simply get rid of the operator then all of this is going to be a bit
cleaner with that we're getting the actual operator from the keys
which is good because I call them the operator but now inside of the text I want to
have data this value I called character or at
least I think I did we are using this character here also note for the division we don't have
anything right now but that's okay we will fix that in just a second for the operator we're just going to use the
operator the function we don't have right now so
below the number press I want to have another function that I called math press
like number press this one needs self and a value although again I simply want
to print the value that we are getting for now this function I'm going to pass in here self dot math press
finally we have the column and the row this is information that's quite easy to
get we need the column and we need the row with that we should be having some
buttons and this is looking pretty good let me move it to the side
at the very least we have multiply minus plus and equal and you can also see
these buttons do print the required value the one thing that doesn't work right now is the division button
this part here is looking very sad right now for that we are going to need an image
button to create this one let me get rid of the exercise text and minimize all of the
stuff we have so far what I want to do now is use this image button and then
create another math button that can take an image this is going to be another class
I call it this one math image button this one has to inherit from the image
button this one is going to be quite similar compared to the math button so let me
copy all of it then we have something to work with the major difference is that this math image
button is going to need an image let me create a parameter by removing the font because we don't need that one
anymore in fact we can't use it because the image button doesn't have a font we don't need font anymore
instead now we have to pass in an image which is going to be image
to understand what is going on we once again have to make sure that this super knit is targeting all of the parameters
of the image button in knit method in there we have a parent this one we
have we need a function this one we also have we need column and row those we
also have we need an image this we have text we don't need because we have a
default argument and color we do need because we want to have a different color which we do have
which means now we have a MAV image button we just have to figure out how to create it in the for Loop all of that is
going to happen inside of the calculator although once again first of all I have to import my math image button
I don't need the init method also I can minimize all of these buttons so this is
a bit easier to see inside of this for loop I now want to check if I want to create a math button
or a MAV image button this sounds very much like an if statement
now I just have to figure out the condition which is fortunately quite simple if I look at settings
the thing that makes this division entry unique is it has an image path all of
the other entries simply have none for the image path since none is going to evaluate to false
inside of an if statement all I have to do is instead of this if statement check my data and then the image path
which is telling me if this is true I have an image
however if that is not the case so else I don't have an image meaning I just want to create a math button
just to test this let me add a pair statement in here run this again the
calculator still works just fine but now we have nothing in here because this is what we
singled out with the if statement this I now want to replace with a math image button
this one to get the parameters let me copy it from the buttons in here I need
all of these and once again we need a parent and this parent is
simply going to be self I realized I didn't get rid of the text let's remove it right now in fact inside of the
buttons this text here shouldn't exist at all I have to remove it from the parameters
and from the init method that's much better next up the operator is simply going to
be the operator the function is going to be self dot
math press next up we have the column this in fact these two entries I can
copy from the math press let me paste them in here like so and
the final thing we need is an image since for this one we have a slightly
larger line I want to create this in a separate variable I'm going to call this one the Divide image
which is going to be ctk ctk image we as always going to need two arguments
we need a light image and we need a dark image
both of those we are getting with image dot open and then a file path
this file path we are going to get from inside of settings we have image path
which is going to be another dictionary with light and dark entries this we access with data inside of here
we have an image path for the light image so the image for the
light mode I want to have the dark image because remember light image means we have a bright background so we want to
have a dark image without this we wouldn't have any contrast the same thing I want to do for the dark
image with the one difference that now we want to have a light image this is giving us the Divide image this
I'm passing into the image and now I can run this thing and there we go we have
the division button I can also click on it and we get divide with that we have all of the buttons
working on top of that I can now minimize the
calculator I want to test if this is also working with light mode which I can check by
adding faults into the calculator run this now and there we go now we are getting a dark image for this
button although it still also works but once again I want to use the dark mode
with that I can minimize all of the classes and we have made a ton of
progress this covers the entirety of the layout now that we have the entire layout we can start working on the logic
of the calculator which means I can type some numbers and actually get a result
unfortunately for all of this we have to cover quite a bit of logic I think this
is best done when I jump right in and explain it while we are doing it the logic here does get a tiny bit more
advanced fortunately we can work entirely inside of the calculator that works because we
don't need the init method we also have all of our widgets we have these methods
here numpress is giving us all of the numbers math press will give us the math
buttons and then we have clear percent and invert these are all of the buttons
of the calculator which is quite handy I don't have to worry about the buttons or the settings
although as a reminder there's one important thing in terms of data that we
have to be aware of inside of the init method we have a result string and a
formula string result is going to show the results and formula out the formula
that was a very pointless sentence sorry but basically what we want to start with
is when I'm pressing the button I want to show the number inside of the result
string this is actually quite simple all we have to do inside of the nump press
instead of printing the value I want to update self dot result string and then
set this to the value if I run this now let me move this to the middle I can click on all of the
numbers and this is looking really good well really good is relative because
right now we only ever get a single number so how can we get multiple
to achieve that I want to create another entry inside of my data I'm going to
need a list I call this one let's call it the display
nums this is simply going to be a list what we're now going to do inside of
numpress we are not going to set the value of the result string instead we
are simply going to get the display nums and append the current value
although I really want to make sure that I am only working with strings here that is really important meaning when I'm
getting this value I want to convert it to a string right away let's see what this is going to give us I want to print
self dot display nums now if I click on the buttons I get a
list that gets increasingly longer this list I now want to convert to an actual
number let's do this with a variable I want to have the full number for this we
need a string and then the method join really important here this string needs
to be empty inside of this join we need a list which we have
this is our display nums I want to print the full number
now if I run this let me move it to the side I get a number that becomes increasingly
large I can also have the dot and this is looking good which means now I can set this full
number as my value for self.result string like so with that I
can click on all of this and I'm getting a pretty good result
I can also use the dot and then at some point the number gets too long but well I'm not too concerned about that
now that we have that I can minimize numpress and work on my math press as a
reminder in here we are going to do our math operations the very first thing that I want to
check in here is that we actually have a number let me actually return to the print
statement let's say we have the calculator these buttons here for equal plus minus
multiply and divide that should only be possible to use once we have a number for example if I have a 6 then I should
be able to use these numbers however if we don't have a number they shouldn't be available or at the very
least when we are pressing them they shouldn't do anything for that I first of all want to get my
let's call it the current number this is going to be the same thing I
have done inside of numpress I can literally just copy it now I want to check if the current
number exists if that is the case let's for now print
do stuff also I want to print the current number
just so you know what's happening if I now click on the X we can't see
anything because we get an empty string that well doesn't do very much but if I now click on 66 and now I'm
minus we get 66 and do stuff and you can see here we have two empty Fields this
is this empty string which means we know that this is working
inside of the current number we now have to figure out what to do with these
values the thing that I started with is another list inside of the init method I
want to have self dot let's call it the full operation which is going to be an
empty list when we get started with that I can also minimize the init method because these are the only two
lists that we are going to need basically what I want to do if we have a current number I want to get my self dot
goal operation and then append the current number
that way we're getting the current input besides that what I want to do I want to
get self.fully operation again and then append the value which in this case is
going to be the operation to demonstrate what's happening let me print self dot full operation
I want to type on 56 then multiply it now we get 56 and multiply
if I now click on 3 and plus we get some decently looking results but it's not
perfect at the very least we can work with this but we do have to make some updates first of all I want to start with
another if statement that if the value is different from equal
only then do I want to do some math operations if that is not the case let me add an
else statement right away I want to print result
the logic here should be quite obvious if I run the calculator again these four
buttons here for divide multiply minus and Plus data to actual math operations however the equal sign should simply
give us the result the logic for this one is slightly different this is why I'm separating the two if however we
don't have the equal sign then I want to append the current value
besides that I also want to get my display nums and then clear the list
which is simply going to empty all of it that way we don't get duplicate values
in fact let me print self dot not display nums but full operation that's
the one we care about right now I can now get 12 and plus which gives me 12
and plus which looks like a decent operation but now if I go to 34 and minus now we are separating all of this
properly the way you have to understand this this is quite important so let me
cover it in a bit more detail we are always starting with a numpress at the end of it in terms of data we are
getting display nums this could for example be a list with
one and two both are going to be strings but this one doesn't matter right now
once we have that and we are pressing MF button if there is a current number which we do
have right now we'll be running this bit here which is going to give us another list inside of this list we are
combining these values which right now would give us a 12.
after that if we don't have an equal sign we get to this bit here which is
going to append the value this could be a plus
with that we have another list what is really important now is this line here this is going to clear the
display numbers which means we're getting rid of this one and this 2 in our case
as a consequence the next time we are clicking on the number press we are adding new numbers in here
those could for example be three and four could be as many numbers as you want
after that if we press on this again we are now combining these two numbers add
them in here and after that we are adding the value once again so we get 34
and then we would get minus which is then going to give us a really
clear operation that we can work with that is literally all that I wanted the issue we have right now is that the
result cannot be seen but that we can fix quite easily what I want to do is if
we are clicking on any of the math operators I want to get myself and my
result string and set this to an empty value that way we can't see anything in the
result to account for that I want to get self dot formula string and set this value
what I want in here is a string then join I want to join self dot full operation
what this is going to give us I can type in some numbers in here and now if I had
multiply we get the operation I can also add more numbers
or as long as I want this is working pretty well
although what I don't like right now is all of this is really close to each other to fix that I have to add a space
I should have mentioned this earlier the value you add inside of this string is what will be between the characters
if it's an empty string it is simply going to be a tiny bit of space which looks much cleaner although you could
add I don't know XXX in here now this is going to look horrible now we get XXX a whole bunch
I simply want to have an empty value also I should be adding comments in here
let's call this one update data and this one should be update output
with that we are getting the value so next up I want to work on the result
the really important question you might have for this one is let's say we have
some kind of string that is 12 plus 43. we can print this but how would we get
the result the answer here is one special function inside of python that is called eval
let me run this one actually if I type any kind of number then I can use these buttons here if I now click on
equal we get 55. this 55 is 12 plus 43.
eval is simply going to evaluate some code and then give it a result
I mentioned this in the introduction to python but this eval you have to use very very carefully
if for example you allow the user to type some text then they could execute
some code using this eval which would be a huge security risk in
our case though we are making a calculator the security here isn't terribly important also we don't have
user input so this shouldn't be an issue if however you're making a database for a website then this is definitely
something to keep in mind so with that we can evaluate a formula
which means we have to actually get our formula let's create another variable that I
call formula this needs to be a string so I want an empty string with the join method and
all of my operation is inside of this full operation attribute let me simply paste it in here
I can run this now I can click on some math numbers so I get an operation and
now if I have a number here I can click on equal we are getting the math operation this is looking quite good to
get the result all I have to do is use eval and then we should be good to go for example if I have 56 minus 32 and
click on eval and we're getting 24. that looks accurate this result I want to store the result
is going to be eval of the formula once I have that
I want to update my output I want to clear the full operation list
finally display nums should have the
value of the result and nothing else
these three things are going to be reasonably straightforward meaning they are going to be your exercise pause the
video now and try to figure this one out you're working entirely inside of this else statement
I'm going to start by updating the output this is going to be quite similar compared to what we have done up here in
fact let me simply copy it I want to first of all update the results string using set although now I
don't want to empty it instead I want to get the result for the formula I could use this full
operation here but I don't really like that because I already have the formula up here
and there shouldn't be a space for this one with that we should be having a working output meaning now I can type 2 plus 3
and then equal and we're getting five also we're getting the formula however there's no space between the values
this I can fix quite easily all I need is a space in here eval doesn't care about that whatsoever
which means now let's say six minus five is going to be one and we have a nice
looking formula this is going to update the output besides that to cover these
two bits here I want to update the data this once again is going to be somewhat
comparable to what we have done up here I'm going to copy these two values first of all the full operation I now
want to clear that way once we start typing again we're getting completely new values
although to retain the result we have gotten I want to get my display num and set this to
a new list that has a single entry which is going to be the result
although this result right now is going to be a number but I only want to work with strings
what this means if I now type 2 plus 3 get my equal now I can type on
multiply and then you can already see we now have inside of the formula 5
multiplied let's say by 9 and we get 45 from this I can keep on working minus 31
and we get 14. which is going to give us a basic
working calculator meaning I can now get rid of the exercise text and we are nearly done
there's one thing I want to cover that isn't exactly breaking but very annoying
if I run this again and I type something like 8 divided by two if that is the
case we are getting the correct result but this point zero is well entirely
pointless also it might be confusing to some people so I would rather get rid of it
on top of that if I run all of this again if I have something like 8 divided by 7
we are getting a really really precise result but that isn't really necessary
I would rather round this so it doesn't get too confusing which means inside of this bit here I
want to add a tiny bit more logic let's call this one format the result
for this I first of all want to check if the result is a floating Point number because only then do we get the weird
Behavior this I can check with if is instance in
here we need two arguments the first one is the value we want to check in my case this is going to be the result
besides that the second argument is going to be the data type we're checking this result against which in this case
is going to be a float which means all of this is going to check if the result is the data type
load and this is going to return either true or false let's try this actually if this is the
case I want to print float now if I type 5 divided by 2 and get the
result we are getting float the result here is looking really good but this
isn't given for example if I divide this by three we're getting some very strange Behavior once again which I want to
account for the result you have just seen is we have too many numbers after
the decimal this is the first problem the second problem is that we have an
integer is formatted like a float which means we
get stuff like 4.0 these two cases we have to address
separately to account for them I want to start with if the integer is formatted
like a float to check for this kind of behavior if we have stuff like 4.0 python actually has
another inbuilt method it is called if I want to check my result and the method
here is called is underscore integer this is basically checking a number if
it is an integer or not which means if we have a floating point value with 4.0 this is going to be true if that is the
case I want to get my result the value I want to assign is integer of
the result to explain this one right now when we are getting this result here we might be
getting something like 4.0 let me write it in here 4.0
inside of this if statement we are then checking if this is a floating point value or not since we do have a DOT and
a decimal value we know that this is a floating point value however this is statement here is going
to check this value and see that it's simply dot 0 so we can simply ignore it
this is actually an integer and because of that we're going to force
it to be an integer which will remove anything after the decimal point and we
simply get the number so I can run this again and now 8 divided by 2 is simply giving us 4. that
is feeling much better for the other case we can identify this with an else statement
so let me get rid of this text here if this else statement is true we know we
have an actual floating point value I'm going to keep the logic simple for this one I am simply going to assign a new
value to the results this new value is going to be the rounded value of the
result with let's say three values after the decimal point with that I can get rid of this comment
as well and now we should be good to go if I now type 8 divided by 7 get the
result I get 1.143 now this logic is quite crude and not
ideal because sometimes a user really wants to have precise results
but well this is something you can work on yourself it shouldn't be too hard to implement
for the next part we are going to account for the free operator buttons so clear percent and invert but other than
that we are basically done now that we have the basic logic of a calculator we only have to account for these three
buttons here to explain what they are doing let me type some numbers in here
like so AC is simply going to clear the calculator to get a value back again we
can now use this plus and minus button all that this one is doing is it gives us minus or plus so it inverts the
current number the percentage sign divides the current value by a hundred that way we are getting well the
percentage these are the three buttons we are going to create and they are not terribly difficult let's Jump Right In here I'm
back in the code and I want to work inside of clear percent and invert Lear
is by far the easiest one let's start with that one all I have to do in here is clear the output and clear the data I
want to get myself dot result string and set this to a zero this is our default
value for the result string besides that self dot formula string
should simply be an empty string I also want to clear the data which is
going to be self dot displaynums dot clear
don't forget to call it besides that self Dot
full operation this should also be cleared with that we have one part covered I can
now type some numbers in here get the result if I now click on AC everything disappears
that was quite easy I can now hide this method and not worry about it again
next up we have to do either percent or invert let's start with invert this is the
slightly more difficult one we first of all have to get the current number I want to get the current number this we
get an empty string then join and then self dot display nums this is the same
thing we have done inside of math press this button like the math buttons is
only going to work if we have a number so if current number then we want to
invert something Bishop makes sense because if we have 0 as the default value this isn't going to do anything
plus and negative 0 is just going to be zero if we have a number however I want
to check if it is positive or negative this is going to be an if statement to
do an example let's say instead of display nums we have 1.5
because of join this is going to become 1.5 as a string
this number I now have to turn into a floating Point number that way I can check if it is positive or negative
hence inside of this if statement I want to create a float from my current number
if this resulting number is greater than zero then I know this is positive
however if that is not the case else then I have a negative number
what we now have to figure out is what to do with these results right now we have this case here our value is
positive so how can we turn it negative for this one you do have to be careful
because the number we want to make negative is this one here
the value we are working with right now all of this is only temporary this is what we created here this is not the
actual number that the calculator is working with what we ultimately have to do is add another value in here at the
beginning this value has to be a negative and this we can do quite easily all we
have to do is get self dot display nums and then insert a value
this value has to be inserted at index 0 and the value we want to add is a minus
to test this one in the else statement I'm going to add a pass and also what we
have to do is we have to update the output which we do with self dot result
string I want to set this and once again I need dot join
and self.d display nums let's try this by now if I simply click
on invert nothing is going to happen this is because it only works if we have
a number inside of display nums let's say if I click on 8 and 9. now if I click on negative we get Negative
however if I click on it again nothing is going to happen but at the very least we do have a start
this line here is working we now to figure out this one to explain how we need to approach this
one let's do another example we now have to create a negative number the important thing here inside of display
nums we have to start with a negative number the numbers afterwards don't really matter let's say one and two
what this join is going to give us is negative 12.
because of this if statement here we know that this is going to be negative so we are working inside of this else
statement which means now we have to figure out what to do in here
the answer for this one is actually quite simple we simply have to remove the first item from display nums and
then we are good because that way we are turning a negative number into a positive number which means we're
getting simply rid of this minus literally all I want to do is delete
self dot display nums the value with the index 0. with that I
can run this again let me type in 56 now now if I click on invert it's minus if I
click on it again we get plus and this keeps on working also if I clear the calculator I can do
one plus three if I now click on the result this is also going to work
so this is looking quite nice we have covered invert
next up we have to work on percent this one is going to be your exercise
figure out what to do with this button as a reminder the actual functionality here is divide the current value by 100.
pause the video now and try to figure out this one
to get started with this one I have to check if we have any kind of numbers inside of display nums
this is going to be kind of similar compared to what we have done with invert however for this one I don't want
to get the current number I simply want to know if there's something inside of display nums or not which means I simply
want to check if self.d display nums or not only if that is the case I want to
create a current number this has to be a float
off I need to use join and now the display nums
several display numbers to be accurate you might be wondering now why am I
doing this this way you might be tempted in here to type something like current number
is going to be float and then the actual value and then check if or a number
this unfortunately would not work let me get rid of it and demonstrate this on a separate code
editor I am printing a value and the value I'm printing is the float value of some kind
of string for example in here this could be one two three point four five this
will be working just fine the problem is if this float is
completely empty I am getting a value error which would crash the entire thing
and with this kind of setup I'm avoiding that anytime I'm creating the current number which I want to turn into a float
right away but I can only do this if the display nums so the list is not empty
although once I have that I can convert this number I got this one the percent
number this is simply going to be the current number divided by 100.
also let me add some comments again I want to get the percentage number
once I have that I want to update the data and output
I have to start with self dot display nums what we now have to figure out is how to
turn this percent number back into a list so we can keep on working with it also I realized there's a typo this is
much better actually let's first test if this is working I simply want to print percent
number if I now run this again I can click on 6 and then press send and we get 0.06
I can also clear this and three plus six is equal to 9 and percent again gives me
0.09 I can also click on this again multiple times but this doesn't do anything
that we're going to work on in just a second what we now have to do is turn this
percentage number back into display nums list that way we can keep on working with it
to achieve that we need list string and then percent
number the way you want to think about this this percent number could be 0.06
which is going to be a floating point value if we're turning this into a string like
so we didn't achieve very much however a string is some kind of list in a very
primitive sense which means when we are putting it into the list function
all we're doing is we are separating each value with a comma and then we have a list
around it that way we get the list from the number the last thing that we have to do now is
to update our result so result string dot set this is going to be a string
again with join self Dodge display nums and then we
should be good to go let's try if I now click on 9 then the percent this is working and since I turn the
result into display nums again I should be able to click on it again and now we get increasingly smaller numbers
also if I click on AC this returns everything back to normal and
this is still looking pretty good cool with that I can get rid of this
exercise command and other than that we have a calculator
in this tutorial we're going to create an image editor you can see the result right here I can click on open image and
import an image the one test image I have right now is called Otter if I open this one you can see we have
the image this is by the way also responsive so I can resize it quite easily but much more importantly on the
left side I have quite a few different options the first one is rotation this one rotates the image I can also zoom in
or invert the image and revert all of this besides that I can change the color
for example the brightness or the Vibrance I can also use black and white or invert
after that we have effects and here I can set some blurriness or some contrast
and I can work with extra options like Contour is going to be really visible and all of those options also work
together for example if I use blur with this one you're not going to see anything so you
do have to be careful here but for example if I return to color I can make all of this black and white
or remove the invert then it becomes White finally I can export the image I can
give it a file name let me call it dark water I can select a file path open
Explorer I want to save it on the desktop so I select the folder and finally if I click on Save we have
exported the image which means now if I open my desktop I have dark otter
besides the normal author meaning this has worked also I can close the image
and open another image for example the dark otter and then work with this image
literally any image is fine so you can do whatever you want in here for this kind of project we are going to need the
pillow Library which we have already used to some extent but for this video I'm going to go into much more detail
now I am not going to cover everything I will only talk about the parts that we actually need
that being said if you're interested in pillow I have made a whole separate video on YouTube that talks about all of
the library in detail check this one out if you're interested but all of that is a couple of videos in the future for now
I just want to create a basic window before I start with that I want to have
a look at the folder this one is going to look like that let me increase the size a bit
we are starting with two files we have main.pi and settings.pi main.pi contains
the entirety of the logic settings contains the settings let's Jump Right In and let's see what we have right now
main.pi is completely empty besides that we have settings.pi this one contains a
couple of elements not terribly much all of this stuff here are the default values that we are going to need much
later for example we have the default value for rotate which is going to be 0 degrees
besides that we have a couple of colors and this space shouldn't be there these are the
colors for the styling of the app I am not going to go too crazy on The Styling because I want to focus on the actual
logic but obviously you can apply your own Styles here it's quite easy to do with that let's create the basic app
by the end of this video I want to have something like this a basic window with one button in the middle it should be
really easily done for that first of all I have to import custom tkinter as ctk
once I have that I want to create a class that I usually call app which inherits from ctk then we need it under
init method with self and nothing else once we have that we can set up the
window the most important thing in here is going to be super and then Thunder init without any arguments
also for this app I want to keep the styling a bit simpler which basically
means I always want to use the dark mode this I get with cdk and set the
appearance mode with dark as the only argument in here
besides that I want to run the app so we have something this I achieve with self dot main Loop
after that I can create an instance of the app run the code
and we are getting a basic window this isn't looking too bad with that covered
I want to add a tiny bit more styling first of all I want to set a starting size which I get with geometry
the starting size here should be 1000 by 600.
let's see how that looks this seems fine besides that I want to update a title
which I do with self.title I got this one the photo editor
and there we can see in the top left we have photo editor for this app I am not going to color in the title bar because
this one just seems fine although I do want to set a minimum size
which I get with self.min size this one wants two arguments for
the width and the height which I want to set to 800 and 500. which means if I run
this now let me show my mouse I can resize this window however I can only
make it this small later on when we have all of the widgets if the app gets smaller than this it's
going to look really weird with that covered I want to create a
layout once we have that layout I can create my widgets the One widget I want to create
for now is some kind of import button although to be a bit more specific here
this import button is going to be another widget which is going to be a frame with a button but first of all we
have to think about the layout for that let me draw a tiny bit this is going to
be the entire window once again imagine I can draw straight lines what I want to create right now is going to be a simple
button right in the middle this we could achieve with basically any kind of layout method Place grid and pack would
all work for this one however later on I want to have another kind of layout I
want to have a panel on the left roughly here besides that I want to have a main panel
in this area here for the image as a consequence our layout has to account for this button here and for this more
elaborate layout although it's not that much more elaborate basically all I have done is I have used
the grid layout to create one row and two columns the rows I get with row
configure we only have a single row so row 0 with
a weight of one the more important one is the column
let me duplicate it actually right away those two columns are going to have different sizes the left one so column 0
is going to have a weight of two the right one column one is going to have a weight of six
that is all we need for now in here which means now we can work on the import button or rather the frame with a
button this import button I want to create in a separate file simply because later on
mannaut Pi is going to contain a ton of logic for the image manipulation which means I want to create a new file
with Ctrl s and save this as let's call it image widgets don't forget dot pi
inside of this file I'm going to contain the widgets for the image import and the image output
for both of them we have to import custom t Kinder as ctk
with that I can create another class this one is going to be called image
import we're just going to inherit from cdk and ctk frame
this one is going to be fairly straightforward I want this Frame to cover the entire window on top of that
it should contain a single button right in the middle the button should say open
image this should be fairly straightforward so it's going to be your exercise create
this widget and then call it inside of main.pi the result should look something
like this possibly now and try to figure this one out
first of all we have to create a thunder init method this one itself and we need
a parent once we have that we can call Super right away the only thing we have to add
in here is Master needs to be the parent next up we have to place this widget
which we do with self dot grid this one wants a column
which is going to be zero however since I have specified two columns and I want
my widget to span both of them I have to add column span answer this to two
row is going to be super easy it's simply going to be zero finally I want to have sticky with north south east and
west that way this widget is going to cover the entire window let's try it actually backend main.pi I
want from image widgets
and I want to import everything also I should fix my typo this is
looking much better what I can do now down here under my widgets I can create this image import
let me paste it right in we only need one argument which is sell for the parent
if a run is now we can see that well we can't really see anything that is because this app here and this
image import have the same background color we can change that though by setting FG
color of the image import to something like red now if I run main.pi again we
have a completely red app which means all of this is working that's a good start
all we have to do now is that the button with ctk and ctk button
the parent here is going to be self text is going to be open image that is all we
need for now although we do have to place this button this we can do with the pack method by simply setting expand
to true now if I run main.pi again we have a button right in the middle on top of
that if I resize the window this button is always going to stay in the middle which is perfect for my purposes
before I finish this video there's one more thing that I want to do let me run the app again when I'm clicking on open
image I want to run a function however I want to contain all of the logic for the
image inside of the app which is going to be a tiny bit of a problem because I want to contain all of
the logic in here but the image import widget is going to call the function as
a consequence I want to create the function in here I call This One
Import image this one is going to need self and a
path although for now we are simply going to print that path the path we're going to
get in the next video it's going to be the file path towards an image this import image I now want to pass
into the import image widget which I do with self dot import image
the naming here arguably isn't ideal but this one here is a class whereas this is
a method inside of the app class so now inside of image widgets I need
another parameter let's call it the import function
I can also get rid of the exercise text and create an attribute with import this
shouldn't be Fung this should be Funk or function which is going to be the argument we
just got after we have that this cdk button is going to need a
command which is going to be a separate method I call this one the open dialog
let's create this one right away Define open dialog inside of this method we have to create
some kind of path for now we cannot really do that so let me simply ADD test
in here besides that I want to import the image which I do with the import function
meaning I want to call it with the path I just created this means now inside of main.pi I can
run this method here when I'm clicking on this button let's try it if I now click on open
image I can say test in the bottom left meaning this is working perfectly fine
with that we have a really good start so in the next video we can work on importing the image now that we have a basic window I want
to figure out if I click on the button how can I get this dialog on top of that
if I open an image like this author how can I display this image which means we have to create an opening
dialog and a canvas to display the image this shouldn't be too difficult to do let's Jump Right In back in my code
inside of the class the issue right now is that this import image is simply
printing a path later on we actually want to import an image for that though
we have to create a proper path right now inside of the image import we always
have test for the path this I want to change right away
instead what I want to have in here is some kind of file dialog then this file
dialog is going to return the path that I want to use for that tick enter has all we need
although we do have to import something what we have to import is from tkinter import file dialog
this is going to be a file dialog that can open a file or rather give us a path to a file
to use it we have to get file dialog and then ask open file all in one word also
don't forget to call it what this one is going to do if I run
may not Pi again I can now click on open image and we get a file dialog on top of
that if I open this order I can double click on it and now we are printing
something else this is what we're getting from the path this path here is what we are printing
right now most of the information in here isn't really important the only thing we
really care about is the name because this one contains the file path to the image this is what we actually want to
get which is quite nice because this part we can get very easy it's inside of the
name of this path which means when I'm opening the path I want to get all of
this which is going to return the object you have just seen this object has one attribute called name this name contains
the actual path which means now if I run all of this again I can click on open image
now I'm getting the proper path to the image of the author with that I can minimize the image
import class and focus on main.pi what I now want to figure out is how to
actually use this path to import an image for that first of all we're going to need the pillow Library which you
usually use with from pil import image this I can now use to create an
attribute let's call it self dot image which we are getting with image dot open
the argument we have to pass in here is the path once we have that python is going to
import the image and store it inside of an attribute that I called image we can actually test if this is working
right away I can do for example self dot image dot show and then python over our
pillow is going to show the image let's try I can click on open image
otter and now I have to wait a bit and there we go python has opened the
image meaning this is working just fine although this isn't actually what I want
to do let me get rid of it instead I want to display this image
inside of tkinder now for that we are going to need another widget I put this
inside of the image widgets in here all the way at the bottom I want
to create another class which is going to be image output let me minimize the image import because
we don't need this one what is really important and what I talked about in the past is that to display an image in
tkinder you want to use a canvas which means this image output is going to
inherit from the canvas since the canvas is a part of tkinder we
have to import this one separately as well which means besides the file dialog I want to have the canvas
first of all inside of the class I as always want a Dunder in it method with
self and parent there are two things I want to do in here the first one is super Thunder init
and set the master to the parent besides that I want to use self dot grid
and place the Grid in row 0 and column one also sticky should be north south
east and west on top of that just to make sure that we can see this
canvas I want to change the background to Red also I realized I forgot row 0
here once I have that back inside of main.pi I have to figure out something else
let me run the app to demonstrate right now we have the image open Button if I click on it I can select an image but
now this image open still sticks around which would be annoying to display anything else as a consequence I want to
get rid of this image import which could actually be a pretty good exercise for you
I want you guys to hide the image import widget pause the video now and try to figure
this one out first of all we have to figure out how
to Target this image import we do have an instance of it but to Target it we
have to store it inside of an attribute I call this one image import
now that we have this attribute I can get self dot image import
and now to hide it I need Grid or get let's try this one I can now click on
open image click on the other and now the import button disappears
which means this part is already done next up after hiding the import I want
to create self dot image output this is going to be the widget I just
created this image output here I can place it all the way at the end
add cell for the parent and now let's run it and let's see what we get if I
click on open image the author now we can see we have the canvas on the right side
although I don't like the border around it to get rid of this one inside of the
image output class we have to add a few more arguments in here those are BD is equal to zero then we
have highlight thickness which is also going to be zero
and finally relief should be rich
let's try all of this I can click on open image and the author again and now we have a plain red background
although this red color is not exactly what I want instead I want to have this
color this is the same color as the background for custom tkinter which means now if I run all of this click on
the utter we can't see a difference although the canvas is still there it
just has the same color as the background this ensures that when we add an image later on it looks like the
image is just by itself although that being said this color here should be inside of the settings
let me put it all the way to top I got this one the background or rather the background color
this should be this color here and I want to replace it with background color I can copy the color in Here and Now
inside of image widgets all you have to do is from settings import everything
with that I should have the same results like so this one is still working the
last thing that we have to figure out is how to put the image on the canvas and for that there's one really important
thing to understand you might be tempted to place this image inside of the image output
something like as a second argument self dot image this would be possible but that's not
what I want to do instead I want to make sure that the image only stays inside of
the app since there are going to be a lot of changes to the image later on I really want to make sure that the logic stays
contained which for now means that this image output is not going to get the
image itself instead what I'm going to do is I'm going to create another method
that I called resize image for now this image doesn't need any arguments I
simply want self in here and what is going to happen at the end of this method is self dot image output
dot create image discrete image we can use on any canvas and since our image
output this one here simply is a canvas we can use this method
and with that we're going to place the image there are three arguments we need to
place in here we need x y and the image or more specifically we need an image TK
X and Y for now can just be 0 and 0. although I will change those later on
image Decay we don't have right now we simply have the image but this we have
to convert for it to work properly with t kinder to create that although at the top
besides image I also want to import image TK once I have that
after I'm importing the image I want to create self dot image underscore TK this
is created with image TK then dot photo image
the only argument we have to pass in here is self dot image with that we have an image TK which we
can set as the image for the canvas all we have to do now is call this
method here which I'm doing at the end of the import method self dot resize
image if I now run all of this again I can click on open image click on the other
and we can see we have one part of the author this isn't working perfectly yet
also if I resize all of this we're getting some weird Behavior
but at the very least we can open a file dialog and we can import the image from this dialog
for the next part we are going to make all of this look much better which means the image is going to fill the entire
available space and also resize with the window we now have an image however the image
we have doesn't look anything like the final thing which means for this part I want to make sure we can see the actual
image and also if I'm resizing the image the image is being resized as well
for that we have to add quite a bit of logic to update the image and to place it properly
although the entirety of the logic I have covered in an earlier video on how to use images in tkinter I am basically
going to use all of that so if you want to have a lot more detail check out that video
here I'm back in the code and let me demonstrate what we have right now I can click on open image open the author and
now you can see that what we have is an ideal I suppose what we can start with
is to place the image right in the center of the canvas roughly here for that though I have to work inside of
resize image and in here what I'm placing 0 and 0 I need to know the size
of my canvas the best way to get that is to use an event
although this event I can't easily get right now I'm simply calling resize image in here this I don't want to do
anymore instead what I'm going to do is when I'm creating the image output I will insert
this resize image method into it as an argument self dot resize image
what this is going to do inside of the image widgets in image output
first of all I have to create a resize image method
and this resize image method I want to call anytime I am creating or resizing
this image which we can get with self dot bind the event here is called configure
if that is the case I want to get my resize image method
which means we are now going to call this method here and we get the size of
the canvas via the event as a matter of fact let me print the
event and let's see what we get if I now run all of this again open the image and the other
we can now see at the bottom we have configure event we have an X in the Y position those we
don't care about but then we have a width and a height this is the width and the height of the canvas
we could use that for example with event dot with and then divide it by 2 for X
for y this is going to be event Dot height divided by 2.
now if I try this and I click on open image we get something that looks significantly better
also if I resize the image this will always stay in the middle although since
we're not getting rid of the previous images we get a lot of weird stuff behind but at the very least we have a
start also let me get rid of this print here that's going to be annoying first of all
this resize image we are now going to call when we are creating this image
output and when we are resizing it which means whenever we are resizing the window this resize image will be called
the issue with that is that we are creating new images but we don't discard the old images
as a consequence we end up with way too many images and this is eventually going to tank performance
to account for that I want to get myself dot image output and then delete
with the argument the string all this gets rid of anything on the canvas which
means now once again I can get the other and now I can resize this thing and this
is looking significantly better with that we can place the image what we
now have to figure out is how to resize it for that we're going to need quite a bit of logic and once again for the entirety
of the logic that you need here check out the dedicated video I will go over it briefly but for the
full detail check out that video I suppose let me start with the biggest problem if I open the image again we want the
image to always be fully visible which isn't the case right now I can go
a bit further to the right and we can see more of the image so only with this do we show the entire
image however if I make the image smaller we are cutting off some bits
which means what I have to figure out is how can I not cut off certain parts
for this one I have to know the aspect ratio of the image and of the canvas
for example if this is the canvas
if I have an image that looks something like this in this example the image
would be taller than the canvas but less wide
as a consequence when I'm resizing the image I want to scale the height down so
that the entire image would end up something like this
however the other side is if this is the canvas again
I could also have an image that looks something like this in this example I
would want to scale the width of the image to fit into the canvas
as a consequence we want to start by figuring out if the image is wider or
taller than the canvas for that we will need the aspect ratio both of the image and of the canvas
let's start with the image we have the image up here and I want to get self dot let's call it
image ratio to get the ratio all I want is the width divided by the height both of these
numbers we can get quite easily the width we get with self dot image dot size this is going to return a tuple I
want to have the one with zero that's the width the height is going to be the
entrance with one so a one in here let's try this one I want to print self
dot image ratio if I now run this I can open an image
and we get 1.5 this means that the image is one point
times as wide as it is tall this specific number here doesn't matter but I do have to know it
which means I don't need a print statement anymore but instead now I have to figure out the aspect ratio of the
canvas which I can do inside of a resize image I want to get the current canvas ratio
let me store this inside of a variable as well canvas ratio and this number I
get with event dot width divided by event dot height basically the same operation we have
done up here except we're getting our width and our height via different methods once we have that order resizing I now
want to get a width and a height of the image although for that I first of all have to
check if the image is wider or taller than the canvas for that we can use the
canvas ratio for example I can check if the canvas ratio is greater than self
dot image ratio this means the canvas is wider than the
image if that is the case I want to get a new image height
which is going to be the event DOT type in the case we have right now this one
here is this version here what is really important to understand
is that the canvas the yellow area is wider than the image
as a consequence I want to scale the image in such a way that the top and the
bottom touch the top and the bottom of the canvas which means they have the same height which I am achieving with this
line here or at the very least for now I'm simply getting the height of the canvas but
later on we're going to use the image height to resize the image which means all I have to figure out now
is the image with this is very easily done because I have
the image ratio for example for this image I know it is always one point times as wide as it is tall
since I have the height I can simply get the image height and multiply this with self dot
image ratio with that we have a new height and a new weft this we can now use to resize the
image before we are placing it I am going to store this in a separate variable resized image this is going to
be self dot image dot resize this method wants a tuple with the new
width and a new height which in my case is going to be the image with and the
image height with that we have a new image this image
we now have to set as the TK image the one we created earlier but now we have a
new image which means self dot image PK is going to be the same line I have
used earlier let me just copy it and paste it in here although I don't
want to have self.image now I want to have the resized image
with that we have a start however we only cover one of the cases
we need an else in here else like so we have to cover
the canvas is taller than the image
which means in here we're going to need an image with and an image
height once again figuring out these two numbers is going
to be your exercise figure out these two numbers
once you have that all of this should be working and we can display an image
pause the video now and try to figure this one out
for this one if I open the drawing again the case we're working with right now is this one here
which means the image is wider than the canvas as a consequence we want to scale
the image to such a degree that we are covering the entire width of the canvas
and then the height comes as a consequence so to get started I want to set the
image width to the width of the canvas which can do very easily this is simply going to be event.wift
from that I can also get the height I simply have to get the image with
now for this one I know that the image is always one point times as wide as it is tall this we can also flip around
which we simply do by dividing the image with with self dot image ratio
these two operations here are doing the same thing we simply move them around a tiny bit
with that we have an image with and an image height for all aspect ratios let's
try this one now I can click on open image the author and now we're getting an error that
float object cannot be interpreted as an integer the issue here is that when we are
resizing an image the resize method wants integers for both the image width
and the image height but right now when we're doing some of these operations we're going to end up with floating
Point numbers that fortunately is very easy to fix I simply have to get all of these results
and then wrap them inside of an INT function now if I try this again I can click on
image utter and we have an otter what is really important now if I resize all of
this we are almost okay we're getting a tiny bit of an error but most of this is
working the error I got is that this event height is an attribute so I cannot call
it let's try it now it should be working there we go we have the others and
they're always looking pretty good this seems like the appropriate scaling
Behavior with that I can get rid of this comment
here for the exercise minimize all of the methods and we have covered another really important aspect
there's one more thing that we have to work on before we can work on the actual input buttons If I open all of this
again we do have the image but we don't have a close button which I want to add
for this video this is a very easy thing to add let's Jump Right In back in my code I want to
start by creating a widget for the close button this I want to do inside of the image widgets might not be the perfect
position but I think it's good enough we are only showing the close button when we are showing an image so I think it
fits in here quite okay this is going to be another class that I have called close output for The
Inheritance here we are only going to need a ctk button although this button is going to need a
thunder image method we need itself and I want a parent
now we're just going to place it to place it we need this super thunder in it method Master is going to be the
parent the text for this one is simply going to be an X after that I want to use the place
method to place the button in the top right for that I want to use relative x with
0.99 and then relative y with 0.01 finally I want to set the anchor to
North East this should give me a button that I can see all the way in the top right of the
window which means inside of main.pi after I have imported the image I have created
all of this stuff here I now want to create the self dot let me call it close
button this will be the close output button we just created and we just need self in
here as the one argument let's try this one I can click on the other and there we go we have a button
in the top right it doesn't do anything right now but we have something although it looks pretty bad
but that we can work on inside of the widget I want to update the text color which
should be Pure White this white we're getting from the settings this right here
after that what is even more visible is the FG color this I want to be
transparent besides that I also want to set a custom height and a custom width both of those
are going to get the same number which means the width is going to be 40 and the height is going to be 40 as well
since we are having a bunch of arguments I'm going to put all of this over multiple lines
that is much easier to read Also let's try it before I continue just in case I made a mistake
if I now click on open image and the author now on the top right we have a button that looks much better
what I now want to add is a corner radius with zero and finally I want to
have a hover color which I have set to close red
now if I try this one I can click on open image the auto once again and now I
have a close button in the top right cool with that we have the close button
but it doesn't do anything right now for that I want to create another method I
call this one close edit this one itself and nothing else
I want to hide the image and the close button
this is going to be your exercise and it's going to be somewhat similar
compared to what I have done here oh also I forgot we want to recreate the import button
essentially I want to hide the image output and the close button and then show the image import button again that
way we can import another image pause the video now and try to figure it out yourself
to get started I want to hide the image and the close button since I have the
attributes for both I can simply Target self dot image output and then use Grid
or get for the image output I also want to use forget except this one has to be Place
forget because we're using the place method to place it or the other part to
recreate the import button I want to create self dot image import
is going to be this is the same line we have used inside of the init I want to
copy this one here and assign it to image import
with that we're getting rid of the image and the close button although this one should be image output it should be the
close button and we are recreating the import this is almost working except there's
one thing missing we are never calling this close edit right now we have this close button
but there's no command which means it doesn't do anything but that we can add quite easily we need a command in here
this one is going to need some kind of close function this close function we
don't have available but we can pass it into the widget so I want to get the
close function from the parameter now back inside of main.pi this close
button when we are creating it needs cell for the parent and on top of that we need self Dot close edit that way we
are calling this method let's try now I can open the image open the others we
can see the authors and if I click on X we are back to open image I can click on this one and open another image and this
one seems to be working just fine with that we can open and close the editor
and that finishes another major part of this project at this point we have the image this is
the first major part done which means now we can start working on the menu this one contains quite a few different
parts I will be going through them step by step the one I'm going to start with now
is this main panel here this is a custom tkinder widget that is a container that
has different panels it's really easy to implement let's have a look at this one back in my code editor I want to create
another widget for this container since this is going to be a larger project I
am going to create a new file I will save this one as menu dot pi
first of all as always we need to import custom t Kinder as ctk
this allows me to create another class which I called menu
what makes this one special is that for the inheritance we are using ctk tab
View this is basically a frame with tabs although other than that we need the
dunder init method with self and the parent and later on we're going to add more but that's enough for now
after that we need Super init and set the master to the parent
last step I want to place this menu right away using grid with row being
zero and the column being 0 as well on top of that I want to set sticky to
north south east and west with that we have a menu let's use it right away inside of main.pi for that
first of all we have to import it which means from men you import menu
this I will create inside of import image because in here
we are first of all closing the input button and then we are creating the image editing stuff so the image output
and the close button besides that I want to create a third thing which is going
to be self dot menu for that I am going to use the menu class I've just created the one argument
we need for now is sell for the parent on top of that for close edit I should
get rid of the exercise in fact I should get rid of all of the text we don't need that anymore like so
what I want to do inside of this method now is to hide this menu as well
just like I have hidden the image output and the close button which means in here self dot menu dot grid underscore forget
then everything should be working let's try I get the usual menu and now we get
some slightly weird Behavior but at the very least for now we have a container so something is happening
although right now there's an issue and that is these columns are not properly
represented let me run the entire thing again really quick you can see here that roughly the image
on the right this with here is roughly as large as
this width here which is not what I specified earlier these two lines don't seem to work
properly anymore that is because I have to specify uniform and set this to some
kind of string it has to be the same for both of them if I now run this click on open image
and an image now this is looking much better all right with that we have the proper
menu so let me minimize all of this now we can work inside of the menu
first of all what I want to create in here are the tabs those you create using self and then the
add method the one argument you want for this one is the name of the tab for example the first one that I want is
called position let's try this one if I now click on open image and an image we can see
position this is going to be the only tab for now although in my case I want to have four
tabs I want to have the color I want to have effects and finally I want to have
export let's try this one one more time and there we go now we have four tabs
that we can toggle between so now we have to figure out how to attach a frame to any of these tabs
I am going to start with the class position frame which is going to be just a ctk frame
this one is going to work like any other frame we have created so far which means we need self and a parent after that
called super Thunder init and set the master to the parent
once we have something like this inside of the menu I can create the widgets
well now I just want to create a position frame although now when we are setting the parent we are not using self
instead we are using self dot Tab and then the tab we want to attach the
widget to which in this case is going to be position although if I were to run this you
wouldn't really see a difference because this widget here is going to look identical to the background of the menu
we can change that by setting the FG color to something like blue
and to really make sure that this is working let me duplicate the entire class and change position to let's say
alert is the second one this one is going to work in basically the same way except for now I'm going to
change the background color to Green finally for the position frame I want to
add a duplicate and change position to color with the parent being the color tab not
the position let's try all of this now I can run the app again click on open image click on
utter and now we can see that nothing happened the reason for that is that these two
frames position and color also need to be placed like any other widget for them I can simply use pack because
they're supposed to fill the entire area which means I want to set expand to true and fail to both
let me duplicate this one and now let's try this again click on open image otter and there we have a
completely blue tab if I click on color it's entirely green effects and Export don't have anything yet so they are
empty but at the very least this is working with that I can set the background color for both of them to transparent
and now I have to figure out what to add inside of these frames
since that is going to be quite a bit of logic in and of itself I have created another python file that I have saved as
panels dot pi the way you want to think about it if I
open the finished project and open image really quick
basically what we have right now is a frame for each of these tabs what we now have to create are these
panels here these are going to be reusable components for example this slider box
here and this slider box here are the same class the only difference between them is that I inserted different
arguments as a matter of fact inside of color we have two more slider boxes these two
here and inside of effects we have two more all of these sliders are the same
class I simply use different arguments to customize them although besides them we have other widgets like this one here
or like these toggles or like this box here
all of these we have to create for now I'm simply going to start with this slider box this is going to be a fairly
simple one although for now it's not going to do anything but that I am going to work on in the next part
I want to work inside of the panels in here I have to first of all import custom tkinter as ctk
once I have that I want to create a class that I called panel this one has
to inherit from ctk and ctk frame first of all in here we are going to
need to done their init method with self and the parent we have done this multiple times by now after that super
Thunder init with master being the parent
finally I want to use self.pack this one should set fill to X
on top of that I want pad y to be 4 and iPad y to be 8. this will create a
fairly basic panel that doesn't do much by itself also I forgot one more thing I want to set an FG color in here which is
going to be dark gray this is the dark gray that I'm getting from the settings this dark gray
although for this to work I have to add from settings import everything let's
try to use this one right away inside of menu dot Pi I want
from panels import everything with that inside of the position frame I
want to create a simple panel with self as the parent
now let's try to use this one open image order and there we have a simple
container which is ideal because in here we could now write a sliders some text we could
add switches basically whatever we wanted the idea basically is that this panel is
going to be a parent class and from this I'm going to create the actual
panels that you are going to see for example the one I will be using the most is the slider panel this one is a child
of the panel which means inside of the image method
after self I have to specify a parent also I now want to specify some kind of
text to display what kind of box we are going to have Adobe I am still going to need Super
init or this one I have to set the parent to the parent because remember this parent
here refers to this parent which is going to set the master
what we are now able to do inside of the slider panel I can for example create a
ctk and ctk label self is going to be the parent
the text I can now set from the text the one I've specified inside of the parameter
just so we can see something I want to pack this thing right away once I have that inside of menu I don't
want to have a panel anymore instead I want to have a slider panel beside itself for the parent this is going to
need some kind of text let's add test in here once again I can run this open image
order and now we can see we have one panel that says test that is working really good
which means now we can create all of the stuff for an actual slider panel in here as a reminder what this is going to look
like let me open the final thing I want to create this slider box here or
this one here they're the same creating this layout is going to be your exercise I want you guys let me clean this up a
tiny bit I want you guys to recreate this slider box most of you now and try
to figure this one out let's get started in my case I used a
grid layout which means I want to start with a layout we need self.row configure
I have zero and one rows that both have a weight of one
the same thing I want to do for the column configure which means we have two
rows and two columns with that this ctk label shouldn't use
pack anymore instead we need grid and this text I want to have in the top left which means column is going to be 0 row
is going to be zero and let's stick with that for now besides that I want to have a second
piece of text that for now is simply going to say 0.0
I should do all of this actually this is going to be the text box and
because of these two lines here we have basically created this kind of layout
the first item I have set in here is the first ctk label which is going to occupy this top left cell here this is 0 and 0.
these numbers next up I want to create another ctk label that should be 0.0 in the top
right which means we are still going to be in row 0 but column should be 1 now
let's try those two I can click on open image again utter and now we get test
and 0 and 0. however I want to make one more change this test should be all the
way on the left roughly here while this 0.0 should be all the way on the right roughly here
to achieve that I can use sticky a title text for this box should stick
to the west side is 0.0 should only stick to the east which means the right
side let's try this one again now and that is an improvement but now I
think the issue is that both of these text labels are far too close to the Border
this I can fix as well by using some padding both of these labels should get pad X of
5 and now we should have a good result there we go I am happy with this one you
could probably add a tiny bit more padding but well experiment around finally I want to add ctk and ctk slider
order parent I'm going to set self here and then we can place this using the grid method right away
row should be one column should be zero and since I want this slider to span the
entire wift column span should be 2. let's try this one open image click on
the order again and there we have a slider that's not looking bad at all although a few tiny more changes I want
to set sticky to East and West so we are covering the entire horizontal space
although just like with the labels I want to add a tiny bit of horizontal
padding now let's try this again open image otter and well this looks
basically identical but now we have a bit more control over it also we can try to add for the slider a
bit of vertical padding let's go with five as well I think that's going to make the entire
thing look a bit more open yeah I do like this one better although the difference is quite minor
all right what we can do now inside of position frame rename this label to
rotation what this allows us to do if I open the entire thing again we now have the
rotation text box this one is looking pretty good oh although there's one thing that I did
forget inside of panels or in this slider I want to set an F G
color which is going to be slider PG from
settings this color here what this one is going to do is make the
slider background a tiny bit brighter so it's easier to see the change once again is not very pronounced
now we have the actual box for the slider what is even more important now
we have the rotation box this is this slider panel but now I can duplicate this because the
second box I want is called Zoom what this one does if I rerun everything
we now have a second box that can work independently so with that we have made a ton of
progress although unfortunately neither of those do anything so this I do have to work on
although before we get to that there's one more change that I would like to make there is right now no padding
between the menu and the image which seems a bit cramped so I want to
add a tiny bit of padding both for the menu and for the image for the menu when
I'm using the grid method to place it up here I want to add pad Y which is going
to be 10 and Pad X is also going to be 10. besides that inside of the image
widgets the image output in the grid method I also want to add pad X and such as to 10
pad Y is going to be the same finally I can run my DOT Pi again the
otter now the entire thing looks a bit more spacious so next up we can make all of this
actually work now that we have the basic layout we can start working on the actual functionality of this image editor what
I want to start with is the rotation which means this rotation slider actually rotates the image
to make this kind of thing work we are going to need a couple of things most importantly to understand the basics is
that this rotation slider is going to be connected to a custom taken to a
variable and when this variable changes we are going to update the image in a certain
way for this particular case we're going to rotate the image but this could also later become a zoom or it could become
an invert or any of the color or effects but let's do all of this in code this is
going to be much easier to understand once again I am inside of main.pi
what I want to do in here is first of all I want to create another method that
I called init rameters which one itself and nothing else for
its own parameters what I want to do in here is to initiate the parameters that are going to track
the data for the image manipulation later on there will be quite a few in here but for now I simply want to create
self dot rotate and this is going to be a float this is going to be an object ctk and
double VAR this one is also going to have a start value which I set with the value a start
value I am getting from the settings this rotate default here is what I want I can copy it and use it for the value
with this we have some kind of way to track the value of the rotation of the
image by default it's going to be zero now once we have that we want to do a
couple of things number one we want to connect the
VAR to the slider which means this
rotation needs to be accessible or rather changeable from inside of this
slider panel so we have to somehow get it in there once we have that number two we need to
trace changes to the VAR which means once this slider panel is changing the
variable we want to do a certain thing finally number three
we want to use the VAR value to change the image
which in this case means anytime we're moving the slider we're updating the VAR and then we're updating the image
so let's go through this one by one number one we have to connect the VAR to
the slider although before we can do that we have to call this method this is going to happen inside of init before we
are creating the widgets I want to self dot init parameters
I suppose we can do this right at the top it makes a bit more sense there with that I can minimize the init method
because now I want to work inside of import image the reason for that is that the menu
needs to have access to this self.rotate float that way let me pass it right in self
dot rotate float that way inside of menu the class I can create another parameter
let's call this the rotation the rotation I want to pass right through to the position frame which means the next
argument in here is going to be the rotation with that inside of the position frame I
have the rotation available and now I can pass this into the slider panel
rotation for this one that way the slider panel has access to
the rotation which means inside of the panels I can work inside of the slider panel
although first of all I have to give this another parameter the rotation what
this allows me to do for example I can set the text well I can remove it right away and instead get a text variable
which is going to be the rotation I can do the same thing for the slider
although this one is going to be a variable which is also going to be the rotation
with that when we're moving the slider the text should also update let's try this one actually
I can open the image and now if I click on rotation we get something so
definitely we're making progress although the number here is way too precise
also let me comment out the zoom for now because this one is going to cause an error well now I want to keep on working
inside of the rotation they had too much of problems actually the first one is that this ctk slider I
think goes from zero to one which is fine for a starting value but I want
this to go from 0 to 360. as a reminder a full circle so a full rotation starts
at zero and then goes all the way around to 360. which means the slider let me do
this over multiple lines right away the slider is going to need
two more arguments we need from and underscore this should start at zero
and then go to and this should be 360. which means now
we should get the numbers from zero this is a good starting point and I can go
all the way to 360. although the problem now is that the number is way too
precise we don't need this many numbers before we can get to that we have another issue this zero and the
460 are only unique to this particular slider panel if I want to create another
slider panel for example for the zoom the numbers might be different as a consequence these numbers cannot be hard
coded although that is very easy to change I want to add another parameter or rather two parameters
that are Min value and max value ROM is going to be the Min value 2 is
going to be the max value for the slider with that back in menu I can add two
more arguments that are going to be 0 and 360. that way this slider panel
becomes actually a reusable component where we have a name a variable and then
a start and an end value later on for the zoom panel we can simply copy it and
add different numbers and then we have a completely new panel before we can work on that we have to update this ctk label
the issue once again is that the numbers we are getting from the text variable are much too precise
to fix that I want to round them but for that we have to add a tiny bit more logic first of all I want to get access
to this ctk label by turning it into an attribute let's call it the num label
this is simply going to be the widget we just created after that I
want to place it with the grid method so self.num label so far this is going to
be the exact same result although this one is not going to get a text variable instead I am just going to
set the text which is going to be self dot rotation
dot get by default this one is going to be zero with that let me run the code again
we are getting an error this isn't going to be self this is just going to be the
rotation now let's try it again there we go now we have rotation and the
number on the top right doesn't do anything because we are simply getting the value of the rotation but then not
using it this one here doesn't do anything right now for that I want to
create a separate method I call this one update text
this one is going to need self for the parameters besides self we are also going to need a value
this value we need because we are calling this update text from the slider
via the command this is going to be self dot update text
what this optic text is doing let me demonstrate right away I want to print the value
if I now run this again a slider is going to print whatever
number we have inside of it which means now the numbers go from 0 to 360.
these numbers I want to use to update this num label
which means I can copy it and use configure to update the text in there
I simply want to update the text which is going to be an F string
I simply want to round the value I'm getting from the slider with two decimal points
with that I can run main.pi again click on the utter and now we have the text
updating in the proper way this looks significantly cleaner
righty with that we have connected the VAR to the slider although inside of the panel this
shouldn't be called rotation because later on the slider panel should also connect to other kinds of variables let
me simply rename rotation to data VAR that way the slider panel becomes a bit
more generic ready but now we have covered the first bit
which means I can get rid of it now we have to trace the changes to this
variable which means whenever this rotation field changes we want to do something
that is actually super easily done all we need is self.the rotation float and I
want to run the trace method whenever we are changing the value or more specifically whenever we are writing a
new value in it then I want to call a method the method I want to call is going to be
manipulate image that doesn't exist right now let's
create it self dot manipulate image for this one we need self and we need the
arcs these arcs are passed into it automatically whenever we are calling a method using Trace
inside of this manipulate image we can now make changes to the actual image which means we have covered the second
part as well now we have to cover how to update the image
essentially what we are going to do we are going to take this self image and then run some methods on it the pillow
library has lots of methods to change an image for example we could blurred rotate it
Zoom it flip it add some contrast or some other effects also change the brightness or the grayscale there are
lots of things that we can do however for this one we have to be careful because we don't want to make
changes that we cannot reverse for that when we are importing the image I am
actually going to create a self dot original and this is where we are
storing the image so image open Dot path is going to get the original and then
self.image is going to be a copy of self.original that way I can make
whatever change I want to the image whereas original is going to stay unchanged that way if I make too many
changes I can always revert back to the original that is a super important thing to start with now inside of manipulate
image first of all I want to override self.image with self.original once again
that way I am always starting with the original image once I have that I can apply the
different changes to it for example if I want to apply rotate I could get myself dot image
and to apply rotation I want self dot image and then
rotate this method wants a single argument which is going to be the rotation
which I'm getting from self dot rotate float dot get
that method is going to return a new image which we're now storing inside of the original image all we have to do now
is to set this new image as the image we are outputting which we have done
earlier inside of this resize image down here
we essentially want to call all of this again except now with a new image which
means I want to reuse this code as a consequence I'm going to turn all of this into a separate method that I
called place image which needs self and nothing else
although with that we have to make a few more changes first of all after we are
resizing the image we have to call self.place image to make sure that this
works in the first place unfortunately now we have to make a few more changes because of the local scope
of these methods the basic issue is that these variables are only available
inside of this scope while they are not available in this scope
which is going to cause an error so we have to account for it the way around it the way I approached
it is let me actually minimize all of these methods otherwise this will get confusing inside of the init method
before I'm creating the widgets I want to create some canvas data
this is going to be self Dodge image with which is going to be 0 by default
then we have an image height which is also going to be zero then we have a canvas with and a canvas
height once we have those numbers inside of resize image
every time we are resizing the image I want to update the numbers I have just created
this means all of these image width and image Hive variables need to be
parameters which I Do by adding self in front of them also this image height and this image
width needs to have self as well with that I have covered the image width and the image Hive but I
also have to update the canvas width and the canvas height which means
I want to add another section here with update canvas attributes
this is quite easy done all I need is self dot canvas with is going to be the event dot with then I
can duplicate this and simply change the wift to right
with that I can minimize resize image although I do have to make some changes to place image image output.delete all
still works just fine although resize image now needs to work with the
attributes self dot image with and self.image height self.mhdk is working just as before this
one doesn't need any changes although for the image output this image width divided by 2 should be
replaced with self dot canvas with divided by two same for event height
this should be self dot canvas height divided by two this should be all the changes that we
have to make let's try all of this again I can click on the other and there we go
the order still works although the rotation right now doesn't work at all
because inside of manipulate image we're not calling this place image we're
simply updating the image but we're not setting it to the output for that I simply have to call
self.place Image at the end of manipulate image now let's try this
again open the image author and now the rotation is working just fine
and with that we have the first part of the rotation now I think so far this is
probably a bit confusing I think the best way to approach this is to do
another example inside of the parameters I want to create a second attribute this time for
the zoom which means I want to have self dot Zoom underscore float this is also
going to be a ctk double VAR as a matter of fact I can simply copy this one although the start value is well it's
also going to be zero but I want this to connect properly so Zoom default here is
the start value also I can get rid of this text that's going to be confusing this Zoom float I
now have to pass into the menu which is happening inside of import image in here
besides rotate float I also want self.zoom float which means now inside
of the menu besides rotation I also need Zoom this Zoom I want to pass right away
into the position frame right after rotation which means zoom in here and I
am also going to need another parameter which is going to be Zoom what this allows me to do is to Simply
uncomment the slider panel and add in the zoom in here this one should go from
0 to 200. with that I have connected the variable to the panel so I can minimize
the import image next up I have to trace it for that I can simply duplicate this
method and change rotate float to zoom float with that we are calling manipulate
image whenever we are changing the zoom float value with that I can call
manipulate image in here I want to have the zoom this is going to work just as
before I want to update self.image to change this one though we have to
import another module from the pillow Library this one is called image
Ops the way you are using this is you first need image Ops and then dot drop
this one wants two arguments the first one is going to be the image which in our case is always going to be
self.image besides that it is expecting a border
this border we are getting from self dot Zoom float dot get
with that we can run the entire thing I can click on open image get the order now we have two panels I can rotate it
still but now Zoom is also going to work although it's not perfect Zoom it
stretches the image a tiny bit but this is the easiest way to get zoom in pillow
and I guess for our purposes this is good enough but you could totally update this to get proper Zoom
I guess but it's really important to understand here is that we first of all copy the original to the image then we
are creating a new image if we are rotating the image then next up this rotated image we are
zooming if we are using the zoom that way we are applying both of these changes
now before I'm changing this video I have made a couple of changes to how the image is being displayed and I think I
should talk about those because it's probably a bit confusing so let's go through how the image output
is going to work first of all when we are calling the edit method we are declaring a couple of
basic variables we need to get the image width and the image height and the canvas width and the canvas height all
of those are zero by default that one should be fairly easy after we are doing that we are calling import image in here
we are importing the image but then most importantly we are getting the image
ratio this we only have to get once because we care about the ratio of the original
image for the rest we're simply getting rid of the import button and then display the image so this we can ignore
for now what is much more important next up is we are resizing the image for that
we're getting the canvas ratio and then we're updating the attributes for the canvas with and the canvas height
after we have that we are resizing the image in such a way that it fits into
the canvas perfectly finally inside of place image
we are getting whatever image we currently have this could either be the original or the manipulated image and
then we're getting the image width and the image height we have set up here this we are then turning into an image
TK and finally we are creating an output and to get the center of the canvas we
are getting this canvas width and canvas height and divided by two I am not quite sure how confused you are by this but
your main exercise for this part is to try to understand the logic here of how the image is being displayed ideally try
to recreate all of this and try to do all of this from scratch the logic for this one unfortunately does get a tiny
bit more advanced but well we can continue so let me minimize all of this and I'll see you in
the next video at this point we have the basic layout and some rudimentary
functionality which means we can rotate the image and we can zoom into the image
from this point forward we have to cover two important steps number one we have
to create a whole lot more variables to cover all of the different options for example right now we have a variable for
the rotation and for the zoom we are also going to need one for the invert
after that we need three more variables to cover everything inside of color three more to cover these final panels
which means we're going to need nine variables in total which means we have to organize our data management a tiny
bit better this is what I am going to start with other than that we have to create a few
more panels for example this invert panel here doesn't exist yet this switch panel here we also have to
create and finally for the effects we have to create this box here which is a
drop down menu for example for these kind of effects back in my code I want to work inside of
init parameters this one creates two attributes right now rotate float and
zoom float which is fine but that's not exactly what I want to do since we have to
create quite a lot of variables this is not going to be efficient what I want to do instead is create a
couple of dictionaries for example the first one is going to be self dot pause vars
this one is going to have an entry for rotate the associated value is the one
we have created earlier the ctk double VAR with the start value of rotate default
I can copy this one more time next up we have zoom this is also going to be a
double bar although the default value is going to be Zoom default finally there's one more that I want
this is going to be flip this one we haven't used yet this is going to be a
ctk string VAR or the start value for this one we are
going to need one but it's going to work a tiny bit different compared to what we have done before essentially if you look
at settings we have flip options and this is a list
later on when we have the effects this is going to work in a similar way the idea is that we have a couple of options
and 0 is always the default which means when I assign the value I want to have flip options with the index 0. this
would cover all of my position variables with that I can get rid of these two
entries here although I do have to cover the tracing this one also wouldn't work
right now to replace that let me add a comment in here tracing I want to use a
for Loop for VAR in I want to check self dot pause vars
dot values and don't forget to call this one this is going to give me all of the vars
this double VAR this double VAR and this string VAR I want to get all of them
and then use the trace method the arguments are going to be the same that we have covered down here
with that we can get rid of this bit as well and now we are organizing our data much
more elegantly although that being said when I am running import image
rotate float and zoom float don't exist anymore so I want to get rid of them I
will replace them with self.posvars which means now in the menu we also have
to update the parameters I am just going to have the position variables
those I'm going to pass right through to the position frame and here I want to
have to pause the vars this also means inside of position frame rotation and zoom should go instead I
want to have my position bars finally when I'm creating these slider panels
instead of rotation I want to have my pulse vars in here I want to get the key
rotate I think that's what I called it yeah rotate this one
or the zoom I want to have my passwords dictionary with the key Zoom
with that the app should work just as before if I open the image I can still rotate
well I can't and I do know why because inside of manipulate image we are still using
rotate flow.get and we're using zoomflow.get neither of those exist anymore
instead I want to get my self.posvars the first one is going to be rotate
Zoom float should be post virus with the key Zoom now this should be working
let's try the author and now we're getting another error
ah right I see the error I forgot the get method for both of them
now this should be working I hope I don't want to know what promise auto rotate now this is working both for zoom
and for rotate cool which means now we have the basic
variables and tracing for the position next up I want to create another
dictionary with self dot color virus
this is going to work in basically the same way that we have seen up here except we are creating variables for
other attributes also I want to indeed these key value pairs that makes all of this look a bit
cleaner borde Calaveras we have four values in
total we have brightness this one is going to be a ctk double VAR a start
value for this one we're getting from settings somewhere in here we have brightness default this one is going to
be one next up we have grayscale this one is a ctk Boolean VAR a start
value for this one once again we are getting from settings grayscale default
it's just going to be false after that we have invert
this one is also going to be a Boolean VAR meaning I can just copy all of this although I do have to change the start
value this one is invert default finally we have Vibrance
which is going to be a ctk double VAR which also has a start value
which we are getting from Vibrance default there we go this covers all of the data
for the colors there's one more that we need and that is
self.effect vars and for this one I don't want to bore
you so let me just copy it in this one is going to look like this
we have blur contrast and effect blur being a double VAR contrast being a
ctk intvar and effect is going to be a string VAR blur and contrast both have a simple
default value whereas the effect is going to work like the flip which means
effect options inside of settings is going to give me a list where the first value is none but other than that we
have emboss find edges contour and Edge enhance I am for now simply picking the first
entry with that we have all of our tkinter
variables that are going to track the changes we are making to the image let me minimize them what we now have to
figure out is how to trace through all of them for that you could create three four
Loops but that wouldn't exactly be elegant instead I want you guys to try an exercise
I want you guys to apply Trace to all of the nine variables using a single for
Loop the one I have already created pause the video now and try to figure this one out
the way you want to approach this one is you can simply add a plus to get for
example self dot color vars.values
although this by itself if I run all of it is not going to work because right now we are trying to add dictionary
values to other dictionary values which isn't going to work you can only add
lists together and that way you are getting a combined list which should be giving you the answer because all we
have to do is convert both of these dictionary values to a list
that way all of this is simply going to work although since we have three
dictionaries we have to do this one more time plus a list of self dot effect bars
dot values there we go with that we have one for Loop that applies Trace to all of the
variables although in my case I want to store all of them inside of a separate
variable that way you don't have to scroll let's call it combined vars is going to
be the list I just created which I want to Loop over so for VAR in
Combined bars then we are applying the tracing to it the way you want to think about this
kind of logic in here is that you can very easily combine lists but dictionaries are much more difficult to
work with as a consequence it's quite a common thing to convert a dictionary to a list and then work with it for a bit
because lists are much much easier to work with all right but with that we
have initiated all of the parameters what we now have to do is to pass all of
them into the menu which means besides the position variables we also have self
dot color vars and we have self dot effect variables
to make all of that work inside of the menu we need two more parameters
we have the color vars and the effect vars the color vars I want to pass right
through to the color frame after that I can create an effect
frame that is going to have self dot tab
effects as the parent besides that it is going to get the effect variables
this effect frame doesn't exist right now let's create it all the way at the
bottom I want to have class effect frame this one is just going to be a ctk
frame with it under in it method as a matter of fact I can copy all of this since
it's going to be the same although the color frame is going to
need the color vars while the effect frame is going to
get the effect vars now this is going to work
with that we can work purely inside of these frames because they have all the
data that they are going to need first of all inside of the color frame I want to create two more slider panels which I
can do very easily I just have to copy the slider panel the first point is going to be the rightness with the color
vars of brightness the minimum for this one is going to be
zero but the maximum is going to be 5. then I can duplicate this panel and
change brightness to Vibrance the Calaveras variable we are looking at
is going to be Vibrance as well which is also going to go from 0 to 5. neither of these panels
are going to do anything right now but at the very least we should be able to see them although if I run the code I
get an error that a bracket was never closed this happens inside of when I'm creating
this list which is going to be inside of init parameters or this one all the way at
the end I forgot one bracket now let's try this again we can still open an
image is this looking good and now if I go to color we have brightness and Vibrance both of which start at one I
can move the slider but it doesn't do anything right now but at the very least we can see something
while we are here I can also work on the effect frame because this one is going to get two slider panels as well
we get one slider panel for the blur which is going to have the variable from
effect virus with blur the values here go from 0 to 3. and I
can duplicate this one because the next one is going to be contrast which is going to get the dictionary entry for
contrast and the values go from 0 to 10. and I hope while you are watching this
you can see why these panels are super useful I can simply duplicate them and
then I get a whole panel that can influence one specific variable all right let's try out of this we
should be having three panels now we have position color and effects and all
of this is looking really good the numbers also update along with it I'm very happy with this one
which means now we have to create a few more panels to cover the other kind of
variables this is going to happen inside of the panels first of all I want to create another
class for I call it this one is segmented panel
let me run the final app again the panel we are going to create is this one
it's quite simple to be honest we have a label at the top and this thing here is
a ctk widget although both of those are going to be
inside of a panel which is going to be the parent inside of this one I want to have a
Dunder init method with self this one needs a parent then
we have some text next up we need a data variable finally we're going to need the
options for this panel first of all we need the super Thunder init method which sets the parent to the
parent we have gotten from the parameters after that I want to create a ctk label the parent is going to be self
and text is going to be whatever we are getting from the parameters since the layout is going to be simple
pack here is totally fine the actually interesting widget for this
panel is going to be ctk segmented button I hope I spelled it correctly
it's looking good this one wants to have a parent as
always and then we are going to need values these values we are going to get from
the parameters this is going to be options after we have that I want to pack the
widget as well I want expand to be true fill should be both finally I want to
have pad X to be 4 and Pad y should also be 4.
this is going to give me a segmented panel we now have to figure out how to call it this will happen inside of the
menu and since I'm importing everything from the panels I can use it right away
this segment panel I want to use inside of the position frame because in here I
have my position variables I want to get my segment panel the
parent is going to be self besides that the other parameters are text Data VAR
and options let me copy them in the text we can just set as whatever we
want I caught this one invert the data variable we are getting from
the position vars which I called invert or at least I think I did
if I look at the position bars in here we have lip which means there should be
flip instead of invert the options I am getting from the settings I want to get flip options and add them
for the options this should be all I need if I now run all of this select the auto once again
we're getting an error that segment panel is not defined which probably
means I made a typo I call this the segmented panel not the segment panel
let's fix that one let's try it again if I now try it again there we go we
have an invert button or panel or segmented button whatever you want to call it
although it doesn't do anything right now but we can work on that in just a bit for now though there's one more thing
that I want to do and that is anytime I am clicking on any field inside of this segmented button I want to update this
data VAR for that inside of the segmented panel we can add a variable
which is going to be the data bar with that we have this segmented panel
I can now create another class which is going to be a switch panel
once again the parent here is going to be the panel let me demonstrate what this is going to look like at the end in
the final app inside of color we have this top panel here where we have a
couple of switches that either activate black and white or invert color not a particularly difficult panel to
create I want self and the parent as usual however now for this one I want to
account for an unknown number of switches which means there could be two there could be one there could be five
in here I want to panel to handle all of these cases as a consequence the parameter
here is going to be arcs or Asterix args to be more specific what I am expecting
ultimately is a tuple and this Tuple contains other tuples inside of these in
our two boards we have a variable and then some text the variable will be connected to the switch and the text is
going to be the name of the switch inside of this Tuple you can have as many inner tuples as you want this is
actually very easy to add although first of all we're going to need Super thunder in it
where we set the parent to the parent next up we have to account for all of
these arcs this is going to happen inside of a for Loop or VAR and text
inside of the arcs this is going to give me a variable and a text
this I want to use to create a ctk and ctk switch
the parent is going to be self as always since I have the text right away I can
set this as the text for the switch and I can also set the variable for this switch as the variable I'm getting from
the Tuple for these sliders I also want to apply a tiny bit of styling they get
a button color which is going to be blue this blue I'm getting from the settings blue
also they are going to get an FG color
which will be the same as the slider background they're resulting widget I want to store
let's call it switch once I have that
I want to hack this switch widget
the important thing for this one is the side should be left other than that expand should be true
bill should be both and then I want to have pet X of 5 and Pad y of 5.
this is going to cover the panel let's try to use this one I am going to need
this inside of the color frame I want to create a switch panel
the parent is going to be self as always next up we have to cover these arcs
which are going to be well basically two bolts I can add one tube in here we need a VAR
and some text the text is the easy bit the first one is black and white I shortened this to b w
the variable we are getting from the color vars the entry name is gray scale
then I can duplicate all of this because the next entry is going to be color vars
and invert the name for this part is going to be invert
with that we have another panel let's try and click on utter and color and
there we go we have the invert buttons once again they don't do very much but
at the very least we have the visible part next up inside of the panels there's one
more of the main panels that we have to create this is going to be a class of
drop down panel this is going to be a tiny bit different
because we are not going to use the panel instead we will inherit from ctk
option menu I should actually demonstrate what this one is doing if I open the final app
again inside of effects we are creating this widget it's simply a drop down menu I can click
in here find edges Contour etch enhance and then you get different effects
applied to the image the effects apply part we don't do yet but we are going to
create this drop down menu this one works kind of similar compared to the segmented panel or rather the ctk
segmented button in the sense that you need a variable and some values
which means this should be fairly doable it's going to be your exercise
create this drop down panel pause the video now and try to figure
this one out you will have to apply a bit of custom styling so play around and see how far you get
as always we have to start with a Dunder init method this one itself it needs a
parent it needs a data variable finally we need options
pretty much exactly what we have done for the segmented panel for this one we are now going to need a
super init method there are going to be a couple of
options so I'm going to do this over multiple lines right away the most obvious one is now we have to
set the master it's not going to be the parent anymore because we inherit from a ctk widget not from the panel
other than that we have to set values which are going to be the options
once we have all of that I want to use self.pack to pack the widget
I want to set fill to X and Pad y to four
with that part covered we should at the very least have something let's see what
we get when we create it I want to create this panel inside of the effect frame
once again all the way at the top I want to have it drop down panel
for that we have to copy all of the parameters parent datavar and options
parent is the easy one self all the data variable I want to get the
effect of ours the key we are looking for here is called effect finally for the options this one we are
getting from the settings effect options I just want to copy and paste and then
we should be good to go let's try main.pi open image otter effects and we get a drop down
menu this one looks pretty good we can click on things and we get the right option although The Styling doesn't work
out right now and this also doesn't do anything but this we can work on quite easily
first of all for the styling I want to set an FG color to dark gray
after that we have to set a button color then we need a button
hover color finally we're going to need a drop down
FG color all of these colors we are getting from the settings although I did realize I
didn't actually create them so let me paste them in at this point there we go these are the three colors
that I want to use we have dropped on main color dropped on Hover color and dropped on menu color
drop down main color is going to be the button color the button hover color is
going to be the drop down hover color finally the drop down FG color is going
to be the drop down menu color sorry about the colors I completely didn't realize
let's try all of this one now if I click on open image otter effects and there we
go this is looking significantly better finally we have to connect the variable
to this menu so it actually does something What You Do by setting the variable this
one is going to get the data bar with that we have all of the main panels
let's try all of this I can click on the utter the rotation works and the zoom
also works both of us do something but for the invert we get nothing next up we
have colors and some sliders and then we have effects that works and we have blur
and contrast so all of this is working but well this video is getting quite long so for the
next part we are going to make all of these variables actually do something at this point this is quite easy to
implement so I'll see you there at this point we have all of the panels and all of the data to organize our app we can
actually start working to implement all of the functionality I'm going to work on the invert button
on the colors so we have brightness Vibrance invert and black and white and
we are getting the colors like blur contrast and stuff like Contours we're
going to apply all of that in this video back in my code editor I want to work
inside of manipulate image this method is going to organize all of the image manipulation
we already have a couple of things in here now the really important thing that you absolutely have to understand is
that we always start this method by assigning a new image this image always
starts with the original this image we are then going to transform for example
we are starting by rotating it this is going to give us a whole new image this
new image we are then using inside of this line and then adding a zoom that
way we have a rotation and a zoom at the same time this we simply have to continue forever for example to add a
blur or to change the brightness or to flip the entire thing we basically take the image we have and we keep on adding
changes for example what we could be doing to finish up the positioning is the flip logic although this one is a
tiny bit different compared to what we have done with rotate and zoom first of all though I have to check if self dot
pause virus the key I'm looking for here is called lib
I want to get the value of this variable and for this
one we have a couple of different options for example we have capital x then we
want to do a certain thing for now I'm going to write pass besides that we also have
that the flip could have the value of y finally we could have a value of both
these are the values I specified in settings we have x y and both these flip
options we are passing into the panels specifically let me minimize all of this in the segment panel we are passing in
these options which means when we are clicking on one of these buttons this data variable becomes the option we have
selected I suppose just to test this let me print X I want to print Y and finally
I can print both let's try this one now I can click on
open image the author and now I have none this one doesn't do anything but if I click on X Y and both we get X Y in
both this is working really well although I don't want to print X Y or
both instead I want to assign a new self.image this new image we are getting once again
from image Ops the one we have already used up here except for this one we need
either mirror or flip mirror is going to flip
the image in the horizontal axis which means we are only going to need a single
argument in here which is the image we already have so essentially what's going to happen at this point
we are taking our original image then we are rotating it then we are zooming it and if this condition is true then we
are flipping it on the horizontal axis this should already be working let's try once again I can open the image and now
if I click on X we have a flipped image this is working perfectly fine
which means next up I can duplicate this line get rid of the print statement the only
change I have to make is that this mirror should now be flip this is flipping the image on the
vertical axis let's try this one I can click on the author and why and
there we go now we have X and Y separately which means to combine the two I simply
have to run both of these methods I want to get this one and this one
I want to mirror and flip the image if both is selected which means we can try
this one more time now we get none then we have x y and both
and this is working perfectly fine with that we can work on the next bit
I'm going to put it right below let's work on the brightness as a matter of fact let's work on
brightness and Vibe rinse because the work in basically the same
way although for this one we're going to need another module of pillow which
means all the way at the top I want to import image and hence
the way this one is working is we first of all have to create what is called an enhancer for example if I want to create
a brightness enhancer I have to get image enhance
and then write this this one now wants to have the image
by itself this is not going to do anything that is going to be visible however what we can do now is get our
image and then use the brightness enhancer to enhance this one spelling
this correctly would also help inside of this method we can now add the argument
in my case I want self dot color vars the key is going to be brightness and
don't forget get with that this should be working let's
try I can click on the author this one is in colors and now brightness makes the image brighter or darker
and I can make this really bright or completely black now that we have covered this part we
can also create the Vibrance enhancer because it's going to work in the same way I want to have image enhance
this one is called color once again it is going to need
self.image with that I can get myself.image the
Vibrance enhancer and then enhance for this one we need self dot color vars
the key for this one is Vibrance and once again I want to get this value
this covers another important part let's try it hello Vibrance
and you can see this is working really well and I can also make this image black and
white via this Vibrance method also I can combine the two I can make the image more vibrant
also this is going to work with rotation and zoom and invert all of this is
coming together quite nicely next up we can work on the colors
this is going to include let me actually write it grayscale and invert of the
colors this returns to Simply getting self.image the value here we're getting
from image Ops the one we have already used a couple of times for example for the zoom
the method we need for this one is gray scale as the one argument it wants the image
although the issue for this one is that we are always applying the grayscale mode as a consequence we have to make sure to
wrap this thing inside of an if statement so that we only apply it if a certain
condition is true which in my case is if self dot color vars with the key gray
scale this is a Boolean VAR which means if I get the value this is either going to be
true or False only if it is true do I want to apply this effect
don't forget the colon also now I can duplicate these two lines
because invert is going to work in basically the same way I want to check the invert key
and inside of image Ops I want to use invert with self.image
this should be enough to activate the grayscale and the invert effect let's try this one open image the utter
color now we have black and white and we have invert also this is still working with the other sliders so everything is
going pretty well finally we have to apply the blur and the contrast
those are special effects which means we are going to need another part of pillow all the way at the top I want to import
image filter to apply this effect I want to get self.image and assign self dot image dot
filter the argument here needs to be image filter
and then dots the kind of effect that you want for example for the blur I want
to have a gaussian blur there are different kinds of blur that
you can apply gaussian blur is one of the really common ones this one is expecting a single argument which is
going to be self.effectivars the key blur
and from that I want to get the value it should be all we need let's try this
one I want to get my otter inside of effects we have blur
and this one is applying a tiny bit of a blur it might even be difficult to see
to make this effect a bit stronger let's go to menu or this one I want to look at
my effect frame right now blur is going from 0 to 3. let's go from 0 to 30.
and let's see how much that changes back to my other effects blur
now this is blurring significantly more this is covering the blur next up we can
work on the contrast for that I duplicated this line because I only really have to make some minor changes
instead of the gaussian blur I want to have what is called an unsharp mask
this is going to apply a contrast for that the value is not going to be blur
it is going to be contrast with this I can try the same thing again
effects now I have a contrast and this is applying a lot of contrast
nice there's only one more thing that we need and that is the effect of ours for that
I'm going to use a match case statement I want to match self dot effect virus
or this one the key is going to be effect this effect is going to work
somewhat like the flip in the sense that we have different options we want to look at to get all of them you have to
look at settings we have none emboss find edges contour and Edge enhance
we have to account for the letter 4 cases none we can simply ignore this one isn't supposed to do anything
which means inside of the match case statement I want to have one case for
example for emboss this would be the second entry inside of effect
options if that is the case I want to get self dot image and assign self dot image dot
filter or this one we once again need the image filter
dot all in uppercase letters m boss this one doesn't expect any arguments we
simply have to apply it like that let's try it actually if I now click on open image again
otter I can go to effects we have the drop down menu if I now click on emboss we are getting nothing and I think I
know why I keep on making the same mistake in the match case statement for match I'm only getting the T kinta
variable I am not getting the value inside of it now let's try it again open image
otter effects now Amber should be working and there we go a strange effect
but well it is what it is this is giving us the first case which
means I can simply duplicate this three times because besides emboss I want to
have find edges I have Contour and finally I have H and Hans
these are the options I've specified in the settings although I did realize there should be a lowercase edges to
apply these filters we have to update the image filter for example for find edges we want all
uppercase letters again find underscore edges for Contour we want Contour finally for
etch enhance we want to have h n and more
let's try all of that open image otter effects emboss is working find edges is
working on tour is working and etch enhance is also working although it
might be a bit hard to see if I compare etch enhance to none you can definitely tell the difference
with that we have applied all of the effects now there's one issue that I want to
address and that is performance let me run the entire thing again and apply a couple of effects so far I only really
ever applied one or two effects at a time however if I now apply rotation Zoom invert
some brightness Vibrance and if I come to blurb you can see that everything is
getting really really slow
this is happening because we always apply all of these effects
and Python and pillow simply aren't designed for that if we wanted to have something like Photoshop where these
effects are instantaneous then we would have to add a whole lot more logic there's a ton of optimization that you
could be doing with this but in my case I want to keep it simple I only want to
apply for example rotation if the rotation value is different from the
default value this one here figuring out how to do that is going to be your exercise
I want you guys to only apply the effect if the value is
different from the default most of you now and try to figure this
one out the way you want to think about it is I
only want to apply the rotation if self dot pause vars and rotate
is different from this rotate default
only if that is the case doesn't make any sense to apply the rotation which means only then do I want to apply this
method and create a new image if the value for this one is simply zero then we don't have to apply the effect
that is literally it although once again I did forget get
I keep on doing that sorry about it but well all we have to do now is to apply
this logic to all of the effects I only want to apply the zoom if the
zoom is different from zero I only want to apply flip if
self flip and get is different from I want to get the flip
options with the value 0. only if that is the
case then I want to do any of this next up for brightness and Vibrance I
want to get the value of brightness for example and only apply all of this if
the value is different from my settings the brightness default
this bracket shouldn't be there next up I only want to apply the Vibrance if
self colors vibrance.get is different from
Vibrance default next up we have the grayscale and we
have the invert although those are already perfectly fine because we are applying this effect only if this
variable or this variable return true those we can just leave as they are
although next up we have blur contrast and the effects those are particularly
difficult to process so they definitely need an if statement I want to check if self dot effect virus
dot get is different from the blur default
also besides that I want to get the value for contrast
this one if this effect is different from the
contrast default only then do I want to apply the effect
the match case statement we can leave as it is because if none of these cases are true then this isn't going to do
anything with that we should have significantly better performance
let me run the author I can now rotate it I can zoom it I can invert the thing
then for the color I can apply some colors and this does feel much snappier
probably very hard to see on video but definitely try yourself now that being
said if I apply all of the effects then this is still going to get slower simply
because we are doing a ton of different things anytime we are updating the image at this point we have a really processor
intensive app so you have to be aware of that although for our purposes this is
still fine which means I can minimize all of this and this covers a really
important aspect of the app at this point we have all of the effects let me apply a couple
there we go what I want to do now is to add a revert button that way I can revert all of this and start from
scratch this revert button is going to work for every single panel which means in color I can change the color and then
revert all of the colors once again since we have all of the data in place
this should be fairly straightforward back in the code I want to have a look at the menu
the menu itself is totally fine we don't have to add anything for this one however inside of the position frame the
color frame and the effect frame I want to add another panel at the bottom
this would be a revert button this one doesn't exist right now let's
create it inside of the panels I want to create a new class that I call
revert button this is just going to be a button so ctk and ctk button
after that we are going to need a thunder image method this one is going
to itself and apparent after that we're going to need one more
argument basically how I want to approach this when I am inside of the menu for example
in the position frame this revert button has to have access to all of these variables we need rotation
zoom and invert on top of that we have to get the value
for example rotation should be set back to zero the value we have specified inside of the settings
also this needs to be flexible so we can use it for the position frame the color frame and the effect frame
for example for the position frame we have three different values whereas for the color frame we have four the way I
approach this in terms of the arguments first of all I am always going to add self in here for the parent after that
I'm going to do roughly the same thing I have done for the switch panel which means we have a couple of two
bolts that always have a variable and then some other information for this
revert button I want to add a tuple with for example the position vars and rotate
after I have that I want to set the value I want it to set once we're clicking on this button which is going
to be rotate default also all of this is going to be over
multiple lines because we have a couple of values in here besides the POS vars I also want to get
the zoom which has a zoomed default
finally I want to have the lip the default value for this one
is going to be flip options with the value 0. these are the
values I want to set also let me clean this up a tiny bit that looks a bit better I suppose if I organize it like this
this is the most readable these things are a bit subjective but now I have to create some kind of
logic to capture all of these arguments this is going to happen inside of panels This one is going to need an Asterix and
then arcs you could name it whatever you want but arcs is what people usually call it
once we have that first of all I have to create super thunder in it
set the master to the parent also we're going to need some kind of
text let's call it revert also we have to pack this revert button
since all of these panels are simply using pack this one for example we can
use pack for this one as well with the one difference that I want to set the side to bottom to give it a tiny bit of
padding I want to have pad Y and set this to 10. this should actually already
work let's try I can open main.pi again and now at the bottom we
have revert it doesn't do anything right now but at the very least we have something
what we now have to figure out is how to get the variables via this arcs and then update the value
to demonstrate what we have inside of arcs let me just print it if I now run main.pi again open image otter
here you can see we have a tick and tavar somewhere in our memory and then
we have the value for example this first entry is the rotation variable and rotate
default is to zero this is going to bring us to the exercise
when clicking on the button get the variables and set the value to
the default pause the video now and try to figure this one out
first of all we have to make sure that we can run some kind of function when we
are clicking on this button or when the user is clicking on the button for that I want to have command
I will call the method I want to call revert to create this one I need to Define
revert without any custom parameters next up we have to make sure that we
have access to the arcs inside of the revert method which we don't have right
now to account for that I want to create an attribute let's simply call it the arcs this is
going to be arcs with that I can use them inside of a for loop I want for VAR
and value in self dot arcs what this is going to give me let me print it I want
to print the VAR and I want to get the value let's try it again open image otter by
default we can't see anything but if I click on the button we are getting
the variable and the value that is looking really good which means
now back in the revert button I can simply use the VAR and then set the
value we are targeting the VAR then we are using set and then we assign the value
to the VAR that's literally it I can get rid of the exercise text back
in main.pi run on of this again change a couple of values
and now if I click on revert we are back to normal although there's one more change that we
do have to make you might have seen it already these numbers here don't work out anymore let's have a look what's
going wrong back in the panels the revert button is working just fine so I can minimize it
but if I open the slider panel the issue for this one is that we are
only updating the text the text to display what number we have when we are moving the slider from this command
if we're updating the value in any other way this method is not going to be run
as a consequence the number doesn't update to a code for that we have to make a couple of changes
first of all I want to store the data VAR inside of an attribute which means
self.datavar is going to be datavar once I have that I want to use tracing data
VAR dot Trace I want to check when the value is changing then I want to call
Self dot update text because of that we have to update this
update text I don't want to have value anymore instead I want to have arcs because once again when we are calling a
method using the trace method then Trace is going to automatically add a couple of arcs although we're not going to use
them but you do have to add a parameter because of this logic we don't need this
command anymore or this simple reason that the variable
is still attached to the ctk slider which means when we are using the slider this data VAR is going to be updated
although to be a bit more consistent here with the naming let me call it self.datavar which means what is going to happen when
the user is using the slider the slider updates the variable because of this
update this Trace method is going to be triggered which triggers this method
which is then going to update the label on top of that what is much more
important when I'm now clicking on revert button and we are updating the
value inside of this for Loop this update text is also going to run it
is going to run every time we are updating the variable although before we can run it I have to
make one more change this bit here is not going to work anymore because we
don't have value instead I want to get self.datavar dot get
now all of this should be working let's try I want to open the image get the otter
apply rotation all of that is still working just fine and now if I click on revert we are all back to 0 and 0.
with that we have the proper Logic the last one we have to do is to use this revert button for the other frames as
well for example the color frame needs a revert button let me copy in the values
actually otherwise you have to watch me type for ages I want to have these for two bolts color bars and brightness with
brightness default then we have grayscale invert Vibrance all with the
default value finally for the effect frame I want to have the revert button again with self
after that the two builds I want to pass in this one are these ones
let me format them a tiny bit better there we go we have effect verse blur
blur default effect was contrast contrast default and effect was effect effect options 0.
this should be all we need now we can try the app open the auto once again
rotation and zoom and invert should still work just fine this is looking
good next up color I want to have black and white more brightness and more Vibrance
now I can click on revert and well back to normal finally I want to apply some blur and
some contrast and find edges now you can't see anything anymore so I
want to revert all of this and we are back to the others perfect
with that we have the app itself the last thing we have to figure out is how to export the image and then we have
finished the entire thing we are nearly done with the app at this point let me apply some changes I want
to have a rotation and brightness Vibrance doesn't really matter what it is what I now want to do is to work on
the export or this one we have two panels I can type a name let's call it weird
otters I can also select jpeg or PNG depending on what I select I am getting
a preview of the file name importantly for this one the user can type is space
in the input field but when we are outputting it we're getting an underscore this isn't actually necessary for
Windows but I think it's a nice thing to add here other than that I can click on Explorer select a folder
and then I get a preview of the folder this can also be changed for example if I didn't want a desktop or
anything in here I could simply type whatever I want although this is not what I want I want to work on the
desktop once we have all of that we can work on the export although for now let's simply
work on the panels and let's see how far we get back in the code I want to work inside of the menu for this one we
already have a position frame a color frame and an effect frame I want to add one more which is going to be the export
frame this just as before is going to be a ctk frame
as a matter of fact I can literally just copy most of the stuff from the effect
frame because they're all quite similar with this we have an export frame we do
have to make sure that we are attaching it to the menu though also we have to create it which means export frame self
dot Tab and export although this one is not going to get a
tkinter variable which means the effect vars we can
simply remove at least for now with that we have to populate this
export frame with a couple of panels this is going to happen inside of the panels I want to minimize everything in
here first of all let me put it below this switch panel I want to create a class
that I called file name panel this is going to be just another
panel in here I'm going to need a thunder init method this one will need itself it will
need a parent and then we need two more things I call them a name String and if file string
the name String is going to account for the name the file string will be the file ending this could either be jpeg or
PNG I will create those in just a second although first of all I want to run
super Thunder init and set the parent to the parent
now we have to figure out how to get the name String and the file string so far we created all of the variables in the
app specifically inside of the init parameters
all of these are important but for this particular case we don't need to go that
far we can create these variables in the export frame for this one I want to have
self.name string this one is going to be a ctk
string VAR without a default value besides that I
want to have a self.file string which is also going to be a ctk string VAR
although this one is going to get default value of jpeg
also I should add comments here to organize all of this a bit better let's call this section the data because next
up I also want to create widgets the first widget we already have is the
file name panel let me paste it in we need self we need self
dot name String and self dot file string
with that we have the T kind of variables for this one although those I want to turn into
attributes which means self Dot file string is going to be the file
string self dot name String is going to be the name String
although name String should come first that just feels better you don't have to do it once we have the data I want to
create the widgets we are going to need is ctk entry
which is going to need self then we need a text
variable which is going to be self dot name String after way of that I want to
pack the entire thing I want to fill X I want to have pad X of 20 and Pad y of
5. and let's actually run the entire thing to see if all of this is working and now
click on open image otter export and there we have one panel with an entry field we can also type in here although
it doesn't do anything at this point next up I want to create two check boxes
to draw all of this this is going to be the panel on the top
right now we have an entry field the entry field we created here besides that
I want to have a frame below which is going to contain two check boxes for
that we have to create a frame we're just going to contain the two
checkboxes I want to start by creating the frame which is going to be a ctk frame
self is going to be the parent also I'm going to set the FG color to trends
air rent next up I want to create a ctk and ctk check box the frame will be the
parent the text for this one is going to be jpeg I guess I want to assign this to a
variable let's call it the jpeg check next up I want to get my jpeg check and
pack the entire thing site needs to be left because I want to create a second one and they're supposed
to be next to each other I want to set fill to X finally expand should be true
with that we have one check button I want to duplicate all of this because besides jpeg check I also want to add
PNG check the text for this one is going to be PNG although other than that the pack method
is going to work in exactly the same way finally I want to pack this Frame by
setting expand to True fill to X and Pad
X to 20. with that we should have the two switches let's try this one
otter export and there we go right now we can activate both we are
going to work on that in just a second before that I want to add one more thing
let me reopen the drawing one thing I forgot all the way at the bottom of the widget is some kind of preview
so when we are typing into the field and select one of the boxes the text field is going to give us a preview of what
the final text is going to be like this text I want to store in an attribute let's call it output it is
going to be a ctk label self will be the parent and text is
going to be nothing this output text I want to pack right away without any arguments for the pack
now with that I can run all of this and we're not going to see it but there's a
tiny bit more space at the bottom of this panel which means at the very least we know that this output exists but well we're
going to work with it also as always I want to add a few comments here to organize all of this
better let's call this one the check boxes or file format
finally I want to have the preview text what I now want to work on is to connect
this name String to the output which basically means that in the name
String we could have a value like I think I call it weird otter earlier this
inside of the output should become weird
water later on when we account for the logic for these switches here this is going to
become dot PNG or JPEG but this I'm going to not work on for now to get that
I want to get myself dot name string and use Trace once again
I want to check if this value changes if that is the case I want to run
self.update text which means once again I need a method called update text with
self and the arcs in this method I want to check if
self.namestring dot get actually exists if it doesn't there's no point doing any
of this if that is the case I first of all want to get my text which is going to be self
Dodge name String dot get although right now this might have some
white space for example we could have weird water and I want to get rid of
this bit here almost specifically I want to replace it with an underscore
to get that I want to add one more method which is called replace
this replays wants two arguments the first is the character we want to replace which in my case is an empty
character the second argument is the character we want to replace the value with which in my case is an underscore
once we have that I simply have to get my output the text we have created up here and then configure it
and set the text to the text we just created with that I can run main.pi click on
open image the utter export now I can type in here
we are getting some text on top of that if I now type weird Auto we're getting
an underscore between the two words that is a really good start we have
covered the first bit next up we have to work on the check boxes right now we can check both of
them which is not what I want to account for that let me actually put them right next to
each other we have jpeg check the widget and then PNG check also a widget and
below that we are packing them this way it's easier to compare the two
this is important because both are going to get the same variable which is going to be self dot file string
this right now would get us some weird results you make all of this work properly we
are going to need an on value and an off value basically for the jpeg Widget the on
value is going to be jpeg while the off value is going to be PNG
whereas for the PNG check the on value is going to be PNG
while the off value will be JPEG that way self.file string can
either be jpeg or PNG and it will activate or deactivate one of these
buttons although on top of that we are going to need one more thing and that is a
command the command I want to create is going to be a click although this
click is going to itself and a value the value we are going to get when we
are calling the command because of that we will need a Lambda function I want to use Lambda self dot click
because of that logic I can now pass in an argument for the jpeg widget button I want to
have jpeg as the argument for the PNG widget I want to have PNG
and this is a really long line I hope you could follow along but now we
are going to call the method click either with jpeg or with PNG all I need
for this one is self dot then the file string and set this to the value we have
specified the value we are getting from click it could either be jpeg or PNG
after way of that I want to call self.update text again without any
arguments that way we are going to update all of this although before that let's actually
try all of this open image otter export and now JPEG and PNG
will only ever active if the other is inactive the reason why that is working is
because they have these on and off values which means when we are setting file
string to jpeg then jpeg is activated for this one and off for the other
switch and then the other way around for PNG finally the last thing that we have to work on is update text should also give
us the file ending we already have the text I want to add a tiny bit at the end
I want to get self dot file string dot get and that is literally it although I
forgot one thing there needs to be a DOT between the two which means I simply want to add a string dot
between the two with that we should be good to go if I now run main.pi one more time
otter export by default nothing is going to be visible however once I type some
text we get JPEG and we get PNG also if I add a space multiple times
this is working just fine cool with that we have the first panel
this was the more complicated one I can minimize it now next up we are
going to need a class file path panel once again this is going to be a panel
we are going to need it under init method with self we need a parent and
then we need a path string this path string I want to create inside
of the export frame once we have that inside of the file path panel I want to
open a file dialog and then select a folder all of this is going to be your exercise
what I want you guys to do is this bit here number one I want you guys to
create a path string variable in the export frame and pass it to this widget we already have the parameter so this
you should be using next up add a button and an entry field to this widget
finally when you click on the button you should get a file dialog that will return the path as a string I have
already done this earlier so check this bit out finally the entry field should display the return path
I suppose I should show you the final thing is going to look like
this pause the video now and try to figure this one out
let's work on it together first of all number one we have to create a path string variable this
happens inside of menu I want self.path string this is going to be ctk stringvar
without any default value once we have that I want to create a
file path panel this needs self for the parent and then self.path string
with that we can work inside of the class the entire first bit is covered
although I should also add this super thunder in it method with the parent as
the parent so that we have some functionality besides that I also want to turn the
path string into an attribute meaning path string is going to be the path string
next up and let me reorganize all of this a tiny bit I want to add a button and an entry
field which means I want to have a ctk button with self as the parent the text I
called open explorer that is all we need for now and I want to pack this thing with a pad y
of 5. besides that I want to have a ctk entry
widget with self this I want to pack right away as well I want to set expand
to True fill to both finally pad X should be 5 and pet y
should also be 5. this covers the second bit what I did forget was the colon after
the download method and I think at this point it's a good idea to check if all of this is even working
since we can see some widgets there is at the very least something inside of export we now have open Explorer and an
entry field although neither is doing anything right now for that we have to work on the third
part all of this is going to happen inside of a method I want to open file dialog
this one itself and no other argument what this one is going to do is going to
be quite similar compared to the image import for this one we're getting a file
dialog and ask open file although for this one we have to import from decanter file dialog this I want to
copy and paste at the top below my custom tkinder import
now we can use it I want to get my file dialog dot ask this one is called
directory and at this point I realized I didn't teach you this bit you only knew about
where is it ask open file the difference between these two is that ask open file is asking for a specific
file whereas us directory is only looking for a folder sorry about that I
should have mentioned it but other than that this one is working in the same way this open file dialog I want to call
whenever we are pressing the button which means the button is going to get a command self dot open file dialog
let's try that one I can click on open image otter export and open Explorer and there
we go we are opening a file dialog what is really important about this one is that now we are clicking on select
folder we are not selecting a specific image anymore you can tell because in the desktop we
cannot see the images we created earlier there's no Auto or weird Auto in here because right now we are only looking at
folders not files which is perfect for my purposes
the last thing I have to do is to capture the string or the path that is being returned by this ask directory
all I have to do for that is self.path string dot set and then whatever we get
returned from us directory to connect this to the entry widget I
want to set a text variable and this should be self dot path string
this is going to cover the third bit of the exercise let's try out of that I want to open the
image Auto export open Explorer I want to select my desktop and there we go I
have the path to my desktop on top of that I can type a name in here
weird otter with the file ending and with that I have a file name and a path
so for the next video we can export this image I'll see you there Friday this is going
to be the last video for this project let me apply a couple of changes I want to have rotation Zoom invert and let's
add a bit of Vibrance and blur now I have a changed image this I want
to export for that we already have the name panel or the name I want to go with
last otter I want to export a JPEG file then I want to open the Explorer save all of
this on the desktop and what I want to do for this video is implement the save button which means if I click on Save we
have the file exported which means if I open the folder for the desktop now we have the last order this
is then finishing up the project I guess you could Implement some kind of message that the image was saved but you
can work on this yourself it's not that important for this project back in the code I want to work inside
of my app class because this one contains the image itself
to export it I want to create another method I call this one export image
this one is going to need three arguments besides self obviously we need a name we need a file and we need a path
all three of those we are getting from the menu because in the export frame we
have a name String a file string and a path string those we want to use to export the image
the way I want to use them is I want to create an export string this is just
going to be an F string where I am connecting the path
then a slash then I am adding the file name
after that I have a DOT and then we have the file ending
I suppose the best way to demonstrate what this one is doing is to actually call Export image
this we can do by going into import image the method
because this one creates the menu all the way at the bottom this is going to get another argument which will be self
dot export image with that inside of the menu
we can add another parameter which is going to be export image this export
image I want to pass right through to the export frame I just have to copy it in now we are
good to go for the menu with that in the export frame we can have the export
image as another parameter although the issue right now is that we don't have a button that can execute
this method this I want to create inside of panels let's do it below the revert button
let me add a tiny bit of white space I want to create a class that I'm calling
save button this is going to be a ctk button meaning ctk and button we are as always starting
with a Dunder init method itself and we need a parent after that we also want to capture the
export image method finally to make the export image work we
have to get the three string vars name String file string and
path string which means for the parameters I want to have a name String a file string and a
path string once we have that I can get this super
thunder in it method pass in the master which is going to be the parent
next up we have to specify some kind of text I simply called this one save
for the last thing we are going to need a command I call this one self dot safe
this method we can create right away Define save with self and nothing else
this method is supposed to execute export image although for that it needs
to have access to it via the attributes to achieve that I want to create an
export image attribute which is going to get the export image method
that allows me to self.export image and call this thing although now we are
going to need three arguments inside of main.pi we can see the actual method we need the
parameter for a name for a file and for the path I approach this by creating three more
attribute self.name string is going to be name String and self dot file string is going
to be the file string finally self.path string is going to be the path string
that's why I have access to everything I need all I have to do now is get self.name string also do not forget the
get then we need self.file string dot get
and for last one self.path string dot get this is going to give us the button with
that back inside of many.pi we can at the bottom of the widgets create the
save button this one itself for the parent then we
are going to need the export image which we have it is the export image we're
getting this from the parameters after that we need self. name String
then self dot file string and self dot path string although while
I am looking at it there's one important thing missing we're not placing this button this we can change quite easily
all we need is self dot pack decide importantly here needs to be
bottom besides that I want to have pad y being 10.
but with that we have the panels and inside of export frame we also have the
save button if I run main.pi I can open an image click on the author then inside
of export I can type some text choose whatever file ending I want open the
Explorer get the file and now on the bottom we have a save button if I click
on it nothing is happening and I can also tell you why it is
because I am not printing the export string let's start off this again by actually printing the export string so
we can see something sorry about that export some gibberish
open Explorer select folder now save and there we go the path you can see
printed right now is a combination of the path the name and the file path is
the first bit all of this bit here next up we have the slash this we are adding
or this one then we have the name this one's quite straightforward finally we
are adding a DOT and the file itself the dot is this one the file is this one
this is all we are going to need to export the image the last command that we are going to
need for this one is going to be self dot image dot save this one simply wants
to have an export string the one we just created
since we also have the file ending it is either going to export a PNG or JPEG file depending on what the user
specified and well this is all we need if I run this app again click on the author I can
make a few more changes let's say for this one I want to have some really vibrant authors that are inverted
I want to export let's call them the Disco otters on the desktop also this should be a PNG
file if I now click on Save nothing happened at least on the surface
however if I open the desktop we have some discorders also this is a PNG file
and it looks like we applied all of the effects which means this is working just fine I
guess you can work a bit more on all of the logic here to maybe clear the fields but I think for all practical purposes
we have finished this app