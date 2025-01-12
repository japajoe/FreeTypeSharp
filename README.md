# FreeTypeSharp
A slightly modified version of [the original FreeTypeSharp](https://github.com/ryancheung/FreeTypeSharp)

I've made some changes because I could not get the orignal Nuget package to work on my Linux installation, it kept resolving the built-in libfreetype on my system, which is a bit out of date. When I finally managed to load the right library, it could not find the right version of `libc`. 

# Changes I've made
- Removed the native library resolving at runtime.
- Renamed the native libraries so they can not possibly collide with system libraries.
- Recompiled the native library for Linux so it works at least on my Debian installation.
- Removed all the non-desktop target platforms because I do not feel like maintaining those.

# Installation
```
dotnet add package JAJ.Packages.FreeTypeSharp --version 3.0.3
```

# Note
I am not trying to replace the original package, I was simply in need of an immediate solution for my unique situation. All credits go to [Ryan Cheung](https://github.com/ryancheung/FreeTypeSharp).