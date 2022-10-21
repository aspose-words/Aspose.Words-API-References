---
title: XamlFlowSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  or  format.
type: docs
weight: 626
url: /java/com.aspose.words/xamlflowsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class XamlFlowSaveOptions extends SaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [XamlFlowSaveOptions()](#XamlFlowSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) format. |
| [XamlFlowSaveOptions(int saveFormat)](#XamlFlowSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getImagesFolder()](#getImagesFolder--) | Specifies the physical folder where images are saved when exporting a document to XAML format. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | Specifies the physical folder where images are saved when exporting a document to XAML format. |
| [getImagesFolderAlias()](#getImagesFolderAlias--) | Specifies the name of the folder used to construct image URIs written into an XAML document. |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct image URIs written into an XAML document. |
| [getImageSavingCallback()](#getImageSavingCallback--) | Allows to control how images are saved when a document is saved to XAML. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | Allows to control how images are saved when a document is saved to XAML. |
### XamlFlowSaveOptions() {#XamlFlowSaveOptions--}
```
public XamlFlowSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) format.

### XamlFlowSaveOptions(int saveFormat) {#XamlFlowSaveOptions-int-}
```
public XamlFlowSaveOptions(int saveFormat)
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


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/xamlflowsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/xamlflowsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) event handler.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/xamlflowsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/xamlflowsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) event handler.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getImagesFolderAlias() {#getImagesFolderAlias--}
```
public String getImagesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is not an empty string, then the image URI written to XAML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is an empty string, then the image URI written to XAML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is set to '.' (dot), then the image file name will be written to XAML without path regardless of other options.


[Image 1]: 

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String-}
```
public void setImagesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is not an empty string, then the image URI written to XAML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is an empty string, then the image URI written to XAML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/xamlflowsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/xamlflowsaveoptions\#setImagesFolderAlias-java.lang.String-) is set to '.' (dot), then the image file name will be written to XAML without path regardless of other options.


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to XAML.

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value.
### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to XAML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) | The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value. |

