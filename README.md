ripcd
=====

`ripcd` is a wrapper around [whipper] that I use to rip my CDs to FLAC.

[whipper]: https://github.com/whipper-team/whipper

Usage
-----

Before your first run:

    $ whipper drive analyze
    $ whipper drive list

Then lookup your drive's offset in the [AccurateRip offset database], before running:

    $ whipper find -o <offset>

Then, to rip each disc:

    $ ./ripcd

[AccurateRip offset database]: http://www.accuraterip.com/driveoffsets.htm

Features
--------

### Choosing the CD's release

If multiple releases of the CD you're ripping are found in the MusicBrainz database, `whipper` will choose one for you by default. I'd rather choose the right one myself, but don't want to have to remember to pass the `--prompt` switch every time I run `whipper cd rip`.

So `./ripcd` always passes the `--prompt` switch.

### Setting the genre

I've got `whipper` set to retrieve metadata from MusicBrainz. I'm finding that some of my CDs don't have a genre tag defined in the MusicBrainz database. `ripcd` asks me to define the genre myself.

Notes
-----

While recent versions of `whipper` support downloading album art, the versions that ship with Debian or via the Docker image haven't yet been updated.

I'm not too bothered about this, as I download album art with with https://beets.io instead. Beets is a fully fledged music library management (and tagging) tool, and is well worth checking out.
