---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words لـ Java"
description: "يحدد النسبي الذي يُحسب بناءً عليه عرض الشكل أو إطار النص أفقيًا في Java."
type: docs
weight: 562
url: /ar/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

يحدد نسبيًا إلى ماذا يُحسب عرض الشكل أو إطار النص أفقيًا.

 **Examples:** 

يظهر كيفية ضبط الحجم النسبي والموضع.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | يحدد أن العرض يُحسب نسبيًا على حجم منطقة الهامش الداخلي، وعلى حجم منطقة الهامش الأيسر للصفحات الفردية وعلى حجم منطقة الهامش الأيمن للصفحات الزوجية. |
| [LEFT_MARGIN](#LEFT-MARGIN) | يحدد أن العرض يُحسب نسبيًا على حجم منطقة الهامش الأيسر. |
| [MARGIN](#MARGIN) | يحدد أن العرض يُحسب نسويًا على المسافة بين الهامش الأيسر والهامش الأيمن. |
| [OUTER_MARGIN](#OUTER-MARGIN) | يحدد أن العرض يُحسب نسبياً إلى حجم مساحة الهامش الخارجي، إلى حجم مساحة الهامش الأيمن للصفحات الفردية وإلى حجم مساحة الهامش الأيسر للصفحات الزوجية. |
| [PAGE](#PAGE) | يحدد أن العرض يُحسب نسبياً إلى عرض الصفحة. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | يحدد أن العرض يُحسب نسبياً إلى حجم مساحة الهامش الأيمن. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


يحدد أن العرض يُحسب نسبيًا على حجم منطقة الهامش الداخلي، وعلى حجم منطقة الهامش الأيسر للصفحات الفردية وعلى حجم منطقة الهامش الأيمن للصفحات الزوجية.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


يحدد أن العرض يُحسب نسبيًا على حجم منطقة الهامش الأيسر.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


يحدد أن العرض يُحسب نسويًا على المسافة بين الهامش الأيسر والهامش الأيمن.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


يحدد أن العرض يُحسب نسبياً إلى حجم مساحة الهامش الخارجي، إلى حجم مساحة الهامش الأيمن للصفحات الفردية وإلى حجم مساحة الهامش الأيسر للصفحات الزوجية.

### PAGE {#PAGE}
```
public static int PAGE
```


يحدد أن العرض يُحسب نسبياً إلى عرض الصفحة.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


يحدد أن العرض يُحسب نسبياً إلى حجم مساحة الهامش الأيمن.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
