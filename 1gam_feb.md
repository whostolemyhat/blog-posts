#1GAM Feburary - Copycat

**Name:** [Copycat](http://www.jamestease.co.uk/games/copycat/)
**Genre:** Memory game
**Engine:** HTML5 / Javascript
**Source:** [Github](https://github.com/whostolemyhat/feb-1gam)

*In which I learn the value of planning*

For [February's game](http://www.jamestease.co.uk/games/copycat/), I decided to learn from my mistakes by writing the game from scratch and leaving everything to the last minute. This was, as I discovered last month, not the best idea.

The theme for February was 'Sound', so I decided to make a memory game similar to  'Bop it'. This seemed fairly straightforward to make in HTML - just create a load of links, play a sound then get the user to click on the relevant link.

However, due to my inept planning, I didn't end up using sound at all, and the game morphed into a visual memory game like 'Simon' - users had to repeat a sequence which was shown to them at the start of each round. 

From a technical point of view this is fairly simple - have some coloured blocks, populate an array at random, then read through the array and highlight the relevant block to create the sequence.  The interesting part is highlighting the blocks and getting the timing of the playback correct (so blocks don't all highlight at once, overlap each other or break the page they're sitting in).

The animation timing was an area which tripped me up - I used [Javascript's setTimeout function](https://developer.mozilla.org/en/docs/DOM/window.setTimeout), and, as every time I use it, I forgot that there shouldn't be brackets after the function you pass in:

	setTimeout(animateBlocks(), 1000); // WRONG!
	
	setTimeout(animateBlocks, 1000); // CORRECT!
	
The first line (wrong!) will execute the code in the `animateBlocks` function immediately rather than waiting for one second, since having the brackets after the function name **calls the function**. (I forget this every single time I use setTimeout, and end up spending a frustrating hour trying to work out why everything's happening at once. Perhaps it'll sink in this time.) Passing just the name of the function to setTimeout makes everything run as expected.

However, later on in my code, I needed to pass variables to a function called by setTimeout. "No problem", I thought, "I'll just add the brackets back in with the variables":

	setTimout(animateBlock(block), 1000);
	
Yep, this executes the function immediately. To call functions with variables in setTimeout, you need to wrap the function with an anonymous function (or rather, contain it within a closure so it isn't called immediately):

	setTimeout(function() { animateBlock(block); }, 1000);
	
If nothing else, I'm pleased that making Copycat has taught me how to use setTimeout properly :)

The game itself was pretty rushed, which I think shows - the score is pretty much an afterthought, and there's no progression in the game - i.e. the length of the sequence stays the same, and there aren't any different mechanics in the game. This really hammered home the importance of planning in making a game - for the March entry, I've given myself weekly targets to make sure I don't end up trying to cram everything into the last week again!

[Source on Github](https://github.com/whostolemyhat/feb-1gam)
[Play the game!](http://www.jamestease.co.uk/games/copycat/)


##Tools
- [Yeoman](http://yeoman.io/) - used to quickly set up project, server and live reload
- [jQuery](http://jquery.com/) - because browsers
- [Compass/Sass](http://compass-style.org/) - just can't go back to plain CSS!
- [Sublime Text 2](http://www.sublimetext.com/2) - love it