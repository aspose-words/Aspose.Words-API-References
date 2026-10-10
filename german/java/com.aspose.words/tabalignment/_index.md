---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung/Art eines Tabstopps in Java an."
type: docs
weight: 652
url: /de/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Gibt die Ausrichtung/den Typ eines Tabstopps an.

 **Examples:** 

Zeigt, wie benutzerdefinierte Tabstopps für einen Absatz festgelegt werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BAR](#BAR) | Zeichnet einen vertikalen Strich an der Tabstopp-Position. |
| [CENTER](#CENTER) | Zentriert den Text um den Tabstopp. |
| [CLEAR](#CLEAR) | Löscht jeden Tabstopp an dieser Position. |
| [DECIMAL](#DECIMAL) | Richtet den Text am Dezimalpunkt aus. |
| [LEFT](#LEFT) | Richtet den Text nach dem Tabstopp linksbündig aus. |
| [LIST](#LIST) | Der Tab ist ein Trennzeichen zwischen der Nummer/Aufzählungszeichen und dem Text in einem Listenelement. |
| [RIGHT](#RIGHT) | Richtet den Text am Tabstopp rechtsbündig aus. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Zeichnet einen vertikalen Strich an der Tabstopp-Position.

### CENTER {#CENTER}
```
public static int CENTER
```


Zentriert den Text um den Tabstopp.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Löscht jeden Tabstopp an dieser Position.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Richtet den Text am Dezimalpunkt aus.

### LEFT {#LEFT}
```
public static int LEFT
```


Richtet den Text nach dem Tabstopp linksbündig aus.

### LIST {#LIST}
```
public static int LIST
```


Der Tab ist ein Trennzeichen zwischen der Nummer/Aufzählungszeichen und dem Text in einem Listenelement.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Richtet den Text am Tabstopp rechtsbündig aus.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
