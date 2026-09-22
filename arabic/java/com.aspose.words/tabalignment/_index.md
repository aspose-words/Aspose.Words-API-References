---
title: "TabAlignment"
linktitle: "TabAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد محاذاة/نوع علامة التبويب في Java."
type: docs
weight: 652
url: /ar/java/com.aspose.words/tabalignment/
---

**Inheritance:**
java.lang.Object
```
public class TabAlignment
```

يحدد محاذاة/نوع نقطة التبويب.

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
| [BAR](#BAR) | يرسم شريطًا عموديًا عند موضع علامة التبويب. |
| [CENTER](#CENTER) | يتمركز النص حول علامة التبويب. |
| [CLEAR](#CLEAR) | يمسح أي علامة تبويب في هذا الموضع. |
| [DECIMAL](#DECIMAL) | يضبط محاذاة النص عند النقطة العشرية. |
| [LEFT](#LEFT) | يضبط محاذاة النص إلى اليسار بعد علامة التبويب. |
| [LIST](#LIST) | علامة التبويب هي فاصل بين الرقم/الرصاصة والنص في عنصر القائمة. |
| [RIGHT](#RIGHT) | يضبط محاذاة النص إلى اليمين عند علامة التبويب. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String tabAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int tabAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tabAlignment)](#toString-int) |  |
### BAR {#BAR}
```
public static int BAR
```


يرسم شريطًا عموديًا عند موضع علامة التبويب.

### CENTER {#CENTER}
```
public static int CENTER
```


يتمركز النص حول علامة التبويب.

### CLEAR {#CLEAR}
```
public static int CLEAR
```


يمسح أي علامة تبويب في هذا الموضع.

### DECIMAL {#DECIMAL}
```
public static int DECIMAL
```


يضبط محاذاة النص عند النقطة العشرية.

### LEFT {#LEFT}
```
public static int LEFT
```


يضبط محاذاة النص إلى اليسار بعد علامة التبويب.

### LIST {#LIST}
```
public static int LIST
```


علامة التبويب هي فاصل بين الرقم/الرصاصة والنص في عنصر القائمة.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


يضبط محاذاة النص إلى اليمين عند علامة التبويب.

### length {#length}
```
public static int length
```


### fromName(String tabAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tabAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tabAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int tabAlignment) {#getName-int}
```
public static String getName(int tabAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| tabAlignment | int |  |

**Returns:**
java.lang.String
