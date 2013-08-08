#1GAM January - Pew Pew

**Name:** Pew Pew

**Genre:** Shoot-em-up

**Engine:** HTML5 Canvas

[Source on Github](https://github.com/whostolemyhat/fruit-shoot)

I only decided to take part in 1GAM in the middle of January, so had only about a week or so to make my first entry (getting my excuses in early!). I've built a couple of simple games (Pong, Noughts and Crosses) using HTML5 canvas, so this seemed like a good place to start - learning a new game engine or framework well enough would have taken me past the end of the month.

I decided on a shoot-em-up game mainly because I haven't made one before, and it involves a fair number of things used in a lot of games:

- simple AI (enemies)
- player input (for controls)
- collision detection
- powerups!
- sprites/art (my previous games only used basic shapes rather than any artwork)


##What went right

The main thing I got right: I finished in time! In fact, I finished a day early, and spent it tarting up the webpage for the game. I also amanaged to add most aspects I planned for (despite massive cuts to get it finished in time) - enemies, powerups and a final boss were the key elements I wanted to add. 


##What went wrong

I decided to write the game from scratch, which turned out to be a huge mistake. I felt that using a framework or game engine would somehow be cheating (which seems to be [quite a common feeling](http://scientificninja.com/blog/write-games-not-engines)), but it meant that I had a huge amount of work to do in a very short space of time, even though my game was very small. The only reason I was able to finish was by using (read: nicking) code from [tutorials](http://www.html5rocks.com/en/tutorials/canvas/notearsgame/) to handle sprites and sounds. **Lesson learned: always use a game engine!** (unless you have a really really good reason)

This was my first entry into a time-limited contest, so my initial game turned out to be vastly too ambitious to finish. Originally I had planned on several enemies, different powerups, mutiple waves of enemies and an end boss. The finished game has a shield powerup, one wave of one type of enemy and a boss - basically everything trimmed back as far as possible. I think I lost quite a chunk of time towards the start of the project by trying to make everything in the code reusable - i.e. an Enemy object which could be extended for use in multiple enemy types (and the same for bosses and powerups). I soon realised that this was slowing me down, so largely abandoned this approach: in the source code you can see a Powerup object along with a setting which would show which powerup was active; in the end I just used a variable set to either on or off to activate a shield.

The code is also a bit of mess - there's UI code which is quite tightly coupled to the game logic - things like the 'Play' button and the message system (which flashes up 'Win!' or 'Lose') should probably be in another file, or at least abstracted in some way. As I mentioned above, there's also a lot of code which I'm not really using, as a result of trying to make everything reusable.

##Tools/resources
- [HTML5 Rocks tutorial](http://www.html5rocks.com/en/tutorials/canvas/notearsgame/) - never would have finished without this!
- [Starfield tutorial](http://www.gimpusers.com/tutorials/starfield-tutorial)
- [Piq](http://piq.codeus.net/draw) - used to draw pixel art
- [GIMP](http://www.gimp.org/) - Photoshop alternative
- [sxc.hu](http://www.sxc.hu/) - royalty-free images
- [cfxr](http://thirdcog.eu/apps/cfxr) - sound effects
- [Yeoman](http://yeoman.io/) - web development framework