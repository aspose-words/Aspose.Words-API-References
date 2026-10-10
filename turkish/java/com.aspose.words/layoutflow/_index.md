---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words Java için"
description: "Java'da bir metin kutusundaki metin düzeninin akışını belirler."
type: docs
weight: 418
url: /tr/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Metin kutusundaki metin düzeninin akışını belirler.

 **Examples:** 

Bir metin kutusuna metin eklemeyi ve yönünü değiştirmeyi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Metin dikey olarak görüntülenir. |
| [HORIZONTAL](#HORIZONTAL) | Metin yatay olarak görüntülenir. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | İdeografik metin yatay olarak görüntülenir. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Metin dikey olarak görüntülenir. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | İdeografik metin dikey olarak görüntülenir. |
| [VERTICAL](#VERTICAL) | Metin dikey olarak görüntülenir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Metin dikey olarak görüntülenir.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Metin yatay olarak görüntülenir.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


İdeografik metin yatay olarak görüntülenir.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Metin dikey olarak görüntülenir.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


İdeografik metin dikey olarak görüntülenir.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Metin dikey olarak görüntülenir.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
