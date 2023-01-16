# Game Engines

I don't think I have the desire, time, or knowledge to write my own game _and_ engine so I need a game engine.

# Problem

Which game engine should I use?

## Amethyst :x:

[Amethyst](https://amethyst.rs/) is ... [dead](https://amethyst.rs/posts/amethyst--starting-fresh):
> We are officially halting development of Amethyst Engine.

## Bevy :x:

[Bevy](https://bevyengine.org/) is a data-driven ECS game engine, and from what I can gleam it is somewhat higher-level
than the other choices. It further reinforces this by having most (and ideally all) behavior inside individual "plugins"
that contain the individual feature areas, e.g. Windowing, Input. In fact your own game behavior also should be
developed as plugins.

The high-level is a concern for this effort because I am new to both Rust and game development -- but _not_ new to
software development -- and I can easily see frustrations due to impedance mismatches and hidden functionality.

## Caper :?:

[Caper](https://github.com/shockham/caper) is a minimalist game framework written in Rust. I don't think this would be
something to use directly, it might be something to crib from.

## Fyrox :?:

[Fyrox](https://fyrox.rs/) is very much a "full" fledged game engine, with it's own Scene graph editor, Windowing
toolkit, physics engine, scripting engine, plugin system, etc.

I think this may be the best approach (although I get a very weird vibe that this may be too much for what I want..)

## GGez :x:

[ggez](https://ggez.rs/) is based on the [Love](https://love2d.org/), which is designed to be used via Lua, which
worries me that the Rust API could be using Lua instead of the raw C++ engine underneath. More specifically, it won't be
easily obvious when it's using one vs the other.

## Godot Rust :?:

[Godot Rust](https://github.com/godot-rust/gdnative)
> provides high-level Rust bindings to the [Godot game engine](http://godotengine.org/).

## Macroquad :x:

[Macroquad](https://macroquad.rs/) is a game _library_ for Rust inspired by [raylib](https://github.com/raysan5/raylib).

The [GitHub page](https://github.com/not-fl3/macroquad)'s second line is rather worrying to me:
> macroquad attempts to avoid any Rust-specific programming concepts like lifetimes/borrowing, making it very friendly
> for Rust beginners. See the [docs](https://docs.rs/macroquad/0.3.0-alpha/macroquad/index.html).

Unfortunately the provided link doesn't say a whole more about _how_ it avoids using those concepts.

## Nannou :x:

[Nannou](https://nannou.cc/) isn't a "game engine", it's
> An open-source creative-coding framework for Rust

Which unfortunately is too low level for my needs.

## Oxygengine :x:

[Oxygengine](https://psichix.github.io/Oxygengine/) is a 2D only game engine with a focus on the Web. It is also rather
new, hence I don't think it's a serious contender at the moment.

## Piston :x:

[Piston](https://www.piston.rs/) looks rather simple, and the blog posts on the main page aren't even loading...pass!

## raylib-rs :x:

:x:
[raylib-rs](https://github.com/deltaphc/raylib-rs) are Rust bindings for for [raylib](http://www.raylib.com/).

The idea of a lower level, hands-off library like raylib has some appeal, I believe it does not expose _any_ management
of resources, as stated on the GitHub page:
> Resources are automatically cleaned up when they go out of scope ... _This is essentially RAII._

Emphasis mine.

## Rust-SDL2 :/:

[Rust-SDL2](https://github.com/Rust-SDL2/rust-sdl2) are Rust wrappers around the C API
for [Simple DirectMedia Layer (SDL) 2.0](http://www.libsdl.org/). SDL is a _complete_ development library -- graphics,
sound, input, etc.

## Scion :x:

[Scion](https://github.com/grzi/scion) is a very new game engine that seems to be more of a learning journey for the
author than something others should depend on. While I applaud the goals it is definitely not something appropriate for
my current needs.

## Vulkano :?:

[Vulkano](https://github.com/vulkano-rs/vulkano) is a Rust wrapper
around [the Vulcan Graphics API](https://www.khronos.org/vulkan/), which is itself a graphics library intended to
supersede OpenGL.

This may be lower level than desired, and it only deals with graphics not sound or input or any of the other things I'd
need.

# Appendix

## Audio Libraries

* [cpal](https://github.com/RustAudio/cpal) - Audio playback library (usually combined with something like Symphonia).
* [Symphonia](https://github.com/pdeljanov/Symphonia) - Audio decoding and media mixing library.

## Graphics Libraries

* [glyph-brush](https://github.com/alexheretic/glyph-brush) - Fast text rendering and caching.
* [image-rs](https://github.com/image-rs/image) - Image processing library written.
* [keyframe](https://github.com/HannesMann/keyframe) - Keyframe library.
* [pixels](https://github.com/parasyte/pixels) - A tiny hardware-accelerated pixel frame buffer.
* [wgpu](https://wgpu.rs/) is a pure-Rust graphics library.

## Input Libraries

* [gilrs](https://gitlab.com/gilrs-project/gilrs) - Game input library.

## Procedural Libraries

* [modulator](https://github.com/apessino/modulator) - Allows modulating -- i.e. altering -- objects as they move to
  their destination with a kind of randomness that gives them a more "realistic" or at least lock-step look.
* [noise-rs](https://github.com/razaekel/noise-rs) - Generates noise for textures and graphics.
* [sprite_gen](https://github.com/tversteeg/sprite-gen) - Library for procedurally generating 2D sprites.
* [texture-synthesis](https://github.com/EmbarkStudios/texture-synthesis) - API for Multiresolution Stochastic Texture
  Synthesis, a non-parametric example-based algorithm for image generation.

## Tool Libraries

* [asset_manager](https://github.com/a1phyr/assets_manager) - Filesystem abstraction for loading and caching resources.
* [modio-rs](https://github.com/nickelc/modio-rs) - Integrates [Mod.io](https://mod.io/) support.
* [ogmo3](https://github.com/17cupsofcoffee/ogmo3) - Read and write projects and levels built with Ogmo Editor 3.
* [rs-tiled](https://github.com/mapeditor/rs-tiled) - Reads maps created with Tiled.

## Windowing Libraries

* [tao](https://github.com/tauri-apps/tao) - Cross platform windowing library
* [winit](https://github.com/rust-windowing/winit) - The most common pure-Rust low-level windowing library. It _only_
  handles window creation and event listening, it doesn't draw anything on the window.

## Miscellaneous Libraries

* [game_loop](https://github.com/tuzz/game-loop) - A frame-rate-independent game loop.
* [nalgebra](https://nalgebra.org/) - Linear algebra library.
* [Rapier](https://rapier.rs/) - 2D/3D physics library.
* [weasel](https://github.com/Trisfald/weasel) - A customizable battle system for turn-based games.

## Resources

* [Are we game yet?](https://arewegameyet.rs/) - Browsable collection of tools for game development on Rust.
* [Learn wgpu](https://sotrh.github.io/learn-wgpu/)

## Tools

* [Dust3D](https://dust3d.org/) - A simple 3D modeling tool.
* [Mod.io](https://mod.io/) -
* [Tiled](https://www.mapeditor.org/) - Open source, easy to use, and flexible level editor.
* 
