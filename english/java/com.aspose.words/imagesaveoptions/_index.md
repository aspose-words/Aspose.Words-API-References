---
title: ImageSaveOptions
linktitle: ImageSaveOptions
second_title: Aspose.Words for Java
description: Allows to specify additional options when rendering document pages or shapes to images in Java.
type: docs
weight: 390
url: /java/com.aspose.words/imagesaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ImageSaveOptions extends FixedPageSaveOptions implements Cloneable
```

Allows to specify additional options when rendering document pages or shapes to images.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.

 **Examples:** 

Shows how to specify a resolution while rendering a document to PNG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Times New Roman");
 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Resolution" property to "72" to render the document in 72dpi.
 options.setResolution(72f);
 doc.save(getArtifactsDir() + "ImageSaveOptions.Resolution.72dpi.png", options);

 // Set the "Resolution" property to "300" to render the document in 300dpi.
 options.setResolution(300f);
 doc.save(getArtifactsDir() + "ImageSaveOptions.Resolution.300dpi.png", options);
 
```

Renders a page of a Word document into an image with transparent or colored background.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Times New Roman");
 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "PaperColor" property to a transparent color to apply a transparent
 // background to the document while rendering it to an image.
 imgOptions.setPaperColor(new Color(1f, 0f, 0f, .5f));

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

 // Set the "PaperColor" property to an opaque color to apply that color
 // as the background of the document as we render it to an image.
 imgOptions.setPaperColor(Color.cyan);

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
 
```

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Constructors

| Constructor | Description |
| --- | --- |
| [ImageSaveOptions(int saveFormat)](#ImageSaveOptions-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [deepClone()](#deepClone) | Creates a deep clone of this object. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getColorMode()](#getColorMode) | Gets a value determining how colors are rendered. |
| [getCustomTimeZoneInfo()](#getCustomTimeZoneInfo) | Gets custom local time zone used for date/time fields. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getGraphicsQualityOptions()](#getGraphicsQualityOptions) | Allows to specify rendering mode and quality for the java.awt.Graphics2D object. |
| [getHorizontalResolution()](#getHorizontalResolution) | Gets the horizontal resolution for the generated images, in dots per inch. |
| [getImageBrightness()](#getImageBrightness) | Gets the brightness for the generated images. |
| [getImageColorMode()](#getImageColorMode) | Gets the color mode for the generated images. |
| [getImageContrast()](#getImageContrast) | Gets the contrast for the generated images. |
| [getImageSize()](#getImageSize) | Gets the size of a generated image in pixels. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the generated JPEG images. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify how metafiles are treated in the rendered output. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
| [getPageLayout()](#getPageLayout) | Gets the layout used when rendering multiple pages into a single output. |
| [getPageSavingCallback()](#getPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getPageSet()](#getPageSet) | Gets the pages to render. |
| [getPaperColor()](#getPaperColor) | Gets the background (paper) color for the generated images. |
| [getPixelFormat()](#getPixelFormat) | Gets the pixel format for the generated images. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. |
| [getScale()](#getScale) | Gets the zoom factor for the generated images. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getThresholdForFloydSteinbergDithering()](#getThresholdForFloydSteinbergDithering) | Gets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. |
| [getTiffBinarizationMethod()](#getTiffBinarizationMethod) | Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4). |
| [getTiffCompression()](#getTiffCompression) | Gets the type of compression to apply when saving generated images to the TIFF format. |
| [getUpdateAmbiguousTextFont()](#getUpdateAmbiguousTextFont) | Determines whether the font attributes will be changed according to the character code being used. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseGdiEmfRenderer()](#getUseGdiEmfRenderer) | Gets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getVerticalResolution()](#getVerticalResolution) | Gets the vertical resolution for the generated images, in dots per inch. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
| [setCustomTimeZoneInfo(TimeZone value)](#setCustomTimeZoneInfo-java.util.TimeZone) |  |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setGraphicsQualityOptions(GraphicsQualityOptions value)](#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions) | Allows to specify rendering mode and quality for the java.awt.Graphics2D object. |
| [setHorizontalResolution(float value)](#setHorizontalResolution-float) | Sets the horizontal resolution for the generated images, in dots per inch. |
| [setImageBrightness(float value)](#setImageBrightness-float) | Sets the brightness for the generated images. |
| [setImageColorMode(int value)](#setImageColorMode-int) | Sets the color mode for the generated images. |
| [setImageContrast(float value)](#setImageContrast-float) | Sets the contrast for the generated images. |
| [setImageSize(Dimension value)](#setImageSize-java.awt.Dimension) | Sets the size of a generated image in pixels. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the generated JPEG images. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
| [setPageLayout(MultiPageLayout value)](#setPageLayout-com.aspose.words.MultiPageLayout) | Sets the layout used when rendering multiple pages into a single output. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet) | Sets the pages to render. |
| [setPaperColor(Color value)](#setPaperColor-java.awt.Color) | Sets the background (paper) color for the generated images. |
| [setPixelFormat(int value)](#setPixelFormat-int) | Sets the pixel format for the generated images. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setResolution(float value)](#setResolution-float) | Sets both horizontal and vertical resolution for the generated images, in dots per inch. |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. |
| [setScale(float value)](#setScale-float) | Sets the zoom factor for the generated images. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setThresholdForFloydSteinbergDithering(byte value)](#setThresholdForFloydSteinbergDithering-byte) | Sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. |
| [setTiffBinarizationMethod(int value)](#setTiffBinarizationMethod-int) | Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4). |
| [setTiffCompression(int value)](#setTiffCompression-int) | Sets the type of compression to apply when saving generated images to the TIFF format. |
| [setUpdateAmbiguousTextFont(boolean value)](#setUpdateAmbiguousTextFont-boolean) | Determines whether the font attributes will be changed according to the character code being used. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseGdiEmfRenderer(boolean value)](#setUseGdiEmfRenderer-boolean) | Sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setVerticalResolution(float value)](#setVerticalResolution-float) | Sets the vertical resolution for the generated images, in dots per inch. |
### ImageSaveOptions(int saveFormat) {#ImageSaveOptions-int}
```
public ImageSaveOptions(int saveFormat)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

