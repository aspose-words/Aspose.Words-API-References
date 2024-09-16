---
title: TabLeader
linktitle: TabLeader
second_title: Aspose.Words for Java
description: Specifies the type of the leader line displayed under the tab character in Java.
type: docs
weight: 604
url: /java/com.aspose.words/tableader/
---

**Inheritance:**
java.lang.Object
```
public class TabLeader
```

Specifies the type of the leader line displayed under the tab character.

 **Examples:** 

Shows how to set custom tab stops for a paragraph.

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
## Fields

| Field | Description |
| --- | --- |
| [DASHES](#DASHES) | The leader line is made up from dashes. |
| [DOTS](#DOTS) | The leader line is made up from dots. |
| [HEAVY](#HEAVY) | The leader line is a single thick line. |
| [LINE](#LINE) | The leader line is a single line. |
| [MIDDLE_DOT](#MIDDLE-DOT) | The leader line is made up from middle-dots. |
| [NONE](#NONE) | No leader line is displayed. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String tabLeaderName)](#fromName-java.lang.String) |  |
| [getName(int tabLeader)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabLeader)](#toString-int) |  |
### DASHES {#DASHES}
```
public static int DASHES
```


The leader line is made up from dashes.

### DOTS {#DOTS}
```
public static int DOTS
```


The leader line is made up from dots.

### HEAVY {#HEAVY}
```
public static int HEAVY
```


The leader line is a single thick line.

### LINE {#LINE}
```
public static int LINE
```


The leader line is a single line.

### MIDDLE_DOT {#MIDDLE-DOT}
```
public static int MIDDLE_DOT
```


The leader line is made up from middle-dots.

### NONE {#NONE}
```
public static int NONE
```


No leader line is displayed.

### length {#length}
```
public static int length
```


### fromName(String tabLeaderName) {#fromName-java.lang.String}
```
public static int fromName(String tabLeaderName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tabLeaderName | java.lang.String |  |

**Returns:**
int
### getName(int tabLeader) {#getName-int}
```
public static String getName(int tabLeader)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
