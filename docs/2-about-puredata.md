# Introduction

## Puredata history

Created by [Miller Puckette](https://fr.wikipedia.org/wiki/Miller_Puckette) at IRCAM :

* 1980 : Max (Max msp)
* 1990 : [Pure Data](https://fr.wikipedia.org/wiki/Pure_Data) (pd) as an open source fork of Max MSP

Derivated works :

* [libpd](https://puredata.info/dev/summer-of-code/LibPd)
  * pd-for-android
  * pd-for-ios
  * Unity wrappers
  * Unreal wrappers
  * LibGDX wrappers
    * [gdx-pd](https://github.com/mgsx-dev/gdx-pd)
* [WebPD](https://github.com/sebpiq/WebPd) : Web audio API port (support only a subset of PD vanilla)
* PD extended : no longer maintained (do not use it), use pd vanilla instead.
* [Camomile](https://github.com/pierreguillot/Camomile) to use pd patch as VST plugins in DAW
* [L2Ork](http://l2ork.music.vt.edu/main/)
  * [Youtube](https://www.youtube.com/watch?v=xc5I3wbwH_4)


## Examples

Some [MGSX](http://www.mgsx.net/) applications based on PD :

* [rainstick](https://github.com/mgsx-dev/rainstick) illustrate interactive prodedural audio with Puredata
  * [Youtube](https://www.youtube.com/watch?v=dQfsuBqcNso)
  * [Google Play](https://play.google.com/store/apps/details?id=net.mgsx.rainstick)
* [gdx-pd demo](https://github.com/mgsx-dev/gdx-pd-demo) illustrates various usage of Puredata in video games.
  * [Google Play](https://play.google.com/store/apps/details?id=net.mgsx.pd.demo)
* [rest your eyes](https://mgsx.itch.io/eyes-rest) illustrates procedural audio with WebPD in a game jam context.
* [PPP](http://ppp.mgsx.net) illustrates how to make music with Puredata
  * [Youtube](https://www.youtube.com/watch?v=XEymJGuHoMU)

## PD help

* Get the list of PD objects : **Help/List of objects...**
* right click on a pd object to get help (you can write your own help file by creating a patch with the same name suffixed by **-help.pd**)
* find an object by its name : menu **Find/Find...**
* examples and all object documentation can be found in **Help/Browser/PureData/**
* watchout the PD console (the main window) : it print some errors.

## PD GUI

* [CTRL+Z] : IMPORTANT : one only undo level
* [CTRL+SHIFT+1] : create an object (autoconnect first outlet of current sleection)
* [CTRL+SHIFT+...] : see menu **
* [CTRL+E] : switch to edit mode / play mode
* [CTRL+Click Left] : contextual play mode (usefull to change control in edit mode)
* [Click left] (in play mode) : act on controller or send message
* [Shift + Click left] (in play mode) : fine grain control

## PD Resources

Some usefull resources about PD :

* Puredata Official Documentation:
  * [English version](http://write.flossmanuals.net/pure-data)
  * [French version](https://fr.flossmanuals.net/puredata)
* [Textual Tutorials](http://www.pd-tutorial.com/english/index.html)
* [Video Tutorials](https://www.youtube.com/playlist?list=PL12DC9A161D8DC5DC)
* [a SFX generator tutorial](http://www.mgsx.net/articles/pd/bfxr-like-with-pd/bfxr-like-with-pd.html)


# Common pitfall & known issues

* Undo limited to 1 level.
* Mouse pointer coordinates bugs with recent OS grouping windows in tabs (Windows 10, recent versions of OSX)





