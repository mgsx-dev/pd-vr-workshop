# Working with audio files

Note that in Pure Data, you can use relative paths or absolute paths. Absolute paths should be avoided in order to share your works.
Relative path are relative to the patch or abstraction reading the file. For instance if a wav file is in the parent folder of
the patch, its path will be **../myFile.wav**. A common pitfall is when an abstraction is not in the same directory as the patch tht use this abstraction : if the file is loaded by the main patch, the path should be relative to the main patch. If the file is loaded by the abstraction, the path should be relative to the abstraction even if the message containing the path is sent from the main patch.
This behavior is usefull to pack both abstraction and external files as a library : any patch using the abstraction don't have to resolve paths to abstraction's own data.

**For beginners (and this lessons), it's recommended to have all files (PD files and audio files) in a unique folder.**

There is two ways to load an audio file :

* [readsf~] : direct read from files : mainly for big sound files, limited control on playback (play/stop only).
* [soundfiler] : load sound file into arrays : mainly for small files, full control on playback.

Convenient abstractions based on soundfiler are provided to simplify sample manipulation in pd (see corresponding help files) :

* [sampler1~] : a mono sampler
* [sampler2~] : a stereo sampler


## Audio file formats

Pure Data only support raw PCM encoding for the following file formats :

* [WAV](https://en.wikipedia.org/wiki/WAV) : Microsoft
* [AIFF](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format) : Apple
* NeXTSTEP : an old audio format no longer used these days.

In order to work with other formats/encoding (MP3, OGG, ...) you'll need to convert them with some tools :

* Windows : Audacity
* Mac : Audacity
* Linux : Audacity

### Audio format

* sample rate : 44100Hz, 48000Hz, 22050Hz, 96000Hz ...
* sample depth : 16 bits, 8 bits, 24 bits, 32 bits floating-point, ...
* channels : Stereo (2 channels), Mono (1 chanel), 5.1 (6 channels) ...


## Resources

* free audio banks :
    * https://freesound.org
* audio file generators :
	* [BFXR](https://www.bfxr.net/) : web based
	* [PFXR](http://www.mgsx.net/articles/pd/bfxr-like-with-pd/bfxr-like-with-pd.html) : PD based

### About licencing

Note about licences : take care of the licences of works your using and always include information in your projects.
Pay attention to following licences limitations :

* can it be used for commercial purpose ?
* can it be modified/mixed/derivated ? and under which conditions ?
* do you need to give attribution to the author ?

Note that you can't take the ownership of a licenced work nor change its licence.

Note that when a work has no licence, it is copyrighted by the author by default (the most restrictive licence).

Public domain is the most permissive licence (eg. CCO - Creative Common Public Domain Dedication)
