---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words for Java"
description: "指定相对于什么在 Java 中水平计算形状或文本框的宽度。"
type: docs
weight: 562
url: /zh/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

指定相对于什么水平计算形状或文本框的宽度。

 **Examples:** 

展示如何设置相对大小和位置。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [DEFAULT](#DEFAULT) | 默认值是 [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN)。 |
| [INNER_MARGIN](#INNER-MARGIN) | 指定宽度相对于内部边距区域的大小计算，奇数页相对于左边距区域的大小，偶数页相对于右边距区域的大小。 |
| [LEFT_MARGIN](#LEFT-MARGIN) | 指定宽度相对于左边距区域的大小计算。 |
| [MARGIN](#MARGIN) | 指定宽度相对于左、右边距之间的空间计算。 |
| [OUTER_MARGIN](#OUTER-MARGIN) | 指定宽度相对于外部边距区域的大小计算，奇数页相对于右边距区域的大小，偶数页相对于左边距区域的大小。 |
| [PAGE](#PAGE) | 指定宽度相对于页面宽度计算。 |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | 指定宽度相对于右边距区域的大小计算。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


默认值是 [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN)。

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


指定宽度相对于内部边距区域的大小计算，奇数页相对于左边距区域的大小，偶数页相对于右边距区域的大小。

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


指定宽度相对于左边距区域的大小计算。

### MARGIN {#MARGIN}
```
public static int MARGIN
```


指定宽度相对于左、右边距之间的空间计算。

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


指定宽度相对于外部边距区域的大小计算，奇数页相对于右边距区域的大小，偶数页相对于左边距区域的大小。

### PAGE {#PAGE}
```
public static int PAGE
```


指定宽度相对于页面宽度计算。

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


指定宽度相对于右边距区域的大小计算。

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalSize) {#toString-int}
```
public static String toString(int relativeHorizontalSize)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
