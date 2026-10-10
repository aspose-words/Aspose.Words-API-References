---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words لـ Java"
description: "يحدد تدفق تخطيط النص في مربع النص في Java."
type: docs
weight: 418
url: /ar/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

يحدد تدفق تخطيط النص داخل مربع النص.

 **Examples:** 

يوضح كيفية إضافة نص إلى مربع النص وتغيير اتجاهه.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | يتم عرض النص عموديًا. |
| [HORIZONTAL](#HORIZONTAL) | يتم عرض النص أفقيًا. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | يتم عرض النص الإيديوغرافي أفقيًا. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | يتم عرض النص عموديًا. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | يتم عرض النص الإيديوغرافي عموديًا. |
| [VERTICAL](#VERTICAL) | يتم عرض النص عموديًا. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


يتم عرض النص عموديًا.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


يتم عرض النص أفقيًا.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


يتم عرض النص الإيديوغرافي أفقيًا.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


يتم عرض النص عموديًا.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


يتم عرض النص الإيديوغرافي عموديًا.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


يتم عرض النص عموديًا.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
