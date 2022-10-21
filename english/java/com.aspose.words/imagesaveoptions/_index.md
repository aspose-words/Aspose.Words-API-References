---
title: ImageSaveOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when rendering document pages or shapes to images.
type: docs
weight: 340
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

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [ImageSaveOptions(int saveFormat)](#ImageSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. |
| [getPageSet()](#getPageSet--) | Gets the pages to render. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | Sets the pages to render. |
| [getPaperColor()](#getPaperColor--) | Gets the background (paper) color for the generated images. |
| [setPaperColor(Color value)](#setPaperColor-java.awt.Color-) | Sets the background (paper) color for the generated images. |
| [getPixelFormat()](#getPixelFormat--) | Gets the pixel format for the generated images. |
| [setPixelFormat(int value)](#setPixelFormat-int-) | Sets the pixel format for the generated images. |
| [getHorizontalResolution()](#getHorizontalResolution--) | Gets the horizontal resolution for the generated images, in dots per inch. |
| [setHorizontalResolution(float value)](#setHorizontalResolution-float-) | Sets the horizontal resolution for the generated images, in dots per inch. |
| [getVerticalResolution()](#getVerticalResolution--) | Gets the vertical resolution for the generated images, in dots per inch. |
| [setVerticalResolution(float value)](#setVerticalResolution-float-) | Sets the vertical resolution for the generated images, in dots per inch. |
| [setResolution(float value)](#setResolution-float-) | Sets both horizontal and vertical resolution for the generated images, in dots per inch. |
| [getJpegQuality()](#getJpegQuality--) | Gets a value determining the quality of the generated JPEG images. |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Sets a value determining the quality of the generated JPEG images. |
| [getTiffCompression()](#getTiffCompression--) | Gets the type of compression to apply when saving generated images to the TIFF format. |
| [setTiffCompression(int value)](#setTiffCompression-int-) | Sets the type of compression to apply when saving generated images to the TIFF format. |
| [getImageColorMode()](#getImageColorMode--) | Gets the color mode for the generated images. |
| [setImageColorMode(int value)](#setImageColorMode-int-) | Sets the color mode for the generated images. |
| [getImageBrightness()](#getImageBrightness--) | Gets the brightness for the generated images. |
| [setImageBrightness(float value)](#setImageBrightness-float-) | Sets the brightness for the generated images. |
| [getImageContrast()](#getImageContrast--) | Gets the contrast for the generated images. |
| [setImageContrast(float value)](#setImageContrast-float-) | Sets the contrast for the generated images. |
| [getScale()](#getScale--) | Gets the zoom factor for the generated images. |
| [setScale(float value)](#setScale-float-) | Sets the zoom factor for the generated images. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | Allows to specify how metafiles are treated in the rendered output. |
| [getTiffBinarizationMethod()](#getTiffBinarizationMethod--) | Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4. |
| [setTiffBinarizationMethod(int value)](#setTiffBinarizationMethod-int-) | Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4. |
| [getThresholdForFloydSteinbergDithering()](#getThresholdForFloydSteinbergDithering--) | Gets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. |
| [setThresholdForFloydSteinbergDithering(byte value)](#setThresholdForFloydSteinbergDithering-byte-) | Sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. |
| [getGraphicsQualityOptions()](#getGraphicsQualityOptions--) | Allows to specify rendering mode and quality for the java.awt.Graphics2D object. |
| [setGraphicsQualityOptions(GraphicsQualityOptions value)](#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-) | Allows to specify rendering mode and quality for the java.awt.Graphics2D object. |
| [getUseGdiEmfRenderer()](#getUseGdiEmfRenderer--) | Gets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [setUseGdiEmfRenderer(boolean value)](#setUseGdiEmfRenderer-boolean-) | Sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [deepClone()](#deepClone--) | Creates a deep clone of this object. |
### ImageSaveOptions(int saveFormat) {#ImageSaveOptions-int-}
```
public ImageSaveOptions(int saveFormat)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) or vector [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

On different platforms, the supported formats may be different. The number of other options depends on the selected format.

Also, it is possible to save to SVG both via ImageSaveOptions and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) or vector [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

On different platforms, the supported formats may be different. The number of other options depends on the selected format.

Also, it is possible to save to SVG both via ImageSaveOptions and via [SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - The pages to render.
### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | The pages to render. |

### getPaperColor() {#getPaperColor--}
```
public Color getPaperColor()
```


Gets the background (paper) color for the generated images.

The default value is .

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

**Returns:**
java.awt.Color - The background (paper) color for the generated images.
### setPaperColor(Color value) {#setPaperColor-java.awt.Color-}
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

### getPixelFormat() {#getPixelFormat--}
```
public int getPixelFormat()
```


Gets the pixel format for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

Pixel format of the output image may differ from the set value because of work of GDI+.

**Returns:**
int - The pixel format for the generated images. The returned value is one of [ImagePixelFormat](../../com.aspose.words/imagepixelformat) constants.
### setPixelFormat(int value) {#setPixelFormat-int-}
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

### getHorizontalResolution() {#getHorizontalResolution--}
```
public float getHorizontalResolution()
```


Gets the horizontal resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Returns:**
float - The horizontal resolution for the generated images, in dots per inch.
### setHorizontalResolution(float value) {#setHorizontalResolution-float-}
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

### getVerticalResolution() {#getVerticalResolution--}
```
public float getVerticalResolution()
```


Gets the vertical resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

**Returns:**
float - The vertical resolution for the generated images, in dots per inch.
### setVerticalResolution(float value) {#setVerticalResolution-float-}
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

### setResolution(float value) {#setResolution-float-}
```
public void setResolution(float value)
```


Sets both horizontal and vertical resolution for the generated images, in dots per inch.

This property has effect only when saving to raster image formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | Both horizontal and vertical resolution for the generated images, in dots per inch. |

### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Gets a value determining the quality of the generated JPEG images.

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Returns:**
int - A value determining the quality of the generated JPEG images.
### setJpegQuality(int value) {#setJpegQuality-int-}
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

### getTiffCompression() {#getTiffCompression--}
```
public int getTiffCompression()
```


Gets the type of compression to apply when saving generated images to the TIFF format.

Has effect only when saving to TIFF.

The default value is [TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**Returns:**
int - The type of compression to apply when saving generated images to the TIFF format. The returned value is one of [TiffCompression](../../com.aspose.words/tiffcompression) constants.
### setTiffCompression(int value) {#setTiffCompression-int-}
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

### getImageColorMode() {#getImageColorMode--}
```
public int getImageColorMode()
```


Gets the color mode for the generated images.

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**Returns:**
int - The color mode for the generated images. The returned value is one of [ImageColorMode](../../com.aspose.words/imagecolormode) constants.
### setImageColorMode(int value) {#setImageColorMode-int-}
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

### getImageBrightness() {#getImageBrightness--}
```
public float getImageBrightness()
```


Gets the brightness for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Returns:**
float - The brightness for the generated images.
### setImageBrightness(float value) {#setImageBrightness-float-}
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

### getImageContrast() {#getImageContrast--}
```
public float getImageContrast()
```


Gets the contrast for the generated images.

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.

**Returns:**
float - The contrast for the generated images.
### setImageContrast(float value) {#setImageContrast-float-}
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

### getScale() {#getScale--}
```
public float getScale()
```


Gets the zoom factor for the generated images. The default value is 1.0. The value must be greater than 0.

**Returns:**
float - The zoom factor for the generated images.
### setScale(float value) {#setScale-float-}
```
public void setScale(float value)
```


Sets the zoom factor for the generated images. The default value is 1.0. The value must be greater than 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The zoom factor for the generated images. |

### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
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
### getTiffBinarizationMethod() {#getTiffBinarizationMethod--}
```
public int getTiffBinarizationMethod()
```


Gets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4.

The default value is ImageBinarizationMethod.Threshold.

**Returns:**
int - Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4. The returned value is one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) constants.
### setTiffBinarizationMethod(int value) {#setTiffBinarizationMethod-int-}
```
public void setTiffBinarizationMethod(int value)
```


Sets method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4.

The default value is ImageBinarizationMethod.Threshold.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Method used while converting images to 1 bpp format when [getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) is SaveFormat.Tiff and [getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) is equal to TiffCompression.Ccitt3 or TiffCompression.Ccitt4. The value must be one of [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) constants. |

### getThresholdForFloydSteinbergDithering() {#getThresholdForFloydSteinbergDithering--}
```
public byte getThresholdForFloydSteinbergDithering()
```


Gets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) is ImageBinarizationMethod.FloydSteinbergDithering.

The default value is 128.

**Returns:**
byte - The threshold that determines the value of the binarization error in the Floyd-Steinberg method.
### setThresholdForFloydSteinbergDithering(byte value) {#setThresholdForFloydSteinbergDithering-byte-}
```
public void setThresholdForFloydSteinbergDithering(byte value)
```


Sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) is ImageBinarizationMethod.FloydSteinbergDithering.

The default value is 128.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte | The threshold that determines the value of the binarization error in the Floyd-Steinberg method. |

### getGraphicsQualityOptions() {#getGraphicsQualityOptions--}
```
public GraphicsQualityOptions getGraphicsQualityOptions()
```


Allows to specify rendering mode and quality for the java.awt.Graphics2D object.

Use this property to override the Graphics settings provided by Aspose.Words engine by default.

It will take effect only when a document is being saved to an image-like format.

**Returns:**
[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) - The corresponding [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) value.
### setGraphicsQualityOptions(GraphicsQualityOptions value) {#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-}
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

### getUseGdiEmfRenderer() {#getUseGdiEmfRenderer--}
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
### setUseGdiEmfRenderer(boolean value) {#setUseGdiEmfRenderer-boolean-}
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

### deepClone() {#deepClone--}
```
public ImageSaveOptions deepClone()
```


Creates a deep clone of this object.

**Returns:**
[ImageSaveOptions](../../com.aspose.words/imagesaveoptions)
