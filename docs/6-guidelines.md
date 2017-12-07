# Guidelines

## Write documenation

It could be helpfull to write a documentation about your patch : how it works, is there some bugs or limitations, ...

## Comment your patch

It's important to add comment in your patch, it helps other developer or yourself after month of pause in order to remember what you've done.

## Have a readable patch

The more connections you have, the less readable your patch is.

To overcome this situation, group some hardwired parts in subpatches or abstractions.

## Message ordering

By default, messages are triggered depending on wires creation time, you can't based ordering on this because it could break your patch when modifyng it.

To overcome this problem, always use trigger object (t) to enforce trigger ordering.

