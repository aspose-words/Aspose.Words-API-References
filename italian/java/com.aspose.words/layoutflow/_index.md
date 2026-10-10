---
title: "LayoutFlow"
linktitle: "LayoutFlow"
second_title: "Aspose.Words per Java"
description: "Determina il flusso del layout del testo in una casella di testo in Java."
type: docs
weight: 418
url: /it/java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Determina il flusso del layout del testo in una casella di testo.

 **Examples:** 

Mostra come aggiungere testo a una casella di testo e modificarne l'orientamento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Il testo è visualizzato verticalmente. |
| [HORIZONTAL](#HORIZONTAL) | Il testo è visualizzato orizzontalmente. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | Il testo ideografico è visualizzato orizzontalmente. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Il testo è visualizzato verticalmente. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | Il testo ideografico è visualizzato verticalmente. |
| [VERTICAL](#VERTICAL) | Il testo è visualizzato verticalmente. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Il testo è visualizzato verticalmente.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Il testo è visualizzato orizzontalmente.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


Il testo ideografico è visualizzato orizzontalmente.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Il testo è visualizzato verticalmente.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


Il testo ideografico è visualizzato verticalmente.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Il testo è visualizzato verticalmente.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
