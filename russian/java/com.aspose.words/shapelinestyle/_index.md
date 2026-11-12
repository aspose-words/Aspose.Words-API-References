---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words для Java"
description: "Указывает составной стиль линии объекта Shape в Java."
type: docs
weight: 614
url: /ru/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Указывает составной стиль линии для [Shape](../../com.aspose.words/shape/).

 **Examples:** 

Показывает, как изменить свойства штриха.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | Две линии одинаковой толщины. |
| [SINGLE](#SINGLE) | Одна линия. |
| [THICK_THIN](#THICK-THIN) | Две линии, одна толстая, одна тонкая. |
| [THIN_THICK](#THIN-THICK) | Две линии, одна тонкая, одна толстая. |
| [TRIPLE](#TRIPLE) | Три линии: тонкая, толстая, тонкая. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Две линии одинаковой толщины.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Одна линия.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Две линии, одна толстая, одна тонкая.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Две линии, одна тонкая, одна толстая.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Три линии: тонкая, толстая, тонкая.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeLineStyle) {#toString-int}
```
public static String toString(int shapeLineStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
