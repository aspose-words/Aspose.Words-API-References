---
title: FixedPageSaveOptions
second_title: Aspose.Words for Java API Reference
description: Contains common options that can be specified when saving a document into fixed page formats PDF XPS images etc.
type: docs
weight: 272
url: /java/com.aspose.words/fixedpagesaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public abstract class FixedPageSaveOptions extends SaveOptions
```

Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS, images etc).

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getPageSet()](#getPageSet--) | Gets the pages to render. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | Sets the pages to render. |
| [getPageSavingCallback()](#getPageSavingCallback--) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getNumeralFormat()](#getNumeralFormat--) | Gets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) | Sets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | Allows to specify metafile rendering options. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | Allows to specify metafile rendering options. |
| [getJpegQuality()](#getJpegQuality--) | Gets a value determining the quality of the JPEG images inside Html document. |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Sets a value determining the quality of the JPEG images inside Html document. |
| [getColorMode()](#getColorMode--) | Gets a value determining how colors are rendered. |
| [setColorMode(int value)](#setColorMode-int-) | Sets a value determining how colors are rendered. |
| [getOptimizeOutput()](#getOptimizeOutput--) | Flag indicates whether it is required to optimize output. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Flag indicates whether it is required to optimize output. |
| [equals(Object obj)](#equals-java.lang.Object-) | Determines whether the specified object is equal in value to the current object. |
### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - The pages to render.
### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | The pages to render. |

### getPageSavingCallback() {#getPageSavingCallback--}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) value.
### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback-}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) value. |

### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


Gets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) is invoked automatically to update any changes.

**Returns:**
int - \{[NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat) constants.
### setNumeralFormat(int value) {#setNumeralFormat-int-}
```
public void setNumeralFormat(int value)
```


Sets [NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) is invoked automatically to update any changes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat) constants. |

### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Allows to specify metafile rendering options.

**Returns:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) value.
### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Allows to specify metafile rendering options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) | The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) value. |

### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Gets a value determining the quality of the JPEG images inside Html document.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Returns:**
int - A value determining the quality of the JPEG images inside Html document.
### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the JPEG images inside Html document.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the JPEG images inside Html document. |

### getColorMode() {#getColorMode--}
```
public int getColorMode()
```


Gets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode) constants.
### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode) constants. |

### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### equals(Object obj) {#equals-java.lang.Object-}
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
