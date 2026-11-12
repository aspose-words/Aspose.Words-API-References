---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words для Java"
description: "Указывает, к чему относится вертикальное положение фигуры или текстового фрейма в Java."
type: docs
weight: 563
url: /ru/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Указывает, относительно чего определяется вертикальное положение фигуры или текстового кадра.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Указывает, что вертикальное позиционирование должно быть относительно нижнего поля текущей страницы. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Указывает, что вертикальное позиционирование должно быть относительно внутреннего поля текущей страницы. |
| [LINE](#LINE) | Не документировано. |
| [MARGIN](#MARGIN) | Указывает, что вертикальное позиционирование должно быть относительно полей страницы. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Указывает, что вертикальное позиционирование должно быть относительно внешнего поля текущей страницы. |
| [PAGE](#PAGE) | Объект расположен относительно верхнего края страницы. |
| [PARAGRAPH](#PARAGRAPH) | Объект расположен относительно верхней части абзаца, содержащего якорь. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | Значение по умолчанию — [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | Значение по умолчанию — [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Указывает, что вертикальное позиционирование должно быть относительно верхнего поля текущей страницы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Указывает, что вертикальное позиционирование должно быть относительно нижнего поля текущей страницы.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Указывает, что вертикальное позиционирование должно быть относительно внутреннего поля текущей страницы.

### LINE {#LINE}
```
public static int LINE
```


Не документировано.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Указывает, что вертикальное позиционирование должно быть относительно полей страницы.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Указывает, что вертикальное позиционирование должно быть относительно внешнего поля текущей страницы.

### PAGE {#PAGE}
```
public static int PAGE
```


Объект расположен относительно верхнего края страницы.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Объект расположен относительно верхней части абзаца, содержащего якорь.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


Значение по умолчанию — [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


Значение по умолчанию — [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Указывает, что вертикальное позиционирование должно быть относительно верхнего поля текущей страницы.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
