---
title: WatermarkType
second_title: Aspose.Words for Java API Reference
description: Specifies the watermark type.
type: docs
weight: 610
url: /java/com.aspose.words/watermarktype/
---

**Inheritance:**
java.lang.Object
```
public class WatermarkType
```

Specifies the watermark type.
## Fields

| Field | Description |
| --- | --- |
| [TEXT](#TEXT) | Indicates that the text will be used as a watermark. |
| [IMAGE](#IMAGE) | Indicates that the image will be used as a watermark. |
| [NONE](#NONE) | Indicates watermark is no set. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int watermarkType)](#getName-int-) |  |
| [toString(int watermarkType)](#toString-int-) |  |
| [fromName(String watermarkTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### TEXT {#TEXT}
```
public static int TEXT
```


Indicates that the text will be used as a watermark.

Such a watermark corresponds to a WordArt object.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Indicates that the image will be used as a watermark.

Such a watermark corresponds to a shape with image.

### NONE {#NONE}
```
public static int NONE
```


Indicates watermark is no set.

### length {#length}
```
public static int length
```


### getName(int watermarkType) {#getName-int-}
```
public static String getName(int watermarkType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
### toString(int watermarkType) {#toString-int-}
```
public static String toString(int watermarkType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkType | int |  |

**Returns:**
java.lang.String
### fromName(String watermarkTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String watermarkTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermarkTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
