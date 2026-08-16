---
layout: page
site_section: hackground
title: "XMMS InfoPipe"
short_title: "XMMS InfoPipe"
permalink: /hackground/xmms-infopipe
---

**XMMS InfoPipe** was a plugin for an early Linux media player,
[XMMS][wikipedia-xmms], that basically exposed the internal state of
the player to the other applications running on the system.

It created a named pipe, e.g. `/tmp/xmms-info_yourusername.0` (and a
symbolic link `/tmp/xmms-info`), from which you could read the
player's current state:

```console
$ cat /tmp/xmms-info
XMMS protocol version: 2467
InfoPipe Plugin version: 1.3
Status: Playing
Tunes in playlist: 252
Currently playing: 116
uSecPosition: 109201
Position: 1:49
uSecTime: 238288
Time: 3:58
Current bitrate: 128000
Samping Frequency: 44100
Channels: 2
Title: The Laziest Men on Mars - Invasion of the Gabber Robots
File: /usr/local/lib/music/mp3s/sites/mp3.com/techno/Invasion_of_the_Gabber.mp3
```

## History

Unix and Linux software is all about modularity and programs talking
to each other, right? Unfortunately, back in the day, GUI-based
applications were an exception: they just ran in their own isolated
spheres. If you ran a GUI music player, other programs couldn't find
out what it's playing right now.

So, back in the day, I asked "_why_ can't I just read the internal
state of XMMS?" and I had to write a plugin to do so all by myself.
Basically, XMMS InfoPipe was intended to make it much easier to write
programs that read the XMMS state and do interesting things with that
information. I wrote it because I thought that sort of functionality
would be neat as hell.

It was not a very beautiful plugin, I admit. I wasn't very good at
programming in C at the time (and not _much_ better these days). The
XMMS API was also extremely limited in terms of what information the
plugins had access to; for example, plugins could only read the
filename and title of the currently playing song as it appeared in the
player. If you wanted, for example, more granular file tag information
(title/artist/album etc), you had to fetch the file path, then extract
it out of that file yourself.

Luckily, things have gotten significantly better. Currently, many
Gnome and KDE apps use D-Bus to exchange information between each
other. In other words, all applications, even command-line programs or
applications run by web servers, can talk to the graphical
applications just fine and find out their internal state. If other
programs want to sniff out what music you're playing, all they need to
do is to ask your music player nicely. And they can even control the
player!

This was the first piece of software that I've so far written that
ended up being kind of a word-of-mouth run-away success. It even ended
up as [an official package in Debian][debian] (until XMMS stopped
being maintained at upstream and, as a whole, was eventually put out
of its misery by Debian too).

## Applications

So you can read the music player state from an external program. What
can you do with this information?

For some reason, it was obviously incredibly popular to put the
information about currently playing songs to webpages. There were a
few PHP scripts to do this.

I also saw more than a few IRC client scripts that were no doubt used
to relentlessly spam the channels back in the day.

### The late night hack

Just as an fun example of what you could do, consider this tale.

One late night, I was listening to music, using an infrared controller
that controlled XMMS through the [Linux Infrared Remote Control][lirc]
system.

Now, it was late at night, there was some new music in the playlist, a
weird song had just started playing, and I had no idea what it was
called.

I wanted to stay in the bed and didn't want to go back to the computer
all the time to check what the heck these songs were called. So, I thought
it would be cool if XMMS could identify those songs via speech.

So, back to the computer, actually. A few moments of late-night Perl
tinkering later, I had a script that read XMMS state via InfoPipe and
fed it to [Festival][festival]. Then, in LIRC, I bound the script to
the "Info" button on the remote.

Back to bed, hit play. Weird song starts playing. Hit pause, hit
info. Hear the song title. Good. Hit pause to resume. Big problem
solved!

## Downloads

**NOTE:** It goes without saying that this software is totally
unmaintained, and by far, **none** of this stuff is guaranteed to
build on modern Linux systems. _AT ALL._ XMMS itself has probably been
massively broken for a long time, so don't try to actually build these
things if you value your sanity.

Also, I originally used CVS for versioning the code. Badly. The
converted Git repository is what it is.

Also, I apparently had *hella* irritating writing style back in the day.
(...not to even mention the coding style. Yikes!)

That said:

* The [archived code repository][repo] is available for browsing via Codeberg.
* The [final release, 1.3][rel-1-3], is available in Codeberg releases.

The file `xmms-infopipe-1.3.tar.gz` contains the last official release
code, while `xmms-infopipe-garbage.zip` contains some additional text
tidbits in HTML format, and random patches and additions that never
got added to InfoPipe properly.

[wikipedia-xmms]: https://en.wikipedia.org/wiki/XMMS
[debian]: http://archive.debian.net/woody/i386/xmms-infopipe
[lirc]: http://www.lirc.org/
[festival]: http://www.cstr.ed.ac.uk/projects/festival/
[repo]: https://codeberg.org/umbraroze/xmms-infopipe
[rel-1-3]: https://codeberg.org/umbraroze/xmms-infopipe/releases/tag/rel-1-3
