# Guidelines

**Write documenation**

It could be helpfull to write a documentation about your patch : how it works, is there some bugs or limitations, ...

**Comment your patch**

It's important to add comment in your patch, it helps other developer or yourself after month of pause in order to remember what you've done.

**Have a readable patch**

The more connections you have, the less readable your patch is.

To overcome this situation, group some hardwired parts in subpatches or abstractions.

**Ensure proper initialization**

Use loadbang message to initialize some constants, the final patch should work without any manual actions.

**Message ordering**

By default, messages are triggered depending on wires creation time, you can't based ordering on this because it could break your patch when modifyng it.

To overcome this problem, always use trigger object (t) to enforce trigger ordering.

**Minimize size**

Try to minimize project size especially audio files by including only required ones.

The project ZIP file shouldn't exeed 100 MB.

**Include all dependencies**

Include all original pd files, whenether you modified them or not.

Include all your pd own files required to run your project.

**Communicate**

If for some reasons, some parts of your patch doesn't work or require manual steps in order to work properly, just write it in your documentation file.

# Evaluation grid


**Malus points :**
* submission date deadline : -1 point per day late
* delivery zip file size : -1 point if more than 100 MB
* missing documentation or incomplete : -1 point
* some errors in PD console : -1 point
	
**Bonus points : (2 points)**
* atmosphere and consistency (all sounds work well together): 1 point 
* special noticeable concept (creativity) : 1 point

**Global points : (5 points)**
* commented patches : 2 points
* readability (subpatch and abstraction) : 2 points
* global balance of all sounds : 1 point 
	
**Points for spatialization and FX : (5 points)**
* Lateral localization : 2 point
* Distance localization : 1 point
* Reverberation : 1 point
* Underwater FX : 1 point
	
**Points per module : (10 points)**
* Map Toggle : 1 point
* Chest detector : 2 points
    * detector sound : 1 point
    * Helpful to find a chest easily : 1 point
* Soundscape : 2 points
    * at least one dynamic environment based soundscape : 1 point
    * at least two : 1 point
* Player sonification : 2 points
    * walk on ground : 1 point
    * at least one extra sonification : 1 point
* Music from the house : 1 points
* Animals sonification : 2 points
    * One animal type with one state : 1 point
    * At least one extra animal or state : 1 point

