
# Audio spatialization

In this workshop, we will approximate some of audio spatialization concepts. For a quick understanding, please read [this Oculus Documentation page](https://developer.oculus.com/documentation/audiosdk/latest/concepts/audio-intro-localization/). Other pages have useful information as well.

For a full understanding you can read [this article](https://en.wikipedia.org/wiki/Sound_localization)


# Distance Localization

**Loudness**

Sound pressure decrease by distance. This is due to loss of energy : wave sphere become bigger and energy at a point (ears or microphone) is then lower.

As per [inverse distance law](http://www.sengpielaudio.com/calculator-distance.htm), sound pressure decrease by half when doubling distance. We can use following formulas to simulate this factor : 

`level at distance = level at one meter / distance`

or

`level at distance = distance of sound at full level / distance`

see demo-spatial-loundness.pd


**Reverberation**

Initial delay (early reflection) is beyond the scope of the workshop because we son't have this information from the game.

However, we can use Reverberation effect to simulate global reflection.

Mixing direct sound (dry) and full reverb sound (wet) can contribute to simulate distance as well.

Reverb characteristic (parameter) depends on environment : small closed room, exterior desert, and dense forest have very different
reverberation features.

see demo-spatial-reverberation.pd


**Frequency attenuation**

Two physical phenomena can be simulated to contribute to distance perception : 

* [Air damping](http://www.sengpielaudio.com/calculator-air.htm) : when distance increase, high frequencies (abvoe 1k - 10k) get absorbed by air (or gaz) depending on humidity and temperature.

* [Proximity effect](https://en.wikipedia.org/wiki/Proximity_effect_(audio)) : Very close recorded sounds get much more low frequencies (below 150 - 200 Hz), that's why decreasing quickly some low frequencies at close distance can gives a more realistic effect.

Proximity effect is not so relevent in the game so we can leave it for now. 

Air damping calculator gives -3db / 100m for 4 kHz frequencies at 20°C and 50% humidity.
We can approximate it by changing cutoff frequency by distance. Effect won't be noticeable when coupled with loundness attenuation, so we can lower frequency cutoff in order to exaggerate this effect.

see demo-spatial-damping.pd



# Directional Localization

## Lateral

**interaural time difference (ITD)**

We can simulate it using delay lines. 

* Sound speed is around 343m per second. 
* ears distance is about 21.5 cm
* Giving a source distance and angle, we can calculate delay for individual ears

see demo-spatial-itd.pd


**interaural level difference (ILD)**

Head shadowing can be simulated with a low pass fitler with a 2 kHz cutoff frequency. We can then mix original sound and filtered
sound for each ear depending on source angle.

see demo-spatial-ild.pd


## Front/Back/Elevation

HRTF is heavily used in modern 3D spatialization but is beyond the workshop. It provides elevation and listener front/back orientation perception. 

