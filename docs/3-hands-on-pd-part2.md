# Hand on PD (Part 2)

## About the events graph

see **examples/1-audio-vs-messages.pd** (right part)

### GUI controls

Built-in :

* button, toggle
* sliders, selectors

Provided :

* vec3

### Debugging events

Built-in tools

* [print name]
* number box, bang, ...


## Envelops and messages

Until then we have a continuous signal. Now we want to trigger some sound.

Note that envelops are not restricted to amplitude modulation but could be used to shape frequencies or any other things.

see examples : **ad~.pd** and **asd~.pd**

## Metro and random

see example

## Events ordering

* Ordering by convention from right to left.
* The "Hot" input vs "Cold" inputs concept.


## Links between audio graph and events flow

* from events to audio :
  * sig~, line~, vline~, [filters]~ (lop~)
* from audio to events :
  * env~, threshold~, ... 

