---
description: Things to take note of when customizing the theme
---

# For skinners

By default, elements are designed for 1920x1080. If you want to support higher resolutions, you can add **`(doubleres)`** to the filename, scaling the element to fit 3840x2160.\
Example: **`texture.png`** -> **`texture (doubleres).png`**

Almost everything that can be an image, is an image. Easy customization is top priority in tweaktown.

**NOTE: Texture scaling relies on a multiplier that's not 100% precise, so large textures may be a few pixels off. You may need to add a few pixels for fullscreen elements like footers and backgrounds**



Every texture can be animated with a spritesheet if desired. Just remember to add the columns/rows to the filename. Example: **`texture.png`** -> **`texture 11x22.png`**



Every texture has hotplug support, which means if you don't want an element to show up, you can simply delete the texture and the game loads a blank 1x1px placeholder instead. This also counts for optional textures that aren't included by default. See "Textures" section for the whole list.



Most elements are center aligned so you can extend the texture in each direction without being limited. Textures at edges(header, footer, corner pieces etc.) are not center aligned since it's not necessary for them and aligning to the edge can result in smaller resolutions. The latter may come in handy for animations with many frames



Not everything can be customized with textures, but refer to skin.ini for extra configuration. It allows you to easily change colours and various settings on different screens.

**Reload textures and skin.ini: F2**

**Reload skin.ini(takes less time): Shift+F2**



Sadly since we're on the stepmania engine, **customizing fonts is a very painful experience** that I wouldn't recommend messing with. I won't stop anyone, but you've been warned.

\[ADD NEW FONT GEN THING HERE]

That said, **combo and accuracy fonts should be easy enough to edit** since those are small spritesheets. It's when you have to use the font generator that you may go insane.

If you want more stylized texts in places, a lot of text in the game can be colored with skin.ini. Since the skin.ini colors have alpha support, you can simply make things invisible and use textures to go wild instead!



If you find the default set of textures limiting or want to do more, you can add new images arbitrarily on any screen and tinker with a bunch of settings for them. This is more advanced skinning, but the option is there if you need it. Check \[custom sprites wiki page] to learn how this works



While **I'd highly encourage only customizing the theme through textures and skin.ini**, nobody is stopping you from doing whatever you want to the lua files. Just know that the codebase is not robust at all, and **the scope of this project is not to allow easy customization through lua**. If it was, the theme would be based on Rebirth instead of Til Death.

**If you do make changes to lua files and plan to share your version, please document the changes in some way**, so people know what to expect when messing with it. For example if you change texture alignment, interactions, positions etc. it would be helpful to know the differences.