### createSaveOptions(int saveFormat) {#createSaveOptions-int}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String}
```
public static SaveOptions createSaveOptions(String fileName)
```


Creates a save options object of a class suitable for the file extension specified in the given file name.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The extension of this file name determines the class of the save options object to create. |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/) - An object of a class that derives from [SaveOptions](../../com.aspose.words/saveoptions/).
### deepClone() {#deepClone}
```
public ImageSaveOptions deepClone()
```


Creates a deep clone of this object.

 **Examples:** 

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 21000);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a pixel format for the image that the saving operation will generate.
 // Various bit per pixel rates will affect the quality and file size of the generated image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPixelFormat(imagePixelFormat);

 // We can clone ImageSaveOptions instances.
 Assert.assertNotEquals(imageSaveOptions, imageSaveOptions.deepClone());

 doc.save(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
 
```

**Returns:**
[ImageSaveOptions](../../com.aspose.words/imagesaveoptions/)
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

 **Examples:** 

Shows how to change image color with saving options property.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode/) constants.
### getCustomTimeZoneInfo() {#getCustomTimeZoneInfo}
```
public TimeZone getCustomTimeZoneInfo()
```


Gets custom local time zone used for date/time fields.

 **Remarks:** 

This option is available in either .Net framework starting from 3.5 version or .Net Standard.

By default, Aspose.Words uses system local time zone when writes date/time fields, this option allows to set custom value.

**Returns:**
java.util.TimeZone - Custom local time zone used for date/time fields.
### getDefaultTemplate() {#getDefaultTemplate}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Returns:**
java.lang.String - Path to default template (including filename).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

 **Examples:** 

Shows how 3D effects are rendered.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants.
### getDmlRenderingMode() {#getDmlRenderingMode}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render fallback shapes when saving to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants.
### getExportGeneratorName() {#getExportGeneratorName}
```
public boolean getExportGeneratorName()
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getGraphicsQualityOptions() {#getGraphicsQualityOptions}
```
public GraphicsQualityOptions getGraphicsQualityOptions()
```


Allows to specify rendering mode and quality for the java.awt.Graphics2D object.

 **Remarks:** 

Use this property to override the Graphics settings provided by Aspose.Words engine by default.

It will take effect only when a document is being saved to an image-like format.

 **Examples:** 

Shows how to set render quality options while converting documents to image formats.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions();
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON); // SmoothingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON); // TextRenderingHint
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_COLOR_RENDERING, RenderingHints.VALUE_COLOR_RENDER_QUALITY); // CompositingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_RENDERING, RenderingHints.VALUE_RENDER_QUALITY); // CompositingQuality
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_INTERPOLATION, RenderingHints.VALUE_INTERPOLATION_BILINEAR); // InterpolationMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_FRACTIONALMETRICS, RenderingHints.VALUE_FRACTIONALMETRICS_ON); // StringFormat

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 saveOptions.setGraphicsQualityOptions(qualityOptions);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
 
```

**Returns:**
[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions/) - The corresponding [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions/) value.
### getHorizontalResolution() {#getHorizontalResolution}
```
public float getHorizontalResolution()
```


Gets the horizontal resolution for the generated images, in dots per inch.

 **Remarks:** 

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
float - The horizontal resolution for the generated images, in dots per inch.
### getImageBrightness() {#getImageBrightness}
```
public float getImageBrightness()
```


Gets the brightness for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
float - The brightness for the generated images.
### getImageColorMode() {#getImageColorMode}
```
public int getImageColorMode()
```


Gets the color mode for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../com.aspose.words/imagecolormode/\#NONE).

 **Examples:** 

Shows how to set a color mode when rendering documents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 20200);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a color mode for the image that the saving operation will generate.
 // If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
 // the saving operation will apply grayscale color reduction while rendering the document.
 // If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
 // the saving operation will render the document into a monochrome image.
 // If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
 // and preserve all the document's colors in the output image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setImageColorMode(imageColorMode);

 doc.save(getArtifactsDir() + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
 
```

