# Give me the Binary!

A simple game about guessing the base-2 conversion of a base-10 number.

Developed as the first assignment for the Embedded Systems and Internet-of-Things course, part of the Computer Science and Engineering Bachelor Programme at the University of Bologna.

### The game

Before the game starts, a welcome screen is shown to the player, and they can set a difficulty level for their next game.

The game is round-based: each round, the player is given a base-10 number between 0 and 15, and the goal is to guess its base-2 conversion switching on and off 4 bits before the round time expires.

If the player's guess is correct they gain some points, and a new and slightly shorter round starts, with a time decrease that depends on the selected difficulty level. Otherwise, a game over screen with the player's total score is shown for some time before resetting to the initial welcome screen, waiting for a new game to be started.

### The system

The program runs on an Arduino UNO board, which relies on some LEDs and an LCD screen to display output to the user, and some buttons and a potentiometer to receive input.

<img width="569" height="226" alt="canvas" src="https://github.com/user-attachments/assets/91505a16-dcac-4cde-946a-7c99444e3d37" />

In particular, the potentiometer is used before the game starts to select the difficulty level, and the buttons are used during the game to swith on and off the four corresponding green LEDs.

The four green LEDs are used to show the base-2 representation input by the player, and the LCD screen shows the base-10 number to be converted during each round, as well as the welcome and game over messages.  
The red LED is used to signal the current state of the system.
