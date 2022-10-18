---
title: CustomXmlProperty
second_title: Aspose.Words for Java API Reference
description: Represents a single custom XML attribute or a smart tag property.
type: docs
weight: 106
url: /java/com.aspose.words/customxmlproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomXmlProperty implements Cloneable
```

Represents a single custom XML attribute or a smart tag property.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Used as an item of a [CustomXmlPropertyCollection](../../com.aspose.words/customxmlpropertycollection) collection.
## Constructors

| Constructor | Description |
| --- | --- |
| [CustomXmlProperty(String name, String uri, String value)](#CustomXmlProperty-java.lang.String-java.lang.String-java.lang.String-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Specifies the name of the custom XML attribute or smart tag property. |
| [getUri()](#getUri--) | Gets the namespace URI of the custom XML attribute or smart tag property. |
| [setUri(String value)](#setUri-java.lang.String-) | Sets the namespace URI of the custom XML attribute or smart tag property. |
| [getValue()](#getValue--) | Gets the value of the custom XML attribute or smart tag property. |
| [setValue(String value)](#setValue-java.lang.String-) | Sets the value of the custom XML attribute or smart tag property. |
### CustomXmlProperty(String name, String uri, String value) {#CustomXmlProperty-java.lang.String-java.lang.String-java.lang.String-}
```
public CustomXmlProperty(String name, String uri, String value)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. Cannot be null. |
| uri | java.lang.String | The namespace URI of the property. Cannot be null. |
| value | java.lang.String | The value of the property. Cannot be null. |

### getName() {#getName--}
```
public String getName()
```


Specifies the name of the custom XML attribute or smart tag property.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUri() {#getUri--}
```
public String getUri()
```


Gets the namespace URI of the custom XML attribute or smart tag property.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The namespace URI of the custom XML attribute or smart tag property.
### setUri(String value) {#setUri-java.lang.String-}
```
public void setUri(String value)
```


Sets the namespace URI of the custom XML attribute or smart tag property.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The namespace URI of the custom XML attribute or smart tag property. |

### getValue() {#getValue--}
```
public String getValue()
```


Gets the value of the custom XML attribute or smart tag property.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The value of the custom XML attribute or smart tag property.
### setValue(String value) {#setValue-java.lang.String-}
```
public void setValue(String value)
```


Sets the value of the custom XML attribute or smart tag property.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The value of the custom XML attribute or smart tag property. |

