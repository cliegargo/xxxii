# XXXII Documentation
![screenshot](res/cover.png)

## Contents
* [The Process of Making this Game](#the-process-of-making-this-game)
    * [Introduction](#ntroduction)
    * [Planning](#planning)
    * [Analysis](#analysis)
    * [Design](#design)
    * [Implementation](#mplementation)
* [Downloading the Repository](#downloading-the-repository)
* [Requirements](#requirements)
* [Resources Used](#resources-used)
* [Tools Used](#tools-used)
* [Running](#running)
    * [Unix-like](#unix-like)
    * [Windows](#windows)
    * [Usage](#usage)
* [Formatting](#formatting)
* [License](#license)

### About
I am making this game for compliance to my Computer Programming 2 class, using tkinter, random module, and basic maths.


### The Process of Making this Game
##### Introduction
This game makes use of the different widgets provided by the tkinter module, e.g., Frames, Labels, LabelFrame, and PhotoImage. This game incorporates the turn-based style of games.
The game's mechanic (according to the sample provided), is that there are two players in the game, the players will then take turns. In each turn, the player can either attack the other player or heal their HP.
Now, I will go in depth about how I handled each stage of the Software Development Cycle.


##### Planning
In the planning phase, I studied the different widgets in tkinter module. Once I've understood usage, it's now clear that the program can easily be built.


##### Analysis
In the analysis phase, I segmented the different parts of the game, these are:
* Geometry
* Frame transition
* Turn-based system
    * Display whose next turn is it
* Event system 
    * Display how much damage has a player dealt
    * Display how much health has a player recovered


##### Design
In the design phase, I used the list I made in the analysis phase.


##### Implementation
* Geometry: Solved by determining the width and height of the Main Window, Frames, Labels, and LabelFrames.
* Frame transition: Solved by using the destroy() function and calling the assigned function.
* Turn-based system: To solve this, I made a variable named `self.turn = 1`, `self.h_player1`, `self.h_player2`, and `while` loop. If both players HP are above zero (0), the player's turn is determined by the `self.turn`'s value. If the `self.turn`'s value is 1, then it is the first player's turn. Otherwise, it's the second player's turn.
    * Display whose next turn is it: Solved by using the .config() function -- changing the the label depending on whose turn is it
* Event system
    * Display how much damage has a player dealt
        * Solved by using the .config() function -- changed the label depending on how much damage the player dealt
    * Display how much health has a player recovered
        * Solved by using the .config() function -- changed the label depending on how much HP the player recovered


### Requirements
* Python 3 or above
* Python Tkinter


### Resources Used
* [Silver, a font for games by Poppy Works](https://poppyworks.itch.io/silver)
* [PEP 8 Style Guide for Python Code](https://python.org/dev/peps/pep-0008)
* [Battle of Actium](https://en.wikipedia.org/wiki/Battle_of_Actium)
* [Pantheon](https://en.wikipedia.org/wiki/Pantheon,_Rome)
* [Lighthouse of Alexandria](https://en.wikipedia.org/wiki/Alexandria_lighthouse)
* [Caesar Augustus' Bust](https://upload.wikimedia.org/wikipedia/commons/0/0b/Augustus_Bevilacqua_Glyptothek_Munich_317.jpg)
* [Marcus Antonius' Bust](https://upload.wikimedia.org/wikipedia/commons/2/21/Marcus_Antonius_marble_bust_in_the_Vatican_Museums.jpg)


### Tools Used
* [Pop!_OS](https://pop.system76.com/)
* [Python](https://python.org)
* [Atom](https://atom.io)
* [Git](https://git-scm.com)
* [GIMP](https://gimp.org)


### Running
##### Unix-like
Before running the game, copy the Silver font, this is found at the `res/fonts/Silver.ttf` directory. To do this, follow the instructions below:
```bash
# Download the repo
git clone https://github.com/clieg/xxxii.git

# Go the the repo's directory
cd xxxii

# Copy the font to the /.fonts directory
cp -v res/fonts/Silvert.ttf ~/.fonts

# If ~/.fonts directory does not exist
mkdir ~/.fonts

# Run the game
./run_xxxii.py

# Terminal arguments
./run_xxxii.py -h
```


##### Windows
[Download the game](https://github.com/clieg/xxxii/archive/refs/heads/master.zip).
Before running the game, install the Silver font, this is found at the `res/fonts/Silver.ttf` directory. To do this simply double click the font and install it.
```shell
# Run the game
py run_xxxii.py

# Terminal arguments
py run_xxxii.py -h
```
~~If this does not work. Maybe try dual booting, setting up a VM with Linux, or use WSL. I haven't tested this game on Windows machine, but considering that Python is cross-platform, then there shouldn't be any problem.~~
This is no long true.


##### Usage
Using the `argparse` library, I added terminal arguments to the game. Running the command `./run_xxxii.py -h` or `python3 run_xxxii.py` will display the game's terminal help argument:
```bash
usage: run_xxxii.py [-h] [-a] [-v] [-l] [-c] [-V]

optional arguments:
  -h, --help     show this help message and exit
  -a, --author   show author
  -v, --version  show version
  -l, --license  show license
  -c, --credits  show credits
  -V, --Verbose  show verbose
```


### Formatting
This program follows the [PEP 8 Style Guide for Python Code](https://python.org/dev/peps/pep-0008) as much as possible.
To save lines of code, I made this module to store the configuration for the game, e.g., the title, geometry, fonts, colours, and anchors.


### License
Made by [Clint E](https://github.com/clieg). This program is provided under the [GPL-3.0 License](https://github.com/clieg/xxxii/blob/master/LICENSE).