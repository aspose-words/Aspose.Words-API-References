---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words for Java"
description: "指定在 Java 中形状或文本框的高度相对于何物进行垂直计算。"
type: docs
weight: 564
url: /zh/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

指定形状或文本框的高度相对于何物进行垂直计算。

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | 指定高度相对于底部页边距区域的大小进行计算。 |
| [DEFAULT](#DEFAULT) | 默认值为 [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN)。 |
| [INNER_MARGIN](#INNER-MARGIN) | 指定高度相对于内侧页边距区域的大小进行计算，奇数页相对于顶部页边距区域，偶数页相对于底部页边距区域。 |
| [MARGIN](#MARGIN) | 指定高度相对于顶部和底部页边距之间的空间进行计算。 |
| [OUTER_MARGIN](#OUTER-MARGIN) | 指定高度相对于外侧页边距区域的大小进行计算，奇数页相对于底部页边距区域，偶数页相对于顶部页边距区域。 |
| [PAGE](#PAGE) | 指定高度相对于页面高度进行计算。 |
| [TOP_MARGIN](#TOP-MARGIN) | 指定高度相对于顶部页边距区域的大小进行计算。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


指定高度相对于底部页边距区域的大小进行计算。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


默认值为 [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN)。

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


指定高度相对于内侧页边距区域的大小进行计算，奇数页相对于顶部页边距区域，偶数页相对于底部页边距区域。

### MARGIN {#MARGIN}
```
public static int MARGIN
```


指定高度相对于顶部和底部页边距之间的空间进行计算。

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


指定高度相对于外侧页边距区域的大小进行计算，奇数页相对于底部页边距区域，偶数页相对于顶部页边距区域。

### PAGE {#PAGE}
```
public static int PAGE
```


指定高度相对于页面高度进行计算。

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


指定高度相对于顶部页边距区域的大小进行计算。

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalSize) {#toString-int}
```
public static String toString(int relativeVerticalSize)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
