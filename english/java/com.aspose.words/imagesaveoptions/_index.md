---
title: ImageSaveOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when rendering document pages or shapes to images.
type: docs
weight: 342
url: /java/com.aspose.words/imagesaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ImageSaveOptions extends FixedPageSaveOptions implements Cloneable
```

Allows to specify additional options when rendering document pages or shapes to images.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.


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
| [getClass()](#getClass) |  |
| [getColorMode()](#getColorMode) | Gets a value determining how colors are rendered. |
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
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the generated JPEG images. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify how metafiles are treated in the rendered output. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
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
| [getTiffBinarizationMethod()](#getTiffBinarizationMethod) | Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4). |
| [getTiffCompression()](#getTiffCompression) | Gets the type of compression to apply when saving generated images to the TIFF format. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUpdateSdtContent()](#getUpdateSdtContent) | Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseGdiEmfRenderer()](#getUseGdiEmfRenderer) | Gets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getVerticalResolution()](#getVerticalResolution) | Gets the vertical resolution for the generated images, in dots per inch. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
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
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the generated JPEG images. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
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
| [setTiffBinarizationMethod(int value)](#setTiffBinarizationMethod-int) | Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4). |
| [setTiffCompression(int value)](#setTiffCompression-int) | Sets the type of compression to apply when saving generated images to the TIFF format. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean) | Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseGdiEmfRenderer(boolean value)](#setUseGdiEmfRenderer-boolean) | Sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setVerticalResolution(float value)](#setVerticalResolution-float) | Sets the vertical resolution for the generated images, in dots per inch. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String}
```
public static SaveOptions createSaveOptions(String fileName)
```


Creates a save options object of a class suitable for the file extension specified in the given file name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The extension of this file name determines the class of the save options object to create. |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions) - An object of a class that derives from [SaveOptions](../../com.aspose.words/saveoptions).
### deepClone() {#deepClone}
```
public ImageSaveOptions deepClone()
```


Creates a deep clone of this object.

**Returns:**
[ImageSaveOptions](../../com.aspose.words/imagesaveoptions)
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

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos) property is set to  true .

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode) constants.
### getDefaultTemplate() {#getDefaultTemplate}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String) is empty.

**Returns:**
java.lang.String - Path to default template (including filename).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants.
### getDmlRenderingMode() {#getDmlRenderingMode}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) constants.
### getExportGeneratorName() {#getExportGeneratorName}
```
public boolean getExportGeneratorName()
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getGraphicsQualityOptions() {#getGraphicsQualityOptions}
```
public GraphicsQualityOptions getGraphicsQualityOptions()
```


Allows to specify rendering mode and quality for the java.awt.Graphics2D object.

Use this property to override the Graphics settings provided by Aspose.Words engine by default.

It will take effect only when a document is being saved to an image-like format.

**Returns:**
[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) - The corresponding [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) value.
### getHorizontalResolution() {#getHorizontalResolution}
```
public float getHorizontalResolution()
```


Gets the horizontal resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Returns:**
float - The horizontal resolution for the generated images, in dots per inch.
### getImageBrightness() {#getImageBrightness}
```
public float getImageBrightness()
```


Gets the brightness for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Returns:**
float - The brightness for the generated images.
### getImageColorMode() {#getImageColorMode}
```
public int getImageColorMode()
```


Gets the color mode for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**Returns:**
int - The color mode for the generated images. The returned value is one of [ImageColorMode](../../com.aspose.words/imagecolormode) constants.
### getImageContrast() {#getImageContrast}
```
public float getImageContrast()
```


Gets the contrast for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Returns:**
float - The contrast for the generated images.
### getImlRenderingMode() {#getImlRenderingMode}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode) constants.
### getJpegQuality() {#getJpegQuality}
```
public int getJpegQuality()
```


Gets a value determining the quality of the generated JPEG images.

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Returns:**
int - A value determining the quality of the generated JPEG images.
### getMemoryOptimization() {#getMemoryOptimization}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is  false . Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Returns:**
boolean - Value determining if memory optimization should be performed before saving the document.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Allows to specify how metafiles are treated in the rendered output.

When [MetafileRenderingMode.VECTOR](../../com.aspose.words/metafilerenderingmode\#VECTOR) is specified, Aspose.Words renders metafile to vector graphics using its own metafile rendering engine first and then renders vector graphics to the image.

When [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP) is specified, Aspose.Words renders metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text) on the page. Aspose.Words metafile rendering engine will produce more consistent result even on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP).

