---
layout: post
title:  "Inline vs. Inline-Block"
date:   2016-01-18
categories: css
---

### Display = Block

There are many ways use the display property in CSS. However, there is
much confusion about the difference between inline and inline-block: To
understand the difference between inline and inline block, it is first
important to understand that HTML elements have difficult display
values!

For instance, a (paragraph) element is a block level element by default.
This means that if it were in code it would look like
``` display: block ```. To make it easier for me, I think of a block element
like a block in the game Tetris. To make a full block in Tetris, you
have to fill up the whole entire line. A block level element takes up
the entire line. So if you stack two paragraphs next to each other, they
will display one on top of the other.

### Display = Inline

If you have just started to learn HTML, you probably know by now that
you can use certain elements to select code inside of paragraphs, like
span, em, b, etc. These elements are inside of the block so they run
“inline” with the block. These elements only take up as much space as
they need to, unlike block level elements. However, what if you want to
take two paragraphs and stack them up side by side?

### Display = Inline-Block

Both of the examples mentioned above do not require that you change the
display property in CSS because they are all set that way by default.
However, let’s say you want to take two block level elements (such as a
paragraph), and set them side by side so they do not take up the entire
“Tetris Block”. You can set the display property to the value of “Inline
block”! This is a great alternative to floating an element. However, it
is critical that if you use inline block to display two paragraphs
together on the same line that you set the vertical align property to
the value of top(look in my example). This will make certain that both
paragraphs align to the top instead of the bottom.

![Inline block example]({{site.baseurl}}/images/inline-block.png)
