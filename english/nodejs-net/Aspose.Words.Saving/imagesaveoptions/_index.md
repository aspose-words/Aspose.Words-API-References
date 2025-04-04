---
title: ImageSaveOptions class
linktitle: ImageSaveOptions class
articleTitle: ImageSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ImageSaveOptions class. Allows to specify additional options when rendering document pages or shapes to images"
type: docs
weight: 390
url: /nodejs-net/aspose.words.saving/imagesaveoptions/
---

## ImageSaveOptions class

Allows to specify additional options when rendering document pages or shapes to images.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [ImageSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [ImageSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save rendered images in the [SaveFormat.Tiff](../../aspose.words/saveformat/#Tiff), [SaveFormat.Png](../../aspose.words/saveformat/#Png), [SaveFormat.Bmp](../../aspose.words/saveformat/#Bmp), [SaveFormat.Jpeg](../../aspose.words/saveformat/#Jpeg), [SaveFormat.Emf](../../aspose.words/saveformat/#Emf), [SaveFormat.Eps](../../aspose.words/saveformat/#Eps), [SaveFormat.WebP](../../aspose.words/saveformat/#WebP) or [SaveFormat.Svg](../../aspose.words/saveformat/#Svg) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [colorMode](../fixedpagesaveoptions/colorMode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [horizontalResolution](./horizontalResolution/) | Gets or sets the horizontal resolution for the generated images, in dots per inch. |
| [imageBrightness](./imageBrightness/) | Gets or sets the brightness for the generated images. |
| [imageColorMode](./imageColorMode/) | Gets or sets the color mode for the generated images. |
| [imageContrast](./imageContrast/) | Gets or sets the contrast for the generated images. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpegQuality](./jpegQuality/) | Gets or sets a value determining the quality of the generated JPEG images. |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileRenderingOptions](./metafileRenderingOptions/) | Allows to specify how metafiles are treated in the rendered output. |
| [numeralFormat](../fixedpagesaveoptions/numeralFormat/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimizeOutput](../fixedpagesaveoptions/optimizeOutput/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``true``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSavingCallback](../fixedpagesaveoptions/pageSavingCallback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSet](./pageSet/) | Gets or sets the pages to render. Default is all the pages in the document. |
| [paperColor](./paperColor/) | Gets or sets the background (paper) color for the generated images. The default value is aspose.pydrawing.Color.white. |
| [pixelFormat](./pixelFormat/) | Gets or sets the pixel format for the generated images. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.Tiff](../../aspose.words/saveformat/#Tiff), [SaveFormat.Png](../../aspose.words/saveformat/#Png), [SaveFormat.Bmp](../../aspose.words/saveformat/#Bmp), [SaveFormat.Jpeg](../../aspose.words/saveformat/#Jpeg) or vector [SaveFormat.Emf](../../aspose.words/saveformat/#Emf), [SaveFormat.Eps](../../aspose.words/saveformat/#Eps), [SaveFormat.WebP](../../aspose.words/saveformat/#WebP), [SaveFormat.Svg](../../aspose.words/saveformat/#Svg). |
| [scale](./scale/) | Gets or sets the zoom factor for the generated images. |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [thresholdForFloydSteinbergDithering](./thresholdForFloydSteinbergDithering/) | Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../imagebinarizationmethod/) is [ImageBinarizationMethod.FloydSteinbergDithering](../imagebinarizationmethod/#FloydSteinbergDithering). |
| [tiffBinarizationMethod](./tiffBinarizationMethod/) | Gets or sets method used while converting images to 1 bpp format when [ImageSaveOptions.saveFormat](./saveFormat/) is [SaveFormat.Tiff](../../aspose.words/saveformat/#Tiff) and [ImageSaveOptions.tiffCompression](./tiffCompression/) is equal to [TiffCompression.Ccitt3](../tiffcompression/#Ccitt3) or [TiffCompression.Ccitt4](../tiffcompression/#Ccitt4). |
| [tiffCompression](./tiffCompression/) | Gets or sets the type of compression to apply when saving generated images to the TIFF format. |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``false``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useGdiEmfRenderer](./useGdiEmfRenderer/) | Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [verticalResolution](./verticalResolution/) | Gets or sets the vertical resolution for the generated images, in dots per inch. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Creates a deep clone of this object. |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Renders a page of a Word document into an image with transparent or colored background.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Times New Roman";
builder.font.size = 24;
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let imgOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);
// Set the "PaperColor" property to a transparent color to apply a transparent
// background to the document while rendering it to an image.
imgOptions.paperColor = "rgba(0,0,0,0)";

doc.save(base.artifactsDir + "ImageSaveOptions.paperColor.transparent.png", imgOptions);

// Set the "PaperColor" property to an opaque color to apply that color
// as the background of the document as we render it to an image.
imgOptions.paperColor = "#F08080";

doc.save(base.artifactsDir + "ImageSaveOptions.paperColor.LightCoral.png", imgOptions);
```

Shows how to configure compression while saving a document as a JPEG.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let imageOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.jpegQuality = 10;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.jpegQuality = 100;
doc.save(base.artifactsDir + "ImageSaveOptions.jpegQuality.HighQuality.jpg", imageOptions);
```

Shows how to specify a resolution while rendering a document to PNG.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Times New Roman";
builder.font.size = 24;
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.insertImage(base.imageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);

// Set the "Resolution" property to "72" to render the document in 72dpi.
options.resolution = 72;
doc.save(base.artifactsDir + "ImageSaveOptions.resolution.72dpi.png", options);

// Set the "Resolution" property to "300" to render the document in 300dpi.
options.resolution = 300;
doc.save(base.artifactsDir + "ImageSaveOptions.resolution.300dpi.png", options);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