**Returns:**
int - The color mode for the generated images. The returned value is one of [ImageColorMode](../../com.aspose.words/imagecolormode/) constants.
### getImageContrast() {#getImageContrast}
```
public float getImageContrast()
```


Gets the contrast for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
float - The contrast for the generated images.
### getImageSize() {#getImageSize}
```
public Dimension getImageSize()
```


Gets the size of a generated image in pixels.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is (0 x 0), which means that the size of the generated image will be calculated according to the size of the image in points, the specified resolution and scale.

 **Examples:** 

Shows how to render every page of a document to a separate TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 for (int i = 0; i < doc.getPageCount(); i++) {
     // Set the "PageSet" property to the number of the first page from
     // which to start rendering the document from.
     options.setPageSet(new PageSet(i));
     // Export page at 2325x5325 pixels and 600 dpi.
     options.setResolution(600f);
     options.setImageSize(new Dimension(2325, 5325));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
 }
 
```

**Returns:**
java.awt.Dimension - The size of a generated image in pixels.
### getImlRenderingMode() {#getImlRenderingMode}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants.
### getJpegQuality() {#getJpegQuality}
```
public int getJpegQuality()
```


Gets a value determining the quality of the generated JPEG images.

 **Remarks:** 

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

 **Examples:** 

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```

**Returns:**
int - A value determining the quality of the generated JPEG images.
### getMemoryOptimization() {#getMemoryOptimization}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

 **Examples:** 

Shows an option to optimize memory consumption when rendering large documents to PDF.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.PDF);

 // Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
 // at the cost of increasing the duration of the operation.
 // Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
 saveOptions.setMemoryOptimization(memoryOptimization);

 doc.save(getArtifactsDir() + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
 
```

**Returns:**
boolean - Value determining if memory optimization should be performed before saving the document.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Allows to specify how metafiles are treated in the rendered output.

 **Remarks:** 

When [MetafileRenderingMode.VECTOR](../../com.aspose.words/metafilerenderingmode/\#VECTOR) is specified, Aspose.Words renders metafile to vector graphics using its own metafile rendering engine first and then renders vector graphics to the image.

When [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP) is specified, Aspose.Words renders metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text) on the page. Aspose.Words metafile rendering engine will produce more consistent result even on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP).

 **Examples:** 

Shows how to set the rendering mode when saving documents with Windows Metafile images to other image formats.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Windows MetaFile.wmf");

 // When we save the document as an image, we can pass a SaveOptions object to
 // determine how the saving operation will process Windows Metafiles in the document.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Vector",
 // or "MetafileRenderingMode.VectorWithFallback", we will render all metafiles as vector graphics.
 // If we set the "RenderingMode" property to "MetafileRenderingMode.Bitmap", we will render all metafiles as bitmaps.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 options.getMetafileRenderingOptions().setRenderingMode(metafileRenderingMode);
 // Aspose.Words uses GDI+ for raster operations emulation, when value is set to true.
 options.getMetafileRenderingOptions().setUseGdiRasterOperationsEmulation(true);

 doc.save(getArtifactsDir() + "ImageSaveOptions.WindowsMetaFile.png", options);
 
```

**Returns:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) - The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value.
### getNumeralFormat() {#getNumeralFormat}
```
public int getNumeralFormat()
```


Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

 **Examples:** 

Shows how to set the numeral format used when saving to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setLocaleId(1025);
 builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
 // use glyphs from the U+0660 to U+0669 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.Context" to
 // look up the locale to determine what number of glyphs to use.
 // Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
 // use glyphs from the U+06F0 to U+06F9 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
 // Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
 options.setNumeralFormat(numeralFormat);

 doc.save(getArtifactsDir() + "PdfSaveOptions.SetNumeralFormat.pdf", options);
 
```

**Returns:**
int - [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants.
### getOptimizeOutput() {#getOptimizeOutput}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(60385.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191000.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getPageLayout() {#getPageLayout}
```
public MultiPageLayout getPageLayout()
```


Gets the layout used when rendering multiple pages into a single output.

 **Remarks:** 

Use one of the factory methods of [MultiPageLayout](../../com.aspose.words/multipagelayout/) to configure this property.

For [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) the default value is [MultiPageLayout.tiffFrames()](../../com.aspose.words/multipagelayout/\#tiffFrames). For other formats the default value is [MultiPageLayout.singlePage()](../../com.aspose.words/multipagelayout/\#singlePage).

This property has effect only when saving to the following formats: [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.GIF](../../com.aspose.words/saveformat/\#GIF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.WEB\_P](../../com.aspose.words/saveformat/\#WEB-P)

 **Examples:** 

Shows how to save the document into JPG image with multi-page layout settings.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/) - The layout used when rendering multiple pages into a single output.
### getPageSavingCallback() {#getPageSavingCallback}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value.
### getPageSet() {#getPageSet}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

 **Remarks:** 

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

 **Examples:** 

Shows how to extract pages based on exact page ranges.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

Shows how to specify which page in a document to render as an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world! This is page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("This is page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("This is page 3.");

 Assert.assertEquals(3, doc.getPageCount());

 // When we save the document as an image, Aspose.Words only renders the first page by default.
 // We can pass a SaveOptions object to specify a different page to render.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.GIF);

 // Render every page of the document to a separate image file.
 for (int i = 1; i <= doc.getPageCount(); i++) {
     saveOptions.setPageSet(new PageSet(1));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
 }
 
```

