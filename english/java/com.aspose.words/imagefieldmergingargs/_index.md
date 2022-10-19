---
title: ImageFieldMergingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event.
type: docs
weight: 338
url: /java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Provides data for the [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-) event.

To learn more, visit the **Mail Merge and Reporting** documentation article.

This event occurs during mail merge when an image mail merge field is encountered in the document. You can respond to this event to return a file name, stream, or an java.awt.image.BufferedImage object to the mail merge engine so it is inserted into the document.

There are three properties available [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and [getImage()](../../com.aspose.words/imagefieldmergingargs\#getImage--) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs\#setImage-java.awt.image.BufferedImage-) to specify where the image must be taken from. Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command, then select MergeField and type Image:MyFieldName.
## Methods

| Method | Description |
| --- | --- |
| [getImageFileName()](#getImageFileName--) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [getImageStream()](#getImageStream--) |  |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream-) |  |
| [getImage()](#getImage--) | Specifies the image that the mail merge engine must insert into the document. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage-) | Specifies the image that the mail merge engine must insert into the document. |
| [getShape()](#getShape--) | Specifies the shape that the mail merge engine must insert into the document. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape-) | Specifies the shape that the mail merge engine must insert into the document. |
| [getImageWidth()](#getImageWidth--) | Specifies the image width for the image to insert into the document. |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension-) | Specifies the image width for the image to insert into the document. |
| [getImageHeight()](#getImageHeight--) | Specifies the image height for the image to insert into the document. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension-) | Specifies the image height for the image to insert into the document. |
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


Sets the file name of the image that the mail merge engine must insert into the document.

**Returns:**
java.lang.String - The file name of the image that the mail merge engine must insert into the document.
### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


Sets the file name of the image that the mail merge engine must insert into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the image that the mail merge engine must insert into the document. |

### getImageStream() {#getImageStream--}
```
public InputStream getImageStream()
```




**Returns:**
java.io.InputStream
### setImageStream(InputStream value) {#setImageStream-java.io.InputStream-}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.InputStream |  |

### getImage() {#getImage--}
```
public BufferedImage getImage()
```


Specifies the image that the mail merge engine must insert into the document.

**Returns:**
java.awt.image.BufferedImage - The corresponding java.awt.image.BufferedImage value.
### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage value)
```


Specifies the image that the mail merge engine must insert into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | The corresponding java.awt.image.BufferedImage value. |

### getShape() {#getShape--}
```
public Shape getShape()
```


Specifies the shape that the mail merge engine must insert into the document.

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Returns:**
[Shape](../../com.aspose.words/shape) - The corresponding [Shape](../../com.aspose.words/shape) value.
### setShape(Shape value) {#setShape-com.aspose.words.Shape-}
```
public void setShape(Shape value)
```


Specifies the shape that the mail merge engine must insert into the document.

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | The corresponding [Shape](../../com.aspose.words/shape) value. |

### getImageWidth() {#getImageWidth--}
```
public MergeFieldImageDimension getImageWidth()
```


Specifies the image width for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the **null** value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value.
### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Specifies the image width for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the **null** value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value. |

### getImageHeight() {#getImageHeight--}
```
public MergeFieldImageDimension getImageHeight()
```


Specifies the image height for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the **null** value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value.
### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Specifies the image height for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the **null** value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value. |

