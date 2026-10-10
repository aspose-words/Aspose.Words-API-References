---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words для Java"
description: "Указывает, относительно чего высота фигуры или текстового фрейма вычисляется по вертикали в Java."
type: docs
weight: 564
url: /ru/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

Указывает, относительно чего рассчитывается вертикальная высота фигуры или текстового кадра.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Указывает, что высота вычисляется относительно размера области нижнего поля. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Указывает, что высота вычисляется относительно размера внутренней области поля, относительно размера верхнего поля для нечётных страниц и относительно размера нижнего поля для чётных страниц. |
| [MARGIN](#MARGIN) | Указывает, что высота вычисляется относительно пространства между верхним и нижним полями. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Указывает, что высота вычисляется относительно размера внешней области поля, относительно размера нижнего поля для нечётных страниц и относительно размера верхнего поля для чётных страниц. |
| [PAGE](#PAGE) | Указывает, что высота вычисляется относительно высоты страницы. |
| [TOP_MARGIN](#TOP-MARGIN) | Указывает, что высота вычисляется относительно размера верхней области поля. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Указывает, что высота вычисляется относительно размера области нижнего поля.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Указывает, что высота вычисляется относительно размера внутренней области поля, относительно размера верхнего поля для нечётных страниц и относительно размера нижнего поля для чётных страниц.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Указывает, что высота вычисляется относительно пространства между верхним и нижним полями.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Указывает, что высота вычисляется относительно размера внешней области поля, относительно размера нижнего поля для нечётных страниц и относительно размера верхнего поля для чётных страниц.

### PAGE {#PAGE}
```
public static int PAGE
```


Указывает, что высота вычисляется относительно высоты страницы.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Указывает, что высота вычисляется относительно размера верхней области поля.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
