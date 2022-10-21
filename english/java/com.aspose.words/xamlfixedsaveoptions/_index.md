---
title: XamlFixedSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 625
url: /java/com.aspose.words/xamlfixedsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class XamlFixedSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat\#XAML-FIXED) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getResourcesFolder()](#getResourcesFolder--) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String-) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias--) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. |
| [getResourceSavingCallback()](#getResourceSavingCallback--) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat\#XAML-FIXED).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat\#XAML-FIXED).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getResourcesFolder() {#getResourcesFolder--}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is  null .

When you save a [Document](../../com.aspose.words/document) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) property

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String-}
```
public void setResourcesFolder(String value)
```


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is  null .

When you save a [Document](../../com.aspose.words/document) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) property

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourcesFolderAlias() {#getResourcesFolderAlias--}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String-}
```
public void setResourcesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourceSavingCallback() {#getResourceSavingCallback--}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value.
### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) | The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value. |