Shows how to render one page from a document to a JPEG image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set the "PageSet" to "1" to select the second page via
 // the zero-based index to start rendering the document from.
 options.setPageSet(new PageSet(1));

 // When we save the document to the JPEG format, Aspose.Words only renders one page.
 // This image will contain one page starting from page two,
 // which will just be the second page of the original document.
 doc.save(getArtifactsDir() + "ImageSaveOptions.OnePage.jpg", options);
 
```

Shows how to render every page of a document to a separate TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 for (int i = 0; i < doc.getPageCount(); i++) {
     // Set the "PageSet" property to the number of the first page from
     // which to start rendering the document from.
     options.setPageSet(new PageSet(i));
     // Export page at 2325x5325 pixels and 600 dpi.
     options.setResolution(600f);
     options.setImageSize(new Dimension(2325, 5325));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
 }
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - The pages to render.
### getPaperColor() {#getPaperColor}
```
public Color getPaperColor()
```


Gets the background (paper) color for the generated images.

The default value is java.awt.Color\#getWhite().getWhite().

 **Remarks:** 

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

 **Examples:** 

Renders a page of a Word document into an image with transparent or colored background.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Times New Roman");
 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "PaperColor" property to a transparent color to apply a transparent
 // background to the document while rendering it to an image.
 imgOptions.setPaperColor(new Color(1f, 0f, 0f, .5f));

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

 // Set the "PaperColor" property to an opaque color to apply that color
 // as the background of the document as we render it to an image.
 imgOptions.setPaperColor(Color.cyan);

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
 
```

**Returns:**
java.awt.Color - The background (paper) color for the generated images.
### getPixelFormat() {#getPixelFormat}
```
public int getPixelFormat()
```


Gets the pixel format for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat/\#FORMAT-32-BPP-ARGB).

Pixel format of the output image may differ from the set value because of work of GDI+.

 **Examples:** 

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 21000);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a pixel format for the image that the saving operation will generate.
 // Various bit per pixel rates will affect the quality and file size of the generated image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPixelFormat(imagePixelFormat);

 // We can clone ImageSaveOptions instances.
 Assert.assertNotEquals(imageSaveOptions, imageSaveOptions.deepClone());

 doc.save(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
 
```

**Returns:**
int - The pixel format for the generated images. The returned value is one of [ImagePixelFormat](../../com.aspose.words/imagepixelformat/) constants.
### getPrettyFormat() {#getPrettyFormat}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.DOC](../../com.aspose.words/saveformat/\#DOC), [SaveFormat.DOT](../../com.aspose.words/saveformat/\#DOT), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG) or vector [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF), [SaveFormat.EPS](../../com.aspose.words/saveformat/\#EPS), [SaveFormat.WEB\_P](../../com.aspose.words/saveformat/\#WEB-P), [SaveFormat.SVG](../../com.aspose.words/saveformat/\#SVG).

 **Remarks:** 

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/).

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getScale() {#getScale}
```
public float getScale()
```


Gets the zoom factor for the generated images.

 **Remarks:** 

The default value is 1.0. The value must be greater than 0.

 **Examples:** 

Shows how to render an Office Math object into an image file in the local file system.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
float - The zoom factor for the generated images.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getThresholdForFloydSteinbergDithering() {#getThresholdForFloydSteinbergDithering}
```
public byte getThresholdForFloydSteinbergDithering()
```


Gets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod/) is [ImageBinarizationMethod.FLOYD\_STEINBERG\_DITHERING](../../com.aspose.words/imagebinarizationmethod/\#FLOYD-STEINBERG-DITHERING).

 **Remarks:** 

The default value is 128.

 **Examples:** 

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```

**Returns:**
byte - The threshold that determines the value of the binarization error in the Floyd-Steinberg method.
### getTiffBinarizationMethod() {#getTiffBinarizationMethod}
```
public int getTiffBinarizationMethod()
```


Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4).

 **Remarks:** 

