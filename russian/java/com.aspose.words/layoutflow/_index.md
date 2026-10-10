---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words для Java"
description: "Определяет поток текстовой разметки в текстовом поле в Java."
type: docs
weight: 418
url: /ru/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Определяет поток компоновки текста в текстовом поле.

 **Examples:** 

Показывает, как добавить текст в текстовое поле и изменить его ориентацию.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textbox = new Shape(doc, ShapeType.TEXT_BOX);
 textbox.setWidth(100.0);
 textbox.setHeight(100.0);
 textbox.getTextBox().setLayoutFlow(LayoutFlow.BOTTOM_TO_TOP);

 textbox.appendChild(new Paragraph(doc));
 builder.insertNode(textbox);

 builder.moveTo(textbox.getFirstParagraph());
 builder.write("This text is flipped 90 degrees to the left.");

 doc.save(getArtifactsDir() + "Drawing.TextBox.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Текст отображается вертикально. |
| [HORIZONTAL](#HORIZONTAL) | Текст отображается горизонтально. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | Идеографический текст отображается горизонтально. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Текст отображается вертикально. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | Идеографический текст отображается вертикально. |
| [VERTICAL](#VERTICAL) | Текст отображается вертикально. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Текст отображается вертикально.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Текст отображается горизонтально.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


Идеографический текст отображается горизонтально.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Текст отображается вертикально.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


Идеографический текст отображается вертикально.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Текст отображается вертикально.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int layoutFlow) {#toString-int}
```
public static String toString(int layoutFlow)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
