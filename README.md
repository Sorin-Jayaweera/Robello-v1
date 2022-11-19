# Robello-v1, basic ui 

Using Teensy 4.1 to process audio and add effects with a simple button toggle ui, effects including reverb, delay, bitcrusher, etc. 

look at button pins for the layout, it's just an array of 8 buttons and 4 potentiometers.
  - You'll have to change the potentiometer max and min values in the map() functions for your own setup.

What code does:
if playing is active, buttons edit which effects are active
if editing is active, the last toggeled effect is the one who'se parameters are being effected
if live-edit-playing, the changes are sent out immediatly, 
  - fun to do with freeverb quickly up and down for roomsize.
  - also good for testing effects.
  
  
Todo: Add implimentation for wack frequency harmonizer, under name "read frequency" is called every time. Otherwise, just use most recent.
buttons that toggle delay, freeverb, chorus, bitCrusheron, flange, and harmonize to on/off
  -harmonize has two modes, main harmonize editing and instrument editing
    -main 
      -edits how often the instrument repeats/is triggered, except waveform which is constant
      -has the number of semitones above that are being played
    -instrument
      -has effects for each instrument: drums,strings,waveform

button that toggles between playing or editing mode, double tap does live-edit-playing
