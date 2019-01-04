## zTracker

zTracker is a win32 only MIDI tracker/sequencer modeled after Impulse Tracker. 

The original developer ( @cmicali ) no longer maintains this project, and the source is archived here.


## Features

1:1 copy of Impulse Tracker interface
64 track sequencer with variable 32-256 rows/pattern, 256 total patterns
easy use of multiple machines across multiple MIDI devices/interfaces
rock solid timing that tested as good as cubase (3/496ppqn error)
load/save compressed .zt files
volume/effect curve drawing in pattern editor
IT importing (thanks to lipid)
auto sync via midi-clock
.mid export
intelligent midi-in w/ slave to external sync
planned: realtime pattern player (a-la-rebirth)

## Links

zTracker on SourceForge: http://ztracker.sourceforge.net
zTracker prime on GitHub (maintained by @m6502): https://github.com/m6502/ztrackerprime
zTracker for Mac on GitHub ("maintained" a.k.a. severely unfinished by @esaruoho): http://github.com/esaruoho/ztracker_mac/tree/master/skins

## Old building instructions by Daniel Kahlin

### Building ztracker

Written by Daniel Kahlin <tlr@users.sourceforge.net>

Required software:
- Microsoft Visual Studio C++ 6.0
- SDL 1.2.0 or later installed in your MSVC include and library path.
  (can be found at http://www.libsdl.org/)
- zlib 1.1.3 or later installed in your MSVC include and library path (lib\dll32).
  (can be found at http://www.winimage.com/zLibDll/ or at http://www.zlib.org/)
- libpng 1.0.12 or later installed in your MSVC include and library path
  (can be found at http://sourceforge.net/projects/libpng/)

Additionally, if you want to build releases, these must be in your path:
- InfoZip (http://www.info-zip.org/pub/infozip/)
- UPX - the Ultimate Packer for eXecutables (http://upx.sourceforge.net/)

If you want to make modifications to the graphics, you need:
- itf.exe for editing the font file.  (itf v1.61 can be found under
  required devel packages) 
- Adobe Photoshop or similar for editing the graphics in general.

### Building Source Releases

ztracker's source code is cvs based.  A release is built from the contents of the cvs archive at a point of time.  A release tag is set, the whole cvs tree exported and then
finally compressed into a .zip file.

### Building Binary Releases

Binary releases are built from the corresponding source release.

1. From the zt.dsw workspace build zt.exe as release.
2. Change the active project to ztconf.exe and build that as release.
3. Change the active project to ztskin.exe and build that as release aswell.
4. From a MS-DOS prompt, cd to the source directory and run buildrelease.bat.
   (You may want to edit the archive name)
5. Done!
