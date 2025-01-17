# HD Graphics

It's possible to provide alternative HD-Graphics within mods. They will be used if any upscaling filter is activated.

## Preconditions

It's still necessary to add 1x graphics as before. HD graphics are seperate from usual graphics. This allows to partitially use HD for a few graphics in mod. And avoid handling huge graphics if upscaling isn't enabled.

Currently following scaling factors are possible to use: 2x, 3x, 4x. You can also provide multiple of them (increases size of mod, but improves loading performance for player). It's recommend to provide 2x and 3x images.

If user for example selects 3x resolution and only 2x exists in mod then the 2x images are upscaled to 3x (same for other combinations > 1x).

## Mod

For upscaled images you have to use following folders (next to `sprites` and `data` folders):
- `sprites2x`, `sprites3x`, `sprites4x` for sprites
- `data2x`, `data3x`, `data4x` for images

The sprites should have the same name and folder structure as in `sprites` and `data` folder. All images that are missing in the upscaled folders are scaled with the selected upscaling filter instead of using prescaled images.

### Shadows / Overlays

It's also possible (but not necessary) to add HD shadows: Just place a image next to the normal upscaled image with the suffix `-shadow`. E.g. `TestImage.png` and `TestImage-shadow.png`.

Same for overlays with `-overlay`. But overlays are **necessary** for some animation graphics. They will be colorized by VCMI.

Currently needed for:
- flaggable adventure map objects (needs a transparent image with white flags on it)
- creature battle animations (needs a transparent image with white outline of creature for highlighting on mouse hover)
