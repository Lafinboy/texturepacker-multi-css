# Multi-CSS for TexturePacker #

This exporter for the awesome [TexturePacker](http://www.texturepacker.com/), creates a new exporter type called "Multi-CSS" that will use the CSS filename as the image spritesheet class name, and also make sure the width rules for the image classes only apply to an element tagged both with the image name and the spritesheet name.

## Installation ##

    make install


## Why? Isn't the default CSS exporter good enough? ##

Someone may want to have multiple sprite sheets, one for the base site design, and one for the specific content displayed on the page.

The default CSS exporter may break your css if an image name collides with an existing css class.  The default CSS exporter uses a static base class name "sprites" so you can't have multiple sprite sheets on one page without modifying the output css.

Also this exporter provides IE cache busting for the export image because IE disregards modified headers, so the user would have to shift refresh if you change the spritesheet if you use the default CSS exporter.

Although this fixes some of what I consider "bugs", the TexturePacker software is amazing, and you should buy it.  This exporter wouldn't have been possible if the author didn't allow custom exporters.  So *major Kudos to Andreas Löw* for making his software extendable.

## Todo ##

This exporter doesn't support the hover state classes because the [Grantlee](http://www.grantlee.org/apidox/for_themers.html) documentation linked by TexturePacker doesn't list replace or partial string matching filters.  If someone gets that working please do a pull request.
