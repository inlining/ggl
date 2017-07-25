# ggl (GUI Golfing Language)
A simple, esoteric, golfing programming language which primarily serves to create a graphical user interface in a very short amount of space.
## Installation
Simply download the main python script. Requires Python 3.
## Usage
Run the script with `python main.py script.txt`. The file extension for the script does not matter.
## Language Documentation
### Creating a window
Creating a window is implicit. However, in order to change the size of the window, you will need to begin your program with `w800,600"`. You can, of course, swap out `800,600` with whatever size you need. If you want to change the title, you will need to start with a capital `W` and follow with your title, then end with a closing `"`. (eg. `WAmazing Program"` will make the title `Amazing Program`). As of now, there is no way to use both.
### Text
There are several types of text. The main one, a paragraph, and be achieved like so:

`pThis is some text."`, which will display some text with the content `This is some text.`

Likewise, you can use `h` for headers.
### Buttons
Buttons are simple. The syntax is similar to a paragraph, but uses `b` instead of `p`. You can also add python code in between curly braces (`{`, `}`) which will be run when clicking the button.
### Inputs
Labels for these inputs are used the same way as paragraphs. Add `"` to the end to make sure you have ended the label
+ Checkboxes - `c"`
+ Input Boxes - `i"`
+ Number Slider - `n"`
### Dialogues
Dialogues (for now) only include message boxes. A message box can be created with `mContent of Message Box"`.
### Running code
You can add python code by adding any required snippets after a `^`. Anything after will be interpreted as python, and you can not resume normal ggl use.

In the future, it would be nice to implement Pyth usage, so you can golf your software even further.
### Positioning
Not much (as of now) can be done with positioning. Centering can be achieved by wrapping the desired items to be centered with `<` and `>`.
To insert a vertical space, use `v`. There are no arguments for `v`.
### Functionality
Changing another elements text requires a little bit of thinking. Say you have a program like this:
`pClick the button below to change my text!"vbClick me!"`,
and you want to change `p`'s text when you click it.

The way you can do this is by adding an ID to p. This can be done by using a hashtag and then a 1 digit number after `p`:
`p#5Click the button below to change my text!"vbClick me!"`;
This specifies that `p` has the id of `5`. Now, in python code, you can set the text by adding this code to the button:
`_5='I changed my text!`.
Currently, only `p`s can have IDs, and you can only change their text.
## Example Programs
All of these challenges were posted before the creation of this language, so they are technically invalid.


The [Hello World window challenge](https://codegolf.stackexchange.com/questions/15417/hello-world-window) can be achieved with `pHello World` (if it's the end of the code, you do not need to add an end quote). This is a 12 byte answer, which beats every other answer there is.

The [Self Closing Hello World challenge](https://codegolf.stackexchange.com/questions/28370/write-a-hello-world-gui-program-that-closes-itself-after-three-seconds) can be achieved with
```pHello World"^time.sleep(3)
quit()```, which is 34 bytes. Not the smallest, but still very good.

The [Create A Checkbox challenge](https://codegolf.stackexchange.com/questions/109155/create-a-checkbox/109169#109169) can be achieved with `c`. One byte.
