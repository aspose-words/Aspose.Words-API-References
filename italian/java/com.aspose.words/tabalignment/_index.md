---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento/tipo di una tabulazione in Java."
type: docs
weight: 652
url: /it/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Specifica l'allineamento/tipo di una tabulazione.

 **Examples:** 

Mostra come impostare tabulazioni personalizzate per un paragrafo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BAR](#BAR) | Disegna una barra verticale nella posizione della tabulazione. |
| [CENTER](#CENTER) | Centra il testo attorno alla tabulazione. |
| [CLEAR](#CLEAR) | Cancella qualsiasi tabulazione in questa posizione. |
| [DECIMAL](#DECIMAL) | Allinea il testo al punto decimale. |
| [LEFT](#LEFT) | Allinea a sinistra il testo dopo la tabulazione. |
| [LIST](#LIST) | La tabulazione è un delimitatore tra il numero/punto elenco e il testo in un elemento della lista. |
| [RIGHT](#RIGHT) | Allinea a destra il testo alla tabulazione. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Disegna una barra verticale nella posizione della tabulazione.

### CENTER {#CENTER}
```
public static int CENTER
```


Centra il testo attorno alla tabulazione.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Cancella qualsiasi tabulazione in questa posizione.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Allinea il testo al punto decimale.

### LEFT {#LEFT}
```
public static int LEFT
```


Allinea a sinistra il testo dopo la tabulazione.

### LIST {#LIST}
```
public static int LIST
```


La tabulazione è un delimitatore tra il numero/punto elenco e il testo in un elemento della lista.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Allinea a destra il testo alla tabulazione.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
