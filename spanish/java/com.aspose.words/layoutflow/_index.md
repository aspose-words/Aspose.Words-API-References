---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words para Java"
description: "Determina el flujo del diseño de texto en un cuadro de texto en Java."
type: docs
weight: 418
url: /es/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Determina el flujo del diseño de texto en un cuadro de texto.

 **Examples:** 

Muestra cómo agregar texto a un cuadro de texto y cambiar su orientación.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | El texto se muestra verticalmente. |
| [HORIZONTAL](#HORIZONTAL) | El texto se muestra horizontalmente. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | El texto ideográfico se muestra horizontalmente. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | El texto se muestra verticalmente. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | El texto ideográfico se muestra verticalmente. |
| [VERTICAL](#VERTICAL) | El texto se muestra verticalmente. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


El texto se muestra verticalmente.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


El texto se muestra horizontalmente.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


El texto ideográfico se muestra horizontalmente.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


El texto se muestra verticalmente.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


El texto ideográfico se muestra verticalmente.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


El texto se muestra verticalmente.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
