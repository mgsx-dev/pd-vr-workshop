# Hand on PD (Part 1)

Let's see how the audio graph works in PD

## About the audio graph

### in/out

* adc~ : Analog Digital Converter
* dac~ : Digital Analog Converter

### Built-in generators

Built-in atoms :

* osc~
* noise~
* phasor~
* tabosc~4 : TODO what is this ?
* lookup tables and samples : see section on working with audio files

Provided atoms (TODO get from PFXR) :

* square
* triangle
* saw

## About audio synthesis

### additive synthesis

add several simple signals (oscillators) together to form a complex signal.

see example

TODO example with brass tricks (freuency decay)

### substractive synthesis

take a complex signal (white noise, audio sample) and extract a part of it through filters (band pass).

see example

