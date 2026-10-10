---
title: "RevisionColor"
linktitle: "RevisionColor"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier la couleur des révisions de document en Java."
type: docs
weight: 581
url: /fr/java/com.aspose.words/revisioncolor/
---

**Inheritance:**
java.lang.Object
```
public class RevisionColor
```

Permet de spécifier la couleur des révisions du document.

 **Examples:** 

Montre comment modifier l'apparence des révisions dans un document de sortie rendu.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Par défaut. |
| [BLACK](#BLACK) | Représente la couleur 000000. |
| [BLUE](#BLUE) | Représente la couleur 2e97d3. |
| [BRIGHT_GREEN](#BRIGHT-GREEN) | Représente la couleur 84a35b. |
| [BY_AUTHOR](#BY-AUTHOR) | Les révisions de chaque auteur reçoivent leur propre couleur de mise en évidence à partir d'un ensemble prédéfini de couleurs à fort contraste. |
| [CLASSIC_BLUE](#CLASSIC-BLUE) | Représente la couleur 0000ff. |
| [CLASSIC_RED](#CLASSIC-RED) | Représente la couleur ff0000. |
| [DARK_BLUE](#DARK-BLUE) | Représente la couleur 376e96. |
| [DARK_RED](#DARK-RED) | Représente la couleur 881824. |
| [DARK_YELLOW](#DARK-YELLOW) | Représente la couleur e09a2b. |
| [GRAY](#GRAY) | Représente la couleur efeded. |
| [GRAY_25](#GRAY-25) | Représente la couleur a0a3a9. |
| [GRAY_50](#GRAY-50) | Représente la couleur 50565e. |
| [GREEN](#GREEN) | Représente la couleur 2c6234. |
| [LIGHT_BLUE](#LIGHT-BLUE) | Représente la couleur e1f2fa. |
| [LIGHT_GREEN](#LIGHT-GREEN) | Représente la couleur e9f8ce. |
| [LIGHT_ORANGE](#LIGHT-ORANGE) | Représente la couleur fce3d0. |
| [LIGHT_PINK](#LIGHT-PINK) | Représente la couleur fce6f4. |
| [LIGHT_PURPLE](#LIGHT-PURPLE) | Représente la couleur eadfef. |
| [LIGHT_YELLOW](#LIGHT-YELLOW) | Représente la couleur fef4de. |
| [NO_HIGHLIGHT](#NO-HIGHLIGHT) | Aucune couleur n'est utilisée pour mettre en évidence les modifications de révision. |
| [PINK](#PINK) | Représente la couleur ce338f. |
| [RED](#RED) | Représente la couleur b5082e. |
| [TEAL](#TEAL) | Représente la couleur 1b9cab. |
| [TURQUOISE](#TURQUOISE) | Représente la couleur 3eafc2. |
| [VIOLET](#VIOLET) | Représente la couleur 633277. |
| [WHITE](#WHITE) | Représente la couleur ffffff. |
| [YELLOW](#YELLOW) | Représente la couleur fad272. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String revisionColorName)](#fromName-java.lang.String) |  |
| [getName(int revisionColor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionColor)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Par défaut.

### BLACK {#BLACK}
```
public static int BLACK
```


Représente la couleur 000000.

### BLUE {#BLUE}
```
public static int BLUE
```


Représente la couleur 2e97d3.

### BRIGHT_GREEN {#BRIGHT-GREEN}
```
public static int BRIGHT_GREEN
```


Représente la couleur 84a35b.

### BY_AUTHOR {#BY-AUTHOR}
```
public static int BY_AUTHOR
```


Les révisions de chaque auteur reçoivent leur propre couleur de mise en évidence à partir d'un ensemble prédéfini de couleurs à fort contraste.

### CLASSIC_BLUE {#CLASSIC-BLUE}
```
public static int CLASSIC_BLUE
```


Représente la couleur 0000ff.

### CLASSIC_RED {#CLASSIC-RED}
```
public static int CLASSIC_RED
```


Représente la couleur ff0000.

### DARK_BLUE {#DARK-BLUE}
```
public static int DARK_BLUE
```


Représente la couleur 376e96.

### DARK_RED {#DARK-RED}
```
public static int DARK_RED
```


Représente la couleur 881824.

### DARK_YELLOW {#DARK-YELLOW}
```
public static int DARK_YELLOW
```


Représente la couleur e09a2b.

### GRAY {#GRAY}
```
public static int GRAY
```


Représente la couleur efeded.

### GRAY_25 {#GRAY-25}
```
public static int GRAY_25
```


Représente la couleur a0a3a9.

### GRAY_50 {#GRAY-50}
```
public static int GRAY_50
```


Représente la couleur 50565e.

### GREEN {#GREEN}
```
public static int GREEN
```


Représente la couleur 2c6234.

### LIGHT_BLUE {#LIGHT-BLUE}
```
public static int LIGHT_BLUE
```


Représente la couleur e1f2fa.

### LIGHT_GREEN {#LIGHT-GREEN}
```
public static int LIGHT_GREEN
```


Représente la couleur e9f8ce.

### LIGHT_ORANGE {#LIGHT-ORANGE}
```
public static int LIGHT_ORANGE
```


Représente la couleur fce3d0.

### LIGHT_PINK {#LIGHT-PINK}
```
public static int LIGHT_PINK
```


Représente la couleur fce6f4.

### LIGHT_PURPLE {#LIGHT-PURPLE}
```
public static int LIGHT_PURPLE
```


Représente la couleur eadfef.

### LIGHT_YELLOW {#LIGHT-YELLOW}
```
public static int LIGHT_YELLOW
```


Représente la couleur fef4de.

### NO_HIGHLIGHT {#NO-HIGHLIGHT}
```
public static int NO_HIGHLIGHT
```


Aucune couleur n'est utilisée pour mettre en évidence les modifications de révision.

### PINK {#PINK}
```
public static int PINK
```


Représente la couleur ce338f.

### RED {#RED}
```
public static int RED
```


Représente la couleur b5082e.

### TEAL {#TEAL}
```
public static int TEAL
```


Représente la couleur 1b9cab.

### TURQUOISE {#TURQUOISE}
```
public static int TURQUOISE
```


Représente la couleur 3eafc2.

### VIOLET {#VIOLET}
```
public static int VIOLET
```


Représente la couleur 633277.

### WHITE {#WHITE}
```
public static int WHITE
```


Représente la couleur ffffff.

### YELLOW {#YELLOW}
```
public static int YELLOW
```


Représente la couleur fad272.

### length {#length}
```
public static int length
```


### fromName(String revisionColorName) {#fromName-java.lang.String}
```
public static int fromName(String revisionColorName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionColorName | java.lang.String |  |

**Returns:**
int
### getName(int revisionColor) {#getName-int}
```
public static String getName(int revisionColor)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| revisionColor | int |  |

**Returns:**
java.lang.String