**Returns:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) value.
### getNumeralFormat() {#getNumeralFormat}
```
public int getNumeralFormat()
```


Gets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout) is invoked automatically to update any changes.

**Returns:**
int - \{[NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat) constants.
### getOptimizeOutput() {#getOptimizeOutput}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getPageSavingCallback() {#getPageSavingCallback}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) value.
### getPageSet() {#getPageSet}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - The pages to render.
### getPaperColor() {#getPaperColor}
```
public Color getPaperColor()
```


Gets the background (paper) color for the generated images.

The default value is .

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

**Returns:**
java.awt.Color - The background (paper) color for the generated images.
### getPixelFormat() {#getPixelFormat}
```
public int getPixelFormat()
```


Gets the pixel format for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

Pixel format of the output image may differ from the set value because of work of GDI+.

**Returns:**
int - The pixel format for the generated images. The returned value is one of [ImagePixelFormat](../../com.aspose.words/imagepixelformat) constants.
### getPrettyFormat() {#getPrettyFormat}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is  false .

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) or vector [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

On different platforms, the supported formats may be different. The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### getScale() {#getScale}
```
public float getScale()
```


Gets the zoom factor for the generated images. The default value is 1.0. The value must be greater than 0.

**Returns:**
float - The zoom factor for the generated images.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getThresholdForFloydSteinbergDithering() {#getThresholdForFloydSteinbergDithering}
```
public byte getThresholdForFloydSteinbergDithering()
```


Gets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) is [ImageBinarizationMethod.FLOYD\_STEINBERG\_DITHERING](../../com.aspose.words/imagebinarizationmethod\#FLOYD-STEINBERG-DITHERING).

The default value is 128.

**Returns:**
byte - The threshold that determines the value of the binarization error in the Floyd-Steinberg method.
### getTiffBinarizationMethod() {#getTiffBinarizationMethod}
```
public int getTiffBinarizationMethod()
```


Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

The default value is [ImageBinarizationMethod.THRESHOLD](../../com.aspose.words/imagebinarizationmethod\#THRESHOLD).

**Returns:**
int - Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4). The returned value is one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) constants.
### getTiffCompression() {#getTiffCompression}
```
public int getTiffCompression()
```


Gets the type of compression to apply when saving generated images to the TIFF format.

Has effect only when saving to TIFF.

The default value is [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**Returns:**
int - The type of compression to apply when saving generated images to the TIFF format. The returned value is one of [TiffCompression](../../com.aspose.words/tiffcompression) constants.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty}
```
public boolean getUpdateCreatedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving.
### getUpdateFields() {#getUpdateFields}
```
public boolean getUpdateFields()
```


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true . Allows to specify whether to mimic or not MS Word behavior.

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving.
### getUpdateSdtContent() {#getUpdateSdtContent}
```
public boolean getUpdateSdtContent()
```


Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. The default value is  false .

**Returns:**
boolean - Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) and [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) formats this option is used for raster images.

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseGdiEmfRenderer() {#getUseGdiEmfRenderer}
```
public boolean getUseGdiEmfRenderer()
```


Gets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

If set to  true  GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to  false  Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is  true .

**Returns:**
boolean - A value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.
### getUseHighQualityRendering() {#getUseHighQualityRendering}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### getVerticalResolution() {#getVerticalResolution}
```
public float getVerticalResolution()
```


Gets the vertical resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Returns:**
float - The vertical resolution for the generated images, in dots per inch.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos) property is set to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode) constants. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String) is empty.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) constants. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean}
```
public void setExportGeneratorName(boolean value)
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setGraphicsQualityOptions(GraphicsQualityOptions value) {#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions}
```
public void setGraphicsQualityOptions(GraphicsQualityOptions value)
```


Allows to specify rendering mode and quality for the java.awt.Graphics2D object.

Use this property to override the Graphics settings provided by Aspose.Words engine by default.

It will take effect only when a document is being saved to an image-like format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) | The corresponding [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) value. |

### setHorizontalResolution(float value) {#setHorizontalResolution-float}
```
public void setHorizontalResolution(float value)
```


Sets the horizontal resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The horizontal resolution for the generated images, in dots per inch. |

### setImageBrightness(float value) {#setImageBrightness-float}
```
public void setImageBrightness(float value)
```


Sets the brightness for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The brightness for the generated images. |

### setImageColorMode(int value) {#setImageColorMode-int}
```
public void setImageColorMode(int value)
```


Sets the color mode for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The color mode for the generated images. The value must be one of [ImageColorMode](../../com.aspose.words/imagecolormode) constants. |

### setImageContrast(float value) {#setImageContrast-float}
```
public void setImageContrast(float value)
```


Sets the contrast for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The contrast for the generated images. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode) constants. |

