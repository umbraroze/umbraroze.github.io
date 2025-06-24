---
layout: default
---

Welcome!

## So who is this?

I'm **Rose Midford**, just another developer from Finland!
Motto: *Be Weird, Do Code.*

Well, OK, that's just the Notorious Hacker Alias.
The boring name is Urpo Lankinen.

## What will be here?

I used to have an actual personal website, but it's... in a bit of a
state right now. This site will be specifically about my code
projects. Helps me focus, I hope.

## Code? Where??

* **[My GitHub profile](https://github.com/umbraroze)**: This is where
  some of my projects live. Probably the more bigger and more
  interesting projects end up here.
* **[My Codeberg profile](https://codeberg.org/umbraroze)**: This is
  where some others of those projects of mine live.  These are
  probably old, hacky, crusty, random and experimental. Or
  combinations of those things. Or all of those things!

## Current project sites

These are the sub-sites that get built out of my GitHub repositories.

* **[PhotoFlow](/PhotoFlow/)**:
  Photography workflow scripts.
  They importinate.
  They geolocate.
  They do minor stuff.
* **[Conman's Dictionary](/ConmanDictionary/)**:
  A dictionary app for constructed language enthusiasts.
  Also a massive C# desktop development learning exercise.

## Rants, Ramblings and Reminiscings

* **[The Hackground](/hackground/)**:
  I had various weird problems of technological nature. I wanted to
  solve them through technology. Weirdly.
  *Or:* I just wanted to make something weird.
  Point is, things got weird and wonderful.

## Recent blog posts

<ul>
  {% for post in site.posts limit:5 %}
  <li><a href="{{post.url}}">{{post.title}}</a> ({{ post.date | date:"%d %B %Y" }})</li>
  {% endfor %}
</ul>

([See the blog...](blog/))

## Upcoming

* A "portfolio" of sorts will eventually be here.
* Processing hacks, including:
  * Visualisation stuff
  * A weird music insturment control thingie
* Janky hardware jank-hacks with Raspberry Pi
* Some retro projects with Turbo Pascal 'n' stuff
* Old Stuff that *might not be* as good as I remember it was
