# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **MARITZA PADILLA**

Time spent: **2** hours spent in total

Link to project: https://glitch.com/~mememorygeme 

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial

## Video Walkthrough

Here's a walkthrough of implemented user stories:
* [X] User Wins/Complete Pattern: https://cdn.glitch.com/3a7db4a7-bc63-400f-99ed-73b91ba2e42e%2FWonGame.gif?v=1616649202588
* [X] User Loses/Incorrect Guess: https://cdn.glitch.com/3a7db4a7-bc63-400f-99ed-73b91ba2e42e%2FLostGame.gif?v=1616649208084
* [X] Demonstration of Start/Stop Switch: https://cdn.glitch.com/3a7db4a7-bc63-400f-99ed-73b91ba2e42e%2FButtons.gif?v=1616649212476

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
* [X] README Template: https://hackmd.io/YIMgxXoFSDSHv1clapGzfg?edit
* [X] Document Instructions: https://courses.codepath.org/snippets/summer_internship_for_tech_excellence/prework

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
At first I encountered an issue where the game would stop the game and report a it as "lost" seemingly after the user reached pattern.length - 1 turns.
Even if I inputted the pattern correctly, I'd be interrupted. And when I would try the game again by pressing the start button, I'd lose immediately
after one input. After revising my code and thinking upon the issue, I realized it could have been a problem with my guessCounter, since the game's status
is dependent on its value. I figured that reinitialization was occuring improperly, and I decided to check where I was reinitializing the variable in my guess() function. 
I found that my mistake was re-declaring the variable as 0 when I needed to set it equal to 0 instead. (Ex: var guessCounter = 0 instead of guessCounter = 0). After 
removing "var" from my reinitialization, I ran the code again and the game took both correct and incorrect input properly. I also noticed I was having problems
deciding what color pallete to use with my game. After experimenting with some hex codes and deciding on the main colors for the tiles, I realized I needed to make a 
stark contrast between the dark and light colors of the tiles to make the transition/click clear to the user. I gave my game a dark background (since it's easier on the
eyes than light mode) and found it aided in providing the contrast I was looking for.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
I don't have much experience with incorporating audio into my program before, but it was interesting getting to experiment with it.
I have more questions about how to best incorporate audio into webpages, since I know it can be a little unusual/startling for a website
to have sound responsiveness. I also wonder how to best go about designing a website before developing it. I'm familiar with programming
given a webpage design, but I would like to know what contributes to creating a website that best captures the interests of the user.
How can I determine how interactive my website should be, and how can I make best use of the interactive tools at my disposal?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
If I had more time, I would prompt the user to pick between 2 modes: Melody and Cacophony. Melody mode consistently plays unique, respective sounds for each button as is implemented in the 
current version. Cacophony mode, however, plays the sounds randomly. I would see about making use of a rand() function that randomly chooses from a range of 4 sounds to play each time a button is played.
Essentially, buttons are not assigned sounds. Rather, they are randomly played with each click.
Meaning the user can actually be distracted by the sound and select the wrong tile instead of being aided by the sound as seen in Melody mode. 
I would also research ways to incorporate a mode where I prompt the user for a number of tiles to play with (from 4-10 for example). I would likely create different sets of patterns for each number that the user
provides, meaning I would create 7 global variable patterns (pattern1- pattern7) to handle each case. By creating new pattern sets, I should be able to recreate the game with different numbers of tiles.
I noticed that even without clicking on the start button, if I click on any of the tiles in the game, I can hear the sound, and see the button color darken to indicate it was clicked on. I can change the game by
prompting the user to "Click on each of the tiles to memorize their sound. When you're ready, click start. Click on the button that corresponds to the sound you hear." After the user starts the game, they will only
hear the sound but will not see the light that guides them to the correct tile. Essentially, this would be the Light and Sound game with a bonus "Solo Sound" mode.



## License

    Copyright MARITZA PADILLA

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
