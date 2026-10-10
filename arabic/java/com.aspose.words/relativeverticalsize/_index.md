---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words لـ Java"
description: "يحدد نسبياً ما يتم حساب ارتفاع الشكل أو إطار النص عمودياً بناءً عليه في Java."
type: docs
weight: 564
url: /ar/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

يحدد نسبيًا إلى ماذا يُحسب ارتفاع الشكل أو إطار النص عموديًا.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش السفلي. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش الداخلي، إلى حجم مساحة الهامش العلوي للصفحات الفردية وإلى حجم مساحة الهامش السفلي للصفحات الزوجية. |
| [MARGIN](#MARGIN) | يحدد أن الارتفاع يُحسب نسبياً إلى المسافة بين الهامش العلوي والهامش السفلي. |
| [OUTER_MARGIN](#OUTER-MARGIN) | يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش الخارجي، إلى حجم مساحة الهامش السفلي للصفحات الفردية وإلى حجم مساحة الهامش العلوي للصفحات الزوجية. |
| [PAGE](#PAGE) | يحدد أن الارتفاع يُحسب نسبياً إلى ارتفاع الصفحة. |
| [TOP_MARGIN](#TOP-MARGIN) | يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش العلوي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش السفلي.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش الداخلي، إلى حجم مساحة الهامش العلوي للصفحات الفردية وإلى حجم مساحة الهامش السفلي للصفحات الزوجية.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


يحدد أن الارتفاع يُحسب نسبياً إلى المسافة بين الهامش العلوي والهامش السفلي.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش الخارجي، إلى حجم مساحة الهامش السفلي للصفحات الفردية وإلى حجم مساحة الهامش العلوي للصفحات الزوجية.

### PAGE {#PAGE}
```
public static int PAGE
```


يحدد أن الارتفاع يُحسب نسبياً إلى ارتفاع الصفحة.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


يحدد أن الارتفاع يُحسب نسبياً إلى حجم مساحة الهامش العلوي.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
