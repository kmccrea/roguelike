# roguelike

Created by kmccrea while following along with the [RoguelikeDev subreddit](https://old.reddit.com/r/roguelikedev/comments/bz6s0j/roguelikedev_does_the_complete_roguelike_tutorial/).

As a preface, I have never written any code in Python (which is the major motivation behind doing this project). I am simply here to learn, and I'm writing this documentation on the off chance it'll be helpful to anyone else.  Any information here assumes that you are also following along with the tutorial.

Just to be different, I will be completing this tutorial using the following system:
* MacOS Mojave (10.14.5) 
* PyCharm Professional 2018.2 (Built April 10, 2019)

## [Week 1](https://old.reddit.com/r/roguelikedev/comments/c1xj5b/roguelikedev_does_the_complete_roguelike_tutorial/)

### [Part 0 - Setting Up](http://rogueliketutorials.com/tutorials/tcod/part-0/)

I followed all of the instructions linked above, but since I am using PyCharm, I'm fairly certain that it's unnecessary to do so.  I believe one could simply
1. Install the latest version of PyCharm
1. Create a new "Pure Python" project
1. Enable tcod (I followed [these instructions](https://stackoverflow.com/questions/53074663/how-to-properly-import-libtcod-in-pycharm))

This enabled a virtual environment automatically, and I _assume_ that you could also ensure you're on the latest version of Python from within the IDE (mine was already updated). 

I continued the tutorial to create the `engine.py` file to ensure that everything is up and running.

Lastly, I enabled version control and created my remote repository.

### [Part 1 - Drawing the ‘@’ symbol and moving it around](http://rogueliketutorials.com/tutorials/tcod/part-1/)

There's not much to report for this section. The only thing additional I did here was change my player to green.

I found a list of built-in colors [here](http://roguecentral.org/doryen/data/libtcod/doc/1.5.1/html2/color.html).

## Week 2

### [Part 2 - The generic Entity, the render functions, and the map](http://rogueliketutorials.com/tutorials/tcod/part-2/)

~~Perhaps I missed a section at the end of Part 1, but the first time we modify `engine.py`, there were two lines I was meant to be removing that I didn't have. EDIT: on further reflection, we had already removed these lines at the end of Part 1. EDIT 2: Ah yes, then the second time we edit this file, those lines are missing again. Must be an error with the tutorial. No matter.~~

And that's it. We've now got an awesome (albeit stationary) NPC and a small wall to throw ourselves at. Nothing can stop us now! (Except the wall).

EDIT: Reddit user [HexDecimal](https://old.reddit.com/user/HexDecimal) pointed out in [this comment](https://old.reddit.com/r/roguelikedev/comments/c1xj5b/roguelikedev_does_the_complete_roguelike_tutorial/errulhe/) that my project code should not be inside the `venv` folder (which totally makes sense) so I've moved it up a directory. Initially this was probably just a simple misclick on my part, but I didn't know enough to realize that having it inside `venv` doesn't really make sense. I've read through the documentation [here](https://docs.python.org/3/library/venv.html) and would recommend anyone else who doesn't really understand `venv` to do so as well.  Huge thank you to HexDecimal for the tip. EDIT: (PyCharm users) When moving things like this - be sure to update your working directory. This can be found in `Run -> Edit Configurations`. 

### [Part 3 - Generating a dungeon](http://rogueliketutorials.com/tutorials/tcod/part-3/)

Again, this part is fairly straightforward. Simply following the tutorial gives us a generated dungeon!

## Week 3

### [Part 4 - Field of View](http://rogueliketutorials.com/tutorials/tcod/part-4/)

In this part, I've simply followed the tutorial implemented field of view. Also, I've changed the background colors. I don't really like them, so I'll tweak them eventually.

### [Part 5 - Placing Enemies and kicking them (harmlessly)](http://rogueliketutorials.com/tutorials/tcod/part-5/)

Now, since we're adding 'monsters' I've changed some colors around like I promised in the previous section. When we added enemies, they were hard to see on our old background, so now we're just using various shades of the same color to give us the illusion of FOV while maintaining consistent colors. I've also added all colors to the 'colors' array. I assume when we move these values to another location (the tutorial mentioned this in an earlier part) it'll make more sense to have them all together.
