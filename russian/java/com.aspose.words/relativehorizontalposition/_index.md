---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words для Java"
description: "Указывает, к чему относительно задаётся горизонтальное положение фигуры или текстовой рамки в Java."
type: docs
weight: 561
url: /ru/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Указывает, относительно чего определяется горизонтальное положение фигуры или текстового кадра.

 **Examples:** 

Показывает, как вставить изображение и использовать его как водяной знак.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Показывает, как вставить плавающее изображение в центр страницы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CHARACTER](#CHARACTER) | Объект позиционируется относительно левой стороны абзаца. |
| [COLUMN](#COLUMN) | Объект позиционируется относительно левой стороны колонки. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию — [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Указывает, что горизонтальное позиционирование должно быть относительно внутреннего поля текущей страницы (левое поле на нечётных страницах, правое — на чётных). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Указывает, что горизонтальное позиционирование должно быть относительно левого поля страницы. |
| [MARGIN](#MARGIN) | Указывает, что горизонтальное позиционирование должно быть относительно полей страницы. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Указывает, что горизонтальное позиционирование должно быть относительно внешнего поля текущей страницы (правое поле на нечётных страницах, левое — на чётных). |
| [PAGE](#PAGE) | Объект позиционируется относительно левого края страницы. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Указывает, что горизонтальное позиционирование должно быть относительно правого поля страницы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


Объект позиционируется относительно левой стороны абзаца.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Объект позиционируется относительно левой стороны колонки.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию — [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Указывает, что горизонтальное позиционирование должно быть относительно внутреннего поля текущей страницы (левое поле на нечётных страницах, правое — на чётных).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Указывает, что горизонтальное позиционирование должно быть относительно левого поля страницы.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Указывает, что горизонтальное позиционирование должно быть относительно полей страницы.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Указывает, что горизонтальное позиционирование должно быть относительно внешнего поля текущей страницы (правое поле на нечётных страницах, левое — на чётных).

### PAGE {#PAGE}
```
public static int PAGE
```


Объект позиционируется относительно левого края страницы.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Указывает, что горизонтальное позиционирование должно быть относительно правого поля страницы.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
