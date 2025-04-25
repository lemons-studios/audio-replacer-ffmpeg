# audio-replacer-ffmpeg

This repository contains an extremely scuffed, non-standalone and standalone versions of ffmpeg for windows that only contains common audio libraries. I took the configuration options from the gyan.dev essentials build and compiled with msys2

As indicated by the name of the repository, This is meant for [Audio Replacer](https://github.com/lemons-studios/audio-replacer), an audio dubbing tool that uses ffmpeg for custom user-defined audio filters that get applied after recording. The essentials build from Gyan.dev contains many video tools that simply aren't needed for the project, and causes the size of the executable to baloon to 
85.4MB. My build has reduced the size to 38.8MB (a file savings of 46.6MB!)

These executables are ONLY for Windows x64 (most computers). If you want to use my configuration but compile for linux or some other cpu architecture instead, please see my configuration below

You are free to download and use my build for any of your projects, but if you plan to redistribute, please make sure to add some sort of credit to the gplv3 license, or else you may get in some legal trouble

In the future, I may create a github workflow to automatically update this repository, but for now, I will manually be uploading new versions as they come up (and if I remember to compile for those versions when they release)

## Configuration used:

```sh
--enable-cross-compile \
--target-os=win64 \
--arch=x86_64 \
--cross-prefix=x86_64-w64-mingw32- \
--enable-gpl \
--enable-version3 \
--enable-static \
--disable-w32threads \
--enable-libgme \
--enable-libopenmpt \
--enable-libopencore-amrwb \
--enable-libvo-amrwbenc \
--enable-libgsm \
--enable-libopencore-amrnb \
--enable-libmp3lame \
--enable-libopus \
--enable-libspeex \
--enable-libvorbis \
--enable-librubberband
```

You'll want to remove ```--enable-cross-compile``` and ```cross-prefix=x86_64-w64-mingw-32-``` if you are not compiling on msys2. Replace the values of ```target-os``` and ```arch``` to the operating system you are compiling for and the cpu architecutre(s) you are compiling for respectively