The default value is [ImageBinarizationMethod.THRESHOLD](../../com.aspose.words/imagebinarizationmethod/\#THRESHOLD).

 **Examples:** 

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```

**Returns:**
int - Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4). The returned value is one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod/) constants.
### getTiffCompression() {#getTiffCompression}
```
public int getTiffCompression()
```


Gets the type of compression to apply when saving generated images to the TIFF format.

 **Remarks:** 

Has effect only when saving to TIFF.

The default value is [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4).

 **Examples:** 

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Tagged Image File Format.tiff");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 // Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
 // which may result in a very large output file.
 // Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
 // Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
 options.setTiffCompression(tiffCompression);

 doc.save(getArtifactsDir() + "ImageSaveOptions.TiffImageCompression.tiff", options);
 
```

**Returns:**
int - The type of compression to apply when saving generated images to the TIFF format. The returned value is one of [TiffCompression](../../com.aspose.words/tiffcompression/) constants.
### getUpdateAmbiguousTextFont() {#getUpdateAmbiguousTextFont}
```
public boolean getUpdateAmbiguousTextFont()
```


Determines whether the font attributes will be changed according to the character code being used.

 **Examples:** 

Shows how to update the font to match the character code being used.

```

 Document doc = new Document(getMyDir() + "Special symbol.docx");
 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Arial

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateAmbiguousTextFont(true);
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
 run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Angsana New
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty}
```
public boolean getUpdateCreatedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving.
### getUpdateFields() {#getUpdateFields}
```
public boolean getUpdateFields()
```


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

 **Examples:** 

Shows how to update all the fields in a document immediately before saving it to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
 // We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
 // each time we need them to display accurate values.
 builder.write("Page ");
 builder.insertField("PAGE", "");
 builder.write(" of ");
 builder.insertField("NUMPAGES", "");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Hello World!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
 // This is the preferable option if we know that all our fields will be up to date before saving.
 // Set the "UpdateFields" property to "true" to iterate through all the document
 // fields and update them before we save it as a PDF. This will make sure that all the fields will display
 // the most accurate values in the PDF.
 options.setUpdateFields(updateFields);

 // We can clone PdfSaveOptions objects.
 Assert.assertNotSame(options, options.deepClone());

 doc.save(getArtifactsDir() + "PdfSaveOptions.UpdateFields.pdf", options);
 
```

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseGdiEmfRenderer() {#getUseGdiEmfRenderer}
```
public boolean getUseGdiEmfRenderer()
```


Gets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

 **Remarks:** 

If set to  true  GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to  false  Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is  true .

 **Examples:** 

Shows how to choose a renderer when converting a document to .emf.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
 // If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
 // If we set the "UseGdiEmfRenderer" flag to "false", Aspose.Words will use its own metafile renderer.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.EMF);
 saveOptions.setUseGdiEmfRenderer(useGdiEmfRenderer);

 doc.save(getArtifactsDir() + "ImageSaveOptions.Renderer.emf", saveOptions);

 // The GDI+ renderer usually creates larger files.
 if (useGdiEmfRenderer)
     Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.Renderer.emf").length() < 300000);
 else
     Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.Renderer.emf").length() <= 30000);
 
```

**Returns:**
boolean - A value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.
### getUseHighQualityRendering() {#getUseHighQualityRendering}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### getVerticalResolution() {#getVerticalResolution}
```
public float getVerticalResolution()
```


Gets the vertical resolution for the generated images, in dots per inch.

 **Remarks:** 

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Returns:**
float - The vertical resolution for the generated images, in dots per inch.
### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

 **Examples:** 

Shows how to change image color with saving options property.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode/) constants. |

### setCustomTimeZoneInfo(TimeZone value) {#setCustomTimeZoneInfo-java.util.TimeZone}
```
public void setCustomTimeZoneInfo(TimeZone value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.TimeZone |  |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

 **Examples:** 

Shows how 3D effects are rendered.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render fallback shapes when saving to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean}
```
public void setExportGeneratorName(boolean value)
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setGraphicsQualityOptions(GraphicsQualityOptions value) {#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions}
```
public void setGraphicsQualityOptions(GraphicsQualityOptions value)
```


Allows to specify rendering mode and quality for the java.awt.Graphics2D object.

 **Remarks:** 

Use this property to override the Graphics settings provided by Aspose.Words engine by default.

It will take effect only when a document is being saved to an image-like format.

 **Examples:** 

Shows how to set render quality options while converting documents to image formats.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions();
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON); // SmoothingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON); // TextRenderingHint
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_COLOR_RENDERING, RenderingHints.VALUE_COLOR_RENDER_QUALITY); // CompositingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_RENDERING, RenderingHints.VALUE_RENDER_QUALITY); // CompositingQuality
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_INTERPOLATION, RenderingHints.VALUE_INTERPOLATION_BILINEAR); // InterpolationMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_FRACTIONALMETRICS, RenderingHints.VALUE_FRACTIONALMETRICS_ON); // StringFormat

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 saveOptions.setGraphicsQualityOptions(qualityOptions);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions/) | The corresponding [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions/) value. |

### setHorizontalResolution(float value) {#setHorizontalResolution-float}
```
public void setHorizontalResolution(float value)
```


Sets the horizontal resolution for the generated images, in dots per inch.

 **Remarks:** 

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The horizontal resolution for the generated images, in dots per inch. |

### setImageBrightness(float value) {#setImageBrightness-float}
```
public void setImageBrightness(float value)
```


Sets the brightness for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The brightness for the generated images. |

