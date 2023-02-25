---
title: ImageSavingArgs
linktitle: ImageSavingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event in Java.
type: docs
weight: 343
url: /java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

Provides data for the [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs) event.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

By default, when Aspose.Words saves a document to HTML, it saves each image into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the [getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String), [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) and [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable) properties.

To save images into streams instead of files, use the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property.


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCurrentShape()](#getCurrentShape) | Gets the [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved. |
| [getDocument()](#getDocument) | Gets the document object that is currently being saved. |
| [getImageFileName()](#getImageFileName) | Gets the file name (without path) where the image will be saved to. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
| [hashCode()](#hashCode) |  |
| [isImageAvailable()](#isImageAvailable) | Returns  true  if the current image is available for export. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Sets the file name (without path) where the image will be saved to. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


Gets the [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved.

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document. You can use the [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) property to generate a "better" file name by examining shape properties such as [ImageData.getTitle()](../../com.aspose.words/imagedata/\#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/\#setTitle-java.lang.String)(Shape only), [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) (Shape only) and [ShapeBase.getName()](../../com.aspose.words/shapebase/\#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/\#setName-java.lang.String). Of course you can build file names using any other properties or criteria but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability use the [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable) property.

**Returns:**
[ShapeBase](../../com.aspose.words/shapebase/) - The [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved.
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the document object that is currently being saved.

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Gets the file name (without path) where the image will be saved to.

This property allows you to redefine how the image file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the image into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when exporting to HTML format. How the image file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated image file name looks like *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.


[Image 1]: 

**Returns:**
java.lang.String - The file name (without path) where the image will be saved to.
### getImageStream() {#getImageStream}
```
public OutputStream getImageStream()
```




**Returns:**
java.io.OutputStream
### getKeepImageStreamOpen() {#getKeepImageStreamOpen}
```
public boolean getKeepImageStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property after writing an image into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


Returns  true  if the current image is available for export.

Some images in the document can be unavailable, for example, because the image is linked and the link is inaccessible or does not point to a valid image. In this case Aspose.Words exports an icon with a red cross. This property returns  true  if the original image is available; returns  false  if the original image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property is always  true .

**Returns:**
boolean - \{ true  if the current image is available for export.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Sets the file name (without path) where the image will be saved to.

This property allows you to redefine how the image file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the image into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when exporting to HTML format. How the image file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated image file name looks like *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name (without path) where the image will be saved to. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property after writing an image into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

