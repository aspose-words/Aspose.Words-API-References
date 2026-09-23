---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words для Java"
description: "Указывает значения, используемые для вертикального выравнивания текста формы в Java."
type: docs
weight: 667
url: /ru/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Указывает значения, используемые для вертикального выравнивания текста в фигуре.

 **Examples:** 

Показывает, как вертикально выровнять текстовое содержимое текстового поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM](#BOTTOM) | Текст выравнивается по нижнему краю текстового поля. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Текст выравнивается по нижней базовой линии текстового поля. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Текст выравнивается по нижнему центру текстового поля. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Текст выравнивается по нижней центральной базовой линии текстового поля. |
| [MIDDLE](#MIDDLE) | Текст выравнивается по середине текстового поля. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Текст выравнивается по центральному середине текстового поля. |
| [TOP](#TOP) | Текст выравнивается по верхнему краю текстового поля. |
| [TOP_BASELINE](#TOP-BASELINE) | Текст выравнивается по верхней базовой линии текстового поля. |
| [TOP_CENTERED](#TOP-CENTERED) | Текст выравнивается по верхнему центру текстового поля. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Текст выравнивается по верхней центральной базовой линии текстового поля. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Текст выравнивается по нижнему краю текстового поля.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Текст выравнивается по нижней базовой линии текстового поля.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Текст выравнивается по нижнему центру текстового поля.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Текст выравнивается по нижней центральной базовой линии текстового поля.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Текст выравнивается по середине текстового поля.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Текст выравнивается по центральному середине текстового поля.

### TOP {#TOP}
```
public static int TOP
```


Текст выравнивается по верхнему краю текстового поля.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Текст выравнивается по верхней базовой линии текстового поля.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Текст выравнивается по верхнему центру текстового поля.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Текст выравнивается по верхней центральной базовой линии текстового поля.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
