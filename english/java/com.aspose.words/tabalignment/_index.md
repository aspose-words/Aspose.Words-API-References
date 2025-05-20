---
title: TabAlignment
linktitle: TabAlignment
second_title: Aspose.Words for Java
description: Specifies the alignment/type of a tab stop in Java.
type: docs
weight: 642
url: /java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

Specifies the alignment/type of a tab stop.

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
| [BAR](#BAR) | Draws a vertical bar at the tab stop position. |
| [CENTER](#CENTER) | Centers the text around the tab stop. |
| [CLEAR](#CLEAR) | Clears any tab stop in this position. |
| [DECIMAL](#DECIMAL) | Aligns the text at the decimal dot. |
| [LEFT](#LEFT) | Left-aligns the text after the tab stop. |
| [LIST](#LIST) | The tab is a delimiter between the number/bullet and text in a list item. |
| [RIGHT](#RIGHT) | Right-aligns the text at the tab stop. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


Draws a vertical bar at the tab stop position.

### CENTER {#CENTER}
```
public static int CENTER
```


Centers the text around the tab stop.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


Clears any tab stop in this position.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


Aligns the text at the decimal dot.

### LEFT {#LEFT}
```
public static int LEFT
```


Left-aligns the text after the tab stop.

### LIST {#LIST}
```
public static int LIST
```


The tab is a delimiter between the number/bullet and text in a list item.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Right-aligns the text at the tab stop.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
