---
title: ImageSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4890
url: /net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Allows to specify additional options when rendering document pages or shapes to images.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions)(SaveFormat) | Initializes a new instance of this class that can be used to save rendered images in the Tiff, Png, Bmp, Emf, Jpeg or Svg format. Png, Bmp, Jpeg or Svg format. |

## Properties

| Name | Description |
| --- | --- |
| [HorizontalResolution](horizontalresolution) { get; set; } | Gets or sets the horizontal resolution for the generated images, in dots per inch. |
| [ImageBrightness](imagebrightness) { get; set; } | Gets or sets the brightness for the generated images. |
| [ImageColorMode](imagecolormode) { get; set; } | Gets or sets the color mode for the generated images. |
| [ImageContrast](imagecontrast) { get; set; } | Gets or sets the contrast for the generated images. |
| [JpegQuality](jpegquality) { get; set; } | Gets or sets a value determining the quality of the generated JPEG images. |
| [MetafileRenderingOptions](metafilerenderingoptions) { get; } | Allows to specify how metafiles are treated in the rendered output. |
| [PageSet](pageset) { get; set; } | Gets or sets the pages to render. Default is all the pages in the document. |
| [PaperColor](papercolor) { get; set; } | Gets or sets the background (paper) color for the generated images. |
| [PixelFormat](pixelformat) { get; set; } | Gets or sets the pixel format for the generated images. |
| [Resolution](resolution) { set; } | Sets both horizontal and vertical resolution for the generated images, in dots per inch. |
| override [SaveFormat](saveformat) { get; set; } | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster Tiff, Png, Bmp, Jpeg or vector Emf, Svg. |
| [Scale](scale) { get; set; } | Gets or sets the zoom factor for the generated images. |
| [ThresholdForFloydSteinbergDithering](thresholdforfloydsteinbergdithering) { get; set; } | Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [`ImageBinarizationMethod`](../imagebinarizationmethod) is ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](tiffbinarizationmethod) { get; set; } | Gets or sets method used while converting images to 1 bpp format when [`SaveFormat`](./saveformat) is SaveFormat.Tiff and [`TiffCompression`](./tiffcompression) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4. |
| [TiffCompression](tiffcompression) { get; set; } | Gets or sets the type of compression to apply when saving generated images to the TIFF format. |
| [UseGdiEmfRenderer](usegdiemfrenderer) { get; set; } | Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [VerticalResolution](verticalresolution) { get; set; } | Gets or sets the vertical resolution for the generated images, in dots per inch. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](clone)() | Creates a deep clone of this object. |

### Examples

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

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

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

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0 || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Set the "Resolution" property to "300" to render the document in 300dpi.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0 || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### See Also

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
