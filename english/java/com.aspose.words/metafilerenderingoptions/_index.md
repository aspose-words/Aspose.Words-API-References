---
title: MetafileRenderingOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional metafile rendering options.
type: docs
weight: 397
url: /java/com.aspose.words/metafilerenderingoptions/
---

**Inheritance:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Allows to specify additional metafile rendering options.

To learn more, visit the **Handling Windows Metafiles** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getRenderingMode()](#getRenderingMode--) | Gets a value determining how metafile images should be rendered. |
| [setRenderingMode(int value)](#setRenderingMode-int-) | Sets a value determining how metafile images should be rendered. |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode--) | Gets a value determining how EMF+ Dual metafiles should be rendered. |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int-) | Sets a value determining how EMF+ Dual metafiles should be rendered. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf--) | Gets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean-) | Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations--) | Gets a value determining whether or not the raster operations should be emulated. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean-) | Sets a value determining whether or not the raster operations should be emulated. |
| [getScaleWmfFontsToMetafileSize()](#getScaleWmfFontsToMetafileSize--) | Gets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |
| [setScaleWmfFontsToMetafileSize(boolean value)](#setScaleWmfFontsToMetafileSize-boolean-) | Sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |
### getRenderingMode() {#getRenderingMode--}
```
public int getRenderingMode()
```


Gets a value determining how metafile images should be rendered.

The default value depends on the save format. For images it is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP). For other formats it is [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**Returns:**
int - A value determining how metafile images should be rendered. The returned value is one of [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) constants.
### setRenderingMode(int value) {#setRenderingMode-int-}
```
public void setRenderingMode(int value)
```


Sets a value determining how metafile images should be rendered.

The default value depends on the save format. For images it is [MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP). For other formats it is [MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how metafile images should be rendered. The value must be one of [MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) constants. |

### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode--}
```
public int getEmfPlusDualRenderingMode()
```


Gets a value determining how EMF+ Dual metafiles should be rendered.

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**Returns:**
int - A value determining how EMF+ Dual metafiles should be rendered. The returned value is one of [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode) constants.
### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int-}
```
public void setEmfPlusDualRenderingMode(int value)
```


Sets a value determining how EMF+ Dual metafiles should be rendered.

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how EMF+ Dual metafiles should be rendered. The value must be one of [EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode) constants. |

### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf--}
```
public boolean getUseEmfEmbeddedToWmf()
```


Gets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to  true , Aspose.Words uses embedded EMF data when rendering.

When this value is set to  false , Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is  true .

**Returns:**
boolean - A value determining how WMF metafiles with embedded EMF metafiles should be rendered.
### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean-}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to  true , Aspose.Words uses embedded EMF data when rendering.

When this value is set to  false , Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining how WMF metafiles with embedded EMF metafiles should be rendered. |

### getEmulateRasterOperations() {#getEmulateRasterOperations--}
```
public boolean getEmulateRasterOperations()
```


Gets a value determining whether or not the raster operations should be emulated.

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to  true , Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to  false , Aspose.Words does not emulate the raster operations. When Aspose.Words encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Returns:**
boolean - A value determining whether or not the raster operations should be emulated.
### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean-}
```
public void setEmulateRasterOperations(boolean value)
```


Sets a value determining whether or not the raster operations should be emulated.

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to  true , Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to  false , Aspose.Words does not emulate the raster operations. When Aspose.Words encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not the raster operations should be emulated. |

### getScaleWmfFontsToMetafileSize() {#getScaleWmfFontsToMetafileSize--}
```
public boolean getScaleWmfFontsToMetafileSize()
```


Gets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to  true , Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to  false , Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Returns:**
boolean - A value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.
### setScaleWmfFontsToMetafileSize(boolean value) {#setScaleWmfFontsToMetafileSize-boolean-}
```
public void setScaleWmfFontsToMetafileSize(boolean value)
```


Sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to  true , Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to  false , Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |

