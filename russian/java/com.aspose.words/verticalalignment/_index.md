---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает вертикальное выравнивание плавающей формы текстового фрейма или плавающей таблицы в Java."
type: docs
weight: 713
url: /ru/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Указывает вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы.

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
| [BOTTOM](#BOTTOM) | Указывает, что объект должен находиться в нижней части базового вертикального выравнивания. |
| [CENTER](#CENTER) | Указывает, что объект должен быть центрирован относительно базового вертикального выравнивания. |
| [DEFAULT](#DEFAULT) | То же, что [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | Не документировано. |
| [INSIDE](#INSIDE) | Указывает, что объект должен быть внутри базовой горизонтальной выравнивающей линии. |
| [NONE](#NONE) | Объект явно позиционируется, обычно с использованием его свойства **Top**. |
| [OUTSIDE](#OUTSIDE) | Указывает, что объект должен находиться за пределами базовой вертикальной выравнивающей линии. |
| [TOP](#TOP) | Указывает, что объект должен находиться в верхней части базовой вертикальной выравнивающей линии. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Указывает, что объект должен находиться в нижней части базового вертикального выравнивания.

### CENTER {#CENTER}
```
public static int CENTER
```


Указывает, что объект должен быть центрирован относительно базового вертикального выравнивания.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


То же, что [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


Не документировано. Похоже, это возможное значение для плавающих абзацев и таблиц.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Указывает, что объект должен быть внутри базовой горизонтальной выравнивающей линии.

### NONE {#NONE}
```
public static int NONE
```


Объект явно позиционируется, обычно с использованием его свойства **Top**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Указывает, что объект должен находиться за пределами базовой вертикальной выравнивающей линии.

### TOP {#TOP}
```
public static int TOP
```


Указывает, что объект должен находиться в верхней части базовой вертикальной выравнивающей линии.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
