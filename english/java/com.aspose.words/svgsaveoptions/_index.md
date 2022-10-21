---
title: SvgSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 541
url: /java/com.aspose.words/svgsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class SvgSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getShowPageBorder()](#getShowPageBorder--) | Controls whether a border is added to the outline of the page. |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean-) | Controls whether a border is added to the outline of the page. |
| [getTextOutputMode()](#getTextOutputMode--) | Gets a value determining how text should be rendered in SVG. |
| [setTextOutputMode(int value)](#setTextOutputMode-int-) | Sets a value determining how text should be rendered in SVG. |
| [getResourcesFolder()](#getResourcesFolder--) | Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String-) | Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias--) | Specifies the name of the folder used to construct image URIs written into an SVG document. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct image URIs written into an SVG document. |
| [getExportEmbeddedImages()](#getExportEmbeddedImages--) | Specified whether images should be embedded into SVG document as base64. |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean-) | Specified whether images should be embedded into SVG document as base64. |
| [getFitToViewPort()](#getFitToViewPort--) | Specifies if the output SVG should fill the available viewport area (browser window or container). |
| [setFitToViewPort(boolean value)](#setFitToViewPort-boolean-) | Specifies if the output SVG should fill the available viewport area (browser window or container). |
| [getResourceSavingCallback()](#getResourceSavingCallback--) | Allows to control how resources (images) are saved when a document is exported to SVG format. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) | Allows to control how resources (images) are saved when a document is exported to SVG format. |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getShowPageBorder() {#getShowPageBorder--}
```
public boolean getShowPageBorder()
```


Controls whether a border is added to the outline of the page. Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### setShowPageBorder(boolean value) {#setShowPageBorder-boolean-}
```
public void setShowPageBorder(boolean value)
```


Controls whether a border is added to the outline of the page. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTextOutputMode() {#getTextOutputMode--}
```
public int getTextOutputMode()
```


Gets a value determining how text should be rendered in SVG.

Use this property to get or set the mode of how text inside a document should be rendered when saving in SVG format.

The default value is [SvgTextOutputMode.USE\_TARGET\_MACHINE\_FONTS](../../com.aspose.words/svgtextoutputmode\#USE-TARGET-MACHINE-FONTS).

**Returns:**
int - A value determining how text should be rendered in SVG. The returned value is one of [SvgTextOutputMode](../../com.aspose.words/svgtextoutputmode) constants.
### setTextOutputMode(int value) {#setTextOutputMode-int-}
```
public void setTextOutputMode(int value)
```


Sets a value determining how text should be rendered in SVG.

Use this property to get or set the mode of how text inside a document should be rendered when saving in SVG format.

The default value is [SvgTextOutputMode.USE\_TARGET\_MACHINE\_FONTS](../../com.aspose.words/svgtextoutputmode\#USE-TARGET-MACHINE-FONTS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how text should be rendered in SVG. The value must be one of [SvgTextOutputMode](../../com.aspose.words/svgtextoutputmode) constants. |

### getResourcesFolder() {#getResourcesFolder--}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/svgsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/svgsaveoptions\#setExportEmbeddedImages-boolean-) property is false.

When you save a [Document](../../com.aspose.words/document) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) property

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String-}
```
public void setResourcesFolder(String value)
```


Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/svgsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/svgsaveoptions\#setExportEmbeddedImages-boolean-) property is false.

When you save a [Document](../../com.aspose.words/document) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) property

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourcesFolderAlias() {#getResourcesFolderAlias--}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an SVG document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String-}
```
public void setResourcesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an SVG document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getExportEmbeddedImages() {#getExportEmbeddedImages--}
```
public boolean getExportEmbeddedImages()
```


Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean-}
```
public void setExportEmbeddedImages(boolean value)
```


Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFitToViewPort() {#getFitToViewPort--}
```
public boolean getFitToViewPort()
```


Specifies if the output SVG should fill the available viewport area (browser window or container). When set to true width and height of output SVG are set to 100%.

The default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setFitToViewPort(boolean value) {#setFitToViewPort-boolean-}
```
public void setFitToViewPort(boolean value)
```


Specifies if the output SVG should fill the available viewport area (browser window or container). When set to true width and height of output SVG are set to 100%.

The default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getResourceSavingCallback() {#getResourceSavingCallback--}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Allows to control how resources (images) are saved when a document is exported to SVG format.

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value.
### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Allows to control how resources (images) are saved when a document is exported to SVG format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) | The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value. |

