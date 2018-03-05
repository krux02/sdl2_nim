sdl2_nim 2.0.7.1
================

sdl2_nim is a wrapper of the SDL 2 library for the Nim language.

* sdl2_nim docs online: https://vladar4.github.io/sdl2_nim/
* SDL homepage: http://www.libsdl.org/
* Nim homepage: http://nim-lang.org/

You need to have SDL 2 dynamic libraries installed on your system.

Includes:
---------
* SDL 2.0.7
* SDL_gfx 1.0.1 (fully 1.0.3 compatible)
* SDL_gpu 0.11.0
* SDL_image 2.0.2
* SDL_mixer 2.0.2
* SDL_net 2.0.1
* SDL_ttf 2.0.14
* SMPEG 2.0.0

OpenGL:
-------

There are no OpenGL headers here, currently there are two options you can use.
* The official [OpenGL](https://github.com/nim-lang/opengl) binding. The advantage here is that it only loads what you actually use. But the disadvantage is, that it crashes the program if it can't find a function that you use in your code. No error handling possible.
* [glad](https://github.com/Dav1dde/glad) is a binding generator that also happens to support Nim. The advantage is that you can specify exactly what subset of OpenGL you want generated. And you can check at runtime if certain extensions could be loaded.

Versioning scheme:
------------------
```
a.b.c.d

a.b.c - underlying SDL2 version
d     - sdl2_nim revision
```

----------------------------------------

FAQ:
====
**Q**: Why does this exist if there's an official [nim-lang/sdl2](https://github.com/nim-lang/sdl2) repository?

**A**: This wrapper actually was created before the official (Aug. 2013 vs. Mar. 2014). Maybe I wouldn't have made it if there already was a wrapper at the time.

**Q**: How is it different from the official wrapper?

**A**: Obviously, it can't be *much* different, as they both are wrappers for the same library, but what comes to mind:

* This one is fully documented, nim-style, with the generated documentation as a bonus;
* I personally created a series of highly commented examples for almost every aspect of the library and its "satelites" (gfx, ttf, etc.);
* Design decisions that I thought made more sense than official one's (like Event type through {.union.} vs. evConv template with casting; naming sceme closer to the original sdl2, etc.);
* Source files' structure is closely following the original library.

**Q**: Why should I use this one vs. the official?

**A**: No reason. It's a question of preference.

**Q**: Where could I find smpeg2.dll?

**A**: It is distributed within SDL2_mixer 2.0.1 and older builds.


CHANGELOG:
==========

**v2.0.7.1**
* added SMPEG 2.0.0
* updated examples, added smpeg example
* added some convenience templates
* bugfixes and documentation updates

**v2.0.7.0**
* updated to SDL-2.0.7, SDL_image-2.0.2, and SDL_mixer-2.0.2 (see [changelog](https://github.com/Vladar4/sdl2_nim/blob/master/CHANGELOG-2.0.7.md))
* updated documentation

**v2.0.6.1**
* events iterator and memory allocation procedures (by [krux02](https://github.com/krux02))
* tupleToColor converters
* various bugfixes and documentation updates

**v2.0.6.0**
* updated to SDL2-2.0.6 (introduced no breaking changes for 2.0.5, see [changelog](https://github.com/Vladar4/sdl2_nim/blob/master/CHANGELOG-2.0.6.md))
* added SDL_GPU 0.11.0 (kudos to [Serenitor](https://github.com/Serenitor))
* minor bugfixes and documentation updates

**v2.0.5.0**
* changed versioning system to reflect the underlying SDL2 version
* fixed uint8 emum bug
* fixed pixels.nim templates
* fixed windows threads
* various minor improvements
* documentation enhancement

**v0.96 beta**
* added sdl_syswm.nim
* updated SDL2_ttf to v2.0.14
* added more SDL2 examples
* Nim 0.14.0 adaptation
* updated to SDL2-2.0.5

**v0.95 beta**
* Nim 0.12.0 adaptation
* updated to SDL2-2.0.4
* added SDL2-gfx
* type-related fixes
* different fixes
* documentation fixes and formatting
* added html documentation
* added SDL2 examples

**v0.9 alpha**
* added SDL2-mixer
* different fixes

**v0.8 alpha**
* added haptic.nim
* added SDL2-image
* different fixes

**v0.7 alpha**
* added SDL2-net
* added event convertion templates
* different fixes
