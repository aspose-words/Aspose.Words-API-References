---
title: ImageSaveOptions Class
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.ImageSaveOptions. Easily your document rendering with customizable options for high-quality image output.
type: docs
weight: 5980
url: /net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Allows to specify additional options when rendering document pages or shapes to images.

To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initializes a new instance of this class that can be used to save rendered images in the Tiff, Png, Bmp, Jpeg, Emf, Eps, WebP or Svg format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is `false`. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Gets or sets a value determining how colors are rendered. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | When `true`, causes the name and version of Aspose.Words to be embedded into produced files. Default value is `true`. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Allows to specify rendering mode and quality for the Graphics object. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Gets or sets the horizontal resolution for the generated images, in dots per inch. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Gets or sets the brightness for the generated images. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Gets or sets the color mode for the generated images. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Gets or sets the contrast for the generated images. |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | Gets or sets the size of a generated image in pixels. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Gets or sets a value determining the quality of the generated JPEG images. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is `false`. |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Allows to specify how metafiles are treated in the rendered output. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Gets or sets [`NumeralFormat`](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to `true`. Default is `false`. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Gets or sets the pages to render. Default is all the pages in the document. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Gets or sets the background (paper) color for the generated images. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Gets or sets the pixel format for the generated images. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | When `true`, pretty formats output where applicable. Default value is `false`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Called during saving a document and accepts data about saving progress. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Sets both horizontal and vertical resolution for the generated images, in dots per inch. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster Tiff, Png, Bmp, Jpeg or vector Emf, Eps, WebP, Svg. |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Gets or sets the zoom factor for the generated images. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [`ImageBinarizationMethod`](../imagebinarizationmethod/) is FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Gets or sets method used while converting images to 1 bpp format when [`SaveFormat`](./saveformat/) is Tiff and [`TiffCompression`](./tiffcompression/) is equal to Ccitt3 or Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Gets or sets the type of compression to apply when saving generated images to the TIFF format. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determines whether the font attributes will be changed according to the character code being used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is `false`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is `true`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Gets or sets the vertical resolution for the generated images, in dots per inch. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Creates a deep clone of this object. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determines whether the specified object is equal in value to the current object. |

## Examples

Shows how to specify a resolution while rendering a document to PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Set the "Resolution" property to "72" to render the document in 72dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Set the "Resolution" property to "300" to render the document in 300dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

Shows how to configure compression while saving a document as a JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Renders a page of a Word document into an image with transparent or colored background.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Set the "PaperColor" property to a transparent color to apply a transparent
// background to the document while rendering it to an image.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Set the "PaperColor" property to an opaque color to apply that color
// as the background of the document as we render it to an image.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### See Also

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