### setImageColorMode(int value) {#setImageColorMode-int}
```
public void setImageColorMode(int value)
```


Sets the color mode for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../com.aspose.words/imagecolormode/\#NONE).

 **Examples:** 

Shows how to set a color mode when rendering documents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 20200);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a color mode for the image that the saving operation will generate.
 // If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
 // the saving operation will apply grayscale color reduction while rendering the document.
 // If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
 // the saving operation will render the document into a monochrome image.
 // If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
 // and preserve all the document's colors in the output image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setImageColorMode(imageColorMode);

 doc.save(getArtifactsDir() + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The color mode for the generated images. The value must be one of [ImageColorMode](../../com.aspose.words/imagecolormode/) constants. |

### setImageContrast(float value) {#setImageContrast-float}
```
public void setImageContrast(float value)
```


Sets the contrast for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The contrast for the generated images. |

### setImageSize(Dimension value) {#setImageSize-java.awt.Dimension}
```
public void setImageSize(Dimension value)
```


Sets the size of a generated image in pixels.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is (0 x 0), which means that the size of the generated image will be calculated according to the size of the image in points, the specified resolution and scale.

 **Examples:** 

Shows how to render every page of a document to a separate TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 for (int i = 0; i < doc.getPageCount(); i++) {
     // Set the "PageSet" property to the number of the first page from
     // which to start rendering the document from.
     options.setPageSet(new PageSet(i));
     // Export page at 2325x5325 pixels and 600 dpi.
     options.setResolution(600f);
     options.setImageSize(new Dimension(2325, 5325));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The size of a generated image in pixels. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants. |

### setJpegQuality(int value) {#setJpegQuality-int}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the generated JPEG images.

 **Remarks:** 

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

 **Examples:** 

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the generated JPEG images. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

 **Examples:** 

Shows an option to optimize memory consumption when rendering large documents to PDF.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.PDF);

 // Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
 // at the cost of increasing the duration of the operation.
 // Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
 saveOptions.setMemoryOptimization(memoryOptimization);

 doc.save(getArtifactsDir() + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining if memory optimization should be performed before saving the document. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Allows to specify metafile rendering options.

 **Examples:** 

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```

 public void handleBinaryRasterWarnings() throws Exception {
     Document doc = new Document(getMyDir() + "WMF with image.docx");

     MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

     // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
     // it encounters a metafile, which will require raster operations to render in the output PDF.
     metafileRenderingOptions.setEmulateRasterOperations(false);

     // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
     metafileRenderingOptions.setRenderingMode(MetafileRenderingMode.VECTOR_WITH_FALLBACK);

     // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
     // to modify how that method converts the document to .PDF and applies the configuration
     // in our MetafileRenderingOptions object to the saving operation.
     PdfSaveOptions saveOptions = new PdfSaveOptions();
     saveOptions.setMetafileRenderingOptions(metafileRenderingOptions);

     HandleDocumentWarnings callback = new HandleDocumentWarnings();
     doc.setWarningCallback(callback);

     doc.save(getArtifactsDir() + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

     Assert.assertEquals(1, callback.mWarnings.getCount());
     Assert.assertEquals("'R2_XORPEN' binary raster operation is not supported.",
             callback.mWarnings.get(0).getDescription());
 }

 /// 
 /// Prints and collects formatting loss-related warnings that occur upon saving a document.
 /// 
 public static class HandleDocumentWarnings implements IWarningCallback {
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.MINOR_FORMATTING_LOSS) {
             System.out.println("Unsupported operation: " + info.getDescription());
             this.mWarnings.warning(info);
         }
     }

     public WarningInfoCollection mWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) | The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value. |

### setNumeralFormat(int value) {#setNumeralFormat-int}
```
public void setNumeralFormat(int value)
```


Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

 **Examples:** 

Shows how to set the numeral format used when saving to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setLocaleId(1025);
 builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
 // use glyphs from the U+0660 to U+0669 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.Context" to
 // look up the locale to determine what number of glyphs to use.
 // Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
 // use glyphs from the U+06F0 to U+06F9 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
 // Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
 options.setNumeralFormat(numeralFormat);

 doc.save(getArtifactsDir() + "PdfSaveOptions.SetNumeralFormat.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(60385.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191000.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPageLayout(MultiPageLayout value) {#setPageLayout-com.aspose.words.MultiPageLayout}
```
public void setPageLayout(MultiPageLayout value)
```


Sets the layout used when rendering multiple pages into a single output.

 **Remarks:** 

Use one of the factory methods of [MultiPageLayout](../../com.aspose.words/multipagelayout/) to configure this property.

For [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) the default value is [MultiPageLayout.tiffFrames()](../../com.aspose.words/multipagelayout/\#tiffFrames). For other formats the default value is [MultiPageLayout.singlePage()](../../com.aspose.words/multipagelayout/\#singlePage).

This property has effect only when saving to the following formats: [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.GIF](../../com.aspose.words/saveformat/\#GIF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.WEB\_P](../../com.aspose.words/saveformat/\#WEB-P)

 **Examples:** 

Shows how to save the document into JPG image with multi-page layout settings.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MultiPageLayout](../../com.aspose.words/multipagelayout/) | The layout used when rendering multiple pages into a single output. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

 **Remarks:** 

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

 **Examples:** 

Shows how to extract pages based on exact page ranges.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

Shows how to specify which page in a document to render as an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world! This is page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("This is page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("This is page 3.");

 Assert.assertEquals(3, doc.getPageCount());

 // When we save the document as an image, Aspose.Words only renders the first page by default.
 // We can pass a SaveOptions object to specify a different page to render.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.GIF);

 // Render every page of the document to a separate image file.
 for (int i = 1; i <= doc.getPageCount(); i++) {
     saveOptions.setPageSet(new PageSet(1));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
 }
 
```

Shows how to render one page from a document to a JPEG image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set the "PageSet" to "1" to select the second page via
 // the zero-based index to start rendering the document from.
 options.setPageSet(new PageSet(1));

 // When we save the document to the JPEG format, Aspose.Words only renders one page.
 // This image will contain one page starting from page two,
 // which will just be the second page of the original document.
 doc.save(getArtifactsDir() + "ImageSaveOptions.OnePage.jpg", options);
 
```

Shows how to render every page of a document to a separate TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 for (int i = 0; i < doc.getPageCount(); i++) {
     // Set the "PageSet" property to the number of the first page from
     // which to start rendering the document from.
     options.setPageSet(new PageSet(i));
     // Export page at 2325x5325 pixels and 600 dpi.
     options.setResolution(600f);
     options.setImageSize(new Dimension(2325, 5325));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset/) | The pages to render. |

### setPaperColor(Color value) {#setPaperColor-java.awt.Color}
```
public void setPaperColor(Color value)
```


Sets the background (paper) color for the generated images.

The default value is java.awt.Color\#getWhite().getWhite().

 **Remarks:** 

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

 **Examples:** 

Renders a page of a Word document into an image with transparent or colored background.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Times New Roman");
 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "PaperColor" property to a transparent color to apply a transparent
 // background to the document while rendering it to an image.
 imgOptions.setPaperColor(new Color(1f, 0f, 0f, .5f));

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

 // Set the "PaperColor" property to an opaque color to apply that color
 // as the background of the document as we render it to an image.
 imgOptions.setPaperColor(Color.cyan);

 doc.save(getArtifactsDir() + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The background (paper) color for the generated images. |

### setPixelFormat(int value) {#setPixelFormat-int}
```
public void setPixelFormat(int value)
```


Sets the pixel format for the generated images.

 **Remarks:** 

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat/\#FORMAT-32-BPP-ARGB).

Pixel format of the output image may differ from the set value because of work of GDI+.

 **Examples:** 

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 21000);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a pixel format for the image that the saving operation will generate.
 // Various bit per pixel rates will affect the quality and file size of the generated image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPixelFormat(imagePixelFormat);

 // We can clone ImageSaveOptions instances.
 Assert.assertNotEquals(imageSaveOptions, imageSaveOptions.deepClone());

 doc.save(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The pixel format for the generated images. The value must be one of [ImagePixelFormat](../../com.aspose.words/imagepixelformat/) constants. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.DOC](../../com.aspose.words/saveformat/\#DOC), [SaveFormat.DOT](../../com.aspose.words/saveformat/\#DOT), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value. |

### setResolution(float value) {#setResolution-float}
```
public void setResolution(float value)
```


Sets both horizontal and vertical resolution for the generated images, in dots per inch.

 **Remarks:** 

This property has effect only when saving to raster image formats.

 **Examples:** 

Shows how to specify a resolution while rendering a document to PNG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Times New Roman");
 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Resolution" property to "72" to render the document in 72dpi.
 options.setResolution(72f);
 doc.save(getArtifactsDir() + "ImageSaveOptions.Resolution.72dpi.png", options);

 // Set the "Resolution" property to "300" to render the document in 300dpi.
 options.setResolution(300f);
 doc.save(getArtifactsDir() + "ImageSaveOptions.Resolution.300dpi.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | Both horizontal and vertical resolution for the generated images, in dots per inch. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG) or vector [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF), [SaveFormat.EPS](../../com.aspose.words/saveformat/\#EPS), [SaveFormat.WEB\_P](../../com.aspose.words/saveformat/\#WEB-P), [SaveFormat.SVG](../../com.aspose.words/saveformat/\#SVG).

 **Remarks:** 

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/).

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setScale(float value) {#setScale-float}
```
public void setScale(float value)
```


Sets the zoom factor for the generated images.

 **Remarks:** 

The default value is 1.0. The value must be greater than 0.

 **Examples:** 

Shows how to render an Office Math object into an image file in the local file system.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The zoom factor for the generated images. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setThresholdForFloydSteinbergDithering(byte value) {#setThresholdForFloydSteinbergDithering-byte}
```
public void setThresholdForFloydSteinbergDithering(byte value)
```


Sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod/) is [ImageBinarizationMethod.FLOYD\_STEINBERG\_DITHERING](../../com.aspose.words/imagebinarizationmethod/\#FLOYD-STEINBERG-DITHERING).

 **Remarks:** 

The default value is 128.

 **Examples:** 

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte | The threshold that determines the value of the binarization error in the Floyd-Steinberg method. |

### setTiffBinarizationMethod(int value) {#setTiffBinarizationMethod-int}
```
public void setTiffBinarizationMethod(int value)
```


Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4).

 **Remarks:** 

The default value is [ImageBinarizationMethod.THRESHOLD](../../com.aspose.words/imagebinarizationmethod/\#THRESHOLD).

 **Examples:** 

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions/\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions/\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions/\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions/\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression/\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4). The value must be one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod/) constants. |

### setTiffCompression(int value) {#setTiffCompression-int}
```
public void setTiffCompression(int value)
```


Sets the type of compression to apply when saving generated images to the TIFF format.

 **Remarks:** 

Has effect only when saving to TIFF.

The default value is [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression/\#CCITT-4).

 **Examples:** 

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Tagged Image File Format.tiff");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 // Set the "TiffCompression" property to "TiffCompression.None" to apply no compression while saving,
 // which may result in a very large output file.
 // Set the "TiffCompression" property to "TiffCompression.Rle" to apply RLE compression
 // Set the "TiffCompression" property to "TiffCompression.Lzw" to apply LZW compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt3" to apply CCITT3 compression.
 // Set the "TiffCompression" property to "TiffCompression.Ccitt4" to apply CCITT4 compression.
 options.setTiffCompression(tiffCompression);

 doc.save(getArtifactsDir() + "ImageSaveOptions.TiffImageCompression.tiff", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of compression to apply when saving generated images to the TIFF format. The value must be one of [TiffCompression](../../com.aspose.words/tiffcompression/) constants. |

### setUpdateAmbiguousTextFont(boolean value) {#setUpdateAmbiguousTextFont-boolean}
```
public void setUpdateAmbiguousTextFont(boolean value)
```


Determines whether the font attributes will be changed according to the character code being used.

 **Examples:** 

Shows how to update the font to match the character code being used.

```

 Document doc = new Document(getMyDir() + "Special symbol.docx");
 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Arial

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateAmbiguousTextFont(true);
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
 run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Angsana New
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean}
```
public void setUpdateFields(boolean value)
```


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

 **Examples:** 

Shows how to update all the fields in a document immediately before saving it to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
 // We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
 // each time we need them to display accurate values.
 builder.write("Page ");
 builder.insertField("PAGE", "");
 builder.write(" of ");
 builder.insertField("NUMPAGES", "");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Hello World!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
 // This is the preferable option if we know that all our fields will be up to date before saving.
 // Set the "UpdateFields" property to "true" to iterate through all the document
 // fields and update them before we save it as a PDF. This will make sure that all the fields will display
 // the most accurate values in the PDF.
 options.setUpdateFields(updateFields);

 // We can clone PdfSaveOptions objects.
 Assert.assertNotSame(options, options.deepClone());

 doc.save(getArtifactsDir() + "PdfSaveOptions.UpdateFields.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseGdiEmfRenderer(boolean value) {#setUseGdiEmfRenderer-boolean}
```
public void setUseGdiEmfRenderer(boolean value)
```


Sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

 **Remarks:** 

If set to  true  GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to  false  Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is  true .

 **Examples:** 

Shows how to choose a renderer when converting a document to .emf.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
 // If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
 // If we set the "UseGdiEmfRenderer" flag to "false", Aspose.Words will use its own metafile renderer.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.EMF);
 saveOptions.setUseGdiEmfRenderer(useGdiEmfRenderer);

 doc.save(getArtifactsDir() + "ImageSaveOptions.Renderer.emf", saveOptions);

 // The GDI+ renderer usually creates larger files.
 if (useGdiEmfRenderer)
     Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.Renderer.emf").length() < 300000);
 else
     Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.Renderer.emf").length() <= 30000);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### setVerticalResolution(float value) {#setVerticalResolution-float}
```
public void setVerticalResolution(float value)
```


Sets the vertical resolution for the generated images, in dots per inch.

 **Remarks:** 

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

 **Examples:** 

Shows how to edit the image while Aspose.Words converts a document to one.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as an image, we can pass a SaveOptions object to
 // edit the image while the saving operation renders it.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.PNG);
 {
     // We can adjust these properties to change the image's brightness and contrast.
     // Both are on a 0-1 scale and are at 0.5 by default.
     options.setImageBrightness(0.3f);
     options.setImageContrast(0.7f);

     // We can adjust horizontal and vertical resolution with these properties.
     // This will affect the dimensions of the image.
     // The default value for these properties is 96.0, for a resolution of 96dpi.
     options.setHorizontalResolution(72f);
     options.setVerticalResolution(72f);

     // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
     // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
     options.setScale(96f / 72f);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.EditImage.png", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The vertical resolution for the generated images, in dots per inch. |

