# roguelike

Created by kmccrea while following along with the [RoguelikeDev subreddit](https://old.reddit.com/r/roguelikedev/comments/bz6s0j/roguelikedev_does_the_complete_roguelike_tutorial/).

As a preface, I have never written any code in Python (which is the major motivation behind doing this project). I am simply here to learn, and I'm writing this documentation on the off chance it'll be helpful to anyone else.

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

There's not much to report for this section. The only thing additional I did here was change my player to green because obviously.

I found a list of built-in colors [here](http://roguecentral.org/doryen/data/libtcod/doc/1.5.1/html2/color.html).