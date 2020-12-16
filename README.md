ripcd
=====

`ripcd` is a wrapper around [abcde] that I use to rip my CDs to FLAC.

[abcde]: https://abcde.einval.com/wiki/

Features
--------

### Multi-disc album assistance

`abcde` supports ripping multi-disc albums to a single folder, appending "CD 1" (etc) to the metadata and prefixing the disc number to the filenames (e.g. "101 Track Title.flac").

You have to remember to tell `abcde` that you're ripping a disc from a multi-disc album with the `-W` switch, and I find that I forget, leading to time wasted re-ripping CDs once I've realised my error.

So `ripcd` will prompt you for the disc number at the outset.

### Setting the genre

I've got `abcde` set to retrieve metadata from MusicBrainz. I'm finding that some of my CDs don't have a genre tag defined in the MusicBrainz database. `ripcd` asks me to define the genre myself.
