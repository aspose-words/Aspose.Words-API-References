---
title: "TabLeader"
linktitle: "TabLeader"
second_title: "Aspose.Words Java için"
description: "Java'da sekme karakterinin altında gösterilen lider çizgi tipini belirtir."
type: docs
weight: 653
url: /tr/java/com.aspose.words/tableader/
---

**Inheritance:**
java.lang.Object
```
public class TabLeader
```

Sekme karakterinin altında gösterilen lider çizgi tipini belirtir.

 **Examples:** 

Bir paragraf için özel sekme durakları nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DASHES](#DASHES) | Lider çizgi tirelerden oluşur. |
| [DOTS](#DOTS) | Lider çizgi noktalardan oluşur. |
| [HEAVY](#HEAVY) | Lider çizgi tek kalın bir çizgidir. |
| [LINE](#LINE) | Lider çizgi tek bir çizgidir. |
| [MIDDLE_DOT](#MIDDLE-DOT) | Lider çizgi orta noktalardan oluşur. |
| [NONE](#NONE) | Lider çizgi gösterilmez. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String tabLeaderName)](#fromName-java.lang.String) |  |
| [getName(int tabLeader)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabLeader)](#toString-int) |  |
### DASHES {#DASHES}
```
public static int DASHES
```


Lider çizgi tirelerden oluşur.

### DOTS {#DOTS}
```
public static int DOTS
```


Lider çizgi noktalardan oluşur.

### HEAVY {#HEAVY}
```
public static int HEAVY
```


Lider çizgi tek kalın bir çizgidir.

### LINE {#LINE}
```
public static int LINE
```


Lider çizgi tek bir çizgidir.

### MIDDLE_DOT {#MIDDLE-DOT}
```
public static int MIDDLE_DOT
```


Lider çizgi orta noktalardan oluşur.

### NONE {#NONE}
```
public static int NONE
```


Lider çizgi gösterilmez.

### length {#length}
```
public static int length
```


### fromName(String tabLeaderName) {#fromName-java.lang.String}
```
public static int fromName(String tabLeaderName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabLeaderName | java.lang.String |  |

**Returns:**
int
### getName(int tabLeader) {#getName-int}
```
public static String getName(int tabLeader)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
