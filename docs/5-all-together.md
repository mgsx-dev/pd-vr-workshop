# All together

A convenient library is provided to speedup developement, see **help.pd**

# Workshop

Let's play with the openworld !

* Open both the game and the PD template file : **openworld-0-empty.pd**
* It's highly recommended to save your work in different files (like openworld-1.pd, openworld-2.pd, ... and so on) during the workshop.
* Some basic examples are provided for each steps, you can copy them and use it as a based in your project patch.

## Simple map toggle SFX

see example **openworld-1-map-toggle.pd**

goals : 
* get hands on procedural audio by experimenting
* try with different waveforms, additive or substractive synthesis, AM, FM..
* tweak envelops...

## Chest detector

see example **openworld-2-chest-detector.pd**

goals : 
* get hands on 3D vectors computations
* improve or change detector sound
* use distance, occlusion, ...

## Chests as emitters

see example **openworld-3-chest-emitter.pd**

goals : 
* deepening of 3D computations
* binaural spatialization

## Ambiant soundscape

see example **openworld-4-ambiant.pd**

goals :
* integrate other audio sample files
* based on environement information (water, forest)
* improve underwater effect

## Player sonification

see example **openworld-5-steps.pd**

goals :
* integrate other audio sample files
* implements other player states : walk in water, swimming, diving

## Music from the house

see example **openworld-6-house.pd**

goals :
* advanced 3D spatialization with distance falloff and filters
* use reverberation to simulate environnement reflections

# Project finalization

From all workshop above, make a final Pure Data patch **openworld.pd** based on **openworld-0-empty.pd** file including :
* the map toggle on/off sound
* chest detector could be enabled only when map toggle is on (to prevent sounds overlap)
* mix both ambiant soundscape, player movements, chest emitters and music from the house
* all sounds should be affected by an underwater effect.
* adjust all signals amplitude to have a good balance (avoid saturations)

The submitted project should directly work by opening both the final patch and the game.

