# audio-replacer-ffmpeg

This repository contains an extremely scuffed, non-standalone version of ffmpeg for windows that only contains common audio libraries. I took the configuration options from the gyan.dev essentials build and compiled with msys2

As indicated by the name of the repository, This is meant for [Audio Replacer](https://github.com/lemons-studios/audio-replacer), an audio dubbing tool that uses ffmpeg for custom user-defined audio filters that get applied after recording. The essentials build from Gyan.dev contains many video tools that simply aren't needed for the project, and causes the size of the executable to baloon to 
85.4MB. My build has reduced the size to 38.8MB (a file savings of 46.6MB!)

You are free to download and use my build for any of your projects, but if you plan to redistribute, please make sure to add some sort of credit to the gplv3 license, or else you may get in some legal trouble

In the future, I may create a github workflow to automatically update this repository, but for now, I will manually be uploading new versions as they come up (and if I remember to compile for those versions when they release)
