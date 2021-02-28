## Make your first videogame with PICO-8

February 28, 2021

Francisco Rojo


## Overview

Make your first game with PICO-8!

Video games are so cool! But how do you actually make a videogame? Where do you even start? The answer is right here! Using PICO-8, you will make a pixel art game like Undertale in less than an hour, that you can share with your friends and family and enemies and exes and former bosses that you've developed strangely paternal relationships with.



## Notes on asking for help

This is meant to be a beginner-friendly, intro to PICO-8. The goal is to get a working videogame that you can share with a friend as quickly and painlessly as possible.

However, computers can be so finicky! I (Fran) will try to go slow, and address questions in the chat, but for the sake of convering enough content to get a working videogame, I probably won't be able to help everyone with everything.

If you are stuck and want some help, first ask in chat. If we have moved on, you're next best bet is to ask in the #babycastles-academy channel in the Babycastles Discord: https://discord.com/invite/9N42waj


## Some shortcuts

| Key        | Action                          |
| ---------- | ------------------------------- |
| ESC        | Toggle Command Line/Edit Mode   |
| ctrl-S     | Toggle info panel               |
| ctrl-R     | saves the current game          |


## Getting to know PICO-8

PICO-8 opens up into this command line interface.

Here are some useful commands:

| Command            | Decription                                   |
| -------------------| -------------------------------------------- |
| `ls`               | lists the carts you've made                  |
| `save <game>.p8`   | saves the current game                       |
| `load <game>.p8`   | loads a game into the editor                 |
| `run`              | runs the loaded game                         |

Press ESC key to toggle to the editor. The editor is where you'll make a game!

There are 5 tabs in the editor (you can see them in the top right).

Code tab: This is where you write the code
Sprite tab: For drawing sprites
Map tab: Can use sprites to draw a space
SFX tab: Make sound effects
Music tab: Make background music

## Drawing a space

We are make a game where you are a ghost that floats around a graveyard. 

First, we are going to use the sprite editor and the map editor to draw this graveyard.

Our process will be to create the tiles in the sprite editor, and then use the map editor to arrange these tiles into a graveyard.

### Sprite editor

Every sprite is 8 pixels by 8 pixels. (Really small!!)

Select the pencil tool and a color and then click on the big square to draw your sprite. (There are other tools, like the circle tool, but we won't use those today -- unless you want to!)

You "erase" by drawing with black - that's the transparent color.

You can see your sprite start being drawn in the bottom.

We will draw some grass tiles and some tombstone tiles.

### Map editor

Once we've drawn the tiles, we switch over to the map editor to draw our space using the tiles we've just made.

The map editor interface is similar to the sprite editor, but instead of drawing with colors you draw with sprites.

Very important!!: hold SPACE to see the outline of what will be on screen! and also to pan.

We want to draw enough of a map to cover the entire screen.

Our PICO-8 screen is 128x128 pixels. Or in other words, it's 16 8x8 tiles wide (and also that many high).

## Putting the graveyard in the game

Now we're going to put the map in the game and run our game for the first time.

But first! Save your game! Press ESC to go back to the command-line. Save it by typing `save game.p8` (or whatever you want to call your game) and hitting enter.

Now that you've given your game a name, you can save the game at any point by pressing CTRL-S! (or CMD-S on Mac).

### Map()

Go to the code editor (press ESC to go to edit mode and click the parenthases in the top right).

PICO-8 uses Lua as its programming language.

The way that we get things to display on screen, is by putting them in this magic `_draw()` function. PICO-8 will run whatever code is in `_draw()` 30 times a second. AKA 30 frames a second.

PICO-8 has an API, or a set of functions that we can call to make things happen on the screen. The full list is here: https://www.lexaloffle.com/pico8_manual.txt . I like to use this cheat sheet: https://www.lexaloffle.com/bbs/files/16585/PICO-8_Cheat-Sheet_0-9-2.png

We are going to use the `map()` function to draw the space that we made in the map editor.

Write/copy this code into the code editor:

It's important to copy it down exactly!


```

function _draw()
  cls()
  map(0, 0, 0, 0, 16, 16)
end

```

This draws our space from cel (0,0) to cel (16,16) starting from (0, 0) on the screen (which is top-left).

(Also `cls()` clears the screen.)


## Running the game!

Now, press CTRL-R to run the game (CMD-R on mac)

If you've typed the code right, you will now see the graveyard drawn! You might get a syntax error if you typed something wrong. 


## Drawing the player

A game needs a player. Let's make one.

Let's go back to the sprite editor (click on it in the top right).

We're going to draw a ghost. (although you can draw whatever you want!)

## Putting the player in the game

We're going to use the `spr()` function to draw our sprite onto the screen.

```
function _draw()
  cls() 
  map(0, 0, 0, 0, 16, 16)
  spr(3, 60, 60) 
end
```

Remember CTR-R to run the game

## Moving the player :o

It's time for input and buttons and animation!!

We are going to use another magic function in PICO-8 called `_update()`. We use `_update()` to do all the things that aren't drawing. (for example getting input.) `_update()` also runs 30 times a second like `_draw()`."

We are going to use the `btn()` function with some `if then` statements and a `variable` to get input from the player.

First, let's convert the player's X position to a variable.

Create a `player_x` variable at the top and assign it to 60. Then replace the 60 in the `spr()` function that we're using to draw the player.

```
player_x = 60

function _draw()
  cls() 
  map(0, 0, 0, 0, 16, 16)
  spr(3, player_x, 60) 
end
```

Now lets affect that variable with input from the player. Here's the finished code:

```
player_x = 60
player_y = 60

function _update()
  if btn(0) then 
   player_x = player_x - 1
  end

  if btn(1) then 
   player_x = player_x + 1
  end
  
  if btn(2) then 
   player_y = player_y - 1
  end
  
  if btn(3) then 
   player_y = player_y + 1
  end
end

function _draw()
  cls() 
  map(0, 0, 0, 0, 16, 16)
  
  spr(11, player_x, player_y) 
end
```


## Sharing the game

To turn your game into a cart, save it as `game.p8.png`.

To create a label for your game, run your game and press ctrl-7 to grab a screenshot.

Put some comments at the top of your code for the title.



