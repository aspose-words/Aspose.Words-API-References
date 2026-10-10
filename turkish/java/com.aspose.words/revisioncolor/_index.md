---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words Java için"
description: "Java'da belge revizyonlarının rengini belirtmeye izin verir."
type: docs
weight: 581
url: /tr/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Belge revizyonlarının rengini belirtmeye olanak tanır.

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Varsayılan. |
| [BLACK](#BLACK) | 000000 rengini temsil eder. |
| [BLUE](#BLUE) | 2e97d3 rengini temsil eder. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | 84a35b rengini temsil eder. |
| [BY_AUTHOR](#BY-AUTHOR) | Her yazarın revizyonları, önceden tanımlanmış yüksek kontrastlı renk setinden kendi vurgulama rengine sahip olur. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | 0000ff rengini temsil eder. |
| [CLASSIC_RED](#CLASSIC-RED) | ff0000 rengini temsil eder. |
| [DARK_BLUE](#DARK-BLUE) | 376e96 rengini temsil eder. |
| [DARK_RED](#DARK-RED) | 881824 rengini temsil eder. |
| [DARK_YELLOW](#DARK-YELLOW) | e09a2b rengini temsil eder. |
| [GRAY](#GRAY) | efeded rengini temsil eder. |
| [GRAY_25](#GRAY-25) | a0a3a9 rengini temsil eder. |
| [GRAY_50](#GRAY-50) | 50565e rengini temsil eder. |
| [GREEN](#GREEN) | 2c6234 rengini temsil eder. |
| [LIGHT_BLUE](#LIGHT-BLUE) | e1f2fa rengini temsil eder. |
| [LIGHT_GREEN](#LIGHT-GREEN) | e9f8ce rengini temsil eder. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | fce3d0 rengini temsil eder. |
| [LIGHT_PINK](#LIGHT-PINK) | fce6f4 rengini temsil eder. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | eadfef rengini temsil eder. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | fef4de rengini temsil eder. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | Revizyon değişikliklerini vurgulamak için renk kullanılmaz. |
| [PINK](#PINK) | ce338f rengini temsil eder. |
| [RED](#RED) | b5082e rengini temsil eder. |
| [TEAL](#TEAL) | 1b9cab rengini temsil eder. |
| [TURQUOISE](#TURQUOISE) | 3eafc2 rengini temsil eder. |
| [VIOLET](#VIOLET) | 633277 rengini temsil eder. |
| [WHITE](#WHITE) | ffffff rengini temsil eder. |
| [YELLOW](#YELLOW) | fad272 rengini temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Varsayılan.

### BLACK {#BLACK}
```
public static int BLACK
```


000000 rengini temsil eder.

### BLUE {#BLUE}
```
public static int BLUE
```


2e97d3 rengini temsil eder.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


84a35b rengini temsil eder.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Her yazarın revizyonları, önceden tanımlanmış yüksek kontrastlı renk setinden kendi vurgulama rengine sahip olur.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


0000ff rengini temsil eder.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


ff0000 rengini temsil eder.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


376e96 rengini temsil eder.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


881824 rengini temsil eder.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


e09a2b rengini temsil eder.

### GRAY {#GRAY}
```
public static int GRAY
```


efeded rengini temsil eder.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


a0a3a9 rengini temsil eder.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


50565e rengini temsil eder.

### GREEN {#GREEN}
```
public static int GREEN
```


2c6234 rengini temsil eder.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


e1f2fa rengini temsil eder.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


e9f8ce rengini temsil eder.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


fce3d0 rengini temsil eder.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


fce6f4 rengini temsil eder.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


eadfef rengini temsil eder.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


fef4de rengini temsil eder.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


Revizyon değişikliklerini vurgulamak için renk kullanılmaz.

### PINK {#PINK}
```
public static int PINK
```


ce338f rengini temsil eder.

### RED {#RED}
```
public static int RED
```


b5082e rengini temsil eder.

### TEAL {#TEAL}
```
public static int TEAL
```


1b9cab rengini temsil eder.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


3eafc2 rengini temsil eder.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


633277 rengini temsil eder.

### WHITE {#WHITE}
```
public static int WHITE
```


ffffff rengini temsil eder.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


fad272 rengini temsil eder.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
