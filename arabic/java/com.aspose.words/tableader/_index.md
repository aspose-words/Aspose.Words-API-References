---
title: "TabLeader"
linktitle: "TabLeader"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع خط القائد المعروض تحت حرف التبويب في Java."
type: docs
weight: 653
url: /ar/java/com.aspose.words/tableader/
---

**Inheritance:**
java.lang.Object
```
public class TabLeader
```

يحدد نوع خط القائد المعروض تحت حرف التبويب.

 **Examples:** 

يوضح كيفية تعيين علامات تبويب مخصصة لفقرة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [DASHES](#DASHES) | خط القائد مكوّن من شرطات. |
| [DOTS](#DOTS) | خط القائد مكوّن من نقاط. |
| [HEAVY](#HEAVY) | خط القائد هو خط سميك واحد. |
| [LINE](#LINE) | خط القائد هو خط واحد. |
| [MIDDLE_DOT](#MIDDLE-DOT) | خط القائد مكوّن من نقاط وسطية. |
| [NONE](#NONE) | لا يتم عرض خط القائد. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String tabLeaderName)](#fromName-java.lang.String) |  |
| [getName(int tabLeader)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabLeader)](#toString-int) |  |
### DASHES {#DASHES}
```
public static int DASHES
```


خط القائد مكوّن من شرطات.

### DOTS {#DOTS}
```
public static int DOTS
```


خط القائد مكوّن من نقاط.

### HEAVY {#HEAVY}
```
public static int HEAVY
```


خط القائد هو خط سميك واحد.

### LINE {#LINE}
```
public static int LINE
```


خط القائد هو خط واحد.

### MIDDLE_DOT {#MIDDLE-DOT}
```
public static int MIDDLE_DOT
```


خط القائد مكوّن من نقاط وسطية.

### NONE {#NONE}
```
public static int NONE
```


لا يتم عرض خط القائد.

### length {#length}
```
public static int length
```


### fromName(String tabLeaderName) {#fromName-java.lang.String}
```
public static int fromName(String tabLeaderName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tabLeaderName | java.lang.String |  |

**Returns:**
int
### getName(int tabLeader) {#getName-int}
```
public static String getName(int tabLeader)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| tabLeader | int |  |

**Returns:**
java.lang.String
