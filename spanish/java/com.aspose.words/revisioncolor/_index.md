---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words para Java"
description: "Permite especificar el color de las revisiones del documento en Java."
type: docs
weight: 581
url: /es/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Permite especificar el color de las revisiones del documento.

 **Examples:** 

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Predeterminado. |
| [BLACK](#BLACK) | Representa el color 000000. |
| [BLUE](#BLUE) | Representa el color 2e97d3. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Representa el color 84a35b. |
| [BY_AUTHOR](#BY-AUTHOR) | Las revisiones de cada autor reciben su propio color para resaltar de un conjunto predefinido de colores de alto contraste. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Representa el color 0000ff. |
| [CLASSIC_RED](#CLASSIC-RED) | Representa el color ff0000. |
| [DARK_BLUE](#DARK-BLUE) | Representa el color 376e96. |
| [DARK_RED](#DARK-RED) | Representa el color 881824. |
| [DARK_YELLOW](#DARK-YELLOW) | Representa el color e09a2b. |
| [GRAY](#GRAY) | Representa el color efeded. |
| [GRAY_25](#GRAY-25) | Representa el color a0a3a9. |
| [GRAY_50](#GRAY-50) | Representa el color 50565e. |
| [GREEN](#GREEN) | Representa el color 2c6234. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Representa el color e1f2fa. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Representa el color e9f8ce. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Representa el color fce3d0. |
| [LIGHT_PINK](#LIGHT-PINK) | Representa el color fce6f4. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Representa el color eadfef. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Representa el color fef4de. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | No se usa color para resaltar los cambios de revisión. |
| [PINK](#PINK) | Representa el color ce338f. |
| [RED](#RED) | Representa el color b5082e. |
| [TEAL](#TEAL) | Representa el color 1b9cab. |
| [TURQUOISE](#TURQUOISE) | Representa el color 3eafc2. |
| [VIOLET](#VIOLET) | Representa el color 633277. |
| [WHITE](#WHITE) | Representa el color ffffff. |
| [YELLOW](#YELLOW) | Representa el color fad272. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Predeterminado.

### BLACK {#BLACK}
```
public static int BLACK
```


Representa el color 000000.

### BLUE {#BLUE}
```
public static int BLUE
```


Representa el color 2e97d3.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Representa el color 84a35b.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Las revisiones de cada autor reciben su propio color para resaltar de un conjunto predefinido de colores de alto contraste.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Representa el color 0000ff.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Representa el color ff0000.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Representa el color 376e96.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Representa el color 881824.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Representa el color e09a2b.

### GRAY {#GRAY}
```
public static int GRAY
```


Representa el color efeded.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Representa el color a0a3a9.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Representa el color 50565e.

### GREEN {#GREEN}
```
public static int GREEN
```


Representa el color 2c6234.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Representa el color e1f2fa.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Representa el color e9f8ce.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Representa el color fce3d0.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Representa el color fce6f4.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Representa el color eadfef.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Representa el color fef4de.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


No se usa color para resaltar los cambios de revisión.

### PINK {#PINK}
```
public static int PINK
```


Representa el color ce338f.

### RED {#RED}
```
public static int RED
```


Representa el color b5082e.

### TEAL {#TEAL}
```
public static int TEAL
```


Representa el color 1b9cab.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Representa el color 3eafc2.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Representa el color 633277.

### WHITE {#WHITE}
```
public static int WHITE
```


Representa el color ffffff.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Representa el color fad272.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
