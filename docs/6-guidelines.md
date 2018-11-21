# Guidelines

## Write documenation

It could be helpfull to write a documentation about your patch : how it works, is there some bugs or limitations, ...

## Comment your patch

It's important to add comment in your patch, it helps other developer or yourself after month of pause in order to remember what you've done.

## Have a readable patch

The more connections you have, the less readable your patch is.

To overcome this situation, group some hardwired parts in subpatches or abstractions.

## Ensure proper initialization

Use loadbang message to initialize some constants, the final patch should work without any manual actions.

## Message ordering

By default, messages are triggered depending on wires creation time, you can't based ordering on this because it could break your patch when modifyng it.

To overcome this problem, always use trigger object (t) to enforce trigger ordering.

## Minimize size

Try to minimize project size especially audio files by including only required ones.

The project ZIP file shouldn't exeed 100 MB.

## Include all dependencies

Include all original pd files, whenether you modified them or not.

Include all your pd own files required to run your project.

## Communicate

If for some reasons, some parts of your patch doesn't work or require manual steps in order to work properly, just write it in your documentation file.

