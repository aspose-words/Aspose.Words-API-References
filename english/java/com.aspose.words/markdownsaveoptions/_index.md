---
title: MarkdownSaveOptions
second_title: Aspose.Words for Java API Reference
description: Class to specify additional options when saving a document into the  format.
type: docs
weight: 388
url: /java/com.aspose.words/markdownsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.TxtSaveOptionsBase](../../com.aspose.words/txtsaveoptionsbase)
```
public class MarkdownSaveOptions extends TxtSaveOptionsBase
```

Class to specify additional options when saving a document into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [MarkdownSaveOptions()](#MarkdownSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getTableContentAlignment()](#getTableContentAlignment--) | Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setTableContentAlignment(int value)](#setTableContentAlignment-int-) | Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getImagesFolder()](#getImagesFolder--) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getImageSavingCallback()](#getImageSavingCallback--) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64--) | Specifies whether images are saved in Base64 format to the output file. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean-) | Specifies whether images are saved in Base64 format to the output file. |
### MarkdownSaveOptions() {#MarkdownSaveOptions--}
```
public MarkdownSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getTableContentAlignment() {#getTableContentAlignment--}
```
public int getTableContentAlignment()
```


Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment\#AUTO).

**Returns:**
int - A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The returned value is one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment) constants.
### setTableContentAlignment(int value) {#setTableContentAlignment-int-}
```
public void setTableContentAlignment(int value)
```


Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The value must be one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment) constants. |

### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value.
### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) | The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value. |

### getExportImagesAsBase64() {#getExportImagesAsBase64--}
```
public boolean getExportImagesAsBase64()
```


Specifies whether images are saved in Base64 format to the output file. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean-}
```
public void setExportImagesAsBase64(boolean value)
```


Specifies whether images are saved in Base64 format to the output file. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

