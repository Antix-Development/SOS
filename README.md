SOS
SOS is my submission the 2021 js13kGames competition, where over a one month period you create a game based on a theme ("space" for 2021), and then you cram your entire game (code and assets) into a 13Kb zip file and submit it.


Introduction
SOS is a retro shoot-em-up game using pixel art graphics, written in JavaScript, HTML, and CSS.


Gameplay
The goal in SOS is to complete successive attack waves by rescuing a number of marooned space engineers, whilst avoiding and/or destroying the enemy units that are present in the wave.

Attack waves become increasingly difficult and at wave 10 the game is at its most difficult. I acknowledge that the balance could be much better tuned but hey.. I only had a month!


Features
In my opinion, some of the more note-worthy features of SOS are...

An asset generator which takes an 8-color indexed PNG file which is then copied, pasted, and has it's colors remapped to create a fairly large texture atlas.

A rendered 2D logo?

A multi layered self depth sorting parallax starfield in 20 lines of code.

A particle system featuring movement, scaling, fading, and animation, all in maybe 50 lines of code.

Seven different enemies with basic AI which combined, present a quite complex combat scenario.

An entire SHMUP game shoe-horned into a 13Kb zip file!

The features above might be pedestrian to you, but they are the ultimate expression of my feeble programming abilities.


Technologies
SOS was developed using Visual Studio Code and Notepad++.

All Assets were created using GIMP, and Frank Force's fantastic ZzFX.

Base graphical assets were both sourced from Open Game Art, and created by myself.

Base64 Image was used to convert the PNG file to a data URI that was able to be embedded inside index.html. Base64 encoding actually ended up better (zipfile size-wise) than using a PNG file, and also resolved "canvas poisoning" issues.

UglifyJS was used to minify the JavaScript code and I was supprised to discover that it consistently out-performed Google's Closure Compiler.


The Code
First and foremost I must humbly apologize for the state of the SOS code-base. Due to the limitations imposed by the js13k competition, it became kind of messy and not very easy to read quite quickly.

On the plus side, I'm always more than happy to answer any questions you might have regarding the code, just drop me a line at antix.development@gmail.com 😃
