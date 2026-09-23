---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words для Java"
description: "Указывает, относительно чего в Java рассчитывается горизонтальная ширина фигуры или текстового фрейма."
type: docs
weight: 562
url: /ru/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Указывает, относительно чего рассчитывается горизонтальная ширина фигуры или текстового кадра.

 **Examples:** 

Показывает, как задать относительный размер и позицию.

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
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Указывает, что ширина рассчитывается относительно размера внутренней области поля, размера левого поля для нечётных страниц и размера правого поля для чётных страниц. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Указывает, что ширина рассчитывается относительно размера левого поля. |
| [MARGIN](#MARGIN) | Указывает, что ширина рассчитывается относительно пространства между левым и правым полями. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Указывает, что ширина рассчитывается относительно размера области внешнего поля, размера области правого поля для нечётных страниц и размера области левого поля для чётных страниц. |
| [PAGE](#PAGE) | Указывает, что ширина рассчитывается относительно ширины страницы. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Указывает, что ширина рассчитывается относительно размера области правого поля. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Указывает, что ширина рассчитывается относительно размера внутренней области поля, размера левого поля для нечётных страниц и размера правого поля для чётных страниц.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Указывает, что ширина рассчитывается относительно размера левого поля.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Указывает, что ширина рассчитывается относительно пространства между левым и правым полями.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Указывает, что ширина рассчитывается относительно размера области внешнего поля, размера области правого поля для нечётных страниц и размера области левого поля для чётных страниц.

### PAGE {#PAGE}
```
public static int PAGE
```


Указывает, что ширина рассчитывается относительно ширины страницы.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Указывает, что ширина рассчитывается относительно размера области правого поля.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
