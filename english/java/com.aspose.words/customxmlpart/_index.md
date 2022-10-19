---
title: CustomXmlPart
second_title: Aspose.Words for Java API Reference
description: Represents a Custom XML Data Storage Part custom XML data within a package.
type: docs
weight: 104
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

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

A DOCX or DOC document can contain one or more Custom XML Data Storage parts. Aspose.Words preserves and allows to create and extract Custom XML Data via the [Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) collection.
## Methods

| Method | Description |
| --- | --- |
| [getId()](#getId--) | Gets the string that identifies this custom XML part within an OOXML document. |
| [setId(String value)](#setId-java.lang.String-) | Sets the string that identifies this custom XML part within an OOXML document. |
| [getSchemas()](#getSchemas--) | Specifies the set of XML schemas that are associated with this custom XML part. |
| [getData()](#getData--) | Gets the XML content of this Custom XML Data Storage Part. |
| [setData(byte[] value)](#setData-byte---) | Sets the XML content of this Custom XML Data Storage Part. |
| [deepClone()](#deepClone--) | Makes a "deep enough" copy of the object. |
| [getDataChecksum()](#getDataChecksum--) | Specifies a cyclic redundancy check (CRC) checksum of the [getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) content. |
### getId() {#getId--}
```
public String getId()
```


Gets the string that identifies this custom XML part within an OOXML document.

ISO/IEC 29500 specifies that this value is a GUID, but old versions of Microsoft Word allowed any string here. Aspose.Words does the same for ECMA-376 format. But note, that Microsoft Word Online fails to open a document created with a non-GUID value. So, a GUID is preferred value for this property.

A valid value must be an identifier that is unique among all custom XML data parts in this document.

The default value is an empty string. The value cannot be  null .

**Returns:**
java.lang.String - The string that identifies this custom XML part within an OOXML document.
### setId(String value) {#setId-java.lang.String-}
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

### getSchemas() {#getSchemas--}
```
public CustomXmlSchemaCollection getSchemas()
```


Specifies the set of XML schemas that are associated with this custom XML part.

**Returns:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection) - The corresponding [CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection) value.
### getData() {#getData--}
```
public byte[] getData()
```


Gets the XML content of this Custom XML Data Storage Part.

The default value is an empty byte array. The value cannot be  null .

**Returns:**
byte[] - The XML content of this Custom XML Data Storage Part.
### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


Sets the XML content of this Custom XML Data Storage Part.

The default value is an empty byte array. The value cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The XML content of this Custom XML Data Storage Part. |

### deepClone() {#deepClone--}
```
public CustomXmlPart deepClone()
```


Makes a "deep enough" copy of the object. Does not duplicate the bytes of the [getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) value.

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart)
### getDataChecksum() {#getDataChecksum--}
```
public long getDataChecksum()
```


Specifies a cyclic redundancy check (CRC) checksum of the [getData()](../../com.aspose.words/customxmlpart\#getData--) / [setData(byte[])](../../com.aspose.words/customxmlpart\#setData-byte---) content.

**Returns:**
long - The corresponding  long  value.
