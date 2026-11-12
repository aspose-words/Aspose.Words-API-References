---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words для Java"
description: "Указывает стороны границы в Java."
type: docs
weight: 48
url: /ru/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Указывает стороны границы.

Чтобы узнать больше, посетите статью документации [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Показывает, как вставить абзац с верхней границей.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM](#BOTTOM) | Указывает нижнюю границу абзаца или ячейки таблицы. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Указывает диагональную границу в ячейке таблицы. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Указывает диагональную границу в ячейке таблицы. |
| [HORIZONTAL](#HORIZONTAL) | Указывает горизонтальную границу между ячейками таблицы или между соответствующими абзацами. |
| [LEFT](#LEFT) | Указывает левую границу абзаца или ячейки таблицы. |
| [NONE](#NONE) | Значение по умолчанию. |
| [RIGHT](#RIGHT) | Указывает правую границу абзаца или ячейки таблицы. |
| [TOP](#TOP) | Указывает верхнюю границу абзаца или ячейки таблицы. |
| [VERTICAL](#VERTICAL) | Указывает вертикальную границу между ячейками таблицы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Указывает нижнюю границу абзаца или ячейки таблицы.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Указывает диагональную границу в ячейке таблицы.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Указывает диагональную границу в ячейке таблицы.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Указывает горизонтальную границу между ячейками таблицы или между соответствующими абзацами.

### LEFT {#LEFT}
```
public static int LEFT
```


Указывает левую границу абзаца или ячейки таблицы.

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Указывает правую границу абзаца или ячейки таблицы.

### TOP {#TOP}
```
public static int TOP
```


Указывает верхнюю границу абзаца или ячейки таблицы.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Указывает вертикальную границу между ячейками таблицы.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
