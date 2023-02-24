---
title: CustomXmlPart
linktitle: CustomXmlPart
second_title: Aspose.Words for Java API Reference
description: Represents a Custom XML Data Storage Part custom XML data within a package in Java.
type: docs
weight: 105
url: /java/com.aspose.words/customxmlpart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomXmlPart implements Cloneable
```

Represents a Custom XML Data Storage Part (custom XML data within a package).

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.

A DOCX or DOC document can contain one or more Custom XML Data Storage parts. Aspose.Words preserves and allows to create and extract Custom XML Data via the [Document.getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) collection.


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Makes a "deep enough" copy of the object. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getData()](#getData) | Gets the XML content of this Custom XML Data Storage Part. |
| [getDataChecksum()](#getDataChecksum) | Specifies a cyclic redundancy check (CRC) checksum of the [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) content. |
| [getId()](#getId) | Gets the string that identifies this custom XML part within an OOXML document. |
| [getSchemas()](#getSchemas) | Specifies the set of XML schemas that are associated with this custom XML part. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setData(byte[] value)](#setData-byte) | Sets the XML content of this Custom XML Data Storage Part. |
| [setId(String value)](#setId-java.lang.String) | Sets the string that identifies this custom XML part within an OOXML document. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### deepClone() {#deepClone}
```
public CustomXmlPart deepClone()
```


Makes a "deep enough" copy of the object. Does not duplicate the bytes of the [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) value.

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart/)
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
### getData() {#getData}
```
public byte[] getData()
```


Gets the XML content of this Custom XML Data Storage Part.

The default value is an empty byte array. The value cannot be  null .

**Returns:**
byte[] - The XML content of this Custom XML Data Storage Part.
### getDataChecksum() {#getDataChecksum}
```
public long getDataChecksum()
```


Specifies a cyclic redundancy check (CRC) checksum of the [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) content.

**Returns:**
long - The corresponding  long  value.
### getId() {#getId}
```
public String getId()
```


Gets the string that identifies this custom XML part within an OOXML document.

ISO/IEC 29500 specifies that this value is a GUID, but old versions of Microsoft Word allowed any string here. Aspose.Words does the same for ECMA-376 format. But note, that Microsoft Word Online fails to open a document created with a non-GUID value. So, a GUID is preferred value for this property.

A valid value must be an identifier that is unique among all custom XML data parts in this document.

The default value is an empty string. The value cannot be  null .

**Returns:**
java.lang.String - The string that identifies this custom XML part within an OOXML document.
### getSchemas() {#getSchemas}
```
public CustomXmlSchemaCollection getSchemas()
```


Specifies the set of XML schemas that are associated with this custom XML part.

**Returns:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection/) - The corresponding [CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection/) value.
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




### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Sets the XML content of this Custom XML Data Storage Part.

The default value is an empty byte array. The value cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The XML content of this Custom XML Data Storage Part. |

### setId(String value) {#setId-java.lang.String}
```
public void setId(String value)
```


Sets the string that identifies this custom XML part within an OOXML document.

ISO/IEC 29500 specifies that this value is a GUID, but old versions of Microsoft Word allowed any string here. Aspose.Words does the same for ECMA-376 format. But note, that Microsoft Word Online fails to open a document created with a non-GUID value. So, a GUID is preferred value for this property.

A valid value must be an identifier that is unique among all custom XML data parts in this document.

The default value is an empty string. The value cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The string that identifies this custom XML part within an OOXML document. |

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

