---
title: RelativeHorizontalSize
linktitle: RelativeHorizontalSize
second_title: Aspose.Words for Java
description: Specifies relatively to what the width of a shape or a text frame is calculated horizontally in Java.
type: docs
weight: 553
url: /java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Specifies relatively to what the width of a shape or a text frame is calculated horizontally.

 **Examples:** 

Shows how to set relative size and position.

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
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Default value is [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Specifies that the width is calculated relatively to the inside margin area size, to the left margin area size for odd pages and to the right margin area size for even pages. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Specifies that the width is calculated relatively to the left margin area size. |
| [MARGIN](#MARGIN) | Specifies that the width is calculated relatively to the space between the left and the right margins. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Specifies that the width is calculated relatively to the outside margin area size, to the right margin area size for odd pages and to the left margin area size for even pages. |
| [PAGE](#PAGE) | Specifies that the width is calculated relatively to the page width. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Specifies that the width is calculated relatively to the right margin area size. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Specifies that the width is calculated relatively to the inside margin area size, to the left margin area size for odd pages and to the right margin area size for even pages.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Specifies that the width is calculated relatively to the left margin area size.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Specifies that the width is calculated relatively to the space between the left and the right margins.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Specifies that the width is calculated relatively to the outside margin area size, to the right margin area size for odd pages and to the left margin area size for even pages.

### PAGE {#PAGE}
```
public static int PAGE
```


Specifies that the width is calculated relatively to the page width.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Specifies that the width is calculated relatively to the right margin area size.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
