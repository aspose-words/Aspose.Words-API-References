---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words per Java"
description: "Consente di specificare il colore delle revisioni del documento in Java."
type: docs
weight: 581
url: /it/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Consente di specificare il colore delle revisioni del documento.

 **Examples:** 

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Predefinito. |
| [BLACK](#BLACK) | Rappresenta il colore 000000. |
| [BLUE](#BLUE) | Rappresenta il colore 2e97d3. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Rappresenta il colore 84a35b. |
| [BY_AUTHOR](#BY-AUTHOR) | Le revisioni di ciascun autore ricevono un proprio colore per l'evidenziazione da un insieme predefinito di colori ad alto contrasto. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Rappresenta il colore 0000ff. |
| [CLASSIC_RED](#CLASSIC-RED) | Rappresenta il colore ff0000. |
| [DARK_BLUE](#DARK-BLUE) | Rappresenta il colore 376e96. |
| [DARK_RED](#DARK-RED) | Rappresenta il colore 881824. |
| [DARK_YELLOW](#DARK-YELLOW) | Rappresenta il colore e09a2b. |
| [GRAY](#GRAY) | Rappresenta il colore efeded. |
| [GRAY_25](#GRAY-25) | Rappresenta il colore a0a3a9. |
| [GRAY_50](#GRAY-50) | Rappresenta il colore 50565e. |
| [GREEN](#GREEN) | Rappresenta il colore 2c6234. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Rappresenta il colore e1f2fa. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Rappresenta il colore e9f8ce. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Rappresenta il colore fce3d0. |
| [LIGHT_PINK](#LIGHT-PINK) | Rappresenta il colore fce6f4. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Rappresenta il colore eadfef. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Rappresenta il colore fef4de. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | Nessun colore è usato per evidenziare le modifiche di revisione. |
| [PINK](#PINK) | Rappresenta il colore ce338f. |
| [RED](#RED) | Rappresenta il colore b5082e. |
| [TEAL](#TEAL) | Rappresenta il colore 1b9cab. |
| [TURQUOISE](#TURQUOISE) | Rappresenta il colore 3eafc2. |
| [VIOLET](#VIOLET) | Rappresenta il colore 633277. |
| [WHITE](#WHITE) | Rappresenta il colore ffffff. |
| [YELLOW](#YELLOW) | Rappresenta il colore fad272. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Predefinito.

### BLACK {#BLACK}
```
public static int BLACK
```


Rappresenta il colore 000000.

### BLUE {#BLUE}
```
public static int BLUE
```


Rappresenta il colore 2e97d3.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Rappresenta il colore 84a35b.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Le revisioni di ciascun autore ricevono un proprio colore per l'evidenziazione da un insieme predefinito di colori ad alto contrasto.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Rappresenta il colore 0000ff.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Rappresenta il colore ff0000.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Rappresenta il colore 376e96.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Rappresenta il colore 881824.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Rappresenta il colore e09a2b.

### GRAY {#GRAY}
```
public static int GRAY
```


Rappresenta il colore efeded.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Rappresenta il colore a0a3a9.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Rappresenta il colore 50565e.

### GREEN {#GREEN}
```
public static int GREEN
```


Rappresenta il colore 2c6234.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Rappresenta il colore e1f2fa.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Rappresenta il colore e9f8ce.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Rappresenta il colore fce3d0.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Rappresenta il colore fce6f4.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Rappresenta il colore eadfef.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Rappresenta il colore fef4de.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


Nessun colore è usato per evidenziare le modifiche di revisione.

### PINK {#PINK}
```
public static int PINK
```


Rappresenta il colore ce338f.

### RED {#RED}
```
public static int RED
```


Rappresenta il colore b5082e.

### TEAL {#TEAL}
```
public static int TEAL
```


Rappresenta il colore 1b9cab.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Rappresenta il colore 3eafc2.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Rappresenta il colore 633277.

### WHITE {#WHITE}
```
public static int WHITE
```


Rappresenta il colore ffffff.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Rappresenta il colore fad272.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
