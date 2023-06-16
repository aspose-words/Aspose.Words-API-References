---
title: MetafileRenderingOptions
linktitle: MetafileRenderingOptions
second_title: Aspose.Words for Java
description: Allows to specify additional metafile rendering options in Java.
type: docs
weight: 416
url: /java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Allows to specify additional metafile rendering options.

To learn more, visit the [ Handling Windows Metafiles ][Handling Windows Metafiles] documentation article.


[Handling Windows Metafiles]: https://docs.aspose.com/words/java/handling-windows-metafiles/
## Methods

| Method | Description |
| --- | --- |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode) | Gets a value determining how EMF+ Dual metafiles should be rendered. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations) | Gets a value determining whether or not the raster operations should be emulated. |
| [getRenderingMode()](#getRenderingMode) | Gets a value determining how metafile images should be rendered. |
| [getScaleWmfFontsToMetafileSize()](#getScaleWmfFontsToMetafileSize) | Gets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf) | Gets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [getUseGdiRasterOperationsEmulation()](#getUseGdiRasterOperationsEmulation) | Gets a value determining whether or not to use the GDI+ for raster operations emulation. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int) | Sets a value determining how EMF+ Dual metafiles should be rendered. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean) | Sets a value determining whether or not the raster operations should be emulated. |
| [setRenderingMode(int value)](#setRenderingMode-int) | Sets a value determining how metafile images should be rendered. |
| [setScaleWmfFontsToMetafileSize(boolean value)](#setScaleWmfFontsToMetafileSize-boolean) | Sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean) | Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [setUseGdiRasterOperationsEmulation(boolean value)](#setUseGdiRasterOperationsEmulation-boolean) | Sets a value determining whether or not to use the GDI+ for raster operations emulation. |
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode}
```
public int getEmfPlusDualRenderingMode()
```


Gets a value determining how EMF+ Dual metafiles should be rendered.

 **Remarks:** 

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

**Returns:**
int - A value determining how EMF+ Dual metafiles should be rendered. The returned value is one of [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) constants.
### getEmulateRasterOperations() {#getEmulateRasterOperations}
```
public boolean getEmulateRasterOperations()
```


Gets a value determining whether or not the raster operations should be emulated.

 **Remarks:** 

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to  true , Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to  false , Aspose.Words does not emulate the raster operations. When Aspose.Words encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Returns:**
boolean - A value determining whether or not the raster operations should be emulated.
### getRenderingMode() {#getRenderingMode}
```
public int getRenderingMode()
```


Gets a value determining how metafile images should be rendered.

 **Remarks:** 

The default value depends on the save format. For images it is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). For other formats it is [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

**Returns:**
int - A value determining how metafile images should be rendered. The returned value is one of [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) constants.
### getScaleWmfFontsToMetafileSize() {#getScaleWmfFontsToMetafileSize}
```
public boolean getScaleWmfFontsToMetafileSize()
```


Gets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

 **Remarks:** 

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to  true , Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to  false , Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Returns:**
boolean - A value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf}
```
public boolean getUseEmfEmbeddedToWmf()
```


Gets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

 **Remarks:** 

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to  true , Aspose.Words uses embedded EMF data when rendering.

When this value is set to  false , Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is  true .

**Returns:**
boolean - A value determining how WMF metafiles with embedded EMF metafiles should be rendered.
### getUseGdiRasterOperationsEmulation() {#getUseGdiRasterOperationsEmulation}
```
public boolean getUseGdiRasterOperationsEmulation()
```


Gets a value determining whether or not to use the GDI+ for raster operations emulation.

 **Remarks:** 

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to  true , Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to  false , Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is  false .

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
boolean - A value determining whether or not to use the GDI+ for raster operations emulation.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int}
```
public void setEmfPlusDualRenderingMode(int value)
```


Sets a value determining how EMF+ Dual metafiles should be rendered.

 **Remarks:** 

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode/\#EMF-PLUS-WITH-FALLBACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how EMF+ Dual metafiles should be rendered. The value must be one of [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode/) constants. |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean}
```
public void setEmulateRasterOperations(boolean value)
```


Sets a value determining whether or not the raster operations should be emulated.

 **Remarks:** 

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to  true , Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to  false , Aspose.Words does not emulate the raster operations. When Aspose.Words encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not the raster operations should be emulated. |

### setRenderingMode(int value) {#setRenderingMode-int}
```
public void setRenderingMode(int value)
```


Sets a value determining how metafile images should be rendered.

 **Remarks:** 

The default value depends on the save format. For images it is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode/\#BITMAP). For other formats it is [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode/\#VECTOR-WITH-FALLBACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how metafile images should be rendered. The value must be one of [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode/) constants. |

### setScaleWmfFontsToMetafileSize(boolean value) {#setScaleWmfFontsToMetafileSize-boolean}
```
public void setScaleWmfFontsToMetafileSize(boolean value)
```


Sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

 **Remarks:** 

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to  true , Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to  false , Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

 **Remarks:** 

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to  true , Aspose.Words uses embedded EMF data when rendering.

When this value is set to  false , Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining how WMF metafiles with embedded EMF metafiles should be rendered. |

### setUseGdiRasterOperationsEmulation(boolean value) {#setUseGdiRasterOperationsEmulation-boolean}
```
public void setUseGdiRasterOperationsEmulation(boolean value)
```


Sets a value determining whether or not to use the GDI+ for raster operations emulation.

 **Remarks:** 

Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to  true , Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to  false , Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is  false .

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use the GDI+ for raster operations emulation. |

