# Hand on PD (Part 1)

Let's open our openworld patch and live code through pratical examples

## About the audio graph

### in/out

* adc~ : Analog Digital Converter
* dac~ : Digital Analog Converter

### Built-in generators

TODO with a noise and a filter ? or an oscillator ?

* osc~
* noise~
* phasor~
* tabosc~4 : TODO what is this ?
* lookup tables and samples : see section on working with audio files

## About the events graph

TODOC : ordering right to left convention

TODOC : list vs message ... ?

## Links between both flows

* from events to audio :
  * TODOC sig~, [filters]~
* from audio to events :
  * TODOC env~