# All together

A convenient library is provided to speedup developement, see **help.pd**

# Workshop

Let's play with the openworld !

* Open both the game and the PD template file : **openworld-template.pd**
* It's highly recommended to save all your work in **openworld.pd** file during the workshop.
* It's highly recommended to use subpatch for individual workshop modules.


## 1 - Simple map toggle SFX

please read [audio basics](audio-basics.md) and [messaging basics](messaging-basics.md) first.

Goal:
* play 2 differents procedural sounds on mini map toggle on/off (Space key in game)

what you learn : 
* get hands on procedural audio by experimenting
* try with different waveforms, additive or substractive synthesis, AM, FM..
* use envelops and basic messaging (select)

see **example-procedural.pd**


## 2 - Chest detector

Goal:
* play a sound to help player finding chest (by using distance and/or camera direction)
* only play detector sound when minimap is open.

what you learn : 
* get hands on 3D vectors calculation
* continuous procedural sound and modulations
* advanced messaging (route)

see **example-chest-detector.pd**


## 3 - Ambiant soundscape

please read [Working with audio files](working-with-audio-files.md.md) first.

Goal:
* play some audio soundscape to improve ingame immersion based on water and/or forest and/or altitude.
* create an underwater effect : applied when camera is under water.

what you learn :
* integrate audio sample files and play them
* use environement information (water, forest)
* underwater effect

see **example-samplers.pd** and **example-underwater.pd**

## 4 - Player sonification

goals:
* player sonification (walk, swim, dive) with audio samples : walk on ground, on water, swin, dive, etc.

what you learn :
* deepening audio sample files handling and messaging

see **example-footsteps.pd**


## 5 - Music from the house

please read [spatialization guide](spatialization.md) first. Some provided demo examples are included.

goals:
* simulate a sound coming from the house (music) in a 3D environment by applying 3D spatialization effects.

what you learn :
* 3D spatialization basics.
* Abstractions


## 6 - Animals spatialization

goals:
* Animals sonification with 3D spatialization.

what you learn :
* deepening 3D spatialization.
* advanced message handling, abstraction, alternate audio routing (throw/catch)

# Project finalization

From all workshop modules above, ensure your have a final Pure Data patch **openworld.pd** based on **openworld-template.pd**.

* chest detector should be enabled only when map toggle is on (to prevent sounds overlap)
* all sounds (except map toggle and chest detector) should be affected by the underwater effect.
* mix all modules together and adjust all signals amplitudes to have a good balance (avoid saturations)

The submitted project should directly work by opening both the final patch and the game.

please read [Project Guidelines](guidelines.md) for detailed information.
