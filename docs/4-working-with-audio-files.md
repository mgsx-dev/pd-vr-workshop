# Working with audio files

TODOC working with external files, the path problem : relative to the patch ??? or not ???

There is two ways to load an audio file :

* [readsf~] : direct read from files : mainly for big sound files, limited control on playback (play/stop only).
* [soundfiler] : load sound file into arrays : mainly for small files, full control on playback.

Convenient abstractions based on soundfiler are provided to simplify sample manipulation in pd (see corresponding help files) :

* [sampler1~] : a mono sampler
* [sampler2~] : a stereo sampler

TODO : finalize the stereo version with absolute time based play and code the mono version.

## Audio file formats

Pure Data only support raw PCM encoding for the following file formats :

* [WAV](https://en.wikipedia.org/wiki/WAV) : Microsoft
* [AIFF](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format) : Apple
* NeXTSTEP : an old audio format no longer used these days.

In order to work with other formats/encoding (MP3, OGG, ...) you'll need to convert them with some tools :

* Windows : ???
* Mac : ???
* Linux : Audacity

### Audio format

* sample rate : 44100Hz, 48000Hz, 22050Hz, 96000Hz ...
* sample depth : 16 bits, 8 bits, 24 bits, 32 bits floating-point, ...
* channels : Stereo (2 channels), Mono (1 chanel), 5.1 (6 channels) ...


## Resources

* free audio banks :
    * https://freesound.org
* audio file generators :
    * TODOC PFXR, SFXR, BFXR

### About licencing

Note about licences : take care of the licences of works your using and always include information in your projects.
Pay attention to following licences limitations :

* can it be used for commercial purpose ?
* can it be modified/mixed/derivated ? and under which conditions ?
* do you need to give attribution to the author ?

Note that you can't take the ownership of a licenced work nor change its licence.

Note that when a work has no licence, it is copyrighted by the author by default (the most restrictive licence).

Public domain is the most permissive licence (eg. CCO - Creative Common Public Domain Dedication)
