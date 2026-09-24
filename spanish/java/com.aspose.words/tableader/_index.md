---
title: "TabLeader"
linktitle: "TabLeader"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de línea guía mostrada bajo el carácter de tabulación en Java."
type: docs
weight: 653
url: /es/java/com.aspose.words/tableader/
---

**Inheritance:**
java.lang.Object
```
public class TabLeader
```

Especifica el tipo de la línea de guía mostrada bajo el carácter de tabulación.

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
| [DASHES](#DASHES) | La línea guía está compuesta de guiones. |
| [DOTS](#DOTS) | La línea guía está compuesta de puntos. |
| [HEAVY](#HEAVY) | La línea guía es una única línea gruesa. |
| [LINE](#LINE) | La línea guía es una única línea. |
| [MIDDLE_DOT](#MIDDLE-DOT) | La línea guía está compuesta de puntos centrales. |
| [NONE](#NONE) | No se muestra ninguna línea guía. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tabLeaderName)](#fromName-java.lang.String) |  |
| [getName(int tabLeader)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabLeader)](#toString-int) |  |
### DASHES {#DASHES}
```
public static int DASHES
```


La línea guía está compuesta de guiones.

### DOTS {#DOTS}
```
public static int DOTS
```


La línea guía está compuesta de puntos.

### HEAVY {#HEAVY}
```
public static int HEAVY
```


La línea guía es una única línea gruesa.

### LINE {#LINE}
```
public static int LINE
```


La línea guía es una única línea.

### MIDDLE_DOT {#MIDDLE-DOT}
```
public static int MIDDLE_DOT
```


La línea guía está compuesta de puntos centrales.

### NONE {#NONE}
```
public static int NONE
```


No se muestra ninguna línea guía.

### length {#length}
```
public static int length
```


### fromName(String tabLeaderName) {#fromName-java.lang.String}
```
public static int fromName(String tabLeaderName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabLeaderName | java.lang.String |  |

**Returns:**
int
### getName(int tabLeader) {#getName-int}
```
public static String getName(int tabLeader)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tabLeader) {#toString-int}
```
public static String toString(int tabLeader)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
