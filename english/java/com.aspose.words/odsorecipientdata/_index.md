---
title: OdsoRecipientData
linktitle: OdsoRecipientData
second_title: Aspose.Words for Java
description: Represents information about a single record within an external data source that is to be excluded from the mail merge in Java.
type: docs
weight: 468
url: /java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Represents information about a single record within an external data source that is to be excluded from the mail merge.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

 **Remarks:** 

If a record shall be merged into a merged document, then no information is needed about that record. However, if a given record shall not be merged into a merged document, then the value of the unique key for that record shall be stored in the [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) property of this object to indicate this exclusion.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Returns a deep clone of this object. |
| [getActive()](#getActive) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. |
| [getColumn()](#getColumn) | Specifies the column within the data source that contains unique data for the current record. |
| [getHash()](#getHash) | Represents the hash code for this record. |
| [getUniqueTag()](#getUniqueTag) | Specifies the contents of a given record in the column containing unique data. |
| [setActive(boolean value)](#setActive-boolean) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. |
| [setColumn(int value)](#setColumn-int) | Specifies the column within the data source that contains unique data for the current record. |
| [setHash(int value)](#setHash-int) | Represents the hash code for this record. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Specifies the contents of a given record in the column containing unique data. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Returns a deep clone of this object.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getColumn() {#getColumn}
```
public int getColumn()
```


Specifies the column within the data source that contains unique data for the current record. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### getHash() {#getHash}
```
public int getHash()
```


Represents the hash code for this record. Sometimes Microsoft Word uses [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) of a whole record instead of a [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) value. The default value is 0.

**Returns:**
int - The corresponding  int  value.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Specifies the contents of a given record in the column containing unique data. The default value is  null .

**Returns:**
byte[] - The corresponding byte[] value.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Specifies the column within the data source that contains unique data for the current record. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Represents the hash code for this record. Sometimes Microsoft Word uses [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) of a whole record instead of a [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) value. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Specifies the contents of a given record in the column containing unique data. The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The corresponding byte[] value. |

