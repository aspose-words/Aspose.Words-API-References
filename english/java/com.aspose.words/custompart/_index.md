---
title: CustomPart
second_title: Aspose.Words for Java API Reference
description: Represents a custom arbitrary content part that is not defined by the ISO/IEC 29500 standard.
type: docs
weight: 102
url: /java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

This class represents an OOXML part that is a target of an "unknown relationship". All relationships not defined within ISO/IEC 29500 are considered "unknown relationships". Unknown relationships are permitted within an Office Open XML document provided that they conform to relationship markup guidelines.

Microsoft Word preserves custom parts during open/save cycles. Some additional info can be found here http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words also roundtrips custom parts and in addition, allows to programmatically access such parts via the [CustomPart](../../com.aspose.words/custompart) and [CustomPartCollection](../../com.aspose.words/custompartcollection) objects.

Do not confuse custom parts with Custom XML Data. Use [CustomXmlPart](../../com.aspose.words/customxmlpart) if you need to access Custom XML Data.
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Gets this part's absolute name within the OOXML package or the target URL. |
| [setName(String value)](#setName-java.lang.String-) | Sets this part's absolute name within the OOXML package or the target URL. |
| [getRelationshipType()](#getRelationshipType--) | Gets the relationship type from the parent part to this custom part. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String-) | Sets the relationship type from the parent part to this custom part. |
| [isExternal()](#isExternal--) | \{ False  if this custom part is stored inside the OOXML package. |
| [isExternal(boolean value)](#isExternal-boolean-) | \{ False  if this custom part is stored inside the OOXML package. |
| [getContentType()](#getContentType--) | Specifies the content type of this custom part. |
| [setContentType(String value)](#setContentType-java.lang.String-) | Specifies the content type of this custom part. |
| [getData()](#getData--) | Contains the data of this custom part. |
| [setData(byte[] value)](#setData-byte---) | Contains the data of this custom part. |
| [deepClone()](#deepClone--) | Makes a "deep enough" copy of the object. |
### getName() {#getName--}
```
public String getName()
```


Gets this part's absolute name within the OOXML package or the target URL.

If the relationship target is internal, then this property is the absolute part name within the package. If the relationship target is external, then this property is the target URL.

The default value is an empty string. A valid value must be a non-empty string.

**Returns:**
java.lang.String - This part's absolute name within the OOXML package or the target URL.
### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets this part's absolute name within the OOXML package or the target URL.

If the relationship target is internal, then this property is the absolute part name within the package. If the relationship target is external, then this property is the target URL.

The default value is an empty string. A valid value must be a non-empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | This part's absolute name within the OOXML package or the target URL. |

### getRelationshipType() {#getRelationshipType--}
```
public String getRelationshipType()
```


Gets the relationship type from the parent part to this custom part.

The relationship type for a custom part must be "unknown" e.g. a custom relationship type, not one of the relationship types defined within ISO/IEC 29500.

The default value is an empty string. A valid value must be a non-empty string.

**Returns:**
java.lang.String - The relationship type from the parent part to this custom part.
### setRelationshipType(String value) {#setRelationshipType-java.lang.String-}
```
public void setRelationshipType(String value)
```


Sets the relationship type from the parent part to this custom part.

The relationship type for a custom part must be "unknown" e.g. a custom relationship type, not one of the relationship types defined within ISO/IEC 29500.

The default value is an empty string. A valid value must be a non-empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The relationship type from the parent part to this custom part. |

### isExternal() {#isExternal--}
```
public boolean isExternal()
```


\{ False  if this custom part is stored inside the OOXML package.  True  if this custom part is an external target.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### isExternal(boolean value) {#isExternal-boolean-}
```
public void isExternal(boolean value)
```


\{ False  if this custom part is stored inside the OOXML package.  True  if this custom part is an external target.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getContentType() {#getContentType--}
```
public String getContentType()
```


Specifies the content type of this custom part.

This property is applicable only when [isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) is  false .

The default value is an empty string. A valid value must be a non-empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setContentType(String value) {#setContentType-java.lang.String-}
```
public void setContentType(String value)
```


Specifies the content type of this custom part.

This property is applicable only when [isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) is  false .

The default value is an empty string. A valid value must be a non-empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getData() {#getData--}
```
public byte[] getData()
```


Contains the data of this custom part.

This property is applicable only when [isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) is  false .

The default value is an empty byte array. The value cannot be  null .

**Returns:**
byte[] - The corresponding byte[] value.
### setData(byte[] value) {#setData-byte---}
```
public void setData(byte[] value)
```


Contains the data of this custom part.

This property is applicable only when [isExternal()](../../com.aspose.words/custompart\#isExternal--) / [isExternal(boolean)](../../com.aspose.words/custompart\#isExternal-boolean-) is  false .

The default value is an empty byte array. The value cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | byte[] | The corresponding byte[] value. |

### deepClone() {#deepClone--}
```
public CustomPart deepClone()
```


Makes a "deep enough" copy of the object. Does not duplicate the bytes of the [getData()](../../com.aspose.words/custompart\#getData--) / [setData(byte[])](../../com.aspose.words/custompart\#setData-byte---) value.

**Returns:**
[CustomPart](../../com.aspose.words/custompart)
