# *The Nothings Suite*

*Nothing to see here! But don't move along! You can really see the nothing here! Examine the nothing! Think about the nothing! The nothing is where it all begins!*

[![Splash](info/images/splash.png)](https://pippinbarr.github.io/the-nothings-suite/)

---

_The Nothings Suite_ is a collection of (extremely) short videogames made with diverse videogame engines such as Unity, Twine, and PICO-8. In each case, a game has been produced with the engine using, as much as possible, no creative input at all. That is, in the ideal scenario I open the game engine, save the project it creates by default as "Nothing" and export it for play. This means you get to see each game engine's idea of what "nothing" (or at least no effort) looks like when you set out to make a game with it.

*The Nothings Suite* currently consists of the following 14 nothings:
* [Nothing (Twine)](#nothing-twine)
* [Nothing (Inky)](#nothing-inky)
* [Nothing (Bitsy)](#nothing-bitsy)
* [Nothing (Flickgame)](#nothing-flickgame)
* [Nothing (PuzzleScript)](#nothing-puzzlescript)
* [Nothing (PICO-8)](#nothing-pico-8)
* [Nothing (Inform 7)](#nothing-inform-7)
* [Nothing (Construct 3)](#nothing-construct-3)
* [Nothing (Stencyl)](#nothing-stencyl)
* [Nothing (Unity)](#nothing-unity)
* [Nothing (Godot)](#nothing-godot)
* [Nothing (Unreal Engine 4)](#nothing-unreal-engine-4-with-andrew-baker)
* [Nothing (Ren'Py)](#nothing-renpy)
* [Nothing (Print-and-Play)](#nothing-print-and-play)

You can also read about the suite's [development and thought process](#would-you-like-to-know-more).

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/twine/) (Twine)

[Twine](http://twinery.org/) is a flexible hypertext creation tool. The minimal Twine game is a single webpage with default styling containing the instruction: *"Double-click this passage to edit it."* This is the only engine profiled here that references its own user interface by default, pointing the nothing-player to the underlying idea of *making* a Twine game.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/twine/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/inky/) (Inky)

[Inky](https://github.com/inkle/inky/releases/tag/0.12.0) is the editor for the [Ink](https://www.inklestudios.com/ink/) scripting language, used to write interactive fiction. This Nothing is interesting for the way it promotes its own tool, proclaiming *"WRITTEN IN INK"* at the top of its webpage. To actually export this this empty Ink story, I had to first write a character, save the file, then delete it and save again. Is it really nothing, or does the ghost of that character remain?

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/inky/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/bitsy/) (Bitsy)

[Bitsy Game Maker](https://ledoux.itch.io/bitsy) (by Adam LeDoux) is an accessible tool for creating "little games or worlds", generally in low resolution 2D visuals. The "nothing" produced here is extensive, containing a title screen, an avatar the player can navigate around a room, and a cat for them to talk to (*"I'm a cat"*). This impressively "playable" nothing is telling the accessibility of the tool: these elements are in place by default so that a user new to the Bitsy Game Maker is able to quickly edit the visuals and texts already in place to begin their own project.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/bitsy/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/flickgame/) (Flickgame)

[Flickgame](https://www.flickgame.org/) by [Increpare](https://www.increpare.com/index.html) is an ultra-accessible tool for creating a game made up of hyperlinked hand-drawn images, where links between pages are based on colors. This "nothing" is an empty aubergine purple rectangle that links to nothing, the absence of a drawing and the absence of links. The exported HTML file is only 17KB, the smallest (potentially) interactive nothing in this collection. The source code is also quite readable in the HTML, emphasizing Increpare's commitment to open source with this tool ([repository here](https://github.com/increpare/flickgame)).

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/flickgame/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/puzzlescript/nothing.html) (PuzzleScript)

[PuzzleScript](https://www.puzzlescript.net/) is an open source puzzle game engine by [Increpare](https://www.increpare.com/index.html). This "nothing" is the only "playable game" in this overall suite in the traditional sense: a simple [Sokoban](https://en.wikipedia.org/wiki/Sokoban) level the player can interact with and complete (walkthrough: press the right arrow three times!). This is another nod to accessibility, in this case helping to explain to the user of PuzzleScript through example how its underlying scripting language works at its most fundamental. This is multi-layered nothing - with no additional level data, nor PuzzleScript, nor underlying JavaScript - pointing to the complexity of even "simple" tools.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/puzzlescript/nothing.html)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/pico8/) (PICO-8)

[PICO-8](https://www.lexaloffle.com/pico-8.php) is a "fantasy console" with an associated development environment for making limited but potential-filled small games. Producing this "nothing" was challenging because PICO-8 is less immediately "friendly" than other game engines, in keeping with its demand that you commit to its technical fantasy world. The nothingness here is due to an empty source code file (`.p8` extension) being used to "create" the resulting game. The game freezes at *"BOOTING CARTRIDGE..."*, but displays no errors either in the fantasy console or the JavaScript console. There's just nothing there for PICO-8 to do.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/pico8/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/inform7/Nothing.gblorb) (Inform 7)

[Inform 7](http://inform7.com/) is a "Design System for Interactive Fiction", prominently featuring a natural-language programming environment. The source code for this "nothing" is first the line `"Nothing" by Pippin Barr` and then the line `Example Location is a room.`, the default generated on creating a new project. Despite the almost total lack of content, the resulting game is expansive thanks to the nature of the Inform 7 engine. In particular, you can perform many actions in its world - such as jumping, talking, and looking at yourself (*"as good-looking as ever"*) - because the engine itself has so many default responses in place. Of course, this world is also incredible claustrophobic - the abyss of its nothingness shows.

**Note:** Because the only way to make an Inform 7 game playable in the browser is to add text to its existing code, I was unable to make it accessible in that way. Instead, you'll have to download the `.gblorb` file and play it with an *interpreter*. Consider [Spatterlight](http://ccxvii.net/spatterlight/) (Mac), [Filfre](http://maher.filfre.net/filfre/index.html) (Windows), or [Gargoyle](http://ccxvii.net/gargoyle/) (Linux).

[Download this nothing](https://pippinbarr.github.io/the-nothings-suite/inform7/Nothing.gblorb)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/construct3/) (Construct 3)

[Construct 3](https://www.construct.net/en) is a game creation tool focused on visual scripting and accessibility to non-programmers. This was one of the least eventful nothings to create, and yields a fairly standard player experience: a loading screen (*"Powered by Construct 3"*) followed by a blank white canvas that is totally non-interactive. This feels like it mirrors the rather banal nature of Construct 3 and other more generic forms of game engine that attempt, at some level, to be all things to all people. The only element of note that surprised me that in a default export of a Construct 3 game it includes an "offline mode" to make the game playable without an internet connection - a nice feature, but one which took over my machine's local server setup and made it impossible to develop my own work. A deeply invasive nothing.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/construct3/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/stencyl/) (Stencyl)

[Stencyl](http://www.stencyl.com/) is a similar tool to Construct 3. It, too, has a visual scripting environment and the ability to export to many platforms. The nothing was similarly easy to create, though the resulting experience is distinct in that it doesn't advertise Stencyl itself by default. The default template used is called "Blank Game" and it sure is blank - I quite like that it fades from black (loading screen) to white, effectively erasing itself from view as it presents its nothingness to the player.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/stencyl/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/unity/) (Unity)

[Unity](https://unity.com/) is one of the major "make absolutely anything" game engines along with Unreal Engine and Godot, with a particular focus on 3D game creation. I've made a number of games in Unity previously, so the process was smooth to create an empty project and then export it to WEBGL for viewing on a webpage. The player experience of the nothing is a standard Unity loading screen followed by an empty horizon above a brown/gray nothingness. By implication there's also a camera (that you're seeing through) and a light (that is illuminating the scene). To me, this is the iconic nothing.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/unity/) (currently broken in some versions of Chrome)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/godot/Nothing.html) (Godot)

The [Godot Engine](https://godotengine.org/) is a free and open source game engine in a similar vein to Unity. Not having made a game in the engine before, creating this nothing was a bit of an adventure as I first had to install a specific "export template" (400MB!) to create the WEBGL version and it felt a little less clear than other software. That said, once it was ready to export, it exported fine. The player experience is actually an *error* however: if you check the JavaScript console in the browser you see `Error: Can't run project: no main scene defined.`. That is, Godot does not provide a default "scene" for your new game to take place in, you must create it explicitly. Now that's nothing.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/godot/Nothing.html)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/unrealengine4/) (Unreal Engine 4, with [Andrew Baker](https://failrate.itch.io/))

[Unreal Engine 4](https://www.unrealengine.com/) is the third of the big 3D engines in this suite. This nothing was unique in that I required a collaborator in Andrew Baker to actually produce the resulting game according to the project brief of creating a game with the engine include no or minimal additions to the engine default. Andrew was extremely thorough and the resulting nothing is representative of Unreal's "Blank" project. As with both Bitsy and PuzzleScript, the blankness is actually rather developed as the player can fly around a in a first-person view and bump into a single platform floating there. It is therefore complete with lighting, physics, player input, and so on. Due to the web export, it also comes with an unsightly additional default interface around it for toggling logs, pausing the game, and more. A whole lot of nothing.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/unrealengine4/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/renpy/) (Ren'Py)

The [Ren'Py Visual Novel Engine](https://www.renpy.org/) is software for creating visual novels. I had originally thought this would be an interesting way for me to engage with visual novel culture, but this particular nothing handily demonstrated to me that the pursuit of "nothing" in a game engine tends to obfuscate rather than clarify the nature of a tool. As such, I know next to nothing about Ren'Py or visual novel production. The nothing produced, however, is intriguing in its sheer complexity. It includes a download sequence, a loading screen with a picture of a woman holding a globe, and a detailed menu system. It also names the game *Nothing 1.0* which I enjoy significantly. Starting the game itself from the menu leads to overlapping errors around missing images that Ren'Py does not provide defaults for, but also two lines of dialog from a character called Eileen: `You've created a new Ren'Py game.` and `Once you add a story, pictures, and music, you can release it to the world!` No, nothing ironic about that.

[Play this nothing](https://pippinbarr.github.io/the-nothings-suite/renpy/)

---

#### [Nothing](https://pippinbarr.github.io/the-nothings-suite/print-and-play/nothing.pdf) (Print-and-Play)

In the tradition of "print and play" games that provide instructions for how to play non-digital games such as LARPs, board games, card games and more. The nothing here is therefore a blank PDF, produced in Microsoft Word as a blank document before exporting. A mere 12KB for so much potential. The implied player experience is somehow one of unlimited freedom because the game context is the real world rather than the constrained world of a videogame engine (perhaps Inform 7 comes the closest to this sense of freedom in a digital context?). With no rules and no aesthetic forms to guide you on how to "play" this nothing, you could do anything? Or is it that you can do nothing?

[Download this nothing](https://pippinbarr.github.io/the-nothings-suite/print-and-play/nothing.pdf)

---

## Would you like to know more?

#### Read the [Press kit](https://pippinbarr.github.io/the-nothings-suite/press) for press information
#### Read the [Process documentation](https://pippinbarr.github.io/the-nothings-suite/process) for process journal, to do list, and related work
#### Read the [Commit History](https://github.com/pippinbarr/the-nothings-suite/commits/main) for step-by-step information about how the project was built
#### Look at the [Code Repository](https://github.com/pippinbarr/the-nothings-suite) for source code etc.

---

*The Nothings Suite* is an no-source game licensed under a [Creative Commons Attribution-NonCommercial 3.0 Unported License](http://creativecommons.org/licenses/by-nc/3.0/). You can obtain the source code from its [code repository](https://github.com/pippinbarr/the-nothings-suite) on GitHub. All code generated by the engines used in these projects has its own copyright that you should respect separately.
