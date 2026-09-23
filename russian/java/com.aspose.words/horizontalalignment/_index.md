---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает горизонтальное выравнивание плавающей формы текстового фрейма или плавающей таблицы в Java."
type: docs
weight: 374
url: /ru/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Указывает горизонтальное выравнивание плавающей фигуры, текстовой рамки или плавающей таблицы.

 **Examples:** 

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
| [CENTER](#CENTER) | Указывает, что объект должен быть центрирован относительно базового горизонтального выравнивания. |
| [DEFAULT](#DEFAULT) | То же, что и [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Указывает, что объект должен быть внутри базовой горизонтальной выравнивающей линии. |
| [LEFT](#LEFT) | Указывает, что объект должен быть выровнен по левому краю относительно базового горизонтального выравнивания. |
| [NONE](#NONE) | Объект явно позиционируется, обычно используя его свойство **Left**. |
| [OUTSIDE](#OUTSIDE) | Указывает, что объект должен находиться за пределами базового горизонтального выравнивания. |
| [RIGHT](#RIGHT) | Указывает, что объект должен быть выровнен по правому краю относительно базового горизонтального выравнивания. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Указывает, что объект должен быть центрирован относительно базового горизонтального выравнивания.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


То же, что и [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Указывает, что объект должен быть внутри базовой горизонтальной выравнивающей линии.

### LEFT {#LEFT}
```
public static int LEFT
```


Указывает, что объект должен быть выровнен по левому краю относительно базового горизонтального выравнивания.

### NONE {#NONE}
```
public static int NONE
```


Объект явно позиционируется, обычно используя его свойство **Left**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Указывает, что объект должен находиться за пределами базового горизонтального выравнивания.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Указывает, что объект должен быть выровнен по правому краю относительно базового горизонтального выравнивания.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
