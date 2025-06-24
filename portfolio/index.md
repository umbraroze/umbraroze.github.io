---
layout: default
title: Portfolio of Weird Code
permalink: /portfolio/
---

This part of the site is a showcase of random weird coding projects that
I've done over years, perhaps to illustrate the sort of programming
projects I do on my own. Not all of these projects are publicly
available (yet).


## Photo Importinator

> **Language:** Python  
> **Libraries/Frameworks:** exiv2  
> **Other Tools:** dnglab  
> **Website/repository:** Website, GitHub, Taiga.io

I was never quite happy with built-in image import tools that were
available in digital photo managers or DAMs, yet the ability to import
photos to my storage locations is pretty crucial thing to get right.
So, of course, I wrote my own tool for this!

## Photo Geo Scooper

> **Language:** Python  
> **Libraries/Frameworks:** exiv2, pykml
> **Website/repository:** Website, GitHub, Taiga.io

(Description...)

## TheremiDIMI

> **Language:** C++  
> **Libraries/Frameworks:** OpenCV, SDL3, Dear IMGUI, ...  
> **Website/repository:** GitHub

(Description...)

## Librariator

> **Language:** Ruby (main application), Python (desktop GUI tools)  
> **Libraries/Frameworks:** Ruby on Rails (Web/API), Qt/PySide (desktop GUI)  
> **Website/repository:** GitHub

This project of mine aims to be my personal solution to managing a
DVD/Blu-Ray collection, and I will probably expand it later to
also cover books. Making this one was pretty necessary, personally,
because apparently people lost interest in making solid personal
library management tools for regular users.

## Conman's Dictionary

> **Language:** C#  
> **Libraries/Frameworks:** Avalonia UI  
> **Website/repository:** GitHub

One of my hobbies is writing fantasy fiction, and what is fantasy fiction
without constructed artificial languages? For that purpose, I needed a
dictionary application.

This app has been basically my long-standing big hobby project for
trying to learn building productivity apps using Java desktop GUI
technologies - and later, the same in C#.

## XMMS InfoPipe

> **Language:** C  
> **Website/repository:** No longer up?

InfoPipe was a plugin for the Linux music player XMMS 1.x which
exposed its state as a named pipe. Every time another program
read from the named pipe, the plugin wrote out the information about
the current song and the player status. This was handy in the age
before the now prevalent Linux GUI app interop layers like D-Bus.

What was this handy for? Eeeh, I suppose a lot of people found it
handy for extracting the information about the currently playing
song for various display purposes. Everyone was fond of spamming their
current jam on IRC chats, and I guess I may have made the problem worse.
I made a script that feeds the current song title to text-to-speech
so I can just press a remote control button and the computer will speak
the name of the song, which was handy if I was listening to music
away from the computer.
