This is a list of general information that should be known regarding Chunithm's file format, as well as this collection of research. This includes a list of files of interest, the general overview of them, and links to additional documentation if available, as well as meta information about this research document.

# Meta

* Chunithm makes frequent use of ``.xml`` files. This document will, for the sake of simplicity, assume that you understand the basic format of ``.xml`` files.
* References to "music" and "song" will refer to the files in the ``music`` folder, which includes ``Music.xml``, as well as the chart files. References to ``audio`` will refer to the files in the ``cueFile`` folder. 

# Folders

Chunithm's method of receiving updates involves storing the new information in separate "AXXX" folders, found in ``root¥app¥data``. These folders will have varying numbers replacing the Xs depending on the update. Any references to "AXXX" in this document will refer to an unspecified ``A`` Folder. It is worth noting that, while songs usually have their complementary files (audio, jackets, rights) in the same ``A`` folder, it is possible that they are also in other folders. At the moment, it is assumed that newer AXXX folders will overwrite the older AXXX folders' data in terms of being in-game, although the older files will remain intact, however this is not confirmed. It is worth noting that Chunithm's updates will regularly remove certain songs that were prexisting, usually from rights expiring. It is also worth noting that the major updates for Chunithm that change branding and add new features (for example, Amazon to Crystal, or Crystal to Paradise) will not involve new AXXX files, instead condensing them all into the A000 folder. The .exe in ``root¥app¥bin`` may also be overwritten, among other binaries.

# File Types

This is a list of file types of interest, the locations of them, and links to additional info if necessary. This is **not** an extensive list, some files that are not of interest will not be included.

## Audio Files

Audio files for music are found in ``root¥app¥data¥AXXX¥cueFile¥cueFileXXXXXX``. The ID of the cueFile can be found in the XML ``<cueFileName>`` tag of the ``Music.xml`` file in the same folder as the chart files for the song of interest. More often than not, these files share the same ID as their corresponding music ID. These files are encoded in the proprietary [CRIWARE ADX2 audio format](https://en.wikipedia.org/wiki/ADX_(file_format)), in pairs of ``.awb`` and ``.acb`` files. These files can be played and converted by the [vgmstream](https://vgmstream.org/) library, specifically the component for [foobar2000](https://www.foobar2000.org/). Typical audio formats cannot be encoded into the ADX2 file format through freeware means, although CRIWARE should be able to encode these files.

## Jacket Files

Jacket files, otherwise known as the images that are associated with the song, are found in the same folder as the chart files in a ``.dds`` (DirectDraw Surface) file format, which can be opened in software such as [GIMP](https://www.gimp.org/). Jacket files are always in a resolution of 300x300.