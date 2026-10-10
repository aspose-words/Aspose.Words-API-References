---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words für Java"
description: "Bestimmt den Fluss des Textlayouts in einem Textfeld in Java."
type: docs
weight: 418
url: /de/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Bestimmt den Fluss des Textlayouts in einem Textfeld.

 **Examples:** 

Zeigt, wie Text zu einem Textfeld hinzugefügt und seine Ausrichtung geändert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Text wird vertikal angezeigt. |
| [HORIZONTAL](#HORIZONTAL) | Text wird horizontal angezeigt. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | Ideografischer Text wird horizontal angezeigt. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Text wird vertikal angezeigt. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | Ideografischer Text wird vertikal angezeigt. |
| [VERTICAL](#VERTICAL) | Text wird vertikal angezeigt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Text wird vertikal angezeigt.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Text wird horizontal angezeigt.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


Ideografischer Text wird horizontal angezeigt.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Text wird vertikal angezeigt.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


Ideografischer Text wird vertikal angezeigt.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Text wird vertikal angezeigt.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
