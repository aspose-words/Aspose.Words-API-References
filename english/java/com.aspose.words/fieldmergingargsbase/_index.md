---
title: FieldMergingArgsBase
second_title: Aspose.Words for Java API Reference
description: Base class for  and .
type: docs
weight: 219
url: /java/com.aspose.words/fieldmergingargsbase/
---

**Inheritance:**
java.lang.Object
```
public abstract class FieldMergingArgsBase
```

Base class for [FieldMergingArgs](../../com.aspose.words/fieldmergingargs) and [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs).

To learn more, visit the **Mail Merge and Reporting** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldMergingArgsBase()](#FieldMergingArgsBase--) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) object for which the mail merge is performed. |
| [getDocumentFieldName()](#getDocumentFieldName--) | Gets the name of the merge field as specified in the document. |
| [getField()](#getField--) | Gets the object that represents the current merge field. |
| [getFieldName()](#getFieldName--) | Gets the name of the merge field in the data source. |
| [getFieldValue()](#getFieldValue--) | Gets the value of the field from the data source. |
| [getRecordIndex()](#getRecordIndex--) | Gets the zero based index of the record that is being merged. |
| [getTableName()](#getTableName--) | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object-) | Sets the value of the field from the data source. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FieldMergingArgsBase() {#FieldMergingArgsBase--}
```
public FieldMergingArgsBase()
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Returns the [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) object for which the mail merge is performed.

**Returns:**
[Document](../../com.aspose.words/document) - The [getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) object for which the mail merge is performed.
### getDocumentFieldName() {#getDocumentFieldName--}
```
public String getDocumentFieldName()
```


Gets the name of the merge field as specified in the document.

If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then **DocumentFieldName** returns field name without the prefix, that is "MyFieldName".

**Returns:**
java.lang.String - The name of the merge field as specified in the document.
### getField() {#getField--}
```
public FieldMergeField getField()
```


Gets the object that represents the current merge field.

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - The object that represents the current merge field.
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


Gets the name of the merge field in the data source.

If you have a mapping from a document field name to a different data source field name, then this is the mapped field name.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then **FieldName** returns field name without the prefix, that is "MyFieldName".

**Returns:**
java.lang.String - The name of the merge field in the data source.
### getFieldValue() {#getFieldValue--}
```
public Object getFieldValue()
```


Gets the value of the field from the data source. This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

**Returns:**
java.lang.Object - The value of the field from the data source.
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


Gets the zero based index of the record that is being merged.

**Returns:**
int - The zero based index of the record that is being merged.
### getTableName() {#getTableName--}
```
public String getTableName()
```


Gets the name of the data table for the current merge operation or empty string if the name is not available.

**Returns:**
java.lang.String - The name of the data table for the current merge operation or empty string if the name is not available.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFieldValue(Object value) {#setFieldValue-java.lang.Object-}
```
public void setFieldValue(Object value)
```


Sets the value of the field from the data source. This property contains a value that has just been selected from your data source for this field by the mail merge engine. You can also replace the value by setting the property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | The value of the field from the data source. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

