# First thoughts (Tuesday, 22 December 2020, 11:12AM)

It's been a fast-paced project. I started it officially yesterday morning and since then I've accumulated 11 nothings. That's a whole lot of nothing.

Currently the big one I'm missing in the Unreal Engine, which I can't install on my laptop as it takes up too much space. I *can* release this suite without it, but it does feel a bit fundamental, so I'm pondering ways to deal with that. Seems like Unreal does have a web export ([community supported](https://github.com/UnrealEngineHTML5/Documentation)), so that would mean I could potentially create this version on the gaming laptop rather than install Unreal on this MacBook Pro.

It has felt nice to be so "productive" in terms of churning out different engines' ideas of nothing. They do tend to differ in significant ways, which I'm glad of - it's not just a series of blank screens that don't tell you much. There is, unsurprisingly *something there*. Duh duh duh! Big reveal music effect here.

I feel like this project could be subject to a bunch of different forms of analysis, including some kind of code forensics, as well as the basic aesthetics of the nothing, as well as some of the signification of producing nothing, as well as the processual aspects of producing nothing. I can probably do some basic versions of all of these things here. It's going to make the most sense to write an engine-by-engine review of the nothing experience I assume.

That's a bit of a larger bite than I want to take out of it this morning, but I'll perhaps write a bit about it later today or tomorrow while it remains at least somewhat fresh.

---

# Twine and Inky (Wednesday, 23 December 2020, 10:32AM)

Alright well, as promised I thought I'd write some notes about the specific instances of Nothing I've created so far. I also realized a number of Nothings not yet made like Godot and Adventure Game Studio, so I'll get onto those where possible. Anyway, on with specific notes, roughly in order of creation? Or no just in some order.

## [Twine](https://twinery.org/), originally created by [Chris Kilmas](https://chrisklimas.com/)

Should I be listing specific version numbers of software? No I don't think that's all that important, this isn't an archival effort, though it has a kind of archiving flavour.

Twine involved firing up the software and then exporting it to HTML. The project gets titled Nothing, which displays as the page title in the browser. The default Twine starting point has a single text node with default text in it "Double-click this passage to edit it.". It displays in the default CSS, it has no links and is not interactive.

I quite like that there is content here and that the content explicitly references the process of making a Twine game, even if it's an instruction the player cannot follow. It really marks the distinction between creation and play in a neat and tidy way, the ability to change the game versus the ability to play the game.

As with many of the Nothings, I like that it's *not* nothing too, of course, and that's a recurring theme. It's not a blank page. As with any Twine, under the hood is the actually Twine JavaScript as well, so it's a 295KB file despite being just some text on the screen. I don't know enough about Twine to know whether the JS is reading data in from the page and then rendering it to the screen or not. When I inspect the page I see the same tags etc. so I think this particular passage, being the starting passage, is pre-rendered into the HTML, which makes the JS actually completely non-functional (except that it may well still be doing some stuff on startup anyway?). Looking through the minified code doesn't tell me a lot - I can't find a `window.onload` anywhere to most obviously suggest there's code running from the very beginning, ... oh wait, there it is. There's an `addEventListener` for "DOMContentLoaded", so it's likely there's JavaScript running on the page, even if it's not "needed". Such is life for game engines. They can't know in advance what content you're providing for them to interpret, so they have to try to interpret what's there, even if it turns out not to need interpreting.

So, quite a lot of nothing going on with this one. I think the reveal of the inner part of the application through its default "Double-click here" message is really nice for this one. The creation application shows up explicitly (through language) in the played artifact.

## [Inky](https://www.inklestudios.com/ink/), by [inkle studios](https://www.inklestudios.com/)

Inky isn't a tool I've ever used to actually make something, though I've played a few Inky games I believe. The nothing in this case is just the word "nothing" in a pleasing font, representing the title of the "story". Actually, this is true of Twine too to some extent, but there's something worth noticing about the fact that in the context of this tool what we're seeing is a *story* of Nothing rather than a game per se?

An immediately noticeable extra part here is that there's a link at the top of the page "WRITTEN IN INK" that links to the "ink" page on the inklestudios website. So this is another way of referring to the tool of production, but more explicit, more like advertising. I quite like the accessibility implications of this, even if it's perhaps not so artistically satisfying as a hermetically sealed story in a webpage. Someone looking at this story (or a less nothing one) gets to find the tool itself if they're interested in crossing over.

The source code for the Inky version shows very simple HTML as well as linking to three separate JS files. There's `ink.js` which is presumably the ink engine itself, obfuscated via minification. Can't make much of it at all. There's also `Nothing.js` which is interesting given that the story has no content at all. It contains the following:

```javascript
var storyContent = ﻿{"inkVersion":19,"root":[[["done",{"#f":5,"#n":"g-0"}],null],"done",{"#f":1}],"listDefs":{}};
```

Most of that is mystifying (especially the `#f`s), but you can see it's roughly speaking just the base level data structure for the story and contains almost nothing. Not nothing though.

`main.js`, the last source file, is not minified and is not super long and is even commented! Can see that a `continueStory()` function is being called to kick off the story, which presumably stalls out when it finds out there's no data. It's interesting how little code there seems to be here in the main script to drive the engine forwards - feels like a neat package, all the action is in `ink.js` I guess.

Also of note with Inkle, the software I used to make this, is that I couldn't export the "nothing" it starts out with. The program loads with a blank page, but I couldn't export it to HTML until I typed a character, saved it, deleted it, and saved it again. So there was this sense I had to really consciously signal I wanted the nothing that was already there. Raises the question of whether it's still "nothing" if I had to exert this particular effort to get it to a releasable state, even if that state is (roughly speaking) the same as the starting state? Is there a ghost of that character (I think it was an "e") that I typed hovering over this project?

