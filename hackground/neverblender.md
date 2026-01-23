---
layout: default
title: NeverBlender
permalink: /hackground/neverblender
---

([Back to the Hackground](/hackground/))

# NeverBlender: A look back

**NeverBlender** was a Python script that allowed exporting
[Neverwinter Nights][wikipedia-nwn] format Bioware MDL files from
[Blender][blender].

It supported exporting basic model geometry and texture UV maps.
It also allowed keeping MDL-specific settings in a text block in model file.

The fancy future direction would have been to support animation
exporting and some of the other features supported by MDL file format.
At the time, the prefered 3D modeling program for making MDL files was
Discreet's Gmax (a cut-down freeware version of 3DS Max), and it only
supported a single timeline, which sounded janky because Blender supported
multiple animations.

Git-ified version of the
[original NeverBlender repository][neverblender-codeberg] is available
in Codeberg.

It was originally developed between 2003–2006, and as such, you'll
probably have no luck getting it running on modern versions of Blender.

I currently have no ambitions in getting back to developing it. I was
not a good Python developer at the time, and people who contributed to
the code did Cleverer Things I Was Able To Do. But then again, Gmax was
discontinued by Autodesk, so maybe there's interest in this again...?


[wikipedia-nwn]: https://en.wikipedia.org/wiki/Neverwinter_Nights_(2002_video_game)
[blender]: https://www.blender.org/
[neverblender-codeberg]: https://codeberg.org/umbraroze/NeverBlender
