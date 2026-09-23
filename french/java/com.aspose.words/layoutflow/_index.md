---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words pour Java"
description: "Détermine le flux de la mise en page du texte dans une zone de texte en Java."
type: docs
weight: 418
url: /fr/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Détermine le flux de la mise en page du texte dans une zone de texte.

 **Examples:** 

Montre comment ajouter du texte à une zone de texte et modifier son orientation.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Le texte est affiché verticalement. |
| [HORIZONTAL](#HORIZONTAL) | Le texte est affiché horizontalement. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | Le texte idéographique est affiché horizontalement. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Le texte est affiché verticalement. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | Le texte idéographique est affiché verticalement. |
| [VERTICAL](#VERTICAL) | Le texte est affiché verticalement. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Le texte est affiché verticalement.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Le texte est affiché horizontalement.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


Le texte idéographique est affiché horizontalement.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Le texte est affiché verticalement.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


Le texte idéographique est affiché verticalement.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Le texte est affiché verticalement.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
