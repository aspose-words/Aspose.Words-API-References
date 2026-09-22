---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد لون مراجعات المستند في Java."
type: docs
weight: 581
url: /ar/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

يسمح بتحديد لون مراجعات المستند.

 **Examples:** 

يعرض كيفية تعديل مظهر المراجعات في مستند الإخراج المُعرض.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | افتراضي. |
| [BLACK](#BLACK) | يمثل اللون 000000. |
| [BLUE](#BLUE) | يمثل اللون 2e97d3. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | يمثل اللون 84a35b. |
| [BY_AUTHOR](#BY-AUTHOR) | تحصل مراجعات كل مؤلف على لون خاص بها للتظليل من مجموعة مسبقة التعريف من الألوان ذات التباين العالي. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | يمثل اللون 0000ff. |
| [CLASSIC_RED](#CLASSIC-RED) | يمثل اللون ff0000. |
| [DARK_BLUE](#DARK-BLUE) | يمثل اللون 376e96. |
| [DARK_RED](#DARK-RED) | يمثل اللون 881824. |
| [DARK_YELLOW](#DARK-YELLOW) | يمثل اللون e09a2b. |
| [GRAY](#GRAY) | يمثل اللون efeded. |
| [GRAY_25](#GRAY-25) | يمثل اللون a0a3a9. |
| [GRAY_50](#GRAY-50) | يمثل اللون 50565e. |
| [GREEN](#GREEN) | يمثل اللون 2c6234. |
| [LIGHT_BLUE](#LIGHT-BLUE) | يمثل اللون e1f2fa. |
| [LIGHT_GREEN](#LIGHT-GREEN) | يمثل اللون e9f8ce. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | يمثل اللون fce3d0. |
| [LIGHT_PINK](#LIGHT-PINK) | يمثل اللون fce6f4. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | يمثل اللون eadfef. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | يمثل اللون fef4de. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | لا يُستخدم أي لون لتسليط الضوء على تغييرات المراجعة. |
| [PINK](#PINK) | يمثل اللون ce338f. |
| [RED](#RED) | يمثل اللون b5082e. |
| [TEAL](#TEAL) | يمثل اللون 1b9cab. |
| [TURQUOISE](#TURQUOISE) | يمثل اللون 3eafc2. |
| [VIOLET](#VIOLET) | يمثل اللون 633277. |
| [WHITE](#WHITE) | يمثل اللون ffffff. |
| [YELLOW](#YELLOW) | يمثل اللون fad272. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


افتراضي.

### BLACK {#BLACK}
```
public static int BLACK
```


يمثل اللون 000000.

### BLUE {#BLUE}
```
public static int BLUE
```


يمثل اللون 2e97d3.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


يمثل اللون 84a35b.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


تحصل مراجعات كل مؤلف على لون خاص بها للتظليل من مجموعة مسبقة التعريف من الألوان ذات التباين العالي.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


يمثل اللون 0000ff.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


يمثل اللون ff0000.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


يمثل اللون 376e96.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


يمثل اللون 881824.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


يمثل اللون e09a2b.

### GRAY {#GRAY}
```
public static int GRAY
```


يمثل اللون efeded.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


يمثل اللون a0a3a9.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


يمثل اللون 50565e.

### GREEN {#GREEN}
```
public static int GREEN
```


يمثل اللون 2c6234.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


يمثل اللون e1f2fa.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


يمثل اللون e9f8ce.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


يمثل اللون fce3d0.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


يمثل اللون fce6f4.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


يمثل اللون eadfef.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


يمثل اللون fef4de.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


لا يُستخدم أي لون لتسليط الضوء على تغييرات المراجعة.

### PINK {#PINK}
```
public static int PINK
```


يمثل اللون ce338f.

### RED {#RED}
```
public static int RED
```


يمثل اللون b5082e.

### TEAL {#TEAL}
```
public static int TEAL
```


يمثل اللون 1b9cab.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


يمثل اللون 3eafc2.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


يمثل اللون 633277.

### WHITE {#WHITE}
```
public static int WHITE
```


يمثل اللون ffffff.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


يمثل اللون fad272.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int revisionColor) {#toString-int}
```
public static String toString(int revisionColor)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
