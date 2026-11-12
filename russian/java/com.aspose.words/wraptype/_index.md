---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words для Java"
description: "Указывает, как текст обтекает форму или изображение в Java."
type: docs
weight: 737
url: /ru/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Указывает, как текст обтекает форму или изображение.

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
| [INLINE](#INLINE) | Фигура остаётся на том же слое, что и текст, и рассматривается как символ. |
| [NONE](#NONE) | Текст не обтекает форму. |
| [SQUARE](#SQUARE) | Обтекает текст со всех сторон квадратного ограничивающего прямоугольника формы. |
| [THROUGH](#THROUGH) | То же, что и Tight, но обтекает внутри всех открытых частей формы. |
| [TIGHT](#TIGHT) | Плотно обтекает края формы, вместо обтекания ограничивающего прямоугольника. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Текст останавливается в верхней части формы и продолжается на строке под формой. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


Фигура остаётся на том же слое, что и текст, и рассматривается как символ.

### NONE {#NONE}
```
public static int NONE
```


Текст не обтекает форму. Форма размещается позади или перед текстом.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Обтекает текст со всех сторон квадратного ограничивающего прямоугольника формы.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


То же, что и Tight, но обтекает внутри всех открытых частей формы.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Плотно обтекает края формы, вместо обтекания ограничивающего прямоугольника.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Текст останавливается в верхней части формы и продолжается на строке под формой.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
