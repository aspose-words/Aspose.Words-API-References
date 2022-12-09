---
title: FieldMergingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the MergeField event.
type: docs
weight: 219
url: /java/com.aspose.words/fieldmergingargs/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class FieldMergingArgs extends FieldMergingArgsBase
```

Provides data for the **MergeField** event.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

The **MergeField** event occurs during mail merge when a simple mail merge field is encountered in the document. You can respond to this event to return text for the mail merge engine to insert into the document.


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
| [getRecordIndex()](#getRecordIndex) | Gets the zero based index of the record that is being merged. |
| [getTableName()](#getTableName) | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [getText()](#getText) | Gets the text that will be inserted into the document for the current merge field. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object) | Sets the value of the field from the data source. |
| [setText(String value)](#setText-java.lang.String) | Sets the text that will be inserted into the document for the current merge field. |
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
### getRecordIndex() {#getRecordIndex}
```
public int getRecordIndex()
```


Gets the zero based index of the record that is being merged.

**Returns:**
int - The zero based index of the record that is being merged.
### getTableName() {#getTableName}
```
public String getTableName()
```


Gets the name of the data table for the current merge operation or empty string if the name is not available.

**Returns:**
java.lang.String - The name of the data table for the current merge operation or empty string if the name is not available.
### getText() {#getText}
```
public String getText()
```


Gets the text that will be inserted into the document for the current merge field.

When your event handler is called, this property is set to  null .

If you leave Text as  null , the mail merge engine will insert [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase\#getFieldValue) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#setFieldValue-java.lang.Object) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

**Returns:**
java.lang.String - The text that will be inserted into the document for the current merge field.
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

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Sets the text that will be inserted into the document for the current merge field.

When your event handler is called, this property is set to  null .

If you leave Text as  null , the mail merge engine will insert [FieldMergingArgsBase.getFieldValue()](../../com.aspose.words/fieldmergingargsbase\#getFieldValue) / [FieldMergingArgsBase.setFieldValue(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#setFieldValue-java.lang.Object) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text that will be inserted into the document for the current merge field. |

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

