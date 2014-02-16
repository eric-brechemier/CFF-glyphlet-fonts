The aim of this repo is to create a small JavaScript thing that
can turn outline data for "a letter" into a tiny OpenType font
using CFF for the glyph model (because CFF does Type2 charstrings,
which model curves with cubic beziers, unlike TFF, which can only
do quadratic beziers. Which are properly nonsense for design work).

The idea is to supply the builder function with a structure similar
to an SVG (compound) path, and get a BASE64-encoded OTF back for
use in an @font-face src property. Define outline, load in, apply
to single letter.

Why is this useful? What a silly question.

 - Pomax
 
 live version: http://pomax.github.io/CFF-glyphlet-fonts