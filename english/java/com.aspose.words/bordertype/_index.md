---
title: BorderType
linktitle: BorderType
second_title: Aspose.Words for Java
description: Specifies sides of a border in Java.
type: docs
weight: 40
url: /java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Specifies sides of a border.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Examples:** 

Shows how to insert a paragraph with a top border.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Specifies the bottom border of a paragraph or a table cell. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Specifies the diagonal border in a table cell. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Specifies the diagonal border in a table cell. |
| [HORIZONTAL](#HORIZONTAL) | Specifies the horizontal border between cells in a table or between conforming paragraphs. |
| [LEFT](#LEFT) | Specifies the left border of a paragraph or a table cell. |
| [NONE](#NONE) | Default value. |
| [RIGHT](#RIGHT) | Specifies the right border of a paragraph or a table cell. |
| [TOP](#TOP) | Specifies the top border of a paragraph or a table cell. |
| [VERTICAL](#VERTICAL) | Specifies the vertical border between cells in a table. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifies the bottom border of a paragraph or a table cell.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Specifies the diagonal border in a table cell.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Specifies the diagonal border in a table cell.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Specifies the horizontal border between cells in a table or between conforming paragraphs.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifies the left border of a paragraph or a table cell.

### NONE {#NONE}
```
public static int NONE
```


Default value.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifies the right border of a paragraph or a table cell.

### TOP {#TOP}
```
public static int TOP
```


Specifies the top border of a paragraph or a table cell.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Specifies the vertical border between cells in a table.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