### setJpegQuality(int value) {#setJpegQuality-int}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the generated JPEG images.

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the generated JPEG images. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is  false . Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining if memory optimization should be performed before saving the document. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Allows to specify metafile rendering options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) | The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) value. |

### setNumeralFormat(int value) {#setNumeralFormat-int}
```
public void setNumeralFormat(int value)
```


Sets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout) is invoked automatically to update any changes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat) constants. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) value. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | The pages to render. |

### setPaperColor(Color value) {#setPaperColor-java.awt.Color}
```
public void setPaperColor(Color value)
```


Sets the background (paper) color for the generated images.

The default value is .

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The background (paper) color for the generated images. |

### setPixelFormat(int value) {#setPixelFormat-int}
```
public void setPixelFormat(int value)
```


Sets the pixel format for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

Pixel format of the output image may differ from the set value because of work of GDI+.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The pixel format for the generated images. The value must be one of [ImagePixelFormat](../../com.aspose.words/imagepixelformat) constants. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is  false .

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) value. |

### setResolution(float value) {#setResolution-float}
```
public void setResolution(float value)
```


Sets both horizontal and vertical resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | Both horizontal and vertical resolution for the generated images, in dots per inch. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) or vector [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

On different platforms, the supported formats may be different. The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### setScale(float value) {#setScale-float}
```
public void setScale(float value)
```


Sets the zoom factor for the generated images. The default value is 1.0. The value must be greater than 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The zoom factor for the generated images. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setThresholdForFloydSteinbergDithering(byte value) {#setThresholdForFloydSteinbergDithering-byte}
```
public void setThresholdForFloydSteinbergDithering(byte value)
```


Sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) is [ImageBinarizationMethod.FLOYD\_STEINBERG\_DITHERING](../../com.aspose.words/imagebinarizationmethod\#FLOYD-STEINBERG-DITHERING).

The default value is 128.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte | The threshold that determines the value of the binarization error in the Floyd-Steinberg method. |

### setTiffBinarizationMethod(int value) {#setTiffBinarizationMethod-int}
```
public void setTiffBinarizationMethod(int value)
```


Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

The default value is [ImageBinarizationMethod.THRESHOLD](../../com.aspose.words/imagebinarizationmethod\#THRESHOLD).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int) is [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF) and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int) is equal to [TiffCompression.CCITT\_3](../../com.aspose.words/tiffcompression\#CCITT-3) or [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4). The value must be one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) constants. |

### setTiffCompression(int value) {#setTiffCompression-int}
```
public void setTiffCompression(int value)
```


Sets the type of compression to apply when saving generated images to the TIFF format.

Has effect only when saving to TIFF.

The default value is [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The type of compression to apply when saving generated images to the TIFF format. The value must be one of [TiffCompression](../../com.aspose.words/tiffcompression) constants. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date) property is updated before saving. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean}
```
public void setUpdateFields(boolean value)
```


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true . Allows to specify whether to mimic or not MS Word behavior.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date) property is updated before saving. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean}
```
public void setUpdateSdtContent(boolean value)
```


Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) and [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) formats this option is used for raster images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseGdiEmfRenderer(boolean value) {#setUseGdiEmfRenderer-boolean}
```
public void setUseGdiEmfRenderer(boolean value)
```


Sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.

If set to  true  GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics object and saved to metafile.

If set to  false  Aspose.Words metafile renderer is used. I.e. content is written directly to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### setVerticalResolution(float value) {#setVerticalResolution-float}
```
public void setVerticalResolution(float value)
```


Sets the vertical resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The vertical resolution for the generated images, in dots per inch. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

