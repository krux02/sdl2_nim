sdl2_nim 2.0.6.0
================

sdl2_nim is a wrapper of the SDL 2 library for the Nim language.

* sdl2_nim docs online: https://vladar4.github.io/sdl2_nim/
* SDL homepage: http://www.libsdl.org/
* Nim homepage: http://nim-lang.org/

You need to have SDL 2 dynamic libraries installed on your system.

Includes:
---------
* SDL 2.0.6
* SDL_gfx 1.0.1
* SDL_gpu 0.11.0
* SDL_image 2.0.1
* SDL_mixer 2.0.1
* SDL_net 2.0.1
* SDL_ttf 2.0.14

What does not implemented here:
-------------------------------

* OpenGL headers (use [opengl](https://github.com/nim-lang/opengl) lib instead)

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
**Q**: Why it exist if there's official [nim-lang/sdl2](https://github.com/nim-lang/sdl2) repository?

**A**: This wrapper is actually was created before the official (Aug.2013 vs. Mar.2014). It may be, I wouldn't make it if there was other wrapper at the time.

**Q**: How it is different from the official wrapper?

**A**: Obviously, it can't be *much* different, as they both are wrappers for the same library, but what comes to mind:

* This one is fully documented, nim-style, with the generated documentation as a bonus;
* I personally created a series of highly commented examples for almost every aspect of the library and its "satelites" (gfx, ttf, etc.);
* Design decisions that I thought made more sence than official one's (like Event type through {.union.} vs. evConv template with casting; naming sceme closer to the original sdl2, etc.);
* Source files' structure is closely following the original library.

**Q**: Why should I use this one vs. the official?

**A**: No reason. It's a question of preference.


CHANGELOG:
==========

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

