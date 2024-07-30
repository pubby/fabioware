# FabioWare

This is a community project to create a WarioWare inspired game for the NES 
using the NESFab programming language.

## How to make a microgame

1. Download the files on this GitHub, along with [NESFab](https://github.com/pubby/nesfab).
2. Create a new folder in the `microgames/` directory. Its name should follow
the pattern: `username_gamename`.
3. Copy `microgames/template.fab` to this folder and rename it to `microgame.fab`.
This file contains directions inside - just edit it!
4. Edit `fabioware.cfg` and `microgames_list.fab` to add your microgame.
5. Compile with the `nesfab` program.
6. Play your new `fabioware.nes` file!

## Tips for graphics

Microgames often involve full-screen graphics without much scrolling or repetition.
To create these, I like to draw the graphics in a generic image editor like [GIMP](https://www.gimp.org/),
then convert them into a NES-compatible format using programs like [NEXXT](https://frankengraphics.itch.io/nexxt)
or [makechr](https://github.com/dustmop/makechr).

For NEXXT, you first must convert your image into a palettized BMP file.
In GIMP, you can do this with `Image -> Mode -> Indexed` and setting the color count to 4,
then saving as a `.bmp` file. Then in NEXXT you can do `File -> Import -> Import BMP` and it should load
your graphics. The final step is to save the `.chr` using `Patterns -> Save 8k`,
and the nametable using `Canvas -> Save as Screen`.
