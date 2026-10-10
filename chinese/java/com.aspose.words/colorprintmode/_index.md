---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中如果设备支持彩色打印时，非彩色页面的打印方式。"
type: docs
weight: 106
url: /zh/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

指定如果设备支持彩色打印时，非彩色页面的打印方式。
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | 检测到的非彩色页面将以灰度方式打印。 |
| [NORMAL](#NORMAL) | 所有页面均按照打印机的功能和设置进行打印。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


检测到的非彩色页面将以灰度方式打印。

 **Remarks:** 

对于检测到的非彩色页面，PageSettings\\#getColor().getColor() / PageSettings\\#setColor(boolean).setColor(boolean) 会自动设置为 false。如果打印机不支持彩色打印，则此设置被忽略。

### NORMAL {#NORMAL}
```
public static int NORMAL
```


所有页面均按照打印机的功能和设置进行打印。

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorPrintMode) {#toString-int}
```
public static String toString(int colorPrintMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
