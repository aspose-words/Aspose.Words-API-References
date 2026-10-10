---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación/tipo de una tabulación en Java."
type: docs
weight: 652
url: /es/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Especifica la alineación/tipo de una tabulación.

 **Examples:** 

Muestra cómo establecer tabulaciones personalizadas para un párrafo.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // If we are in a paragraph with no tab stops in this collection,
 // the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
 Assert.assertEquals(0, doc.getFirstSection().getBody().getFirstParagraph().getEffectiveTabStops().length);

 // We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
 // Each unit on this ruler is two default tab stops, which is 72 points.
 // We can add custom tab stops programmatically like this.
 TabStopCollection tabStops = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getTabStops();
 tabStops.add(72.0, TabAlignment.LEFT, TabLeader.DOTS);
 tabStops.add(216.0, TabAlignment.CENTER, TabLeader.DASHES);
 tabStops.add(360.0, TabAlignment.RIGHT, TabLeader.LINE);

 // We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
 Assert.assertEquals(3, para.getEffectiveTabStops().length);

 // Any tab characters we add will make use of the tab stops on the ruler and may,
 // depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
 para.appendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

 doc.save(getArtifactsDir() + "Paragraph.TabStops.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BAR](#BAR) | Dibuja una barra vertical en la posición de la tabulación. |
| [CENTER](#CENTER) | Centra el texto alrededor de la tabulación. |
| [CLEAR](#CLEAR) | Elimina cualquier tabulación en esta posición. |
| [DECIMAL](#DECIMAL) | Alinea el texto en el punto decimal. |
| [LEFT](#LEFT) | Alinea a la izquierda el texto después de la tabulación. |
| [LIST](#LIST) | La tabulación es un delimitador entre el número/viñeta y el texto en un elemento de lista. |
| [RIGHT](#RIGHT) | Alinea a la derecha el texto en la tabulación. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Dibuja una barra vertical en la posición de la tabulación.

### CENTER {#CENTER}
```
public static int CENTER
```


Centra el texto alrededor de la tabulación.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Elimina cualquier tabulación en esta posición.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Alinea el texto en el punto decimal.

### LEFT {#LEFT}
```
public static int LEFT
```


Alinea a la izquierda el texto después de la tabulación.

### LIST {#LIST}
```
public static int LIST
```


La tabulación es un delimitador entre el número/viñeta y el texto en un elemento de lista.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alinea a la derecha el texto en la tabulación.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tabAlignment) {#toString-int}
```
public static String toString(int tabAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
