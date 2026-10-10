---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает вертикальное положение шрифтов в строке в Java."
type: docs
weight: 36
url: /ru/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Указывает вертикальное положение шрифтов в строке.

 **Examples:** 

Показывает, как установить вертикальное положение шрифтов в строке.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Базовая линия регулируется автоматически. |
| [BASELINE](#BASELINE) | Выравнивается по базовой линии абзаца. |
| [BOTTOM](#BOTTOM) | Выравнивается по нижнему краю каждого шрифта. |
| [CENTER](#CENTER) | Выравнивает центральные точки каждого шрифта. |
| [TOP](#TOP) | Выравнивается по верхнему краю каждого шрифта. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Базовая линия регулируется автоматически.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Выравнивается по базовой линии абзаца.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Выравнивается по нижнему краю каждого шрифта.

### CENTER {#CENTER}
```
public static int CENTER
```


Выравнивает центральные точки каждого шрифта.

### TOP {#TOP}
```
public static int TOP
```


Выравнивается по верхнему краю каждого шрифта.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int baselineAlignment) {#toString-int}
```
public static String toString(int baselineAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
