---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen der Farbe von Dokumentrevisionen in Java."
type: docs
weight: 581
url: /de/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Ermöglicht die Angabe der Farbe von Dokumentrevisionen.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Standard. |
| [BLACK](#BLACK) | Stellt die Farbe 000000 dar. |
| [BLUE](#BLUE) | Stellt die Farbe 2e97d3 dar. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Stellt die Farbe 84a35b dar. |
| [BY_AUTHOR](#BY-AUTHOR) | Revisionen jedes Autors erhalten ihre eigene Hervorhebungsfarbe aus einem vordefinierten Satz hochkontrastierender Farben. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Stellt die Farbe 0000ff dar. |
| [CLASSIC_RED](#CLASSIC-RED) | Stellt die Farbe ff0000 dar. |
| [DARK_BLUE](#DARK-BLUE) | Stellt die Farbe 376e96 dar. |
| [DARK_RED](#DARK-RED) | Stellt die Farbe 881824 dar. |
| [DARK_YELLOW](#DARK-YELLOW) | Stellt die Farbe e09a2b dar. |
| [GRAY](#GRAY) | Stellt die Farbe efeded dar. |
| [GRAY_25](#GRAY-25) | Stellt die Farbe a0a3a9 dar. |
| [GRAY_50](#GRAY-50) | Stellt die Farbe 50565e dar. |
| [GREEN](#GREEN) | Stellt die Farbe 2c6234 dar. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Stellt die Farbe e1f2fa dar. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Stellt die Farbe e9f8ce dar. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Stellt die Farbe fce3d0 dar. |
| [LIGHT_PINK](#LIGHT-PINK) | Stellt die Farbe fce6f4 dar. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Stellt die Farbe eadfef dar. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Stellt die Farbe fef4de dar. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | Es wird keine Farbe verwendet, um Änderungen der Revision hervorzuheben. |
| [PINK](#PINK) | Stellt die Farbe ce338f dar. |
| [RED](#RED) | Stellt die Farbe b5082e dar. |
| [TEAL](#TEAL) | Stellt die Farbe 1b9cab dar. |
| [TURQUOISE](#TURQUOISE) | Stellt die Farbe 3eafc2 dar. |
| [VIOLET](#VIOLET) | Stellt die Farbe 633277 dar. |
| [WHITE](#WHITE) | Stellt die Farbe ffffff dar. |
| [YELLOW](#YELLOW) | Stellt die Farbe fad272 dar. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Standard.

### BLACK {#BLACK}
```
public static int BLACK
```


Stellt die Farbe 000000 dar.

### BLUE {#BLUE}
```
public static int BLUE
```


Stellt die Farbe 2e97d3 dar.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Stellt die Farbe 84a35b dar.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Revisionen jedes Autors erhalten ihre eigene Hervorhebungsfarbe aus einem vordefinierten Satz hochkontrastierender Farben.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Stellt die Farbe 0000ff dar.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Stellt die Farbe ff0000 dar.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Stellt die Farbe 376e96 dar.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Stellt die Farbe 881824 dar.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Stellt die Farbe e09a2b dar.

### GRAY {#GRAY}
```
public static int GRAY
```


Stellt die Farbe efeded dar.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Stellt die Farbe a0a3a9 dar.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Stellt die Farbe 50565e dar.

### GREEN {#GREEN}
```
public static int GREEN
```


Stellt die Farbe 2c6234 dar.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Stellt die Farbe e1f2fa dar.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Stellt die Farbe e9f8ce dar.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Stellt die Farbe fce3d0 dar.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Stellt die Farbe fce6f4 dar.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Stellt die Farbe eadfef dar.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Stellt die Farbe fef4de dar.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


Es wird keine Farbe verwendet, um Änderungen der Revision hervorzuheben.

### PINK {#PINK}
```
public static int PINK
```


Stellt die Farbe ce338f dar.

### RED {#RED}
```
public static int RED
```


Stellt die Farbe b5082e dar.

### TEAL {#TEAL}
```
public static int TEAL
```


Stellt die Farbe 1b9cab dar.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Stellt die Farbe 3eafc2 dar.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Stellt die Farbe 633277 dar.

### WHITE {#WHITE}
```
public static int WHITE
```


Stellt die Farbe ffffff dar.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Stellt die Farbe fad272 dar.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
