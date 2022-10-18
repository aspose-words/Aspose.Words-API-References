---
title: CustomDocumentProperties
second_title: Aspose.Words for Java API Reference
description: A collection of custom document properties.
type: docs
weight: 101
url: /java/com.aspose.words/customdocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection)
```
public class CustomDocumentProperties extends DocumentPropertyCollection
```

A collection of custom document properties.

To learn more, visit the **Work with Document Properties** documentation article.

Each [DocumentProperty](../../com.aspose.words/documentproperty) object represents a custom property of a container document.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.
## Methods

| Method | Description |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String-) | Creates a new custom document property. |
| [add(String name, int value)](#add-java.lang.String-int-) | Creates a new custom document property of the **PropertyType.Number** data type. |
| [add(String name, Date value)](#add-java.lang.String-java.util.Date-) | Creates a new custom document property of the **PropertyType.DateTime** data type. |
| [add(String name, boolean value)](#add-java.lang.String-boolean-) | Creates a new custom document property of the **PropertyType.Boolean** data type. |
| [add(String name, double value)](#add-java.lang.String-double-) | Creates a new custom document property of the **PropertyType.Float** data type. |
| [addLinkToContent(String name, String linkSource)](#addLinkToContent-java.lang.String-java.lang.String-) | Creates a new linked to content custom document property. |
### add(String name, String value) {#add-java.lang.String-java.lang.String-}
```
public DocumentProperty add(String name, String value)
```


Creates a new custom document property.  Creates a new custom document property of the **PropertyType.String** data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | java.lang.String | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object.
### add(String name, int value) {#add-java.lang.String-int-}
```
public DocumentProperty add(String name, int value)
```


Creates a new custom document property of the **PropertyType.Number** data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | int | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object.
### add(String name, Date value) {#add-java.lang.String-java.util.Date-}
```
public DocumentProperty add(String name, Date value)
```


Creates a new custom document property of the **PropertyType.DateTime** data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | java.util.Date | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object.
### add(String name, boolean value) {#add-java.lang.String-boolean-}
```
public DocumentProperty add(String name, boolean value)
```


Creates a new custom document property of the **PropertyType.Boolean** data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | boolean | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object.
### add(String name, double value) {#add-java.lang.String-double-}
```
public DocumentProperty add(String name, double value)
```


Creates a new custom document property of the **PropertyType.Float** data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | double | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object.
### addLinkToContent(String name, String linkSource) {#addLinkToContent-java.lang.String-java.lang.String-}
```
public DocumentProperty addLinkToContent(String name, String linkSource)
```


Creates a new linked to content custom document property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| linkSource | java.lang.String | The source of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty) - The newly created property object or null when the linkSource is invalid.
