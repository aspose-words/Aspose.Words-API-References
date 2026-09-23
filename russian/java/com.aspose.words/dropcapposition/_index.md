---
title: "DropCapPosition"
linktitle: "DropCapPosition"
second_title: "Aspose.Words для Java"
description: "Указывает положение текста с первой буквой (drop cap) в Java."
type: docs
weight: 177
url: /ru/java/com.aspose.words/dropcapposition/
---

**Inheritance:**
java.lang.Object
```
public class DropCapPosition
```

Указывает позицию текста буквицы.

 **Examples:** 

Показывает, как создать первую букву (drop cap).

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
 builder.getFont().setSize(54.0);
 builder.writeln("L");

 builder.getFont().setSize(18.0);
 builder.writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
 builder.writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
         "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Currently, the second and third paragraphs will appear underneath the first.
 // We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
 // Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
 // outside the left-hand side page margin if our text is left-to-right.
 // Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
 // and to wrap the rest of the text around it.
 // "DropCapPosition.None" is the default state for all paragraphs.
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setDropCapPosition(dropCapPosition);

 doc.save(getArtifactsDir() + "ParagraphFormat.DropCap.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [MARGIN](#MARGIN) | Первая буква (drop cap) размещается за пределами поля текста в абзаце‑якоре. |
| [NONE](#NONE) | В абзаце нет первой буквы (drop cap). |
| [NORMAL](#NORMAL) | Первая буква (drop cap) размещается внутри поля текста в абзаце‑якоре. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String dropCapPositionName)](#fromName-java.lang.String) |  |
| [getName(int dropCapPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dropCapPosition)](#toString-int) |  |
### MARGIN {#MARGIN}
```
public static int MARGIN
```


Первая буква (drop cap) размещается за пределами поля текста в абзаце‑якоре.

### NONE {#NONE}
```
public static int NONE
```


В абзаце нет первой буквы (drop cap).

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Первая буква (drop cap) размещается внутри поля текста в абзаце‑якоре.

### length {#length}
```
public static int length
```


### fromName(String dropCapPositionName) {#fromName-java.lang.String}
```
public static int fromName(String dropCapPositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dropCapPositionName | java.lang.String |  |

**Returns:**
int
### getName(int dropCapPosition) {#getName-int}
```
public static String getName(int dropCapPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dropCapPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dropCapPosition) {#toString-int}
```
public static String toString(int dropCapPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dropCapPosition | int |  |

**Returns:**
java.lang.String
