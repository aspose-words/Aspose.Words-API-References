---
title: ShapeMarkupLanguage
second_title: Aspose.Words for Java API Reference
description: Specifies Markup language used for the shape.
type: docs
weight: 519
url: /java/com.aspose.words/shapemarkuplanguage/
---

**Inheritance:**
java.lang.Object
```
public class ShapeMarkupLanguage
```

Specifies Markup language used for the shape.
## Fields

| Field | Description |
| --- | --- |
| [DML](#DML) | Drawing Markup Language is used to define the shape. |
| [VML](#VML) | Vector Markup Language is used to define the shape. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(byte shapeMarkupLanguage)](#getName-byte-) |  |
| [toString(byte shapeMarkupLanguage)](#toString-byte-) |  |
| [fromName(String shapeMarkupLanguageName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### DML {#DML}
```
public static byte DML
```


Drawing Markup Language is used to define the shape. This is the new standard for drawing for Office Open XML which has appeared first in ECMA-376 1st edition (2006), first appeared in MS Word 2007.

### VML {#VML}
```
public static byte VML
```


Vector Markup Language is used to define the shape. A deprecated format included in Office Open XML for legacy reasons only.

### length {#length}
```
public static int length
```


### getName(byte shapeMarkupLanguage) {#getName-byte-}
```
public static String getName(byte shapeMarkupLanguage)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
### toString(byte shapeMarkupLanguage) {#toString-byte-}
```
public static String toString(byte shapeMarkupLanguage)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeMarkupLanguage | byte |  |

**Returns:**
java.lang.String
### fromName(String shapeMarkupLanguageName) {#fromName-java.lang.String-}
```
public static byte fromName(String shapeMarkupLanguageName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shapeMarkupLanguageName | java.lang.String |  |

**Returns:**
byte
### getValues() {#getValues--}
```
public static byte[] getValues()
```




**Returns:**
byte[]
