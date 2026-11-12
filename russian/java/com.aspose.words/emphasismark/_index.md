---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words для Java"
description: "Указывает возможные типы знаков ударения в Java."
type: docs
weight: 187
url: /ru/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Указывает возможные типы знаков акцента.

 **Examples:** 

Показывает, как добавить дополнительный символ, отображаемый над/под глифом.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Нет знака ударения. |
| [OVER_COMMA](#OVER-COMMA) | Знак ударения — это запятая, отображаемая над текстом. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Знак ударения — это сплошной черный круг, отображаемый над текстом. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Знак ударения — это пустой белый круг, отображаемый над текстом. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Знак ударения — это сплошной черный круг, отображаемый под текстом. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Нет знака ударения.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Знак ударения — это запятая, отображаемая над текстом.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Знак ударения — это сплошной черный круг, отображаемый над текстом.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Знак ударения — это пустой белый круг, отображаемый над текстом.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Знак ударения — это сплошной черный круг, отображаемый под текстом.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
