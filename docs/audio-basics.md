# Hand on PD (Part 1)

Some considerations :

* Be carefull when you're using a headphone while modifying a patch !
  * Always pull off your headphone when modifying a patch.
  * Set a low audio level when working
* About the signal range :
  * Audio signal typically range from -1 to 1
  * Audio output can't go over than range (it saturates in this case)
  * Always set a final multilier to scale the overall sound before aoutput
* About DC offset :
  * DC offset is the average signal level tipycally at zero.
  * If DC offset is significant, sounds may be distorted or not eared at all (because it's clamped to -1, 1 range)
  * Removing DC offset is quite easy, since it is constant over the time, it is likely a zero frequency signal and could be easily filtered with a high-pass filter.
  * typically a [hip~ 20] before the [dac~] will both remove DC offset and unwanted infra-bass singals.
* About frequency range : 
  * Human ears typicall range from 20Hz to 20kHz.
  * Low end speakers (like laptop speakers) have a more limited range, typically low frequencies can't be ear (below 300 Hz)
  * With a loud professional sound system, infra bass could cause damages. It is then important to take this into consideration when developing on a laptop and run in concert.

Let's see how the audio graph works in PD

see **examples/1-audio-vs-messages.pd** (left part)

## Flow, Nodes and Connections

* Nodes may have one or many inputs at top, each input as a different meaning : very similar to method parameter in text programming.
* Nodes may have one or many outputs at bottom, each output as a different meaning : like a method returning several values in text programming.
* Flow is top-down : messages or audio stream goes from top to bottom, from a node output to another node input.
* Node help act as its documentation and what happens inside a node is the implementation.


## About the audio graph

### in/out

* adc~ : Analog Digital Converter
* dac~ : Digital Analog Converter

### generators

Built-in atoms :

* osc~
* noise~
* phasor~
* tabosc~4
* tables : see section on working with audio files

Provided atoms :

* sin~
* tri~
* sqr~
* ..more : see **help.pd**


### Debugging audio

Built-in tools

* Meter
* env~
* arrays (complicated)

Provided atoms :

* [oscilloscope] : display an audio signal continuously
* [capture] : display a snapshot of an audio signal (manual triger)

## About audio synthesis

There is several categories of audio synthesis. The most commons are additive synthesis and substractive synthesis.
You can make analogy with sculpture :
  * additive is adding material
  * substractive is removing material

### additive synthesis

add several simple signals (oscillators) together to form a complex signal.

see examples : **examples/2-additive.pd** and **har~-help.pd**

Note : signals are note always added but modulated like AM (Amplitude modultation) and FM (Frequency modulation)

see examples : **examples/2-am.pd** and **examples/2-fm.pd**

### substractive synthesis

take a complex signal (white noise, audio sample) and extract a part of it through filters (band pass) to from simple signals.

see example : **examples/2-substractive.pd**

### other synthesis

Other categories are beyond the scope of this lesson : granular synthesis, ...

## Common pitfalls

* applying an audio filter on a sinusoidal signal (single frequency) act more or less as a on/off switch and is pointless. It has more interest on complex signals with lot of differents frequencies.

