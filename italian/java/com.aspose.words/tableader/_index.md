---
title: "TabLeader"
linktitle: "TabLeader"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione in Java."
type: docs
weight: 653
url: /it/java/com.aspose.words/tableader/
---

**Inheritance:**
java.lang.Object
```
public class TabLeader
```

Specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione.

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
| [DASHES](#DASHES) | La linea guida è composta da trattini. |
| [DOTS](#DOTS) | La linea guida è composta da punti. |
| [HEAVY](#HEAVY) | La linea guida è una singola linea spessa. |
| [LINE](#LINE) | La linea guida è una singola linea. |
| [MIDDLE_DOT](#MIDDLE-DOT) | La linea guida è composta da punti centrali. |
| [NONE](#NONE) | Nessuna linea guida viene visualizzata. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String tabLeaderName)](#fromName-java.lang.String) |  |
| [getName(int tabLeader)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabLeader)](#toString-int) |  |
### DASHES {#DASHES}
```
public static int DASHES
```


La linea guida è composta da trattini.

### DOTS {#DOTS}
```
public static int DOTS
```


La linea guida è composta da punti.

### HEAVY {#HEAVY}
```
public static int HEAVY
```


La linea guida è una singola linea spessa.

### LINE {#LINE}
```
public static int LINE
```


La linea guida è una singola linea.

### MIDDLE_DOT {#MIDDLE-DOT}
```
public static int MIDDLE_DOT
```


La linea guida è composta da punti centrali.

### NONE {#NONE}
```
public static int NONE
```


Nessuna linea guida viene visualizzata.

### length {#length}
```
public static int length
```


### fromName(String tabLeaderName) {#fromName-java.lang.String}
```
public static int fromName(String tabLeaderName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabLeaderName | java.lang.String |  |

**Returns:**
int
### getName(int tabLeader) {#getName-int}
```
public static String getName(int tabLeader)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
