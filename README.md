jpexs-flash-decompiler
=================

Extract resources from SWF using open source jpexs jar library

Dependency
-----------
- `NodeJS` v6.*
- `Java` v8.*

Installation
------------

    npm install jpexs-flash-decompiler --save

Usage
-----

Works only export export tool

Example:

```js
const jpexs = require( 'jpexs-flash-decompiler' );

jpexs.export( {
  file: 'path/to/swf/file',
  output: 'path/to/output/dir',
  items: [ jpexs.ITEM.FONT, ... ],
  format: [ jpexs.FORMAT.FONT.WOFF, ... ]
}, function( err ) {
  if ( err ) {
    console.log( 'Error: ', err.message );
  } else {
    console.log( 'DONE!' );
  }
} );
```

Items
-------

- `jpexs.ITEM.SCRIPT`
  Scripts (Default format: ActionScript source)
- `jpexs.ITEM.IMAGE`
  Images (Default format: PNG/JPEG)
- `jpexs.ITEM.SHAPE`
  Shapes (Default format: SVG)
- `jpexs.ITEM.MORPHSHAPE`
   MorphShapes (Default format: SVG)
- `jpexs.ITEM.MOVIE`
  Movies (Default format: FLV without sound)
- `jpexs.ITEM.FONT`
  Fonts (Default format: TTF)
- `jpexs.ITEM.FRAME`
  Frames (Default format: PNG)
- `jpexs.ITEM.SPRITE`
  Sprites (Default format: PNG)
- `jpexs.ITEM.BUTTON`
  Buttons (Default format: PNG)
- `jpexs.ITEM.SOUND`
  Sounds (Default format: MP3/WAV/FLV only sound)
- `jpexs.ITEM.BINARY`
  Binary data (Default format:  Raw data)
- `jpexs.ITEM.TEXT`
  Texts (Default format: Plain text)
- `jpexs.ITEM.FLA`
  Everything to FLA compressed format
- `jpexs.ITEM.ALL`
  Every resource (but not FLA)

FORMATS
-------

- script
    - `jpexs.FORMAT.SCRIPT.AS`
      ActionScript source
    - `jpexs.FORMAT.SCRIPT.HEX`
      ActionScript Hex only
    - `jpexs.FORMAT.SCRIPT.PCODE`
      ActionScript P-code
    - `jpexs.FORMAT.SCRIPT.PCODEHEX`
      ActionScript P-code with hex
- shape
    - `jpexs.FORMAT.SHAPE.SVG`
      SVG format for Shapes
    - `jpexs.FORMAT.SHAPE.BMP`
      BMP format for Shapes
    - `jpexs.FORMAT.SHAPE.PNG`
      PNG format for Shapes
    - `jpexs.FORMAT.SHAPE.CANVAS`
      HTML5 Canvas format for Shapes
- morph shape
    - `jpexs.FORMAT.MORPHSHAPE.SVG`
      SVG format for MorphShapes
    - `jpexs.FORMAT.MORPHSHAPE.CANVAS`
      HTML5 Canvas  format for MorphShapes
- frame
    - `jpexs.FORMAT.FRAME.BMP`
      BMP format for Frames
    - `jpexs.FORMAT.FRAME.PNG`
      PNG format for Frames
    - `jpexs.FORMAT.FRAME.GIF`
      GIF format for Frames
    - `jpexs.FORMAT.FRAME.PDF`
      PDF format for Frames
    - `jpexs.FORMAT.FRAME.AVI`
      AVI format for Frames
    - `jpexs.FORMAT.FRAME.SVG`
      SVG format for Frames
    - `jpexs.FORMAT.FRAME.CANVAS`
      HTML5 Canvas format for Frames
- sprite
    - `jpexs.FORMAT.SPRITE.PNG`
      PNG format for Sprites
    - `jpexs.FORMAT.SPRITE.GIF`
      GIF format for Sprites
    - `jpexs.FORMAT.SPRITE.AVI`
      AVI format for Sprites
    - `jpexs.FORMAT.SPRITE.SVG`
      SVG format for Sprites
    - `jpexs.FORMAT.SPRITE.PDF`
      PDF format for Sprites
    - `jpexs.FORMAT.SPRITE.BMP`
      BMP format for Sprites
    - `jpexs.FORMAT.SPRITE.CANVAS`
      HTML5 Canvas format for Sprites
- button
    - `jpexs.FORMAT.BUTTON.PNG`
      PNG format for Buttons
    - `jpexs.FORMAT.BUTTON.SVG`
      SVG format for Buttons
    - `jpexs.FORMAT.BUTTON.BMP`
      BMP format for Buttons
- image
    - `jpexs.FORMAT.IMAGE.BMP`
      BMP format for Images
    - `jpexs.FORMAT.IMAGE.PNG`
      PNG format for Images
    - `jpexs.FORMAT.IMAGE.JPEG`
      JPEG format for Images
    - `jpexs.FORMAT.IMAGE.ALL`
      PNG/GIF/JPEG format for Images
- text
    - `jpexs.FORMAT.TEXT.SVG`
      SVG format for Texts
    - `jpexs.FORMAT.TEXT.PLAIN`
      Plain text format for Texts
    - `jpexs.FORMAT.TEXT.FORMATTED`
      Formatted text format for Texts
- font
    - `jpexs.FORMAT.FONT.TTF`
      TTF format for Fonts
    - `jpexs.FORMAT.FONT.WOFF`
      WOFF format for Fonts
- sound
    - `jpexs.FORMAT.SOUND.FLV`
      FLV format for Sounds
    - `jpexs.FORMAT.SOUND.WAV`
      WAV format for Sounds
    - `jpexs.FORMAT.SOUND.ALL`
      MP3/WAV/FLV format for Sounds