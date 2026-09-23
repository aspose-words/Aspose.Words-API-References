---
title: "VariationAxis"
linktitle: "VariationAxis"
second_title: "Aspose.Words for Java"
description: "在 Java 中表示 OpenType 设计变体轴标签。"
type: docs
weight: 704
url: /zh/java/com.aspose.words/variationaxis/
---

**Inheritance:**
java.lang.Object
```
public class VariationAxis
```

表示 OpenType 设计变体轴标签。 https://learn.microsoft.com/en-us/typography/opentype/spec/dvaraxisreg
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ITALIC](#ITALIC) | 罗马体/斜体轴的已注册标签。 |
| [OPTICAL_SIZE](#OPTICAL-SIZE) | 光学尺寸轴的已注册标签。 |
| [SLANT](#SLANT) | 已注册的倾斜轴标签。 |
| [WEIGHT](#WEIGHT) | 已注册的字重轴标签。 |
| [WIDTH](#WIDTH) | 已注册的宽度轴标签。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String variationAxisName)](#fromName-java.lang.String) |  |
| [getName(int variationAxis)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int variationAxis)](#toString-int) |  |
### ITALIC {#ITALIC}
```
public static int ITALIC
```


罗马体/斜体轴的已注册标签。

### OPTICAL_SIZE {#OPTICAL-SIZE}
```
public static int OPTICAL_SIZE
```


已注册的光学尺寸轴标签。注意：光学尺寸轴取代了 OpenType 大小特性。

### SLANT {#SLANT}
```
public static int SLANT
```


已注册的倾斜轴标签。

### WEIGHT {#WEIGHT}
```
public static int WEIGHT
```


已注册的字重轴标签。

### WIDTH {#WIDTH}
```
public static int WIDTH
```


已注册的宽度轴标签。

### length {#length}
```
public static int length
```


### fromName(String variationAxisName) {#fromName-java.lang.String}
```
public static int fromName(String variationAxisName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| variationAxisName | java.lang.String |  |

**Returns:**
int
### getName(int variationAxis) {#getName-int}
```
public static String getName(int variationAxis)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| variationAxis | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int variationAxis) {#toString-int}
```
public static String toString(int variationAxis)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| variationAxis | int |  |

**Returns:**
java.lang.String
