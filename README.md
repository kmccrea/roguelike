![RoguelikeDev does the Complete Roguelike Tutorial](https://i.imgur.com/3MAzEp1.png)

# roguelike

Created by kmccrea while following along with the [RoguelikeDev subreddit](https://old.reddit.com/r/roguelikedev/comments/bz6s0j/roguelikedev_does_the_complete_roguelike_tutorial/).

As a preface, I have never written any code in Python (which is the major motivation behind doing this project). I am simply here to learn, and I'm writing this documentation on the off chance it'll be helpful to anyone else.  Any information here assumes that you are also following along with the tutorial.

Just to be different, I will be completing this 
tutorial using the following system:
* MacOS Mojave (10.14.5) 
* PyCharm Professional 2018.2 (Built April 10, 2019)

## [Week 1](https://old.reddit.com/r/roguelikedev/comments/c1xj5b/roguelikedev_does_the_complete_roguelike_tutorial/)

### [Part 0 - Setting Up](http://rogueliketutorials.com/tutorials/tcod/part-0/)

I followed all of the instructions linked above, 
but since I am using PyCharm, I'm fairly certain that it's unnecessary to do so.  I believe one could simply
1. Install the latest version of PyCharm
1. Create a new "Pure Python" project
1. Enable tcod (I followed 
[these instructions](https://stackoverflow.com/questions/53074663/how-to-properly-import-libtcod-in-pycharm))

This enabled a virtual environment automatically, 
and I _assume_ that you could also ensure you're on the latest 
version of Python from within the IDE (mine was already updated). 

I continued the tutorial to create the `engine.py` file to 
ensure that everything is up and running.

Lastly, I enabled version control and created my remote 
repository.

### [Part 1 - Drawing the ‘@’ symbol and moving it around](http://rogueliketutorials.com/tutorials/tcod/part-1/)

There's not much to report for this section. The only thing 
additional I did here was change my player to green.

I found a list of built-in colors [here](http://roguecentral.org/doryen/data/libtcod/doc/1.5.1/html2/color.html).

## [Week 2](https://old.reddit.com/r/roguelikedev/comments/c52ik4/roguelikedev_does_the_complete_roguelike_tutorial/)

### [Part 2 - The generic Entity, the render functions, and the map](http://rogueliketutorials.com/tutorials/tcod/part-2/)

~~Perhaps I missed a section at the end of Part 1, but the 
first time we modify `engine.py`, there were two lines I was 
meant to be removing that I didn't have. EDIT: on further reflection, 
we had already removed these lines at the end of Part 1. EDIT 2: 
Ah yes, then the second time we edit this file, those lines are 
missing again. Must be an error with the tutorial. No matter.~~

And that's it. We've now got an awesome (albeit stationary) NPC 
and a small wall to throw ourselves at. Nothing can stop us now! 
(Except the wall).

EDIT: Reddit user [HexDecimal](https://old.reddit.com/user/HexDecimal) 
pointed out in [this comment](https://old.reddit.com/r/roguelikedev/comments/c1xj5b/roguelikedev_does_the_complete_roguelike_tutorial/errulhe/) that my project code should not be inside the `venv` folder (which totally makes sense) so I've moved it up a directory. Initially this was probably just a simple misclick on my part, but I didn't know enough to realize that having it inside `venv` doesn't really make sense. I've read through the documentation [here](https://docs.python.org/3/library/venv.html) and would recommend anyone else who doesn't really understand `venv` to do so as well.  Huge thank you to HexDecimal for the tip. EDIT: (PyCharm users) When moving things like this - be sure to update your working directory. This can be found in `Run -> Edit Configurations`. 

### [Part 3 - Generating a dungeon](http://rogueliketutorials.com/tutorials/tcod/part-3/)

Again, this part is fairly straightforward. Simply following the 
tutorial gives us a generated dungeon!

## [Week 3](https://old.reddit.com/r/roguelikedev/comments/c84ryz/roguelikedev_does_the_complete_roguelike_tutorial/)

### [Part 4 - Field of View](http://rogueliketutorials.com/tutorials/tcod/part-4/)

In this part, I've simply followed the tutorial implemented 
field of view. Also, I've changed the background colors. I don't 
really like them, so I'll tweak them eventually.

### [Part 5 - Placing Enemies and kicking them (harmlessly)](http://rogueliketutorials.com/tutorials/tcod/part-5/)

Now, since we're adding 'monsters' I've changed some colors around 
like I promised in the previous section. When we added enemies, 
they were hard to see on our old background, so now we're just 
using various shades of the same color to give us the illusion of 
FOV while maintaining consistent colors. I've also added all colors 
to the 'colors' array. I assume when we move these values to another 
location (the tutorial mentioned this in an earlier part) it'll make 
more sense to have them all together.

## [Week 4](https://old.reddit.com/r/roguelikedev/comments/caw23f/roguelikedev_does_the_complete_roguelike_tutorial/)

### [Part 6 - Doing (and taking) some damage](http://rogueliketutorials.com/tutorials/tcod/part-6/)

Implementing attacks, damage and death! This is a long chapter, 
but I didn't have any issues when following through the tutorial. 

NOTE: I am using the `enum.auto()` function, so be sure to make 
the appropriate changes in that step if you are as well.

NOTE: I didn't like the recommended controls for movement, (if 
that's some kind of standard then I'm sorry). I've changed to WASD, 
then for diagonals it's QEZC.

### [Part 7 - Creating the Interface](http://rogueliketutorials.com/tutorials/tcod/part-7/)

This section is extremely straightforward. I may revisit it at some 
point to see about changing the colors or even the font, just to make 
it stand out better.

## Week 5

### [Part 8 - Items and Inventory](http://rogueliketutorials.com/tutorials/tcod/part-8/)

In this part, I've just followed the tutorial and now we have a working 
inventory system! I've reverted the controls back to the tutorial default 
because we are adding new keys, and I didn't want to over complicate it. 
Eventually I will likely find a mapping that I like.

### [Part 9 - Ranged Scrolls and Targeting](http://rogueliketutorials.com/tutorials/tcod/part-9/)

Again, this is super straightforward. I'll probably want to revisit 
this section to add new mechanics, or perhaps to tweak the spawn rate 
of certain scrolls for balance. 

## Week 6

### [Part 10 - Saving and loading](http://rogueliketutorials.com/tutorials/tcod/part-10/)

A very useful part of any game! 

I spent a fair amount of time here 
trying to figure out how to install `shelve`. I kept getting the error 
`ERROR: Could not find a version that satisfies the requirement shelve 
(from versions: none)` turns out just modifying the code and importing 
shelve works. However, I had a further problem with shelve. When it 
creates a save file `savegame.dat`, it's actually appending another 
suffix behind the scenes here, so my file name is actually 
`savegame.dat.db`. As far as shelve is concerned, this seems ok. 
In the `load_game` function, `shelve.open` works as expected.
 However, in the few lines above that, I had to change 
```python 
 def load_game():
    if not os.path.isfile('savegame.dat'):
        raise FileNotFoundError
```
to
```python 
 def load_game():
    if not os.path.isfile('savegame.dat.db'):
        raise FileNotFoundError
```
Otherwise, it was returning that error and never loading our saved game!

Other than that, fairly straightforward, and now we can save and and resume a game! Nifty!

EDIT: I've actually gone back and changed this function further. 
On different OS this will actually append different suffixes, further
confusing the issue. See [this SO post](https://stackoverflow.com/questions/16171833/why-does-the-shelve-module-in-python-sometimes-create-files-with-different-exten/16231228#16231228).
My function now looks like this, completely skipping the check for the file.
If we had kept the file check, we'd have to look for every different suffix combination,
then, we might find one that isn't actually the one in use (during one test, 3 separate files were created).
Doing it this way will just either work or it won't, and we don't have to care about what type of file it is.

```python
def load_game():
    try:
        with shelve.open('savegame.dat', 'r') as data_file:
            player_index = data_file['player_index']
            entities = data_file['entities']
            game_map = data_file['game_map']
            message_log = data_file['message_log']
            game_state = data_file['game_state']
    except:
        raise FileNotFoundError

    player = entities[player_index]

    return player, entities, game_map, message_log, game_state
```