---

# Bitsy, flickgame (Wednesday, 30 December 2020, 12:36PM)

## [Bitsy](http://www.bitsy.org/), by [Adam Le Doux](https://ledoux.itch.io/)

I'm a major Bitsy fan of course and used it to make [b r 1](http://www.pippinbarr.com/games/2018/05/23/b-r-1.html), [Let's Play: Ancient Greek Punishment: Bitsy Demake](http://www.pippinbarr.com/games/2019/07/17/lets-play-ancient-greek-punishment-bitsy-demake.html) and [b r 3](https://pippinbarr.github.io/b-r-3/info/).

As a nothing it's one of the more something ones. The default setup (care of Adam Le Doux) involves a simple avatar, a room with walls, and a cat that says "I'm a cat" when you walk into it. This speaks to the accessibility of the engine and its general attitude of friendliness (a cat!). This way it provides examples of a large amount of functionality in a really simple way. It also includes a cup of tea, though for some reason that's not positioned in the scene by default so you don't see it in the nothing, though I presume it's in the underlying code? Just checked and yes. In fact there's a "key" in the underlying code as well. At any rate, the way this "nothing" is designed is to bring people into the experience super fast - you could just redraw a couple of things and begin to have your own understanding of the tool but also your own aesthetic stamp on it. So the tool doesn't emphasize its (quite significant) possibility space (as other engines like Unity do by kind of giving you just nothing, a void with a horizon) in favour of being accessible and non-threatening.

Like pretty much every engine, there's a ton of code underneath the "nothing" that represents the engine itself which *could* do a bunch of stuff if there were more data to crunch. As it stands there's data too, but it's the default data for the wall, cat, avatar, key, and room. In the end this nothing is 196KB, which ain't nothing.

## [flickgame](https://www.flickgame.org/), by [Stephen Lavelle](https://www.increpare.com)

This is [Stephen Lavelle](https://www.increpare.com/)'s ultra-accessible game engine in which all interaction is based on hyperlinks which are based on colours. So you have clickable bitmaps where specific colours lead to new scenes/pages. And that's it! It's beautifully simple conceptually.

The nothing is just the default scene, which is quite delightfully a dark aubergine kind of colour. I like that it isn't black or white or something other more "neutral" colour, it indicated a personality despite its extreme blankness. You can't click the colour to go anywhere because there's no link programmed in.

In a testament to the simplicity of the engine, the HTML file is a mere 17KB, almost certainly the smallest of the nothings (well except for the blank PDF print-and-play). In the HTML there's some initial CSS, and then a dataset which I suppose I'd assume is a listing of the colour of every pixel in the one scene that there is? There are a lot of 0s, which you would think would mean black, but maybe it means "blank" in this context? In the end I can't really tell without seriously getting into it, which I don't think I'm up for right now. I could also ask Stephen, but I think it's okay if this remains a mystery at the moment.

It still takes a pretty decent amount of JavaScript to make this whole thing work, and it's not obfuscated which is quite nice - you can genuinely read and understand it, though it's uncommented (for size reasons I'd assume). It's also written entirely in plain JavaScript with the DOM rather than using an extra library like jQuery or similar.

---

# PuzzleScript  (Thursday, 31 December 2020, 12:30PM)

## [PuzzleScript](https://www.puzzlescript.net/), by [Stephen Lavelle](https://www.increpare.com)

Somewhat like Bitsy, PuzzleScript provides a fairly detailed template as it's starting point, with a little Sokoban level to solve if you run it. To this point it's the only "nothing" that represents whatyou might think of as a playable game, even having a menu and a win condition. It's not the world's most complex game (push the right arrow three times to win), but it's a proper game with underlying mechanics and so on.

For that reason it's pretty interesting that the actual PuzzleScript source for the game is really, really simple. Presumably this is the point, to demonstrate the ability to make quite sophisticated gameplay with minimal effort (or at least non-length effort). The PuzzleScript source is 69 lines long, commented, and quite intelligible. This is interesting at least in part because it demonstrates a really concerted separation of gameplay and level design I suppose? With the ruleset provided (moving crates onto targets) we know that you can make the entirety of Sokoban, with arbitrarily complex levels, some of which could be insanely hard to solve etc, when in the underlying source they're effectively just diagrams of levels, with the complexity baked into their arrangement of elements.

PuzzleScript being implemented in the browser, it's actually a higher order language on top of JavaScript, so in this particular nothing you of course end up not just with the PuzzleScript source but the source of the PuzzleScript engine on top. In this case the engine is obfuscated through minification to reduce the file size, and it still only comes in at 296KB which is kind of impressive for an entire engine! (Godot is in the background downloading some 400MB template file just to be able to export anything right now, that's over 1300 PuzzleScript engines). It's not actually as easy as I'd expected to find the source of PuzzleScript (it's not obviously linked from the running engine itself), but it's easy enough to google up: https://github.com/increpare/PuzzleScript. I'm not going to go through the source code itself, but it's interesting somehow that this repository is representative of the "nothing" I have in this suite, just in an expanded and (much) more legible form.

So the aesthetics of this nothing are very detailed, very not-nothing, and very educational in terms of the engine. They show you the most obvious kind of thing to make with it (Sokobans) and they provide a tiny use case along with its source to help you understand basic possibilities.
