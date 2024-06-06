---
public: true
title: Stoke
date: 2013-10-15
slug: stoke
url: false
alive: false
author: Andrew Lovett-Barron
image: ../assets/blog/old/pasted-image-20231128130125.png
description: Interactive Projection Mapped Installation
categories:
  - project
tags:
  - art
  - installation
  - Embedded
  - Cplusplus
feature: true
modified: 2024-06-06T21:09
---

<iframe src="https://player.vimeo.com/video/80308354?h=126a7dc1c9" width="640" height="360" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
<p><a href="https://vimeo.com/80308354">Stoke</a> from <a href="https://vimeo.com/relaystudio">Relay Studio</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

Stoke was an interactive installation I was commissioned to create for OCAD University's Nuit Blanche 2013 great hall space. The goal was to create the experience of being by a campfire revel within an otherwise stark architectural space. This was done by casting the revel outwards, and bringing life to the envisonment through human activity.

Stoke was a consisted of dozens of "trees" that served as projection serfaces for an array ot projectors casting out from the center of the installation. Tthe projectors and trees were hung from the ceiling of OCADU's great hall.

In the center of the trees, a dias sat with a large subwoofer underneath and visitors were enticed to climb the dias and dance.

A C++ program written in OpenFrameworks used openCV to track participant movement, and subdivided the movement into diffesent sectors. Where there was more movement, that part of the fire burned brighter against the trees. This meant that someone could "cast" their dance in a particular direction.

Alongside the visuals, a generative soundtrack played via Ableton live, controlled through OpenSoundControl fron the C++ app.

The installation was done with the collaboration of Adam Carlucci, Nick Crampon, and Eliot Callahan. Special thanks to Marissa Neave, Jeff Zoeller, Michaud Garneau, Car Martin, and Dave Clark. Documentation by Justin Black.

![](../_assets/pasted-image-20231128130125.png)
