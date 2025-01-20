---
title: RevisionColor
linktitle: RevisionColor
second_title: Aspose.Words for Java
description: Allows to specify color of document revisions in Java.
type: docs
weight: 558
url: /java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Allows to specify color of document revisions.

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

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

 doc.save(getArtifactsDir() + "Document.LayoutOptionsRevisions.pdf");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Default. |
| [BLACK](#BLACK) | Represents 000000 color. |
| [BLUE](#BLUE) | Represents 2e97d3 color. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Represents 84a35b color. |
| [BY_AUTHOR](#BY-AUTHOR) | Revisions of each author receive their own color for highlighting from a predefined set of hi-contrast colors. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Represents 0000ff color. |
| [CLASSIC_RED](#CLASSIC-RED) | Represents ff0000 color. |
| [DARK_BLUE](#DARK-BLUE) | Represents 376e96 color. |
| [DARK_RED](#DARK-RED) | Represents 881824 color. |
| [DARK_YELLOW](#DARK-YELLOW) | Represents e09a2b color. |
| [GRAY](#GRAY) | Represents efeded color. |
| [GRAY_25](#GRAY-25) | Represents a0a3a9 color. |
| [GRAY_50](#GRAY-50) | Represents 50565e color. |
| [GREEN](#GREEN) | Represents 2c6234 color. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Represents e1f2fa color. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Represents e9f8ce color. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Represents fce3d0 color. |
| [LIGHT_PINK](#LIGHT-PINK) | Represents fce6f4 color. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Represents eadfef color. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Represents fef4de color. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | No color is used to highlight revision changes. |
| [PINK](#PINK) | Represents ce338f color. |
| [RED](#RED) | Represents b5082e color. |
| [TEAL](#TEAL) | Represents 1b9cab color. |
| [TURQUOISE](#TURQUOISE) | Represents 3eafc2 color. |
| [VIOLET](#VIOLET) | Represents 633277 color. |
| [WHITE](#WHITE) | Represents ffffff color. |
| [YELLOW](#YELLOW) | Represents fad272 color. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Default.

### BLACK {#BLACK}
```
public static int BLACK
```


Represents 000000 color.

### BLUE {#BLUE}
```
public static int BLUE
```


Represents 2e97d3 color.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Represents 84a35b color.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Revisions of each author receive their own color for highlighting from a predefined set of hi-contrast colors.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Represents 0000ff color.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Represents ff0000 color.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Represents 376e96 color.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Represents 881824 color.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Represents e09a2b color.

### GRAY {#GRAY}
```
public static int GRAY
```


Represents efeded color.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Represents a0a3a9 color.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Represents 50565e color.

### GREEN {#GREEN}
```
public static int GREEN
```


Represents 2c6234 color.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Represents e1f2fa color.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Represents e9f8ce color.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Represents fce3d0 color.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Represents fce6f4 color.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Represents eadfef color.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Represents fef4de color.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


No color is used to highlight revision changes.

### PINK {#PINK}
```
public static int PINK
```


Represents ce338f color.

### RED {#RED}
```
public static int RED
```


Represents b5082e color.

### TEAL {#TEAL}
```
public static int TEAL
```


Represents 1b9cab color.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Represents 3eafc2 color.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Represents 633277 color.

### WHITE {#WHITE}
```
public static int WHITE
```


Represents ffffff color.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Represents fad272 color.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
