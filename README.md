# 8-Bit Adventure Toolkit

This project aims to provide a complete toolkit for making 8-Bit adventure games playable and enjoyable in a modern environment.

At present, this mainly consists of links to other tools.  As the project develops, it will fill in the missing pieces between those tools.

[Part 1 of The Very Big Cave Adventure](https://8bat.github.io/vbca/play/) has been adapted for the web using this toolkit.  Part 2 is still in development.

## How to update an 8-bit adventure

### Step one: find a downloadable copy of your game for each platform you're interested in

8-bit games were release for one or more _platforms_, such as the [ZX Spectrum](http://worldofspectrum.org) or [Commodore 64](http://www.lemon64.com/).  Games would often include minor differences between platforms - you might want to focus on a single platform, or merge in the best bits from all of them.

If your game is still under active copyright, you'll have to transfer the data to your computer from your original tape.  You won't be able to find a copy online, and could face legal action if you upload your modernised version.

Happily, most 80's adventure games are considered _abandonware_ - although technically still under copyright, the authors have long since stopped caring (or may even be in favour of people copying their work).  These games can usually be found with a simple search.

### Step two: convert your game to _snapshot_ format.

Load your game in an emulator, such as [Speccy](https://fms.komkon.org/Speccy/), [VICE](http://vice-emu.sourceforge.net/) or [CPCemu](http://www.cpc-emu.org/).  Then save a snapshot once it finishes loading.

Downloads are provided in a variety of formats.  For example, your download might represent the raw contents of a tape, or a zip file containing files that will go on a disk.  To update your game, you will need a _snapshot_ file (which has `.SNA` or `.VSF` extension).

You can skip this step if you downloaded a `.SNA` or `.VSF` file.

### Step three: find out which authoring system your game used (if any)

An _authoring system_ is a program that automates some of the low-level details of creating a game.  The most common 8-bit authoring systems were [The Quill](http://8-bit.info/the-gilsoft-adventure-systems/), [The Professional Adventure Writer](http://8-bit.info/the-gilsoft-adventure-systems/) and the [Graphic Adventure Creator](https://spectrumcomputing.co.uk/index.php?cat=96&id=0006391).  A few games were created with other authoring systems, and many were written by hand with no authoring system at all.

It might take some searching, but this information is usually available online.  For example, [World Of Spectrum](http://www.worldofspectrum.org) includes this in the _Authoring_ section of most games.  The authoring system is very likely to be the same for all platforms, so you can use that information even if you're not interested in the Spectrum version.

If you can't find out the authoring system your game used, you might still be able to update your game.  But it might have been written by hand, in which case you'll need to rewrite it from scratch.

### Step four: decompile your game

A _decompiler_ converts your _snapshot_ back to _source code_ - the instructions the original developer typed into the authoring system.

Over the years, people have written decompilers for all of the well-known authoring systems.  They're all slightly different, and you will need some technical knowledge to use them.  Here is a list of known decompilers:

* The Quill
  * [UnQuill](http://www.seasip.info/Unix/UnQuill/) (note: separate version for the BBC Micro on the same page)
* The Professional Adventure Writer
  * [unPAWs](https://github.com/Utodev/unPAWs) (doesn't extract images)
  * [pawgr](https://www.ifarchive.org/indexes/if-archiveXprogrammingXquill.html) (_only_ extracts images)
  * [inpaws](http://inpaws.speccy.org/) (page in Spanish)
* The Graphic Adventure Creator
  * [ungac](https://www.ifarchive.org/indexes/if-archiveXprogrammingXgac.html)
  * [grackle](https://github.com/tautology0/grackle)
* Phipps Associates
  * [unphipps](http://www.seasip.info/Unix/UnQuill/)
* Artic Computing Ltd. (aka "Planet of Death")  
  * [unplad](http://www.seasip.info/Unix/UnQuill/)

See your decompiler's documentation for more information.

### Step five: decide how to approach the update process

Once you have your source code, most of the most technical work is over.  Now you need to make some artistic decisions.

**How much work do you want to put in?** If this is a weekend project for your personal amusement, you probably just want to do whatever's quickest and easiest.  If you're trying to show the world an amazing game from your youth, you might want to dig further in to the details.

**How faithful do you want to stay to the original?** Games in the 1980's often included jokes that don't make sense today, or relied on quirks of the authoring system that are hard to replicate.  You might have strong opinions about changing the original author's intent, or about modernising for the sake of new players.

The steps below will discuss possible solutions for a range of preferences.

### Step six: choose a modern authoring system

Modern authoring systems choose between _faithful_ and _modernising_ in the same way as you did above.  Faithful authoring systems tend to replicate classic authoring systems bug-for-bug, which makes the initial conversion much less work.  But modernising authoring systems tend to be more powerful and easier to use, which makes it easier to make big changes.

**If you want a modernising authoring system:** There are many of these systems, none of which definitively better than any other.  See for example [this comparison](http://brasslantern.org/writers/howto/chooselang.html).  If you choose a modernising system, you will need to rewrite your source code yourself using that system.

**If you want system that's faithful to The Professional Adventure Writer:** [ngPAWS](http://ngpaws.com/) is a good choice, and includes [instructions for converting old games](https://github.com/Utodev/ngPAWS/wiki/PAWS-to-nGPAWS-conversion)

**If you want a system that's faithful to The Quill:** you might be able to import UnQuill's Z-Code output directly into a modern system like [Inform](http://inform7.com/).  You can also try using [The Inker](https://github.com/8bat/the_inker) - a prototype 8bat tool to translate UnQuill output to [ngPAWS](http://ngpaws.com/) format


A major goal of the 8bat project is to provide better modernisation options.  Please check back in a few months.

### Step seven: make manual changes

You should now have a game that is playable in a modern environment.  But the graphics may look bad, or may not be supported by your decompiler at all.  And the gameplay might feel clunky and the jokes might no longer work.  That's fine if you want something quick and faithful, but the result might not be fun for others to play.

You have the source code for your game, and you can make any changes to it you like.  You can open the file in Notepad to get started, but if you've never done serious work in a text editor before, you might want to try [Notepad++](https://notepad-plus-plus.org/).

Have fun!
