---
title: ImageFieldMergingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event.
type: docs
weight: 340
url: /java/com.aspose.words/imagefieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

Provides data for the [IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) event.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

This event occurs during mail merge when an image mail merge field is encountered in the document. You can respond to this event to return a file name, stream, or an java.awt.image.BufferedImage object to the mail merge engine so it is inserted into the document.

There are three properties available [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and [getImage()](../../com.aspose.words/imagefieldmergingargs\#getImage) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs\#setImage-java.awt.image.BufferedImage) to specify where the image must be taken from. Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command, then select MergeField and type Image:MyFieldName.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDocument()](#getDocument) | Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument) object for which the mail merge is performed. |
| [getDocumentFieldName()](#getDocumentFieldName) | Gets the name of the merge field as specified in the document. |
| [getField()](#getField) | Gets the object that represents the current merge field. |
| [getFieldName()](#getFieldName) | Gets the name of the merge field in the data source. |
| [getFieldValue()](#getFieldValue) | Gets the value of the field from the data source. |
| [getImage()](#getImage) | Specifies the image that the mail merge engine must insert into the document. |
| [getImageFileName()](#getImageFileName) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [getImageHeight()](#getImageHeight) | Specifies the image height for the image to insert into the document. |
| [getImageStream()](#getImageStream) |  |
| [getImageWidth()](#getImageWidth) | Specifies the image width for the image to insert into the document. |
| [getRecordIndex()](#getRecordIndex) | Gets the zero based index of the record that is being merged. |
| [getShape()](#getShape) | Specifies the shape that the mail merge engine must insert into the document. |
| [getTableName()](#getTableName) | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Sets the value of the field from the data source. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage) | Specifies the image that the mail merge engine must insert into the document. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension) | Specifies the image height for the image to insert into the document. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension) | Specifies the image width for the image to insert into the document. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape) | Specifies the shape that the mail merge engine must insert into the document. |
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
### getDocument() {#getDocument}
```
public Document getDocument()
```


Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument) object for which the mail merge is performed.

**Returns:**
[Document](../../com.aspose.words/document) - The [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument) object for which the mail merge is performed.
### getDocumentFieldName() {#getDocumentFieldName}
```
public String getDocumentFieldName()
```


Gets the name of the merge field as specified in the document.

If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [getDocumentFieldName()](../../com.aspose.words/fieldmergingargsbase\#getDocumentFieldName) returns field name without the prefix, that is "MyFieldName".

**Returns:**
java.lang.String - The name of the merge field as specified in the document.
### getField() {#getField}
```
public FieldMergeField getField()
```


Gets the object that represents the current merge field.

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - The object that represents the current merge field.
### getFieldName() {#getFieldName}
```
public String getFieldName()
```


Gets the name of the merge field in the data source.

If you have a mapping from a document field name to a different data source field name, then this is the mapped field name.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [getFieldName()](../../com.aspose.words/fieldmergingargsbase\#getFieldName) returns field name without the prefix, that is "MyFieldName".

**Returns:**
java.lang.String - The name of the merge field in the data source.
### getFieldValue() {#getFieldValue}
```
public Object getFieldValue()
```


Gets the value of the field from the data source. This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

**Returns:**
java.lang.Object - The value of the field from the data source.
### getImage() {#getImage}
```
public BufferedImage getImage()
```


Specifies the image that the mail merge engine must insert into the document.

**Returns:**
java.awt.image.BufferedImage - The corresponding java.awt.image.BufferedImage value.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Sets the file name of the image that the mail merge engine must insert into the document.

**Returns:**
java.lang.String - The file name of the image that the mail merge engine must insert into the document.
### getImageHeight() {#getImageHeight}
```
public MergeFieldImageDimension getImageHeight()
```


Specifies the image height for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value.
### getImageStream() {#getImageStream}
```
public InputStream getImageStream()
```




**Returns:**
java.io.InputStream
### getImageWidth() {#getImageWidth}
```
public MergeFieldImageDimension getImageWidth()
```


Specifies the image width for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Returns:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value.
### getRecordIndex() {#getRecordIndex}
```
public int getRecordIndex()
```


Gets the zero based index of the record that is being merged.

**Returns:**
int - The zero based index of the record that is being merged.
### getShape() {#getShape}
```
public Shape getShape()
```


Specifies the shape that the mail merge engine must insert into the document.

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Returns:**
[Shape](../../com.aspose.words/shape) - The corresponding [Shape](../../com.aspose.words/shape) value.
### getTableName() {#getTableName}
```
public String getTableName()
```


Gets the name of the data table for the current merge operation or empty string if the name is not available.

**Returns:**
java.lang.String - The name of the data table for the current merge operation or empty string if the name is not available.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setFieldValue(Object value) {#setFieldValue-java.lang.Object}
```
public void setFieldValue(Object value)
```


Sets the value of the field from the data source. This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | The value of the field from the data source. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage}
```
public void setImage(BufferedImage value)
```


Specifies the image that the mail merge engine must insert into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | The corresponding java.awt.image.BufferedImage value. |

### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Sets the file name of the image that the mail merge engine must insert into the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the image that the mail merge engine must insert into the document. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Specifies the image height for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value. |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream}
```
public void setImageStream(InputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Specifies the image width for the image to insert into the document.

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the  null  value to this property or set the [MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double) property for the instance of [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) class, returned by this property, to a negative value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | The corresponding [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) value. |

### setShape(Shape value) {#setShape-com.aspose.words.Shape}
```
public void setShape(Shape value)
```


Specifies the shape that the mail merge engine must insert into the document.

When this property is specified, the mail merge engine ignores all other properties like [getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String) or **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | The corresponding [Shape](../../com.aspose.words/shape) value. |

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

